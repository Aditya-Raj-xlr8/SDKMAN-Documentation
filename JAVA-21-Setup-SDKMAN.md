# Java 21 Installation Guide with SDKMAN!

## Installing SDKMAN!

SDKMAN! is a tool for managing parallel versions of multiple Software Development Kits on most Unix-based systems.



```bash
# Download and install SDKMAN!
curl -s "https://get.sdkman.io" | bash

# Load SDKMAN! into your current shell session
source "$HOME/.sdkman/bin/sdkman-init.sh"

# Verify the installation was successful
sdk version

Installing Java 21
With SDKMAN! properly installed, you can now manage multiple Java versions with ease.
Installation Steps

# List all available Java versions
sdk list java

# Install Java 21 (Temurin distribution)
sdk install java 21.0.7-tem

# Optionally set Java 21 as your global default
sdk default java 21.0.7-tem

Project-Specific Java Configuration
SDKMAN! allows you to configure Java versions on a per-project basis, ensuring consistent environments across team members.
Setting Up Project-Specific Java Version

# Navigate to your project directory
cd /path/to/your/project

# Initialize a new .sdkmanrc file
sdk env init

# Edit the .sdkmanrc file and add the following line:
java=21.0.7-tem

# Activate the environment for this shell session
sdk env

Enabling Automatic Environment Switching
# Open the SDKMAN! configuration
sdk config

# Set the auto environment flag to true
sdkman_auto_env=true

With automatic environment switching enabled, SDKMAN! will detect and apply the correct Java version whenever you enter a directory containing a .sdkmanrc file.

# Verification
After completing the installation and configuration, verify that Java 21 is properly installed and active.

# Check the current Java version
java -version

You should see output similar to:

openjdk version "21.0.7"
OpenJDK Runtime Environment Temurin-21.0.7+...
OpenJDK 64-Bit Server VM Temurin-21.0.7+...

Common Commands

| Command                             | Description 
|-------------------------------------|-------------
| sdk list java                       | List available Java versions 
| sdk current java                    | Show current Java version 
| sdk use java 21.0.7-tem             | Use Java 21 temporarily 
| sdk default java 21.0.7-tem         | Set Java 21 as default 
| sdk env                             | Apply environment from .sdkmanrc 