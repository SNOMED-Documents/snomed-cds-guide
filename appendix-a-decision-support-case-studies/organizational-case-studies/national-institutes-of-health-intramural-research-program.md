# National Institutes of Health: Intramural Research Program

{% hint style="info" %}
The Intramural Research Program is the internal research program of the National Institutes of Health. With 1,200 Principal Investigators and more than 4,000 Postdoctoral Fellows conducting basic, translational, and clinical research, [the IRP is the largest biomedical research institution on earth](#user-content-fn-1)[^1].\\

For more information please visit: [https://www.nih.gov/](https://www.nih.gov/).
{% endhint %}

## Overview

The [National Institutes of Health](https://www.nih.gov/) (NIH) is a federally sponsored biomedical research program in the United States. [The NIH is made up of 27 separate institutes and centers.](#user-content-fn-2)[^2] The [Intramural Research Program's](https://irp.nih.gov/about-us/what-is-the-irp) (IRP) [programs are embedded in 24 of the NIH Institutes](#user-content-fn-3)[^3]. One of those institutes, the [National Library of Medicine](https://www.nlm.nih.gov/) (NLM) is the world's largest biomedical library and the SNOMED CT National Release Center for the United States. The NLM curates an extensive collection of medical knowledge in various formats which is used by millions of people around the world. Across the IRP, some of their Principal Investigators (PIs) use SNOMED CT in their research. A selection of the Intramural Research Program's initiatives which relate to SNOMED CT and CDS, are briefly described below.

## Value Set Authority Center

The [Value Set Authority Center](https://vsac.nlm.nih.gov/) (VSAC),[ managed by the NLM, is a service designed to maintain and distribute the value sets defined in](#user-content-fn-4)[^4] [electronic Clinical Quality Measures](https://ecqi.healthit.gov/ecqms) (eCQMs). Each VSAC value set consists of codes and terms from clinical vocabularies such as SNOMED CT, RxNorm, LOINC and ICD-10-CM . Value sets derived from SNOMED CT are used to support the calculation of data quality measures which in turn provide feedback to clinicians about the quality of care. Note that VSAC is a project administered by NLM, but the actual data quality computations are done at individual healthcare sites.

<figure><img src="../../images/123897697.png" alt=""><figcaption><p>VSAC NLM Value Set Repository</p></figcaption></figure>

## Medline Plus Connect

[Medline Plus Connect](https://medlineplus.gov/connect/overview.html) is an [Infobutton](http://www.hl7.org/implement/standards/product_brief.cfm?product_id=208) resource which accepts requests for information on diagnoses (problem codes), medications, and lab tests, and returns related information from [MedlinePlus](https://medlineplus.gov/). The API is available as a web [application](https://medlineplus.gov/connect/application.html) or as a web [service](https://medlineplus.gov/connect/service.html), which can be integrated with an EHR. MedlinePlus accepts SNOMED CT problem codes as input and provides CDS in the form of _targeted information prescription_. The example below shows how the Medline Plus Connect request and response are structured. Note that the response includes the title and link of the matched topic and may include synonyms, attribution acknowledgements, and related links.

|                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Example: A patient diagnosed with 13645005 <mark style="color:blue;">\|</mark> Chronic obstructive lung disease (disorder)<mark style="color:blue;">\|</mark> |

<figure><img src="../../.gitbook/assets/Medline Plus Connect Example.png" alt=""><figcaption></figcaption></figure>





The requests conform to the [HL7 Context-Aware Knowledge Retrieval (Infobutton) Knowledge Request URL-Based Implementation Guide](http://wiki.hl7.org/index.php?title=Product_Infobutton#Product_Name_-_HL7_V3_IG:_URL-Based_Implementations_of_the_Context-Aware_Information_Retrieval_.28Infobutton.29). A screen shot of the application's response to a request for information on <mark style="color:blue;">|</mark> Asthma<mark style="color:blue;">|</mark> is provided below:

<figure><img src="../../images/123897692.png" alt=""><figcaption><p>MedlinePlus Connect web application response to request for information on problem code 195967001 | Asthma (disorder) |</p></figcaption></figure>

## Observational Health Data Sciences and Informatics (OHDSI)

Some NLM researchers also participate in external projects which utilize SNOMED CT. One such project is [OHDSI](http://ohdsi.org/). This collaborative uses SNOMED CT to integrate diagnostic data. This semantic data integration is then used by research studies which in some cases serves as input into the authoring of CDS knowledge artifacts.

One of the programs related to OHDSI is [Innovation in Medical Evidence Development and Surveillance](https://reaganudall.org/projects/research/imeds) (IMEDS), which includes a number of projects led by NIH researchers, such as:

* NIH Investigators
* Ferdinand Dhombres (NIH)

<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&#x26;entry.1767247133=CDS+Guide&#x26;entry.670899847=National%20Institutes%20of%20Health%3A%20Intramural%20Research%20Program" class="button primary">Provide Feedback</a>

[^1]: [https://irp.nih.gov/about-us/what-is-the-irp](https://irp.nih.gov/about-us/what-is-the-irp)

[^2]: [https://en.wikipedia.org/wiki/National\_Institutes\_of\_Health](https://en.wikipedia.org/wiki/National_Institutes_of_Health)

[^3]: [https://irp.nih.gov/about-us/our-programs](https://irp.nih.gov/about-us/our-programs)

[^4]: Based on content from [https://vsac.nlm.nih.gov/](https://vsac.nlm.nih.gov/)
