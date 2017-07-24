# gates

## Description

Many systems cannot send data, directly to Kronometrix. These systems use and provide different interfaces and protocols which are incompatible with Kronometrix data message structure. In order to inter-connect wth such systems, Kronometrix is offering the concept of data input gate, simple a gate.

A Kronometrix gate, is a data input point, capable to receive, filter and convert native, specific traffic into Kronometrix data, as one or many data messages. There can be different types of gates: MQTT, AviMet, DDS, Feedliner. Each gate is responsible for different type of data traffic, its own validation and convertion. A gate can scale horizontaly, to accomodate more traffic, if required.

![Gates](http://www.kronometrix.org/kgte.svg)


## Functions

These are the main functions a gate is offering:

 * no Kronometrix authentication services are offered. It does a simple check on the data received to check a specific condition, a regex, or some pattern and if found valid will be formatted into valid Kronometrix data message(s)
 
 * as soon as we have a valid Kronometrix data message(s), these will be send forward to Kronometrix Auth module for proper, authentication & authorization
 
 * maintains a status of all requests, for example if one requests has been denied proper authentication

 * does not validate a Kronometrix SID or TID

 * does not offer any Kronometrix authorization, authentication mechanism
 

## Configuration

A Kronometrix gate has a configuration file, and it has its own set of binaries. For example if we have deployed two types of gates, we should have 2 gate pckages, each with its own configuration file. A configuration file should simple be a text file, which can offer a very basic pattern check mechanism for gate incoming traffic. (kavmet-1.0.1-freebsd10.3-amd64.txz kmqtt-1.0.2-freebsd10.3-amd64.txz)


## Types

Currently we support the following type of gate systems: Vaisala AviMet, IoT based based systems using DDS, MQTT protocols. Each gate has it own set of settings and binaries.

### AviMet Gate

For more information please check [AviMet repository](https://github.com/kronometrix/avimet), describing all functionality of a Vaisala AviMet gate.
