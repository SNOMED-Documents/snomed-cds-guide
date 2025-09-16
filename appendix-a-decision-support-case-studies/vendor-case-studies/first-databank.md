# First Databank

{% hint style="info" %}
FDB (First Databank)... is the leading provider of drug knowledge that helps healthcare professionals make precise medication-related decisions... FDB enables our information system developer partners to deliver a wide range of valuable, useful, and differentiated solutions. [As the company that virtually launched the medication decision support category, we offer more than three decades of experience in transforming drug knowledge into actionable, targeted, and effective solutions that improve patient safety and healthcare outcomes](#user-content-fn-1)[^1]. &#x20;

For more information please visit [http://www.fdbhealth.com/](http://www.fdbhealth.com/).
{% endhint %}

## Overview

[First DataBank (FDB)](#user-content-fn-2)[^2] were in the first wave of suppliers to recognize the potential of SNOMED CT and begin to integrate support for SNOMED CT into their existing clinical decision support solutions. Their primary use of SNOMED CT in the patient's electronic health record (EHR) is to detect safety issues arising from certain combinations of medications, diagnoses and drug adverse reaction histories. In 2006 FDB introduced support for products and packs encoded using the NHS SNOMED CT UK Drug Extension. In the following year FDB launched new modules within the Multilex drug knowledge base supporting Drug-Condition Checking and Drug Sensitivity (Allergy) checking for the SNOMED CT EHR.

System vendors implementing Multilex decision support within SNOMED CT-enabled medical record applications include CSC (Lorenzo system), EPIC and JAC in secondary care, and CSE Servelec (_RiO system)_ in community/mental health. Currently only pre-coordinated expressions are supported by the live Multilex SNOMED CT based decision support solutions.

## Drug-Condition Contraindication Checks

The contraindications module alerts the clinician when a medication proposed to treat a disorder is incompatible with another of the patient's disorders or clinical states. For example a beta blocker like propranolol might be prescribed to treat someone with high blood pressure. However if that patient also has asthma, their asthma might significantly worsen or a dangerous acute attack might be produced by the drug.

Thousands of such drug-condition contraindications exist and nearly all medications have at least one. Without point of care decision support, the clinician must rely on memory or search reference sources for each drug prescribed. Also there is a risk that a contraindicating condition may be in the record but unknown to the prescribing clinician.

In a SNOMED CT enabled EHR, both the drugs (e.g. [318353009 <mark style="color:blue;">|</mark> propranolol hydrochloride 40mg tablet<mark style="color:blue;">|</mark>](http://snomed.info/id/318353009) ) and the conditions (e.g. [370219009 <mark style="color:blue;">|</mark> moderate asthma<mark style="color:blue;">|</mark>](http://snomed.info/id/370219009) ) are encoded.

Internally FDB maintain their own local ontology representing only those conditions relevant to prescribing decision support (e.g. asthma, gastric ulcer, heart disease, pregnancy). The items in this ontology are linked to SNOMED CT codes as required to support this (contraindication checking) use case. These SNOMED CT links range from the obvious, such as linking [195967001 <mark style="color:blue;">|</mark> asthma<mark style="color:blue;">|</mark>](http://snomed.info/id/195967001) to FDB's 'asthma', to the more subtle, such as linking [447413000 <mark style="color:blue;">|</mark> drainage of amniotic fluid using ultrasound guidance<mark style="color:blue;">|</mark>](http://snomed.info/id/447413000) to FDB's 'pregnancy'.

FDB reviews the relevant SNOMED CT domains (i.e. [<mark style="color:blue;">|</mark> Clinical finding<mark style="color:blue;">|</mark>](http://snomed.info/id/404684003), [<mark style="color:blue;">|</mark> Procedure<mark style="color:blue;">|</mark>](http://snomed.info/id/71388002) and [<mark style="color:blue;">|</mark> Situation with explicit context<mark style="color:blue;">|</mark>](http://snomed.info/id/243796009) ) for concepts applicable to drug-condition checking. The FDB linking tool uses the SNOMED CT [<mark style="color:blue;">|</mark> is a<mark style="color:blue;">|</mark>](http://snomed.info/id/116680003) hierarchy and a SNOMED CT derived transitive closure table to locate and suggest links from the FDB ontology to SNOMED CT concepts. Other SNOMED CT relationships also help find related concepts via the browser but discovery is mainly by clinical knowledge combined with description based searches assisted by the rich synonym content of SNOMED CT.

## Drug Sensitivity (Allergy) Checks

The sensitivities module alerts the clinician when a proposed drug for a patient is _either_ stated in that patient's record to have caused a previous adverse reaction _or_ when an adverse reaction has occurred to a similar drug and thus likely to elicit a similar adverse response. For example, a patient allergic to penicillin is likely to react to most other drugs containing a β-lactam ring in their molecular structures.

In a similar way to how FDB links SNOMED CT conditions to its own internal ontology, SNOMED CT concepts which suggest allergy or previous adverse reactions to a medication are also linked to an internal FDB ontology for representing medication ingredients. This ontology is designed specifically to support allergic and adverse reaction cross-reactivity.

***

[^1]: [https://www.fdbhealth.com/solutions/medknowledge-drug-database](https://www.fdbhealth.com/solutions/medknowledge-drug-database)

[^2]: Please note that the case study on this page is an excerpt from the [Data Analytics with SNOMED CT](http://snomed.org/analytics) guide.






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=CDS+Guide&entry.670899847=First%20Databank" class="button primary">Provide Feedback</a>
