# Changelog
All notable changes to this project will be documented in this file.


The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [1.2] - 2019-02-27
### Added
 - Add a `-c` parameter to run shell commands in the game's installation directory with relevant Wine environment variables.
 - Steam Runtime is now supported and used by default unless disabled with `--no-runtime` flag or `STEAM_RUNTIME` environment variable.

### Fixed
 - All arguments are now correctly passed to winetricks.
 - Games that haven't been launched at least once are now excluded properly.
 - Custom Proton versions with custom display names now work properly.
 - `PATH` environment variable is modified to prevent conflicts with system-wide Wine binaries.
 - Steam installation is handled correctly if `~/.steam/steam` and `~/.steam/root` point to different directories.

## [1.1.1] - 2019-01-20
### Added
 - Game-specific Proton installations are now detected.

### Fixed
 - Proton installations are now detected properly again in newer Steam Beta releases.

## [1.1] - 2019-01-20
### Added
 - Custom Proton installations in `STEAM_DIR/compatibilitytools.d` are now detected. See [Sirmentio/protontricks#31](https://github.com/Sirmentio/protontricks/issues/31).
 - protontricks is now a Python package and can be installed using `pip`.
 
### Changed
 - Argument parsing has been refactored to use argparse.
   - `protontricks gui` is now `protontricks --gui`.
   - New `protontricks --version` command to print the version number.
 - Game names are now displayed in alphabetical order and filtered to exclude non-Proton games.
 - protontricks no longer prints INFO messages by default. To restore previous behavior, use the `-v` flag.

### Fixed
 - More robust VDF parsing.
 - Corrupted appmanifest files are now skipped. See [Sirmentio/protontricks#36](https://github.com/Sirmentio/protontricks/pull/36).
 - Display a proper error message when $STEAM_DIR doesn't point to a valid Steam installation. See [Sirmentio/protontricks#46](https://github.com/Sirmentio/protontricks/issues/46).

## 1.0 - 2019-01-16
### Added
 - The last release of protontricks maintained by [@Sirmentio](https://github.com/Sirmentio).

[Unreleased]: https://github.com/Matoking/protontricks/compare/1.2...HEAD
[1.2]: https://github.com/Matoking/protontricks/compare/1.1.1...1.2
[1.1.1]: https://github.com/Matoking/protontricks/compare/1.1...1.1.1
[1.1]: https://github.com/Matoking/protontricks/compare/1.0...1.1
