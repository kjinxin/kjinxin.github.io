---
layout: post
comments: true
categories: diary
title: SOAP/WSDL
---
## Instruments on SOAP/WSDL
WSDL: Web Services Description Language

SOAP: Simple object access protocal

Element Name	Description in WSDL
types:	A container for abstract type definitions defined using XML Schema

message:	A definition of an abstract message that may consist of multiple parts, each part may be of a different type

portType:	An abstract set of operations supported by one or more endpoints (commonly known as an interface); operations are defined by an exchange of messages

binding:	A concrete protocol and data format specification for a particular portType

service:	A collection of related endpoints, where an endpoint is defined as a combination of a binding and an address (URI)
