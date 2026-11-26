# Voxel-Pulse
Independent Minecraft Java Edition launcher and modpack manager with a custom runtime.
# Voxel Pulse

### Independent Minecraft Java Edition Launcher & Modpack Manager

Voxel Pulse is an independent desktop launcher designed to simplify Minecraft installation, modpack management, runtime configuration, and performance optimization.

## Project Status

**Currently in active development.**

## Current Features

- Custom BUILTIN Minecraft installation engine
- Vanilla Minecraft support
- Fabric Loader support
- Minecraft 26.3 runtime preparation
- Automatic Java 25 runtime installation
- Modrinth integration
- Local .mrpack modpack installation
- Game file integrity verification
- Instance management
- Transactional installation and recovery
- Backup management
- JavaFX graphical user interface
- Command-line interface
- Alternative PrismLauncher integration

## Authentication

Voxel Pulse is designed to use official Microsoft account authentication through Microsoft's OAuth device code flow.

Minecraft API approval is currently required to complete live authentication and game launch testing.

The application does not directly collect Microsoft account passwords and is not intended to bypass Minecraft ownership verification.

## Development Roadmap

- Complete Microsoft authentication integration
- Independent Minecraft game launch
- Quilt, Forge and NeoForge support
- Extended modpack management
- Shader and resource pack management
- Hardware-based performance recommendations
- Intelligent game configuration

## Technology

- Java
- JavaFX
- Gradle
- JUnit
- Microsoft OAuth
- Modrinth API

## Quality Assurance

The current development build has passed 431 automated tests with no failures, errors or skipped tests, according to the project test report.

Minecraft 26.3 Vanilla and Fabric runtime installation have been validated. Actual game launch testing is pending authenticated session availability.

## Disclaimer

Voxel Pulse is an unofficial, independently developed project.

It is not affiliated with, endorsed by, or sponsored by Mojang Studios or Microsoft.

Minecraft is a trademark of Microsoft.

The project is intended to respect the Minecraft EULA and Usage Guidelines.
