# Thunor Web Quickstart

[Thunor Web](https://github.com/alubbock/thunor-web) is a web application for
analyzing and visualizing high throughput cell proliferation data. For more
information, see the [Thunor website](https://www.thunor.net) or the
[Thunor Web documentation](https://docs.thunor.net).

Thunor Web can be deployed using
[Docker Compose](https://docs.docker.com/compose/). This repository contains
an example configuration which you can use to run Thunor Web on any
machine with Docker Compose installed.

## Pre-requisities

* **Docker** and **Docker Compose** (version 1.12 or later). Follow instructions for your platform:
    * [Docker for Windows](https://docs.docker.com/docker-for-windows/), which includes Docker Compose.
    * [Docker for Mac](https://docs.docker.com/docker-for-mac/), which includes Docker Compose.
    * Ubuntu 18.04 or later: `sudo apt install docker-compose`
    * Other platforms: [Docker installation instructions](https://docs.docker.com/install/)
* **Python**. Python 3.6 or later recommended, but other versions will probably work - it is only used for the configuration script.
* **Git**. If you're not sure if you have git, it will be provided with the Anaconda download in the previous step.

## Quick start

1. Download this repository:

    git clone https://github.com/alubbock/thunor-web-quickstart thunorweb
    cd thunorweb

2. Run the deploy script:

    python thunorctl.py deploy

That's it! Thunor Web will now be running on your machine, accessible at
http://localhost (replace `localhost` with the hostname). Simply open
a web browser to that address.

## Next steps

You'll want to set up an admin account so you can log in:

    python thunorctl.py createsuperuser

If you're planning on deploying Thunor Web on any network
accessible server, we highly recommend [enabling TLS encryption](https://docs.thunor.net/enable-https-encryption).

## Other options

If you're interested in editing the source code for Thunor Web,
you'll want to use the [developer installation](https://docs.thunor.net/developer-installation)
instead.

If you're instested in deploying Thunor Web to remote hosts,
you can either remotely log in (e.g. via SSH) and use the
sequence of commands described above, or you can use
[Docker Machine](https://docs.docker.com/machine/overview/),
which allows remote provisioning to cloud providers including
Azure, AWS, and Digital Ocean. This is described in
[remote installation](https://docs.thunor.net/remote-installation).
