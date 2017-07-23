# gates

## Description

Many systems cannot send data, directly to Kronometrix. These systems use and provide different interfaces and protocols which are incompatible with Kronometrix data message structure. In order to inter-connect wth such systems, Kronometrix is offering the concept of data input gate. 

A Kronometrix gate, is a data input point, capable to receive, filter and convert native, specific traffic into Kronometrix data, as one or many data messages. There can be different types of gates: MQTT, AviMet, DDS, Feedliner. Each gate is responsible for different type of data traffic.

![Gates](http://www.kronometrix.org/kgte.svg)

## Types

Currently we support the following type of gate systems: Vaisala AviMet, IoT based based systems using DDS, MQTT protocols. Each gate has it own set of settings and binaries. 

### AviMet Gate

For more information please check [AviMet repository](https://github.com/kronometrix/avimet), describing all functionality of a Vaisala AviMet gate.
