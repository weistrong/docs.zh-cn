---
description: 了解有关以下内容的详细信息： ODBC 架构集合
title: ODBC 架构集合
ms.date: 03/30/2017
ms.assetid: 1bb126a5-ceec-4649-a4bc-8aa19e801046
ms.openlocfilehash: ceac67e49914db7010e315a2dfcdb630bea1e29f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786194"
---
# <a name="odbc-schema-collections"></a>ODBC 架构集合

本节讨论对适用于 Microsoft SQL Server、Oracle 和 Microsoft Jet 的 ODBC 驱动程序的架构集合支持。

## <a name="microsoft-sql-server-odbc-driver"></a>Microsoft SQL Server ODBC 驱动程序

除了通用架构集合之外，Microsoft SQL Server ODBC 驱动程序还支持下列特定的架构集合：

- 表

- 索引

- 列

- 过程

- ProcedureColumns

- ProcedureParameters

- 视图

### <a name="tables-and-views"></a>表和视图

|ColumnName|数据类型|
|----------------|--------------|
|TABLE_CAT|字符串|
|TABLE_SCHEM|字符串|
|TABLE_NAME|字符串|
|TABLE_TYPE|字符串|
|REMARKS|字符串|

### <a name="indexes"></a>索引

|ColumnName|数据类型|
|----------------|--------------|
|TABLE_CAT|字符串|
|TABLE_SCHEM|字符串|
|TABLE_NAME|字符串|
|NON_UNIQUE|Int16|
|INDEX_QUALIFIER|字符串|
|INDEX_NAME|字符串|
|TYPE|Int16|
|ORDINAL_POSITION|Int16|
|COLUMN_NAME|字符串|
|ASC_OR_DESC|字符串|
|CARDINALITY|Int32|
|PAGES|Int32|
|FILTER_CONDITION|字符串|
|SS_TYPE_SCHEMA|字符串|
|SS_DATA_TYPE|Byte|

### <a name="columns"></a>列

|ColumnName|数据类型|
|----------------|--------------|
|TABLE_CAT|字符串|
|TABLE_SCHEM|字符串|
|TABLE_NAME|字符串|
|COLUMN_NAME|字符串|
|DATA_TYPE|Int16|
|TYPE_NAME|字符串|
|COLUMN_SIZE|Int32|
|BUFFER_LENGTH|Int32|
|DECIMAL_DIGITS|Int16|
|NUM_PREC_RADIX|Int16|
|NULLABLE|Int16|
|REMARKS|字符串|
|COLUMN_DEF|字符串|
|SQL_DATA_TYPE|Int16|
|SQL_DATETIME_SUB|Int16|
|CHAR_OCTET_LENGTH|Int32|
|ORDINAL_POSITION|Int32|
|IS_NULLABLE|字符串|
|SS_TYPE_CATALOG|字符串|
|SS_TYPE_SCHEMA|字符串|
|SS_DATA_TYPE|Byte|

### <a name="procedures"></a>过程

|ColumnName|数据类型|
|----------------|--------------|
|PROCEDURE_CAT|字符串|
|PROCEDURE_SCHEM|字符串|
|PROCEDURE_NAME|字符串|
|NUM_INPUT_PARAMS|Int32|
|NUM_OUTPUT_PARAMS|Int32|
|NUM_RESULT_SETS|Int32|
|REMARKS|字符串|
|PROCEDURE_TYPE|Int16|

### <a name="procedurecolumns"></a>ProcedureColumns

|ColumnName|数据类型|
|----------------|--------------|
|PROCEDURE_CAT|字符串|
|PROCEDURE_SCHEM|字符串|
|PROCEDURE_NAME|字符串|
|COLUMN_NAME|字符串|
|COLUMN_TYPE|Int16|
|DATA_TYPE|Int16|
|TYPE_NAME|字符串|
|COLUMN_SIZE|Int32|
|BUFFER_LENGTH|Int32|
|DECIMAL_DIGITS|Int16|
|NUM_PREC_RADIX|Int16|
|NULLABLE|Int16|
|REMARKS|字符串|
|COLUMN_DEF|字符串|
|SQL_DATA_TYPE|Int16|
|SQL_DATETIME_SUB|Int16|
|CHAR_OCTET_LENGTH|Int32|
|ORDINAL_POSITION|Int32|
|IS_NULLABLE|字符串|
|SS_TYPE_CATALOG|字符串|
|SS_TYPE_SCHEMA|字符串|
|SS_DATA_TYPE|Byte|

### <a name="procedureparameters"></a>ProcedureParameters

|ColumnName|数据类型|
|----------------|--------------|
|PROCEDURE_CAT|字符串|
|PROCEDURE_SCHEM|字符串|
|PROCEDURE_NAME|字符串|
|COLUMN_NAME|字符串|
|COLUMN_TYPE|Int16|
|DATA_TYPE|Int16|
|TYPE_NAME|字符串|
|COLUMN_SIZE|Int32|
|BUFFER_LENGTH|Int32|
|DECIMAL_DIGITS|Int16|
|NUM_PREC_RADIX|Int16|
|NULLABLE|Int16|
|REMARKS|字符串|
|COLUMN_DEF|字符串|
|SQL_DATA_TYPE|Int16|
|SQL_DATETIME_SUB|Int16|
|CHAR_OCTET_LENGTH|Int32|
|ORDINAL_POSITION|Int32|
|IS_NULLABLE|字符串|
|SS_TYPE_CATALOG|字符串|
|SS_TYPE_SCHEMA|字符串|
|SS_DATA_TYPE|Byte|

## <a name="microsoft-oracle-odbc-driver"></a>Microsoft Oracle ODBC 驱动程序

