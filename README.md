# Docker Plex Media Server
This is a basic setup for running a Plex Media Server
using the official Plex Media Server image
and docker-compose.

This setup is for access for the **internal network only!**

### To Setup The Plex Media Server...
To use this...
  1. Clone this project in desired location
  2. Change directory to the project
  3. Run the `./make-plex` script and follow the prompts
     to create the Plex Media Server Data Directories
     and `.env` file for the docker-compose orchestration

### To Run The Plex Media Server...

#### Prerequisites
  1. **Plex Account** - You must have a Plex Account
     (free is fine) from https://www.plex.tv/
  2. **Plex Server Media** - You must have the media
     that you want to serve and ideally in the Plex format.

#### Run
To Run your Plex Media Server...
  1. Start Docker and wait until it is fully up and running
  2. You will need a browser to get the Claim token for your
     Plex Server run and to manage your Plex Media Server
  3. Run the `./run-plex` script and follow the prompts
     to run the Plex Media Server using your `.env` file
  4. When promted browse to https://www.plex.tv/claim/ (and login)
     to get the Claim token
  5. Enter the Claim token when prompted by the script
  6. When the script completes, browse to http://app.plex.tv/
     to finish startup and manage your Plex Media Server

#### Stop
To stop your plex Media Server...
  1. Run `PLEX_CLAIM=<your-claim-token-here> docker-compose down`
     to stop your Plex Media Server
