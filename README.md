<p align="center">
  <img width="256" height="256" src="extras/space.png">
  <br><br>
  <b>Sputnik</b><br>
</p>

The idea with Sputnik is to provide an easily deployed and performant monitoring agent for executing health probes and relaying health data. It's also a framework for building plugins.

**Key strengths**

- Lightweight & performant:
  - Native plugins are loaded into memory on startup: no expensive script execution necessary.
  - Uses an event loop for handling monitoring requests and is capable of high, inexpensive concurrency.
- Redundant & scalable:
  - Multiple Sputnik instances connected to a RabbitMQ cluster provides both increased monitoring capacity as well as redundancy.
- Secure:
  - Uses TLS for authentication and communication security for services in its control
  - Input data is validated against the accessed plugin's schema, both for Native and Foreign (such as Nagios scripts) plugins.
- Flexible:
  - Configurable modes
  - Platform independent


**Progress/Modes**

- [ ] Server: Takes monitoring requests from a Sputnik TCP client – WIP
- [ ] Dispatch: Consumes monitoring requests or responses from a message broker
- [ ] Relay: Consumes monitoring responses from a message broker
- [ ] Publisher: Sends results of health checks initiated by Sputnik to RabbitMQ or another Sputnik server
- [ ] Router: Routes requests and results to other Sputnik servers or message brokers

**Progress/Clients**

- [ ] Python client – WIP
- [ ] Golang client

**Progress/Other**

- [ ] Plugin system – WIP
- [ ] Scheduler



Development status
---

pre-alpha, not even close to feature-complete.

Author
------

Robert Wikman \<rbw@vault13.org\>
