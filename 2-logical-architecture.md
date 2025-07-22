# Logical Architecture

This section provides an overview of the logical architecture of an electronic health record (EHR) which uses CDS.

In particular, it focuses on the logical architecture of[ knowledge-based CDSSs](#user-content-fn-1)[^1], which use pre-loaded CDS artifacts (such as rules and guidelines) that closely match a human's natural reasoning process. Non-knowledge-based CDSSs, which use artificial intelligence (AI) or machine learning to acquire knowledge over time, are outside the scope of this guide.

The logical architecture of knowledge-based CDSSs are explored in the following subsections.

## EHR System Architecture

To understand how clinical decision support (CDS) works, it is important to understand how CDS fits within the logical architecture of an [EHR](https://confluence.ihtsdotools.org/display/DOCGLOSS/EHR) system. This section describes the major architectural components of an EHR system, and the interactions between these components.

### Major Components <a href="#id-2.1.ehrsystemarchitecture-majorcomponents" id="id-2.1.ehrsystemarchitecture-majorcomponents"></a>

Table: Descriptions of the major architectural components of an EHR system

<table><thead><tr><th width="222.203125">EHR System Component</th><th>Description</th></tr></thead><tbody><tr><td><img src="https://confluence.ihtsdotools.org/download/thumbnails/123897453/image2016-11-8%2010%3A57%3A46.png?version=1&#x26;modificationDate=1615403803000&#x26;api=v2" alt=""><br><a href="https://app.gitbook.com/o/h8Z6qGxuQrzM9vbx5bPT/s/CEAcChvWjWEu16YmwNrz/"><strong>User Interface</strong></a></td><td>The user interface (UI) is a fundamental component of almost any clinical application, and is used within an EHR to both enter and display patient health records. The UI also has two main CDS functions. Firstly, the UI is used to provide inputs to the CDSS, such as recording a proposed medication or an observed finding. The second function of the UI is to display alerts, advisories and clinical guidelines to the user in an appropriate format, on behalf of the CDSS.</td></tr><tr><td><img src="https://confluence.ihtsdotools.org/download/thumbnails/123897453/image2016-11-8%2010%3A57%3A54.png?version=1&#x26;modificationDate=1615403803000&#x26;api=v2" alt=""><br><strong>Record Services</strong></td><td>Record services are a set of services for managing patient health records. Record services provide functions like entering data into health records, searching for and retrieving health records, querying or extracting data from health records, and communicating or exchanging health records with other systems or applications. Record services interact with other components in this model such as the CDSS and the UI.</td></tr><tr><td><img src="https://confluence.ihtsdotools.org/download/thumbnails/123897453/image2016-11-8%2010%3A58%3A2.png?version=1&#x26;modificationDate=1615403803000&#x26;api=v2" alt=""><a href="https://app.gitbook.com/o/h8Z6qGxuQrzM9vbx5bPT/s/t4wRQcj6gyQPunraJrP0/"><strong>Terminology Services</strong></a></td><td>Terminology services are those services that directly manage the terminology resources. They include functions like querying concepts, relationships and reference sets, and installing or updating SNOMED CT from release files. Terminology services interact with the CDSS component in this model.</td></tr><tr><td><img src="https://confluence.ihtsdotools.org/download/thumbnails/123897453/image2016-11-8%2010%3A58%3A35.png?version=1&#x26;modificationDate=1615403803000&#x26;api=v2" alt=""><strong>Clinical Decision Support System</strong></td><td>The primary role of the CDSS is to execute the decision support logic. The CDSS does this using a number of subcomponents and subprocesses, which will be described in the next section - CDS System Architecture. The CDSS interacts with each of the other major components in the EHR.</td></tr></tbody></table>

### Interactions

The major architectural components of an EHR system that incorporates CDS interact with each other in a variety of ways to support the overall functioning of the EHR. The diagram below uses orange arrows to illustrate the primary interactions between these EHR components.

<figure><img src="images/123897454.png" alt=""><figcaption><p>EHR components and key interactions</p></figcaption></figure>

As shown above, the UI communicates with the record services to facilitate the storage and subsequent retrieval of health record data. The UI also provides inputs to the CDSS and displays alerts and guidelines on its behalf. The CDSS uses the inputs from the UI and data from the record and terminology services to processes decision support rules. The CDSS uses the inputs from the record and terminology services to determine whether or not the CDS conditions have been met, and if so then CDS interventions, such as alerts or knowledge resources, are delivered back to the UI. The internal components and processes of the CDSS will be described in more detail in the next section.

## CDS System Architecture

This section describes the major architectural components of a CDSS and explores how they work together with the components of an EHR, as described in [ EHR System Architecture](2-logical-architecture.md#ehr-system-architecture).

### Major Components <a href="#id-2.2.cdssystemarchitecture-majorcomponents" id="id-2.2.cdssystemarchitecture-majorcomponents"></a>

Table: Descriptions of the major architectural components of a CDSS

<table><thead><tr><th width="161.48046875">CDSS Component</th><th>Description</th></tr></thead><tbody><tr><td><img src="https://confluence.ihtsdotools.org/download/thumbnails/123897466/image2016-11-8%2011%3A16%3A8.png?version=1&#x26;modificationDate=1615403804000&#x26;api=v2" alt=""><a href="https://confluence.ihtsdotools.org/display/DOCCDS/3.+Knowledge+Base"><strong>Knowledge Base</strong></a></td><td><p>The knowledge base (KB) stores clinical knowledge developed by domain experts as CDS artifacts. These knowledge artifacts (e.g. rules and guidelines) are stored in a machine processable format and made available to the inference engine to drive the CDS workflow.</p><p>For additional information on this component please refer to the <a href="https://confluence.ihtsdotools.org/display/DOCCDS/3.+Knowledge+Base">Knowledge Base</a> section.</p></td></tr><tr><td><img src="https://confluence.ihtsdotools.org/download/thumbnails/123897466/image2016-11-8%2011%3A16%3A15.png?version=1&#x26;modificationDate=1615403804000&#x26;api=v2" alt=""><a href="https://confluence.ihtsdotools.org/display/DOCCDS/4.+Inference+Engine"><strong>Inference Engine</strong></a></td><td><p>The inference engine processes the CDS knowledge artifacts, using information from the record services, the terminology services and user input to execute the CDS logic. A key part of this process is to determine which actions should be performed, based on the given patient's circumstances.</p><p>For additional information on this component please refer to the <a href="https://confluence.ihtsdotools.org/display/DOCCDS/4.+Inference+Engine">Inference Engine</a> section.</p></td></tr><tr><td><img src="https://confluence.ihtsdotools.org/download/thumbnails/123897466/image2016-11-8%2011%3A16%3A39.png?version=1&#x26;modificationDate=1615403804000&#x26;api=v2" alt=""><a href="https://confluence.ihtsdotools.org/display/DOCCDS/5.+Communications"><strong>Communications</strong></a></td><td><p>The communications mechanism is responsible for accepting inputs from the user and delivering the outcomes of the inference engine back to the user. For example, when a clinician prescribes a drug, this information is communicated to the inference engine as an input. If the inference engine discovers that the medication is contraindicated, the communications mechanism will deliver an alert to the user interface.</p><p>For additional information on this component please refer to the<a href="https://confluence.ihtsdotools.org/display/DOCCDS/5.+Communications"> Communications</a> section.</p></td></tr></tbody></table>

### Logical Architecture

The diagram below illustrates how the components of the CDSS (shown in the blue box) work together with the components of the EHR system (shown in the red box).

<figure><img src="images/123897780.png" alt=""><figcaption><p>CDSS components and key interactions</p></figcaption></figure>

Internal CDSS interfaces are represented by the green directional arrows, while external CDSS interfaces are represented by the orange arrows. Note that the inference engine interfaces directly with record and terminology services while communications, which is focused on the delivery of CDSS inputs and outputs, interfaces directly with the user interface.

[^1]: [https://en.wikipedia.org/wiki/Clinical\_decision\_support\_system#Knowledge-based\_CDSS](https://en.wikipedia.org/wiki/Clinical_decision_support_system#Knowledge-based_CDSS)
