# gates

## Description

Many systems cannot send data, directly to Kronometrix. These systems use and provide different interfaces and protocols which are incompatible with Kronometrix data message structure. In order to inter-connect wth such systems, Kronometrix is offering the concept of data input gate. 

A Kronometrix gate, is a data input point, capable to receive, filter and convert native, specific traffic into Kronometrix data, as one or many data messages. There can be different types of gates: MQTT, AviMet, DDS, Feedliner. Each gate is responsible for different type of data traffic.

![Gates](http://www.kronometrix.org/kgte.svg)


## Functions

 * A gate does not authenticate requests as Auth module does. It does a simple check on the data received to check a basic regex, or some other condition and if found valid will be formatted in K messages to be send forward to Kronometrix Auth module for authentication.

 * A gate does not validate a SID or TID

 * A gate does not offer any Kronometrix authorization, authentication mechanism
 

## Types

Currently we support the following type of gate systems: Vaisala AviMet, IoT based based systems using DDS, MQTT protocols. Each gate has it own set of settings and binaries. 

### AviMet Gate

For more information please check [AviMet repository](https://github.com/kronometrix/avimet), describing all functionality of a Vaisala AviMet gate.
