# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- AndroidX support configuration in gradle.properties
- Consumer ProGuard rules (consumer-rules.pro) for library distribution
- InputStream support for PUT operations - enables streaming upload of large files
- Complete response body leak fixes across all response handlers

### Fixed
- Response body resource leaks in all response handlers (ExistsResponseHandler, LockResponseHandler, MultiStatusResponseHandler, ResourcesResponseHandler, VoidResponseHandler)
- Memory management issues through proper response.close() calls

### Changed
- Updated consumer ProGuard rules configuration in build.gradle
- Migrated from proguard-rules.pro to consumer-rules.pro for better library packaging

## Previous Changes

### Build System Updates
- Bump JDK to version 17
- Update Android Gradle Plugin to 8.2.2
- Add ProGuard dontwarn rules

### Bug Fixes
- Fix move destination URL encoding
- Add test case for moving to path containing spaces

### Documentation
- Add alternatives section to README.md

### CI/CD
- Remove CircleCI configuration file