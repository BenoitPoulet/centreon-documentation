---
id: hardware-pdu-emerson-snmp
title: Emerson PDU
---

| Current version | Status | Date |
| :-: | :-: | :-: |
| 3.2.0 | `STABLE` | Oct  4 2019 |

## Prerequisites

### Centreon Plugin

Install this plugin on each needed poller:

``` shell
yum install centreon-plugin-Hardware-Pdu-Emerson-Snmp
```

## SNMP

Connect to your PDU Emerson and configure SNMP.

## Centreon Configuration

### Create a new PDU Raritan host

Go to *Configuration \> Hosts* and click *Add*. Then, fill the form as shown by
the following table:

| Field                                | Value                      |
| :----------------------------------- | :------------------------- |
| Host name                            | *Name of the host*         |
| Alias                                | *Host description*         |
| IP                                   | *Host IP Address*          |
| Monitored from                       | *Monitoring Poller to use* |
| Host Multiple Templates              | HW-Pdu-Emerson-SNMP-custom |

Click on the *Save* button.

