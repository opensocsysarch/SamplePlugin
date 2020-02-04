# System Architect SamplePlugin Template

[![GitHub license](https://img.shields.io/badge/license-APACHE2-blue.svg)](https://raw.githubusercontent.com/opensocsysarch/SamplePlugin/master/LICENSE)

## Getting Started

The SamplePlugin infrastructure can be utilized as a template to construct custom 
System Architect plugins.  This repository contains basic source code and Cmake scripts 
necessary to construct a plugin project that builds against the CoreGen libraries.

## Prerequisites
* C++14 Compiler (LLVM/Clang and GCC are tested)
* CMake 3.4.3+
* CoreGen

## Building

The SampleTemplate infrastructure requires that the user have the 
``coregen-config`` binary in the default path.  This tool (from the
CoreGen package) derives the necessary libraries and header paths 
required to build external packages and/or plugins.

1. Clone the SamplePlugin repository.
1. Create a ``build`` directory within the SamplePlugin source tree (and change to that directory)
1. Execute cmake to generate the target-specific makefiles
1. Execute the build

An example of this process is as follows:
```
git clone https://github.com/opensocsysarch/SamplePlugin.git
cd SamplePlugin
mkdir build
cd build
cmake ../
make
```

## Contributing
We welcome outside contributions from corporate, acaddemic and individual developers.  However,
there are a number of fundamental ground rules that you must adhere to in order to participate.  These
rules are outlined as follows:

* All code must adhere to the existing C++ coding style.  While we are somewhat flexible in basic style, you will
adhere to what is currently in place.  This includes camel case C++ methods and inline comments.  Uncommented,
complicated algorithmic constructs will be rejected.
* We support compilaton and adherence to C++11 methods.  We do not currently accept C++14 and beyond.
* All new methods and variables contained within public, private and protected class methods must be commented
using the existing Doxygen-style formatting.  All new classes must also include Doxygen blocks in the new header
files.  Any pull requests that lack these features will be rejected.
* All changes to functionality and/or the API infrastructure must be accompanied by complementary tests
* All external pull requests **must** target the *devel* branch.  No external pull requests will be accepted
to the master branch.
* All external pull requests must contain sufficient documentation in the pull request comments in order to
be accepted.
* All external pull requests that update the CoreGen IR specification or the StoneCutter language specification
(et al. syntax) must contain complementary pull requests for the CoreGen IR spec or the
StoneCutter language spec.
* All pull requests will be reviewed by the core development staff.  Any necessary changes will be marked
in the respective pull request comments.  All pull requests will be tested against in the Tactical
Computing Laboratories development infrastructure.  This includes tests against all supported platforms.
Any failures in the test infrastructure will be noted in the pull request comments.

## License
CoreGen is licensed under an Apache-style license - see the [LICENSE](LICENSE) file for details

## Authors
* *John Leidel* - *Chief Scientist* - [Tactical Computing Labs](http://www.tactcomplabs.com)
* *Frank Conlon* - *Research Engineer* - [Tactical Computing Labs](http://www.tactcomplabs.com)
* *David Donofrio* - *Chief Hardware Architect* - [Tactical Computing Labs](http://www.tactcomplabs.com)

## Acknowledgements
* None at this time

