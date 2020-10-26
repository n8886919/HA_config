# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 2017-06-20
### Added
- first CHANGELOG.md
- automations.yaml
  + Start dehumidification
### Changed
- automations.yaml
  + Stop dehumidification: below 65 -> 60
  + add Time to wake up: srv"select_source" between shuffle_set & play_media
  + add Time to relax: srv"select_source" between shuffle_set & play_media
  + add Time to sleep: srv"select_source" between shuffle_set & play_media
- scene.yaml
  + leaving:
    + add delay 1 in the first
    + move scene activation before broadcast
  + arrival: 
    + srv"select_source" between shuffle_set & play_media
    + wait 5 min and act relax scene
    + mode: single -> restart
- configuration.yaml
  + media_player: host 192.168.31.12 -> 0.0.0.0
  + scenes.yaml: CHANGED a lots!
### Deprecated
- nothing
### Removed
- configuration.yaml
  some comment
### Fixed
- README.md, a newline
### Security
- nothing