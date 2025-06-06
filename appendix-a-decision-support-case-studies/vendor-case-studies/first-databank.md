# First Databank

# Overview  

First DataBank (FDB) were in the first wave of suppliers to recognize the potential of SNOMED CT and begin to integrate support for SNOMED CT into their existing clinical decision support solutions. Their primary use of SNOMED CT in the patient's electronic health record (EHR) is to detect safety issues arising from certain combinations of medications, diagnoses and drug adverse reaction histories. In 2006 FDB introduced support for products and packs encoded using the NHS SNOMED CT UK Drug Extension. In the following year FDB launched new modules within the Multilex drug knowledge base supporting Drug-Condition Checking and Drug Sensitivity (Allergy) checking for the SNOMED CT EHR. 

System vendors implementing Multilex decision support within SNOMED CT-enabled medical record applications include CSC (Lorenzo system), EPIC and JAC in secondary care, and CSE Servelec (_RiO system)_ in community/mental health. Currently only pre-coordinated expressions are supported by the live Multilex SNOMED CT based decision support solutions.

# Drug-Condition Contraindication Checks

The contraindications module alerts the clinician when a medication proposed to treat a disorder is incompatible with another of the patient's disorders or clinical states. For example a beta blocker like propranolol might be prescribed to treat someone with high blood pressure. However if that patient also has asthma, their asthma might significantly worsen or a dangerous acute attack might be produced by the drug.

Thousands of such drug-condition contraindications exist and nearly all medications have at least one. Without point of care decision support, the clinician must rely on memory or search reference sources for each drug prescribed. Also there is a risk that a contraindicating condition may be in the record but unknown to the prescribing clinician.

In a SNOMED CT enabled EHR, both the drugs (e.g. [ 318353009 | propranolol hydrochloride 40mg tablet|](http://snomed.info/id/318353009 "318353009 | propranolol hydrochloride 40mg tablet |") ) and the conditions (e.g. [ 370219009 | moderate asthma|](http://snomed.info/id/370219009 "370219009 | moderate asthma |") ) are encoded.

Internally FDB maintain their own local ontology representing only those conditions relevant to prescribing decision support (e.g. asthma, gastric ulcer, heart disease, pregnancy). The items in this ontology are linked to SNOMED CT codes as required to support this (contraindication checking) use case. These SNOMED CT links range from the obvious, such as linking [ 195967001 | asthma|](http://snomed.info/id/195967001 "195967001 | asthma |") to FDB's 'asthma', to the more subtle, such as linking [ 447413000 | drainage of amniotic fluid using ultrasound guidance|](http://snomed.info/id/447413000 "447413000 | drainage of amniotic fluid using ultrasound guidance |") to FDB's 'pregnancy'.

FDB reviews the relevant SNOMED CT domains (i.e. [ | Clinical finding|](http://snomed.info/id/404684003 "404684003 | Clinical finding |") , [ | Procedure|](http://snomed.info/id/71388002 "71388002 | Procedure |") and [ | Situation with explicit context|](http://snomed.info/id/243796009 "243796009 | Situation with explicit context |") ) for concepts applicable to drug-condition checking. The FDB linking tool uses the SNOMED CT [ | is a|](http://snomed.info/id/116680003 "116680003 | is a |") hierarchy and a SNOMED CT derived transitive closure table to locate and suggest links from the FDB ontology to SNOMED CT concepts. Other SNOMED CT relationships also help find related concepts via the browser but discovery is mainly by clinical knowledge combined with description based searches assisted by the rich synonym content of SNOMED CT.

# Drug Sensitivity (Allergy) Checks

The sensitivities module alerts the clinician when a proposed drug for a patient is  _either_ stated in that patient's record to have caused a previous adverse reaction  _or_ when an adverse reaction has occurred to a similar drug and thus likely to elicit a similar adverse response. For example, a patient allergic to penicillin is likely to react to most other drugs containing a β-lactam ring in their molecular structures.

In a similar way to how FDB links SNOMED CT conditions to its own internal ontology, SNOMED CT concepts which suggest allergy or previous adverse reactions to a medication are also linked to an internal FDB ontology for representing medication ingredients. This ontology is designed specifically to support allergic and adverse reaction cross-reactivity.

* * *

Footnotes Ref | Notes  
---|---  
[1](https://confluence.ihtsdotools.org/display/DOCCDS/First+Databank#FootnoteMarker1-0 "Footnote: Click to return to reference in text") |  [About First Databank (FDB)](http://www.fdbhealth.com/fdb-medknowledge-brochure-landing/?cid=US%20PS%20GG%20NA%20BN%20BN%20TXT%202%20LPD%2010232016%20First%20Databank%20e%201t1&gclid=Cj0KEQiAuJXFBRDirIGnpZLE-N4BEiQAqV0KGl__TfcWShscrMLGt-fk2BkHe3lcc-mIKlwwOQqH6F8aAt1K8P8HAQ)  
[2](https://confluence.ihtsdotools.org/display/DOCCDS/First+Databank#FootnoteMarker2-0 "Footnote: Click to return to reference in text") |  Please note that the case study on this page is an excerpt from the [Data Analytics with SNOMED CT](http://snomed.org/analytics) guide. 
