# Iganis PDFs - Launch Guide

## Prerequisites

Before launching Iganis PDFs, ensure you have:

- **Java 17 or higher** installed
- **Docker** (optional, for containerized deployment)
- **Git** (for cloning the repository)

### Installing Java

#### On macOS:
```bash
# Install Java using Homebrew
brew install openjdk@21

# Or download from Oracle/Adoptium and install manually
```

#### On Ubuntu/Debian:
```bash
# Install OpenJDK 21
sudo apt update
sudo apt install openjdk-21-jdk

# Verify installation
java -version
```

#### On Windows:
1. Download OpenJDK from https://adoptium.net/
2. Install the downloaded package
3. Add Java to your PATH environment variable

## Quick Start - Local Development

### 1. Build the Application

```bash
# Navigate to the project directory
cd /Users/gabriel/Downloads/IGANI-PDF-main

# Make gradlew executable (if needed)
chmod +x gradlew

# Build the application
./gradlew build
```

### 2. Run the Application

```bash
# Run directly with Gradle
./gradlew bootRun
```

The application will start on **http://localhost:8080**

### 3. Access the Application

Open your web browser and navigate to:
- **URL**: http://localhost:8080
- **Default Port**: 8080

## Docker Deployment (Recommended for Production)

### 1. Build the Docker Image

```bash
# Build the JAR file first
./gradlew build

# Build the Docker image
docker build -t iganis/iganis-pdfs:latest .
```

### 2. Run with Docker Compose

```bash
# Copy the example docker-compose file
cp exampleYmlFiles/docker-compose-latest.yml docker-compose.yml

# Start the application
docker-compose up -d
```

### 3. Access via Docker

- **URL**: http://localhost:8080
- **Configuration**: Edit docker-compose.yml for custom settings
- **Data Persistence**: Data is stored in `./iganis-pdfs/` directory

## Configuration

### Environment Variables

Key environment variables you can customize in docker-compose.yml:

```yaml
environment:
  UI_APPNAME: "Iganis PDFs"
  UI_HOMEDESCRIPTION: "Iganis PDFs - Professional PDF Management"
  UI_APPNAMENAVBAR: "Iganis PDFs"
  SYSTEM_DEFAULTLOCALE: "en-US"
  SYSTEM_MAXFILESIZE: "100"
  SECURITY_ENABLELOGIN: "false"  # Set to "true" to enable authentication
```

### Custom Settings

1. **Settings File**: Copy `app/core/src/main/resources/settings.yml.template` to `settings.yml`
2. **Modify**: Update the settings file with your preferences
3. **Mount**: Mount the settings file in Docker or place it in the classpath

## Features

Iganis PDFs includes 50+ PDF operations:

- **Merge & Split** PDFs
- **Convert** PDFs to/from various formats
- **OCR** text recognition
- **Digital Signatures**
- **Watermarking**
- **Compression**
- **Page Organization**
- **Security** features
- And much more!

## Troubleshooting

### Common Issues

1. **Port Already in Use**
   - Change the port mapping in docker-compose.yml: `"8081:8080"`

2. **Java Version Issues**
   - Ensure Java 17+ is installed: `java -version`

3. **Memory Issues**
   - Increase Docker memory limit in docker-compose.yml

4. **Permission Issues**
   - Ensure proper file permissions: `chmod +x gradlew`

### Logs

- **Application Logs**: Available in `./iganis-pdfs/logs/` (Docker)
- **Container Logs**: `docker-compose logs iganis-pdfs`

## Development

### Hot Reload Development

```bash
# Run in development mode with hot reload
./gradlew bootRun --args='--spring.profiles.active=dev'
```

### Building for Production

```bash
# Build optimized production JAR
./gradlew build -x test

# The JAR will be in: app/core/build/libs/
```

## Security

### Enable Authentication

1. Set `SECURITY_ENABLELOGIN: "true"` in docker-compose.yml
2. Set initial admin credentials in settings.yml
3. Restart the application

### HTTPS Setup

For production deployments, use a reverse proxy (nginx/Apache) or configure SSL directly.

## Support

- **GitHub**: https://github.com/iganis/iganis-pdfs
- **Issues**: Report bugs and feature requests on GitHub
- **Documentation**: Check the project README.md

## License

This project is licensed under the MIT License. See LICENSE file for details.

---

**Iganis PDFs** - Professional PDF Management Made Simple