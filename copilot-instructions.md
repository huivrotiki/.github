# AudioKit AI Agent Instructions

This guide helps AI coding agents understand AudioKit's repository structure, conventions, and workflows to be immediately productive.

## Project Architecture

- **Core Components**: AudioKit is modularly structured with the main `AudioKit` repository as the core, with additional specialized modules:
  - `AudioKitEX` - Core audio processing extensions
  - `AudioKitUI` - User interface components
  - Specialized modules (Devoloop, Dunne, Soundpipe, Sporth, STK) for different audio processing capabilities

- **Independent Libraries**: Standalone Swift packages that can be used with or without AudioKit:
  - Controls, Flow, Keyboard, Microtonality, PianoRoll, Tonic, Waveform

## Development Standards

### Code Style and Organization
- Use SwiftFormat for consistent code formatting
- Keep headers single-line for clarity
- Maintain 100% test coverage goal for all modules

### Documentation Structure
1. README.md requirements:
   - Include screenshots/animated PNGs
   - Link to AudioKit.io documentation
   - Document playground/demo availability
2. Include DocC documentation with:
   - Main page containing imagery
   - Link back to GitHub repository

### Repository Requirements
- `.spi.yml` file for Swift Package Index integration
- Social Preview Image for GitHub
- GitHub Actions workflow for CI/CD
- Webhooks configured for Discord (tags, issues, PRs, pushes)

### Testing and Quality
- All repositories must have passing tests with GitHub Actions
- Test status badges must be present in README.md
- Include both playgrounds and demo projects for usage examples

## Version Control
- Use semantic versioning (x.y.z) for all tags
- Keep version tags current and synchronized across dependent packages

## Integration Points
- Swift Package Manager is the primary dependency manager
- Discord webhooks for collaborative development updates
- Swift Package Index for package discovery and documentation

## Key File Locations
- `.github/workflows/` - CI/CD configurations
- `.spi.yml` - Swift Package Index configuration
- `Tests/` - Test suites maintaining 100% coverage goal
- `Playgrounds/` - Interactive examples
- `Documentation/` - DocC documentation files

## Common Commands
```swift
// Initialize test environment
swift test

// Format code
swiftformat .

// Build documentation
swift doc generate
```