# 4.2. Accessing Clinical Records

This section describes the approaches that inference engines use to access EHR records for CDS. The CDS rules that an inference engine executes typically include references to EHR records and terminology. There are two general approaches to accessing health records from these CDS artifacts. The first is the direct access approach, in which a reference to the physical store is used. A simple example of this would be a reference to a patient diagnosis in a database table. The other approach is to base the CDS references on a common logical information model, and then map this to one or more physical datastores, as required. This approach enables a more standardized approach to the development of CDS rules and other artifacts. These two approaches are described in more detail below, along with some of the advantages, challenges, and examples. Please note that standards for accessing clinical records will be discussed in section [4.2.1. Standards for Accessing Clinical Records](4.2.1.-Standards-for-Accessing-Clinical-Records_123897649.html). Approaches to access the terminology which will be discussed in section [4.3. Accessing Terminology](4.3.-Accessing-Terminology_123897656.html). 

# Direct Access

Perhaps the most obvious approach to accessing health records is to use direct references to the locations in the clinical record store that will be used in a CDS rule. Many consider this the more common approach for point of care (POC) decision support today. For example, the pointers within a CDS rule could be expressed to reference a schema, table, and column in an SQL database. This approach requires a detailed knowledge of how the EHR data is stored to achieve an appropriate outcome from CDS tools. The challenge with this approach is that it can be more difficult to share CDS artifacts across institutions that may use different physical data stores.

# Logical Model

The logical model approach aims to standardize all references to EHR data, by specifying a common logical information model upon which all CDS rules are defined. This enables CDS rules to be shared and reused in different physical implementations. However, an additional transformation is usually required for each physical EHR store, to convert the logical references into physical ones. Examples of the logical model approach are presented in section [4.2.1. Standards for Accessing Clinical Records](4.2.1.-Standards-for-Accessing-Clinical-Records_123897649.html).

* * *
