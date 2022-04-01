# Docker-Based Plex Media Server for Mac
> 	:apple: While this _should_ be mostly compatible with any _'nix_
> operating system, it is specifically developed and tested on macOS
> and there are some macOS-specific commands and assumptions in the
> scripts.

Just `git clone` and run the scripts.

This project provides a **scripted** basic Plex Media Server
in the project's directory using the official Plex Media Server
image and Docker Compose.

It has three idempotent and non-destructive scripts:
  1. Run `make-plex` once to create your Plex Media Server
  2. Run `run-plex` to run your Plex Media Server
  3. Run `stop-plex` to stop your running Plex Media Server

> This setup is for access for the **internal network only!**

### To Setup The Plex Media Server...
You should only need to create your Plex Media Server once.

To use this...
  1. Clone this project in desired location
  2. Change directory to the project
  3. Run `./make-plex` script and follow the prompts
     to create the Plex Media Server Data Directories
     and `.env` file for the Docker Compose orchestration

### To Run The Plex Media Server...
Once you have created a Plex Media Server, you can run and stop
it as many times as you want.

#### Prerequisites
  1. **Docker**  - You must have Docker installed
     and running
  2. **Plex Account** - You must have a Plex Account
     (free is fine) from https://www.plex.tv/
  3. **Plex Server Media** - You must have the media
     that you want to serve and ideally in the Plex format

#### Run
To Run your Plex Media Server...
  1. Start Docker and wait until it is fully up and running
  2. You will need a browser to get the Claim token for your
     Plex Server run and to manage your Plex Media Server
  3. Run `./run-plex` script and follow the prompts
     to run the Plex Media Server using your `.env` file
  4. When prompted browse to https://www.plex.tv/claim/ (and login)
     to get the Claim token
  5. Enter the Claim token when prompted by the script
  6. When the script completes, browse to the URL listed
     in the output of the `./run-plex` script to finish startup
     and manage your Plex Media Server

> :point_right: You should always be able to reach your running
> Plex Media Server at http://localhost:32400/

#### Stop
To stop your Plex Media Server...
  1. Run `./stop-plex` script and follow the prompts
     to stop your Plex Media Server
