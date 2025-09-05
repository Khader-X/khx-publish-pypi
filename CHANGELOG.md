# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Comprehensive README.md with modern formatting and detailed documentation
- CHANGELOG.md for version history tracking
- Enhanced error handling and user feedback
- CI/CD integration examples

### Changed
- Renamed `khx-publish-pypi init` command to `khx-publish-pypi run` for better clarity
- Updated repository URL for PyPI uploads (fixed 404 error)
- Improved CLI output formatting and visual feedback

### Fixed
- PyPI upload URL corrected from `https://pypi.org/legacy/` to `https://upload.pypi.org/legacy/`
- Token storage and retrieval improvements

## [0.1.4] - 2025-09-05

### Added
- Version bumping functionality with semantic versioning support
- Interactive token setup and management
- Pre-publish validation checks
- Rich console output with progress indicators
- Support for both TestPyPI and production PyPI publishing

### Changed
- Improved error messages and user guidance
- Enhanced build process with better dependency handling

### Fixed
- Initial release with core publishing functionality

## [0.1.3] - 2025-09-01

### Added
- Basic CLI structure and commands
- Package building with `python -m build`
- Twine integration for PyPI uploads
- Initial token management system

### Changed
- Project structure and organization

## [0.1.2] - 2025-08-25

### Added
- Core publishing logic
- Basic error handling
- Initial documentation

## [0.1.1] - 2025-08-20

### Added
- Project initialization
- Basic CLI interface
- Package structure setup

## [0.1.0] - 2025-08-15

### Added
- Initial project setup
- Basic functionality for Python package publishing
- CLI entry point configuration

---

## Types of changes
- `Added` for new features
- `Changed` for changes in existing functionality
- `Deprecated` for soon-to-be removed features
- `Removed` for now removed features
- `Fixed` for any bug fixes
- `Security` in case of vulnerabilities

## Contributing
When contributing to this project, please:
1. Update the CHANGELOG.md with your changes
2. Follow the existing format
3. Add entries under the [Unreleased] section
4. Move entries to a new version section when releasing

---

*This changelog was started on September 5, 2025.*
