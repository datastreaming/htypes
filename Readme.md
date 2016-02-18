# Overview
This projects describes currently used and agreed message formats for data streaming (at PSI).

In general, data is streamed via ZMQ multipart messages. A logical message consists of at least "two" parts, [[header][content]].

The header of a message holds arbitrary JSON encoded metadata to the data transmitted via the message.
A message and the header attributes is/are identified by the attribute __htype__ (this is the so called *Base Header*). Usually __htype__ strings look like this: __name-1.0__. The htype name specifies and identifies the content and the structure of the message.

The actual data is transferred in the content part. The data can be split into one or more sub-messages. Sub-messages can either contain raw bytes as well as more sub-headers (JSON, UTF-8).

## Base Header

Basically all message header data is optional, however to be able to write services that can perform different type of operations on different message types at least following header attributes have to be provided.

| Name | Type | Default | Comment |
| ---- | ---- | ------- | ------- |
| htype | String | "" | Header compliant to specifications ...|
