# 1. Introduction

## Background

SNOMED CT is a standardized and multilingual clinical terminology used by clinicians and other health care providers to record and share health information. As the most comprehensive terminology in the world, SNOMED CT contains over 300,000 active clinical concepts, each representing a unique clinical meaning. These concepts are organized into hierarchies such as [ 404684003 | Clinical finding|](http://snomed.info/id/404684003 "404684003 | Clinical finding |") ,  [ 71388002 | Procedure|](http://snomed.info/id/71388002 "71388002 | Procedure |") , [ 123037004 | Body structure|](http://snomed.info/id/123037004 "123037004 | Body structure |") and [ 373873005 | Pharmaceutical / biologic product|](http://snomed.info/id/373873005 "373873005 | Pharmaceutical / biologic product |") .

SNOMED CT is increasingly being used in clinical decision support (CDS) systems to support healthcare providers in making well informed clinical decisions. SNOMED CT's polyhierarchy, defining relationships and concept model are just some of the terminology's features that help to link patient records to the appropriate guidance, clinical knowledge and decision support rules.

##  Purpose

The guide [Data Analytics with SNOMED CT](http://snomed.org/analytics) explained how SNOMED CT may be used to support data analytics, and how integrating clinical records with decision support tools can improve the care provided to individual patients by guiding safe, appropriate and effective patient care.

The purpose of this guide is to review the approaches, tools and techniques used to implement clinical decision support with SNOMED CT, and to share developing practice in this area. It is anticipated that this guide will benefit [Members](https://confluence.ihtsdotools.org/display/DOCGLOSS/Member "Glossary link: Members"), vendors and users of SNOMED CT by promoting a greater awareness of how SNOMED CT has been and can be used to enhance clinical decision support implementations.

## Scope

This guide introduces the key components of clinical decision support systems, explores ways in which SNOMED CT can be used to enhance the capabilities within each of these components, and presents some case studies in which SNOMED CT has been used to support clinical decision support. The guide focuses on CDS systems that use a combination of SNOMED CT encoded knowledge artifacts (e.g. CDS rules and guidelines) and SNOMED CT encoded electronic health records. However, using SNOMED CT to enhance non-SNOMED CT enabled CDS and EHR systems is also considered.

## Audience

The target audience of this guide includes:

  * Members who wish to learn about using SNOMED CT for clinical decision support

  * Clinicians, informatics specialists and technical staff involved in the planning, management, design or implementation of clinical record applications or clinical decision support systems
  * Software vendors, data analysts, epidemiologists and others designing SNOMED CT based solutions

This guide assumes a basic level of understanding of SNOMED CT. For background information it is recommended that the reader refers to the [SNOMED CT Starter Guide](https://confluence.ihtsdotools.org/display/DOCSTART/SNOMED+CT+Starter+Guide).

##  Guide Overview

The guide presents an introduction to clinical decision support using SNOMED CT and is structured as follows:

  * [1\. Introduction](1.-Introduction_123897414.html): Chapter 1 provides an introduction to the guide, and defines clinical decision support (CDS) and clinical decision support systems (CDSS). It then presents an overview of CDS (including its scope, history and the 'five rights'), it explores the functional and clinical areas in which CDS is used, the features of SNOMED CT that support CDS, and a table of abbreviations used in this guide.
  * [2\. Logical Architecture](2.-Logical-Architecture_123897452.html): Chapter 2 presents an overview of the logical architecture of an electronic health records system that uses CDS, and the internal components of a CDSS system.
  * [3\. Knowledge Base](3.-Knowledge-Base_123897475.html): Chapter 3 describes the knowledge base of a CDSS, in which the knowledge artifacts that drive the CDS are stored, and how SNOMED CT may be used within these artifacts.
  * [4\. Inference Engine](4.-Inference-Engine_123897580.html): Chapter 4 explains how the inference engine of a CDSS can use SNOMED CT to execute the knowledge artifacts in the knowledge base.
  * [5\. Communications](5.-Communications_123897660.html): Chapter 5 explores some of the considerations around implementing the communication mechanisms in a CDSS.

* * *
