# CoRAL - Corner Reflector Analysis Library

[![Travis](https://img.shields.io/travis/GeoscienceAustralia/CoRAL/master.svg?label=Travis%20CI)](https://travis-ci.org/GeoscienceAustralia/CoRAL)
[![Coverage Status](https://coveralls.io/repos/github/GeoscienceAustralia/CoRAL/badge.svg?branch=master)](https://coveralls.io/github/GeoscienceAustralia/CoRAL?branch=master)

CoRAL is a library of tools for analysing the response of corner reflectors (or other targets) in Synthetic Aperture Radar (SAR) images. The library started as a set of Python scripts developed during corner reflector prototyping experiments at Geoscience Australia. This work, and the implemented algorithms are documented in [Garthwaite 2017](https://doi.org/10.3390/rs9070648).

### Dependencies

This package requires the following non-standard Python modules installed:

```
NumPy
Matplotlib
```

### Authors

* **Matt Garthwaite** - [mcgarth](https://github.com/mcgarth)
* **Thomas Fuhrmann** - [tfuhrmann](https://github.com/tfuhrmann)

### Running

An example script ```Calc_CR_response.py``` is provided, and can be executed as follows:

```python3 Calc_CR_response.py```

This example will calculate the Radar Cross Section (RCS) and Signal to Clutter Ratio (SCR) for a single corner reflector. Results can be viewed in the generated image files (copies are lodged in the ```data\``` directory). 

### Example data

A stack of 9 example SAR images is contained in the ```data\``` directory. The example SAR images are a set of multi-looked intensity images acquired by Sentinel-1 in Interferometric Wide Swath mode. These images have been processed from Single Look Complex data using the GAMMA Remote Sensing software with 4 Looks in range and 1 Look in azimuth.
Each binary data file (```*.mli```) contains 200*200 floating point values. Each data file has an accompanying text file (```*.mli.par```) containing metadata generated by the GAMMA Remote Sensing software.
The example images, in descending-pass radar geometry, cover a small area cropped from the full images containing a test site "SERF" at Samford, Queensland, Australia. A corner reflector target was deployed at SERF for teaching purposes in August 2018.

### Testing

To run unit tests from within CoRAL repository directory: 

```python -m unittest discover tests/```

### License

Copyright 2018 Geoscience Australia

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

