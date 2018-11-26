# Corda Single Node Guide

This guide is for explaining how to set up a new Corda node, using our Azure marketplace solution, and connecting to an already existing Corda network. This network must already have a Network Map in place, as this is necessary in joining a network. You can see our solution for that, [here](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/bcs-technology.bcs-corda-netmap?tab=Overview).

## Required Setup

Before using our solution, you need to have a bundle prepared which includes files used for configurations.

```
bundle
  │
  ├─ certificates
  │      │
  │      ├─ nodekeystore.jks
  │      ├─ sslkeystore.jks
  │      └─ truststore.jks
  │
  ├─ cordapps
  │      │
  │      └─ any cordapp jars
  │
  └─ node.conf
```

The certificates are given by the network map. The `node.conf`s `compatibilityZoneURL` needs to be set using the network map's url.
