# Personal Robotics Lab DART Examples

## Installation
Checkout and build this package,
[DART](https://github.com/dartsim/dart.git) (version 5.1 or above)
and [aikido](https://github.com/personalrobotics/aikido.git) from source. You
can automate the checkout and build by following the
[development environment](https://www.personalrobotics.ri.cmu.edu/software/development-environment)
instructions with this `.rosinstall` file:
```yaml
- git:
    local-name: aikido
    uri: https://github.com/personalrobotics/aikido.git
    version: feature/statespace
- git:
    local-name: dart
    uri: https://github.com/personalrobotics/dart.git
    version: master
- git:
    local-name: dart_examples
    uri: https://github.com/personalrobotics/dart_examples.git
    version: master
- git:
    local-name: herb_description
    uri: https://github.com/personalrobotics/herb_description.git
    version: master
```
You can speed up the build of DART by disabling the included examples, tests,
and tutorials. To do so, pass these options to CMake (e.g. using `catkin
config --cmake-args`):
```shell
-DDART_BUILD_EXAMPLES=OFF -DDART_BUILD_UNITTESTS=OFF -DDART_BUILD_TUTORIALS=OFF
```

## Usage
To load HERB:
```shell
$ rosrun dart_examples load_urdf package://herb_description/robots/herb.urdf
```
