---
description: "System Information Schema Views (Transact-SQL)"
title: "System Information Schema Views (Transact-SQL) | Microsoft Docs"
ms.custom: ""
ms.date: "07/30/2019"
ms.prod: sql
ms.prod_service: "database-engine"
ms.reviewer: ""
ms.technology: system-objects
ms.topic: "reference"
dev_langs: 
  - "TSQL"
helpviewer_keywords: 
  - "information schema views"
  - "schemas [SQL Server], information schema views"
  - "metadata [SQL Server], views"
  - "views [SQL Server], information schema"
  - "system views [SQL Server], information schema"
ms.assetid: 7e9f1dfe-27e9-40e7-8fc7-bfc5cae6be10
author: markingmyname
ms.author: maghan
---
# System Information Schema Views (Transact-SQL)

[!INCLUDE [SQL Server Azure SQL Database Azure SQL Managed Instance](../../includes/applies-to-version/sql-asdb-asdbmi.md)]

An information schema view is one of several methods [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] provides for obtaining metadata. Information schema views provide an internal, system table-independent view of the [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] metadata. Information schema views enable applications to work correctly although significant changes have been made to the underlying system tables. The information schema views included in [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] comply with the ISO standard definition for the INFORMATION_SCHEMA.

> [!IMPORTANT]
> Some changes have been made to the information schema views that break backward compatibility. These changes are described in the topics for the specific views.

[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] supports a three-part naming convention when you refer to the current server. The ISO standard also supports a three-part naming convention. However, the names used in both naming conventions are different. The information schema views are defined in a special schema named INFORMATION_SCHEMA. This schema is contained in each database. Each information schema view contains metadata for all data objects stored in that particular database. The following table shows the relationships between the [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] names and the SQL standard names.

|SQL Server name|Maps to this equivalent SQL standard name|
|---------------------|-----------------------------------------------|
|Database|Catalog|
|Schema|Schema|
|Object|Object|
|user-defined data type|Domain|

This name-mapping convention applies to the following [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] ISO-compatible views.

:::row:::
    :::column:::
        [CHECK_CONSTRAINTS](../../relational-databases/system-information-schema-views/check-constraints-transact-sql.md)

        [COLUMN_DOMAIN_USAGE](../../relational-databases/system-information-schema-views/column-domain-usage-transact-sql.md)

        [COLUMN_PRIVILEGES](../../relational-databases/system-information-schema-views/column-privileges-transact-sql.md)

        [COLUMNS](../../relational-databases/system-information-schema-views/columns-transact-sql.md)

        [CONSTRAINT_COLUMN_USAGE](../../relational-databases/system-information-schema-views/constraint-column-usage-transact-sql.md)

        [CONSTRAINT_TABLE_USAGE](../../relational-databases/system-information-schema-views/constraint-table-usage-transact-sql.md)

        [DOMAIN_CONSTRAINTS](../../relational-databases/system-information-schema-views/domain-constraints-transact-sql.md)

        [DOMAINS](../../relational-databases/system-information-schema-views/domains-transact-sql.md)

        [KEY_COLUMN_USAGE](../../relational-databases/system-information-schema-views/key-column-usage-transact-sql.md)

        [PARAMETERS](../../relational-databases/system-information-schema-views/parameters-transact-sql.md)
    :::column-end:::
    :::column:::
        [REFERENTIAL_CONSTRAINTS](../../relational-databases/system-information-schema-views/referential-constraints-transact-sql.md)

        [ROUTINES](../../relational-databases/system-information-schema-views/routines-transact-sql.md)

        [ROUTINE_COLUMNS](../../relational-databases/system-information-schema-views/routine-columns-transact-sql.md)

        [SCHEMATA](../../relational-databases/system-information-schema-views/schemata-transact-sql.md)

        [TABLE_CONSTRAINTS](../../relational-databases/system-information-schema-views/table-constraints-transact-sql.md)

        [TABLE_PRIVILEGES](../../relational-databases/system-information-schema-views/table-privileges-transact-sql.md)

        [TABLES](../../relational-databases/system-information-schema-views/tables-transact-sql.md)

        [VIEW_COLUMN_USAGE](../../relational-databases/system-information-schema-views/view-column-usage-transact-sql.md)

        [VIEW_TABLE_USAGE](../../relational-databases/system-information-schema-views/view-table-usage-transact-sql.md)

        [VIEWS](../../relational-databases/system-information-schema-views/views-transact-sql.md)
    :::column-end:::
:::row-end:::

Also, some views contain references to different classes of data such as character data or binary data.

When you reference the information schema views, you must use a qualified name that includes the `INFORMATION_SCHEMA` schema name. For example:

```sql
SELECT TABLE_CATALOG, TABLE_SCHEMA, TABLE_NAME, COLUMN_NAME, COLUMN_DEFAULT
FROM AdventureWorks2012.INFORMATION_SCHEMA.COLUMNS
WHERE TABLE_NAME = N'Product';
```

## Permissions  
The visibility of the metadata in information schema views is limited to securables that a user either owns or on which the user has been granted some permission. For more information, see [Metadata Visibility Configuration](../../relational-databases/security/metadata-visibility-configuration.md).

> [!NOTE]  
> Information schema views are defined server-wide and therefore cannot be denied within the context of a user database. To REVOKE or DENY access (SELECT), the master database must be used. By default the public role has SELECT-permission to all information schema views but the content is limited with metadata visibility rules.

## See Also

- [System Views &#40;Transact-SQL&#41;](../../relational-databases/system-views/replication-views-transact-sql.md)
- [Data Types &#40;Transact-SQL&#41;](../../t-sql/data-types/data-types-transact-sql.md)
- [System Stored Procedures &#40;Transact-SQL&#41;](../../relational-databases/system-stored-procedures/system-stored-procedures-transact-sql.md) 
