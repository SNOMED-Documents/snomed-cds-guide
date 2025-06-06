# duodecim

## Duodecim

## EBMeDS

The Evidence-Based Medicine electronic Decision Support system (EBMeDS) was developed by Duodecim. It is a platform-independent service, which can be integrated with any EHR that uses structured patient data. EBMeDS contains over 40,000[3](https://confluence.ihtsdotools.org/display/DOCCDS/Duodecim#Footnote3) decision support rules which can be used to generate reminders, therapeutic suggestions, order sets and diagnosis-specific links to guideline sets and other online resources. EBMeDS can also be used to automatically populate calculators and forms with patient-specific data, and to generate summary views and dashboards. In addition to real-time use, the EBMeDS decision support rules can also be run as batch scripts on patient populations to generate reports that measure quality and analyze care-gaps. The rules of EBMeDS are based on the data in the EBMG collection, with several 3rd party resources also used for evidence collection.

## Using SNOMED CT

EBMeDS receives encoded patient data from EHRs. The coded data pertains to several \_ data groups \_ including diagnoses, medications, vaccinations, investigation results, surgical procedures, and risk factors (such as smoking). Although multiple coding systems are supported, only SNOMED CT and the Read code system are accepted for all data groups. Within EBMeDS, all codes are mapped to internal aliases. For example, for the concept \_ serum or plasma creatinine \_ includes codes from 10 different coding systems. Duodecim is expecting to derive additional benefits from using SNOMED CT when more EHRs are able to provide SNOMED CT encoded records as outputs.

## Deployments

At present, EBMeDS is used mainly in Finland. Duodecim is planning to offer a cloud-based centralized EBMeDS service in the near future, but currently the application is integrated into the local EHR environments. Belgium has a national license for EBMeDS as part of the [EBMPracticeNet](../../EBMPracticeNet_123897699.html) implementation in Belgium. Several pilots and scientific studies are being performed in Italy, Denmark, Estonia, the United States and the UK.

***

| Footnotes Ref                                                                     | Notes                                                                                                                                                    |
| --------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [1](https://confluence.ihtsdotools.org/display/DOCCDS/Duodecim#FootnoteMarker1-0) | [http://www.duodecim.fi/english/](http://www.duodecim.fi/english/)                                                                                       |
| [2](https://confluence.ihtsdotools.org/display/DOCCDS/Duodecim#FootnoteMarker2-0) | [http://www.duodecim.fi/english/duodecim/duodecim-medical-publications-ltd/](http://www.duodecim.fi/english/duodecim/duodecim-medical-publications-ltd/) |
| [3](https://confluence.ihtsdotools.org/display/DOCCDS/Duodecim#FootnoteMarker3-0) | [http://www.ebmeds.org/web/guest/home?n\_id=11411\&lang=en](http://www.ebmeds.org/web/guest/home?n_id=11411\&lang=en)                                    |
