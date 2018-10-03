# Databus

## Description

Many systems cannot send data, directly to Kronometrix. These systems use and provide different interfaces and protocols which are incompatible with Kronometrix data message structure. In order to inter-connect wth such systems, Kronometrix is offering the concept of a data bus.

A Kronometrix databus, is a complete system, capable to receive, filter and convert native, specific traffic into Kronometrix data, as one or many data messages. There can be different types of databuses: MQTT, AviMet, DDS, Feedliner. Each databus is responsible for different type of data traffic, its own validation and convertion. A databus can scale horizontaly, to accomodate more traffic, if required.

![Gates](http://www.kronometrix.org/kgte.svg)


## Functions

These are the main functions a databus is offering:

 * no Kronometrix authentication services are offered. It does a simple check on the data received to check a specific condition, a regex, or some pattern and if found valid will be formatted into valid Kronometrix data message(s)
 
 * as soon as we have a valid Kronometrix data message(s), these will be send forward to Kronometrix Auth module for proper, authentication & authorization
 
 * maintains a status of all requests, for example if one requests has been denied proper authentication

 * does not validate a Kronometrix SID or TID

 * does not offer any Kronometrix authorization, authentication mechanism
 

## Configuration

A Kronometrix databus has a configuration file, and it has its own set of binaries.


## Types

Currently we support the following type of databus systems: Vaisala AviMet, IIoT based based systems using DDS, MQTT protocols.

### AviMet Databus

For more information please check [AvMet repository](https://github.com/kronometrix/avmet), describing all functionality of a Vaisala AviMet databus.
