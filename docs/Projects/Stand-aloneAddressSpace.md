# Object-Oriented Internet - Stand-alone Address Space <!-- omit in toc -->

## Table of Contents <!-- omit in toc -->

- [Keywords](#keywords)
- [Executive Summary](#executive-summary)
- [Subject](#subject)
- [Goal](#goal)
- [Scope](#scope)
- [Related work](#related-work)
- [See also](#see-also)

## Keywords

`OPC UA`, `Information Model`, `Address Space`, `Digital Twin`, `Process Observer`, `State Observer`

## Executive Summary

An important issue for process control is to restore its state and behavior so as to guarantee appropriate quality indicators. The main goal of the project is to prove that a stand-alone implementation of the OPC UA Address Space concept is possible so that it can be used for selected purposes requiring real-time creation of an information replica of an external process.

## Subject

Computer science is a research discipline of using computers to process information. One of the domains of application is real-time process automation. In this approach, an important issue is to restore the state and behavior of the process for the purposes of the process control so as to guarantee appropriate quality indicators. There are many concepts known from the literature, including OPC UA Address Space, Digital Twin, Process Observer, State Observer, etc. Each of these concepts has its advantages and disadvantages that will be investigated in this project. OPC UA Address Space seems to be the most promising, however, this concept is currently used only as a component embedded in the communication server.

## Goal

The main goal of the project is to prove that a stand-alone implementation of the OPC UA Address Space concept is possible so that it can be used for selected use cases requiring the real-time creation of an external process information replica. The selected use cases include but it is not limited to

- control, monitoring, visualization of industrial processes,
- the transmission of process data via computer networks,
- interoperability with a variety of Service Bus concept implementations,
- archiving of process data with the use of various data repositories.

## Scope

As part of the project, references containing a description of the OPC UA Address Space concept, including the OPC UA specification, articles describing this concept, etc., will be selected and analyzed. An important contribution of the project is also the selection and analysis of available implementations of this concept, which will serve as reference solutions. Since the purpose of the project is to implement a certain concept, it will be necessary to select the design environment that will be used to achieve this goal. Then, these tools will be used to implement the OPC UA Address Space concept as an independent library so that it can be reused in various applications. As confirmation of the correctness of the proposed approach, two selected library use cases will be implemented.

Finally, as a result of the project, an independent library will be developed in the selected technology. Its public interface (API) will at least comply with the needs of research resulting from the analysis of selected applications. The API may contain additional elements resulting from the needs indicated in the analytical part. The correctness of the implementation of the concept will be confirmed by the implementation of independent solutions (proof of concept). These implementations will serve as a kind of integration test. The correctness of individual parts of the library will be verified using unit tests.

## Related work

The project is to be harmonized with the Master's Thesis of my student.  The implementation of the Address Space is to be derived from the following existing libraries. The main goal of harmonization is to make sure that the library will be reused by all the mentioned applications.

- [UAModelDesignExport Library](https://github.com/mpostol/OPC-UA-OOI/tree/master/SemanticData/UAModelDesignExport#uamodeldesignexport-library)
- [Address Space Management Implementation](https://github.com/mpostol/OPC-UA-OOI/tree/master/SemanticData/UANodeSetValidation#address-space-management-implementation)
- [Address Space Model Designer](https://github.com/mpostol/ASMD)  - browse option
- [mpostol/UA-.NETStandard](https://github.com/mpostol/UA-.NETStandard)
- [mpostol/UA-ModelCompiler](https://github.com/mpostol/UA-ModelCompiler)

## See also

- [GitHub project entry](https://github.com/mpostol?tab=projects#:~:text=SemanticData.AddressSpace)
- Mariusz Postol, [Machine to Machine Semantic-Data Based Communication: Comprehensive Survey](https://www.researchgate.net/publication/331633195_Machine_to_Machine_Semantic-Data_Based_Communication) in [Computer Game Innovations 2018](https://www.researchgate.net/publication/335524620_Computer_Game_Innovations_2018), Publisher: Lodz University of Technology Press; ISBN: 978-83-7283-999-2
- Postół M. (2020) Object-Oriented Internet Reactive Interoperability. In: Krzhizhanovskaya V. et al. (eds) Computational Science – ICCS 2020. ICCS 2020. Lecture Notes in Computer Science, vol 12141. Springer, Cham; [DOI: https://doi.org/10.1007/978-3-030-50426-7_31](https://doi.org/10.1007/978-3-030-50426-7_31)
  - Postół M. (2020) [Object-Oriented Internet Reactive Interoperability](https://www.researchgate.net/publication/341882427_Object-Oriented_Internet_Reactive_Interoperability), presentation, DOI: 10.13140/RG.2.2.33984.56323
- [UAModelDesignExport Library](https://github.com/mpostol/OPC-UA-OOI/tree/master/SemanticData/UAModelDesignExport#uamodeldesignexport-library)
- [Address Space Management Implementation](https://github.com/mpostol/OPC-UA-OOI/tree/master/SemanticData/UANodeSetValidation#address-space-management-implementation)
