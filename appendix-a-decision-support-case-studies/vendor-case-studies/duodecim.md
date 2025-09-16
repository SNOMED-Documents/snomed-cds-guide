# Duodecim

{% hint style="info" %}
[Duodecim Medical Publications Ltd](#user-content-fn-1)[^1] publishes information content for medical and healthcare professionals in the form of traditional printed products but also as electronic databases, solutions integrated into healthcare systems and an online learning environment. [Evidence-Based Medicine Guidelines (EBMG) is designed to provide you with the information you need quickly and using a single search term. Designed for use at the point of care, the guidelines are delivered in a format that makes it easy for a clinician to make a decision regarding treatment](#user-content-fn-2)[^2].\


For more information please visit [http://www.duodecim.fi/english/](http://www.duodecim.fi/english/).
{% endhint %}

## EBMeDS

The Evidence-Based Medicine electronic Decision Support system (EBMeDS) was developed by Duodecim. It is a platform-independent service, which can be integrated with any EHR that uses structured patient data. EBMeDS contains over 40,000 decision support rules which can be used to generate reminders, therapeutic suggestions, order sets and diagnosis-specific links to guideline sets and other online resources. EBMeDS can also be used to automatically populate calculators and forms with patient-specific data, and to generate summary views and dashboards. In addition to real-time use, the EBMeDS decision support rules can also be run as batch scripts on patient populations to generate reports that measure quality and analyze care-gaps. The rules of EBMeDS are based on the data in the EBMG collection, with several 3rd party resources also used for evidence collection.

## Using SNOMED CT

EBMeDS receives encoded patient data from EHRs. The coded data pertains to several \_ data groups \_ including diagnoses, medications, vaccinations, investigation results, surgical procedures, and risk factors (such as smoking). Although multiple coding systems are supported, only SNOMED CT and the Read code system are accepted for all data groups. Within EBMeDS, all codes are mapped to internal aliases. For example, for the concept \_ serum or plasma creatinine \_ includes codes from 10 different coding systems. Duodecim is expecting to derive additional benefits from using SNOMED CT when more EHRs are able to provide SNOMED CT encoded records as outputs.

## Deployments

At present, EBMeDS is used mainly in Finland. Duodecim is planning to offer a cloud-based centralized EBMeDS service in the near future, but currently the application is integrated into the local EHR environments. Belgium has a national license for EBMeDS as part of the [EBMPracticeNet](../organizational-case-studies/ebmpracticenet.md) implementation in Belgium. Several pilots and scientific studies are being performed in Italy, Denmark, Estonia, the United States and the UK.

***

[^1]: [http://www.duodecim.fi/english/](http://www.duodecim.fi/english/)

[^2]: https://www.duodecim.fi/english/products/ebmg/






<a href="https://docs.google.com/forms/d/e/1FAIpQLScTmbZIf0UEQwYDkY27EEWBkaiYkHSbR0_9DmFrMLXoQLyL7Q/viewform?usp=pp_url&entry.1767247133=CDS+Guide&entry.670899847=Duodecim" class="button primary">Provide Feedback</a>
