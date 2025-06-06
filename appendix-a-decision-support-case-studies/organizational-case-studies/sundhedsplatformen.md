# Sundhedsplatformen

# Overview

Sundhedsplatformen[2](https://confluence.ihtsdotools.org/display/DOCCDS/Sundhedsplatformen#Footnote2 "Footnote: Click here to display the footnote") which translates to _the health platform_ , is a jurisdictional electronic health record (EHR) in Denmark with decision support capabilities. The system, provided by Epic, operates in the Capital and Sealand regions of Denmark, which cover a population of approximately 2.6 million people (almost half of the population of Denmark). The system uses SNOMED CT as the basis for its diagnosis-related decision support services. The first clinical rollout of the system was performed in May 2016. When the rollout is complete at the end of 2017, the system will provide services for up to 45,000 clinical users. 

# Standards and Technology

One of the design considerations of this system is to capture and store clinical data as structured content ( as opposed to unstructured or free text). This use of structured health data reduces the need for mapping and creates many opportunities including clinical decision support. In terms of terminology, Denmark’s national classification system, called _Sundhedsvæsenets Klassifikations System_ (SKS) , is based on ICD-10 and a range of other classification systems. Traditionally, SKS has been used for statistical aggregation and for billing purposes. Although not designed for clinical use, SKS was selected as the primary classification system for the Sundhedsplatformen project to maintain the legacy requirements associated with billing and classification. There was therefore a need to represent both procedures and diagnoses within SKS.

# Use of SNOMED CT

It is worth noting that SNOMED CT is already used in many existing clinical databases and registries throughout Denmark. So from an interoperability perspective, there was incentive for the regional EHR to incorporate SNOMED CT in its implementation approach. As previously mentioned, Epic’s diagnosis-related decision support system is widely based on SNOMED CT. For example, the ability to traverse SNOMED CT’s hierarchy is a key component of all diagnosis-related decision support in the Epic system.[3](https://confluence.ihtsdotools.org/display/DOCCDS/Sundhedsplatformen#Footnote3 "Footnote: Click here to display the footnote") Since the region chose SKS as the classification system, there was a need to map their local concepts to SNOMED CT to be able to perform decision support. Over 20,000 diagnosis concepts from SKS were mapped to SCT over a period of 8 months. The mapping was performed through several steps, the first of which was based on the international SNOMED CT to ICD-10 map. Compared to the alternative (i.e. mapping from scratch), this approach was a major help and significantly increased the speed and ease of the mapping process.

* * *

Footnotes Ref | Notes  
---|---  
[1](https://confluence.ihtsdotools.org/display/DOCCDS/Sundhedsplatformen#FootnoteMarker1-0 "Footnote: Click to return to reference in text") |  <https://www.regionh.dk/sundhedsplatform/om-sundhedsplatformen/Sider/default.aspx>  
[2](https://confluence.ihtsdotools.org/display/DOCCDS/Sundhedsplatformen#FootnoteMarker2-0 "Footnote: Click to return to reference in text") |  Case study uses content from  [Sundhedsplatformen presentation](https://infocentral.infoway-inforoute.ca/en/resources/docs/snomedct/presentations/1023-kitta-lawton-and-gert-galster-presentation-may-17-2016) for Canada Health Infoway, May 17, 2016 . (Account needed to access file.)   
[3](https://confluence.ihtsdotools.org/display/DOCCDS/Sundhedsplatformen#FootnoteMarker3-0 "Footnote: Click to return to reference in text") |  <https://galster.dk/gert/docs/20161013_ESObs_Sundhedsplatformen.pdf>
