# Changelog
All notable changes to this project will be documented in this file.  

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).  

### [1.6.4] - 2023-03-03

### Changed 
- Improve speed by adding concurrency in the findMatches method, using half the number of cpu cores available.
- Mention installation in editable mode in README

### [1.6.3] - 2021-11-24  

### Changed 
- Updated internal NMS code to work with latest OpenCV, and set min OpenCV version to 4.5.4.   

## [1.6.2.post1] - 2021-11-24  

### Changed
- Fix issue with latest OpenCV version, by limiting OpenCV version to 4.3.0.  


## [1.6.2] - 2021-10-05

### Added
- Checking if all templates fit in the search region/image as suggested by @insertscode
- Corresponding tests

### Changed
- Renamed requirements.txt to old_requirements.txt, and removed MTM from requirements. Binder uses setup.py anyway.


## [1.6.1] - 2020-08-20
### Added
- support mask for matchTemplates and findMatches as in cv2.matchTemplates with method 0 or 3
- notebook tutorial with mask
- CHANGELOG.MD

### Changed
- better docstrings

## [1.6.0.post1] - 2020-08-04
### Fixed
- issue when no detection found (see Changed of version 1.5.3.post2)


## [1.6.0] - 2020-08-03
### Changed
- NMS is now using the opencv `cv2.dnn.NMSBoxes` function
- use timeit for benchmark in example notebook

### Removed
- `MTM.NMS.Point_in_Rectangle` and `MTM.NMS.computeIoU` as they are not used anymore for the NMS

## [1.5.3.post2] - 2020-08-04
### Fixed
- issue when no detection found (see Changed)

### Changed
- `MTM.findMatches` return a dataframe with proper column names (not just empty)
- better handle the different opencv matchTemplate methods

## [1.5.3.post1] - 2020-05-11
### Removed
- remove the hardcoded version requirement for opencv-python-headless in setup.py

### Added
- MTM version is now defined in a dedicated version.py file

## [1.5.3] - 2020-04-28
### Added
- `MTM.computeScoreMap` which is like `cv2.matchTemplate` but checking for image types


## [1.5.2] - 2019-12-19
### Changed
- `MTM.findMatches` automatically cast 16-bit images and/or template to 32-bit

## [1.5.1] - 2019-10-10  
### Changed
- use pandas dataframe to return list of hits for `MTM.matchTemplates` and `MTM.findMatches` 