除了通用架构集合之外，Microsoft SQL Server Oracle ODBC 驱动程序还支持下列特定的架构集合：

- 表

- 列

- 过程

- ProcedureColumns

- ProcedureParameters

- 视图

- 索引

### <a name="tables-and-views"></a>表和视图

|ColumnName|数据类型|
|----------------|--------------|
|TABLE_QUALIFIER|字符串|
|TABLE_OWNER|字符串|
|TABLE_NAME|字符串|
|TABLE_TYPE|字符串|
|REMARKS|字符串|

### <a name="columns"></a>列

|ColumnName|数据类型|
|----------------|--------------|
|TABLE_QUALIFIER|字符串|
|TABLE_OWNER|字符串|
|TABLE_NAME|字符串|
|COLUMN_NAME|字符串|
|DATA_TYPE|Int16|
|TYPE_NAME|字符串|
|PRECISION|Int32|
|LENGTH|Int32|
|SCALE|Int16|
|RADIX|Int16|
|NULLABLE|Int16|
|REMARKS|字符串|
|ORDINAL_POSITION|Int32|

### <a name="procedures"></a>过程

|ColumnName|数据类型|
|----------------|--------------|
|PROCEDURE_QUALIFIER|字符串|
|PROCEDURE_OWNER|字符串|
|PROCEDURE_NAME|字符串|
|NUM_INPUT_PARAMS|Int16|
|NUM_OUTPUT_PARAMS|Int16|
|NUM_RESULT_SETS|Int16|
|REMARKS|字符串|
|PROCEDURE_TYPE|Int16|

### <a name="procedurecolumns"></a>ProcedureColumns

|ColumnName|数据类型|
|----------------|--------------|
|PROCEDURE_QUALIFIER|字符串|
|PROCEDURE_OWNER|字符串|
|PROCEDURE_NAME|字符串|
|COLUMN_NAME|字符串|
|COLUMN_TYPE|Int16|
|DATA_TYPE|Int16|
|TYPE_NAME|字符串|
|PRECISION|Int32|
|LENGTH|Int32|
|SCALE|Int16|
|RADIX|Int16|
|NULLABLE|Int16|
|REMARKS|字符串|
|OVERLOAD|Int32|
|ORDINAL_POSITION|Int32|

## <a name="microsoft-jet-odbc-driver"></a>Microsoft Jet ODBC 驱动程序

除了通用架构集合之外，Microsoft Jet ODBC 驱动程序还支持下列特定的架构集合：

- 表

- 索引

- 列

- 过程

- ProcedureColumns

- ProcedureParameters

- 视图

### <a name="tables-and-views"></a>表和视图

|ColumnName|数据类型|
|----------------|--------------|
|TABLE_QUALIFIER|字符串|
|TABLE_OWNER|字符串|
|TABLE_NAME|字符串|
|TABLE_TYPE|字符串|
|REMARKS|字符串|

### <a name="columns"></a>列

|ColumnName|数据类型|
|----------------|--------------|
|TABLE_QUALIFIER|字符串|
|TABLE_OWNER|字符串|
|TABLE_NAME|字符串|
|COLUMN_NAME|字符串|
|DATA_TYPE|Int16|
|TYPE_NAME|字符串|
|PRECISION|Int32|
|LENGTH|Int32|
|SCALE|Int16|
|RADIX|Int16|
|NULLABLE|Int16|
|REMARKS|字符串|
|ORDINAL_POSITION|Int32|

### <a name="procedures"></a>过程

|ColumnName|数据类型|
|----------------|--------------|
|PROCEDURE_QUALIFIER|字符串|
|PROCEDURE_OWNER|字符串|
|PROCEDURE_NAME|字符串|
|NUM_INPUT_PARAMS|Int16|
|NUM_OUTPUT_PARAMS|Int16|
|NUM_RESULT_SETS|Int16|
|REMARKS|字符串|
|PROCEDURE_TYPE|Int16|

### <a name="procedurecolumns"></a>ProcedureColumns

|ColumnName|数据类型|
|----------------|--------------|
|PROCEDURE_QUALIFIER|字符串|
|PROCEDURE_OWNER|字符串|
|PROCEDURE_NAME|字符串|
|COLUMN_NAME|字符串|
|COLUMN_TYPE|Int16|
|DATA_TYPE|Int16|
|TYPE_NAME|字符串|
|PRECISION|Int32|
|LENGTH|Int32|
|SCALE|Int16|
|RADIX|Int16|
|NULLABLE|Int16|
|REMARKS|字符串|
|OVERLOAD|Int32|
|ORDINAL_POSITION|Int32|

### <a name="procedureparameters"></a>ProcedureParameters

|ColumnName|数据类型|
|----------------|--------------|
|PROCEDURE_CAT|字符串|
|PROCEDURE_SCHEM|字符串|
|PROCEDURE_NAME|字符串|
|COLUMN_NAME|字符串|
|COLUMN_TYPE|Int16|
|DATA_TYPE|Int16|
|TYPE_NAME|字符串|
|COLUMN_SIZE|Int32|
|BUFFER_LENGTH|Int32|
|DECIMAL_DIGITS|Int16|
|NUM_PREC_RADIX|Int16|
|NULLABLE|Int16|
|REMARKS|字符串|
|COLUMN_DEF|字符串|
|SQL_DATA_TYPE|Int16|
|SQL_DATETIME_SUB|Int16|
|CHAR_OCTET_LENGTH|Int32|
|ORDINAL_POSITION|Int32|
|IS_NULLABLE|字符串|

## <a name="see-also"></a>请参阅

- [ADO.NET 概述](ado-net-overview.md)
