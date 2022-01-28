# Masterdata Guide

## Overview
Masterdata is the necessary base data to run MOSIP services. The data resides in the [`mosip_master` DB](https://github.com/mosip/admin-services/tree/1.2.0-rc2/db_scripts/mosip_master). This data needs to be customized for a country specific deployment.  Masterdata is bulk uploaded one-time during the [installation process](https://github.com/mosip/mosip-infra/tree/1.2.0-rc2/deployment/v3/mosip/kernel/masterdata) and later may be updated using the [Admin Portal](admin-portal-guide.md). The default data uploaded during sandbox installation is available [here](https://github.com/mosip/mosip-data/tree/lts/mosip_master/xlsx). 

The tables that would need to be modified are listed below.  Other tables in `mosip_master` DB are either system-filled or pre-filled and not to be modified.

## Common guidelines
Applicable for all tables:

* Add/remove rows for the [configured languages](). 

## Documents
|Table|Guide|
|---|---|
|`doc_category`|Categories of documents to be captured|
|`doc_type`| Specific documents related to a country|
|`applicant_valid_document`|Mapping of document category, type and [applicant type](https://github.com/mosip/mosip-config/blob/develop3-v3/applicanttype.mvel)|

## Location
1. loc_hierarchy_list
1. location
1. loc_holiday

## Machine
1. machine_spec
1. machine_type

## ID schema and UI spec
1. `identity_schema`

Refer to [ID Schema customisation](id-schema.md). Update the JSON in `schema_json` column of [`identity_schema.xlsx`](https://github.com/mosip/mosip-data/tree/lts/mosip_master/xlsx/identity_schema.xlsx)

1. `ui_spec`

## Registration center
1. reg_center_type
1. registration_center
1. registration_center_h
1. reg_exceptional_holiday
1. reg_working_nonworking

## Others
1. blacklisted_words
1. dynamic_field
1. title
1. zone
1. reason_list



