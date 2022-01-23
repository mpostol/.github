# Machine to Sensors (M2S) connectivity based on Process-Observer <!-- omit in toc --> 

## Table of Contents <!-- omit in toc -->

- [Keywords](#keywords)
- [Executive Summary](#executive-summary)
- [Subject](#subject)
- [Goal](#goal)
- [Scope](#scope)
- [Related work](#related-work)
- [See also](#see-also)

## Keywords

`OPCUA`, `Process-Observer`, `PubSub`, `Producer`, `Reactive communication`, `ReactiveX`

## Executive Summary

According to the [Reactive Networking of Semantic-Data Library](https://commsvr.gitbook.io/ooi/reactive-communication/semanticdata) architecture, the bindings between the local repository `DataRepository` (i.e. a real-time process replica) and the message content items are provided by the `IBinding` interface and its basic implementation `Binding` class. This class is responsible to decode the data from the format used to construct the message to the syntax required by the local type. It is assumed that `IBinding` abstraction can be applied to provide interconnection with a vast variety of data sources and destinations, including plant floor devices.

The main goal of this project is to prove that the implementation of the `Producer` role fetching data from `Process-Observer` will make the OPC UA Machine to Sensors Connectivity (M2S) possible. Converging results of this project and [Networking.Gateway2Azure][Networking.Gateway2Azure] will make Cloud to Sensors (C2S) connectivity possible.

To get more check out the [project description](https://github.com/mpostol?tab=projects#:~:text=Networking.ProcessObserverProducer)

## Subject

According to the [Reactive Networking of Semantic-Data Library](https://commsvr.gitbook.io/ooi/reactive-communication/semanticdata) architecture, the bindings between the local repository `DataRepository` (i.e. a real-time process replica) and the message content items are provided by the `IBinding` interface and its basic implementation `Binding` class. This class is responsible to decode the data from the format used to construct the message to the syntax required by the local type. It is assumed that `IBinding` abstraction can be applied to provide interconnection with a vast variety of data sources and destinations, including plant floor devices.

Process-Observer is an archetype that allows creation consistent, homogeneous real-time representation of the underlying process. This representation is a kind of a process state and behavior replica, which exposes real-time process data to the network using standardized interfaces like OPC Classic, OPC Unified Architecture, OPC PubSub, AMQP, MQTT, etc. In other words, it supports Machine to Sensors Connectivity (M2S) paradigms, i.e. it allows an open, uniform, secure and standards-based communication solution between sensors, actuators, controllers and the upper layer applications.

Process-Observer has been implemented and published as the [Open-Source Software](https://github.com/mpostol/ProcessObserver) \(\#OSS\). This implementation of the Process-Observer was deployed by [CAS in many highly distributed and demanding applications][OOI] in the production environment. Therefore it is a good candidate to be used as the data source for reactive communications implemented in this library according to the OPC UA PubSub.

## Goal

The main goal of this project is to prove that the implementation of the `Producer` role fetching data from `Process-Observer` will make the OPC UA Machine to Sensors Connectivity (M2S) possible. Converging results of this project and [Networking.Gateway2Azure][Networking.Gateway2Azure] will make Cloud to Sensors (C2S) connectivity possible.

## Scope

- create a VS project encapsulating the implementation of the `Process-Observer` connectivity
- define an interface representing `Process-Observer` API
- implement the `Producer` against this interface to provide `Process-Observer` connectivity
- adopt the implementation of the `Process-Observer` to be compliant with this project, e.g. harmonize target framework
- publish the `Process-Observer` as the NuGet package
- consider using [The Reactive Extensions for .NET \( ReactiveX\)][ReactiveX] to push data from `Process-Observer` to the `Producer` instance using the observer pattern
- harmonize the configuration of both frameworks
- update existing documentation and add a relevant description to the project eBook

## Related work

- [Process Observer - Main Technology Features](https://commsvr-com.github.io/Documentation/CommServer)
- [Process Observer GitHub Repository][PO]

## See also

- Postół M., Szymczak P. (2021) Object-Oriented Internet Cloud Interoperability. In: Paszynski M., Kranzlmüller D., Krzhizhanovskaya V.V., Dongarra J.J., Sloot P.M. (eds) Computational Science – ICCS 2021. ICCS 2021. Lecture Notes in Computer Science, vol 12745. Springer, Cham. <https://doi.org/10.1007/978-3-030-77970-2_43>
  - Available on [ResearchGate](https://www.researchgate.net/publication/352289895_Object-Oriented_Internet_Cloud_Interoperability)
  - ICCS 2021: INTERNATIONAL CONFERENCE ON COMPUTATIONAL Presentation is available on [YouTube](https://youtu.be/yXH09wuWEcA)
- Mariusz Postol, [Object Oriented Internet][OOI], [3rd International Conference on Innovative Network Systems and Applications](https://fedcsis.org/2015/inetsapp), 2015, [IEEE Xplore Digital Library][OOI] [![DOI](https://img.shields.io/badge/DOI-10.15439%2F2015F160-blue)](https://fedcsis.org/proceedings/2015/pliks/160.pdf)
- [Object-Oriented Internet - reactive visualization of asynchronous data using AZURE services \(Networking.Gateway2Azure\)][Networking.Gateway2Azure]
- [The Reactive Extensions for .NET \( ReactiveX\)][ReactiveX]

[OOI]:https://ieeexplore.ieee.org/abstract/document/7321562
[PO]:https://github.com/mpostol/ProcessObserver
[Networking.Gateway2Azure]:https://www.researchgate.net/publication/352289895_Object-Oriented_Internet_Cloud_Interoperability
[ReactiveX]:http://reactivex.io/
