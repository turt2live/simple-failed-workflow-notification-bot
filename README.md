# Workflow failure notification bot

Posts to a Matrix room when a GitHub workflow run fails on the default branch.

## Running / Building

Run `npm install` to get the dependencies.

To build it: `npm run build`.

To run it: `npm run start:dev`

To check the lint: `npm run lint`

To build the Docker image: `docker build -t notif-bot:latest .`

To run the Docker image (after building): `docker run --rm -it -v $(pwd)/config:/bot/config notif-bot:latest`
*Note that this will require a `config/production.yaml` file to exist as the Docker container runs in production mode.*

### Configuration

This project uses a package called `config` to manage configuration. The default configuration is offered
as `config/default.yaml`. Copy/paste this to `config/development.yaml` and `config/production.yaml` and edit
them accordingly for your environment.
