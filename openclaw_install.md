# Installing OpenClaw - Setup Guide

Step 1: Install Homebrew

Homebrew is a package manager for macOS (and Linux). Open your Terminal and run:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

After installation, verify it works:

brew --version

Step 2: Install Node.js and npm

npm comes bundled with Node.js. Install it via Homebrew:

brew install node

Verify both are installed:

node --version

npm --version

Step 3: Install OpenClaw

Once npm is ready, install OpenClaw globally:

npm install -g openclaw

Or add it to a project locally:

npm install openclaw

Verify the installation:

openclaw --version

That's it — you're all set!
