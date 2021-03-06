---
title: "Windows Setup"
permalink: /docs/windows-setup/
excerpt: "Intro to City Scrapers"
last_modified_at: 2018-10-04T20:15:56-04:00
toc: false
---

This tutorial uses Codeanywhere as an alternative to developing on Windows. Codeanywhere runs a Virtual Private Server with its own RAM, disk space and processing power. We'll set up a Linux development environment in a Codeanywhere container to clone the project in.

## Setup Codeanywhere

1. Get a free tier Codeanywhere account at [https://codeanywhere.com/signup](https://codeanywhere.com/signup)
2. Login to Codeanywhere
3. Start a new Container by going to File -> New Connections -> Container.
4. Choose the **Blank: Ubuntu 14.04** container. Name it something that makes sense to you.
5. Wait for the container to deploy, and close out of the welcome message to switch to the terminal window. (If you ever exit out of your terminal, just right click on your Container under Connections and select "SSH Terminal")

## Environment setup and installation

This command runs all of the setup commands at once. Copy and right click to paste into your terminal:

```bash
source <(curl -s https://gist.githubusercontent.com/pjsier/06c03529c8cde7255f2ea0c3dd2d7e7c/raw/9784f283f32073d5e2a83f90b31d70f8b9e0111b/city_scrapers_setup.sh)
```

## Next steps

1. Create your virtual environment:

```shell
$ python3.6 -m venv venv
$ source venv/bin/activate
```

**Note:** these steps differ from those in [Installation](/docs/development#installation). The only difference is that you are using `venv` to set up your virtual environment and specifying which Python 3 version you are using (3.6).

Once you've activated your virtual environment, you should see it appear in parenthesis - named `venv` here:

```shell
(venv) $
```

To deactivate, type `deactivate`. To activate it, re-run the `source venv/bin/activate` command. You'll want to activate the virtual environment when developing for the City Scrapers project.

2. Continue on with the rest of [Installation](/docs/development#installation). You will need to clone your repository and install the requirements in your virtual environment.
