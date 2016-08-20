# docker-mail-forwarder
Simple abstraction over postfix for mail forwarding.

This project is inspired by Zixia SMF (https://hub.docker.com/r/zixia/simple-mail-forwarder/).

The only purpose is for self-education about Docker/Postfix/Linux, so do not expect to much ;)

## Configuration

Work in progress... For the moment it's just a bunch of ideas

Create an *mailAlias* file in the *config* directory with this format:
  
    aliases: 
      - 
       alias1@domainFrom: 
          - dest1
          - dest2
      - 
        alias2@domainFrom: 
          - dest1
          - dest3
      - 
        alias3@domainFrom: dest1
    update: auto # Comment to disable auto-update of postfix config

## Running

Use docker-compose. The config directory is shared

## Todo

1. Install and configure postfix from alpine
2. Use configuration file to configure postfix for mail forwarding
3. Detect configuration change to automatically update postfix
4. Make the auto-update optional
