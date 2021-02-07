---
description: 了解详细信息： Oracle 架构集合
title: Oracle 架构集合
ms.date: 03/30/2017
ms.assetid: 89a75de8-dee8-45e2-a97f-254d7e62e7e1
ms.openlocfilehash: c3093887c9359cbb170846c0ae425e0f77fc2580
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99672408"
---
# <a name="oracle-schema-collections"></a>Oracle 架构集合

除了通用架构集合之外，Microsoft Oracle .NET Framework 数据提供程序还支持下列特定的架构集合：

- 列

- 索引

- IndexColumns

- 过程

- 序列

- 同义词

- 表

- 用户

- 视图

- 函数

- 包

- PackageBodies

- 参数

- UniqueKeys

- PrimaryKeys

- ForeignKeys

- ForeignKeyColumns

- ProcedureParameters

## <a name="columns"></a>列

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|表、视图或群集的所有者。|
|TABLE_NAME|字符串|表、视图或群集的名称。|
|COLUMN_NAME|字符串|列名称。|
|ID|小数|列在创建时的序列号。|
|DATATYPE|字符串|列的数据类型。|
|LENGTH|小数|列的长度（字节数）。|
|PRECISION|小数|对于 NUMBER 数据类型为十进制精度；对于 FLOAT 数据类型为二进制精度；对于所有其他数据类型为 null。|
|SCALE|小数|数字中小数点右侧的位数。|
|NULLABLE|字符串|指定列是否允许 NULL。 如果列上存在 NOT NULL 约束，或列属于 PRIMARY KEY，值为 N。|

## <a name="indexes"></a>索引

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|索引的所有者。|
|INDEX_NAME|字符串|索引的名称。|
|INDEX_TYPE|字符串|索引的类型（NORMAL、BITMAP、FUNCTION-BASED NORMAL、FUNCTION-BASED BITMAP 或 DOMAIN）。|
|TABLE_OWNER|字符串|索引对象的所有者。|
|TABLE_NAME|字符串|索引对象的名称。|
|TABLE_TYPE|字符串|索引对象的类型（例如 TABLE、CLUSTER）。|
|UNIQUENESS|字符串|索引是 UNIQUE 还是 NONUNIQUE。|
|COMPRESSION|字符串|索引是 ENABLED 还是 DISABLED。|
|PREFIX_LENGTH|小数|压缩键的前缀中的列数。|
|TABLESPACE_NAME|字符串|包含索引的表空间的名称。|
|INI_TRANS|小数|初始事务数。|
|MAX_TRANS|小数|最大事务数。|
|INITIAL_EXTENT|小数|初始范围的大小。|
|NEXT_EXTENT|小数|辅助范围的大小。|
|MIN_EXTENTS|小数|段中允许的最小范围数。|
|MAX_EXTENTS|小数|段中允许的最大范围数。|
|PCT_INCREASE|小数|范围大小增加的百分比。|
|PCT_THRESHOLD|小数|每个索引条目允许的块空间的阈值百分比。|
|INCLUDE_COLUMN|小数|要加入通过索引组织的表的主键（非溢出）索引中的最后一列的列 ID。 此列映射到 *_TAB_COLUMNS 数据字典视图的 COLUMN_ID 列。|
|FREELISTS|小数|为此段分配的进程空闲列表数。|
|FREELIST_GROUPS|小数|为此段分配的空闲列表组数。|
|PCT_FREE|小数|块中可用空间的最小百分比。|
|LOGGING|字符串|日志信息。|
|BLEVEL|小数|B* 树级别：从根块到叶块的索引深度。 如果深度为 0，指示根块到叶块相同。|
|LEAF_BLOCKS|小数|索引中的叶块数。|
|DISTINCT_KEYS|小数|不同的索引值数。 对于强制使用 UNIQUE 和 PRIMARY KEY 约束的索引，此值与表中的行数相同 (USER_TABLES.NUM_ROWS)。|
|AVG_LEAF_BLOCKS_PER_KEY|小数|平均叶块数，索引中的每个不同值舍入到最接近的整数。 对于强制使用 UNIQUE 和 PRIMARY KEY 约束的索引，此值始终为 1。|
|AVG_DATA_BLOCKS_PER_KEY|小数|表中通过索引中舍入到最接近整数的不同值指向的平均数据块数。 此统计信息是包含的行中包含索引列的给定值的平均数据块数。|
|CLUSTERING_FACTOR|小数|根据索引值指示表中行的排序数量。|
|状态|字符串|非分区索引是 VALID 还是 UNUSABLE。|
|NUM_ROWS|小数|索引中的行数。|
|SAMPLE_SIZE|小数|用于分析索引的示例的大小。|
|LAST_ANALYZED|DateTime|最近分析此索引的日期。|
|DEGREE|字符串|每个实例用于扫描索引的线程数。|
|INSTANCES|字符串|在其上扫描索引的实例数。|
|PARTITIONED|字符串|此索引是否已分区 (是 &#124; 否) 。|
|TEMPORARY|字符串|索引是否在临时表上。|
|GENERATED|字符串|索引名称是否为系统生成的 (Y&#124;N) 。|
|SECONDARY|字符串|索引是否是由 Oracle9i 数据磁带的 ODCIIndexCreate 方法创建的辅助对象 (Y&#124;N) 。|
|BUFFER_POOL|字符串|用于索引块的默认缓冲区池的名称。|
|USER_STATS|字符串|统计信息是否已由用户直接输入。|
|DURATION|字符串|指示临时表的持续时间：1)SYS$SESSION：在会话期间保留行，2) SYS$TRANSACTION：在 COMMIT 之后删除行，3) Null 表示永久表。|
|PCT_DIRECT_ACCESS|小数|对于通过索引组织的表上的辅助索引，为具有 VALID 猜测的行的百分比。|
|ITYP_OWNER|字符串|对于域索引，为索引类型的所有者。|
|ITYP_NAME|字符串|对于域索引，为索引类型的名称。|
|PARAMETERS|字符串|对于域索引，为参数字符串。|
|GLOBAL_STATS|字符串|对于分区索引，指示统计信息通过整体分析索引进行收集 (YES) 还是通过基础索引分区和子分区上的统计信息进行估计 (NO)。|
|DOMIDX_STATUS|字符串|反映域索引的状态。 NULL：指定的索引不是域索引。 VALID：索引是有效的域索引。 IDXTYP_INVLD：此域索引的索引类型无效。|
|DOMIDX_OPSTATUS|字符串|反映在域索引上执行的操作的状态：NULL：指定的索引不是域索引。 VALID：执行操作而未发生错误。 FAILED：操作发生错误并失败。|
|FUNCIDX_STATUS|字符串|指示基于函数的索引的状态：NULL：这不是基于函数的索引，ENABLED：已启用基于函数的索引，DISABLED：已禁用基于函数的索引。|
|JOIN_INDEX|字符串|指示此索引是否是联接索引。|

## <a name="indexcolumns"></a>IndexColumns

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|INDEX_OWNER|字符串|索引的所有者。|
|INDEX_NAME|字符串|索引的名称。|
|TABLE_OWNER|字符串|表或群集的所有者。|
|TABLE_NAME|字符串|表或群集的名称。|
|COLUMN_NAME|字符串|对象类型列的列名或属性。|
|COLUMN_POSITION|小数|列或属性在索引中的位置。|
|COLUMN_LENGTH|小数|列的索引长度。|
|CHAR_LENGTH|小数|列的最大代码点长度。|
|DESCEND|字符串|列是否按照降序进行排序。|

## <a name="procedures"></a>过程

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|对象的所有者。|
|OBJECT_NAME|字符串|对象的名称。|
|SUBOBJECT_NAME|字符串|子对象（例如分区）的名称。|
|OBJECT_ID|小数|对象的字典对象编号。|
|DATA_OBJECT_ID|小数|包含对象的段的字典对象编号。|
|LAST_DDL_TIME|DateTime|上次通过 DDL 命令修改对象（包括授予和吊销）的时间戳。|
|TIMESTAMP|字符串|指定对象（字符数据）的时间戳。|
|状态|字符串|对象的状态（VALID、INVALID 或 N/A）。|
|TEMPORARY|字符串|对象是否是临时对象（当前会话只能看到其放入此对象本身的数据）。|
|GENERATED|字符串|此对象的名称是否由系统生成？ &#124; N)  (。|
|SECONDARY|字符串|这是否是由 Oracle9i 数据磁带的 ODCIIndexCreate 方法创建的辅助对象 (Y &#124; N) 。|
|CREATED|DateTime|创建对象的日期。|

## <a name="sequences"></a>序列

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|SEQUENCE_OWNER|字符串|序列所有者的名称。|
|SEQUENCE_NAME|字符串|序列名称。|
|MIN_VALUE|小数|序列的最小值。|
|MAX_VALUE|小数|序列的最大值。|
|INCREMENT_BY|小数|序列递增的值。|
|CYCLE_FLAG|字符串|在达到限制时序列是否环绕。|
|ORDER_FLAG|字符串|序列号是否按顺序生成。|
|CACHE_SIZE|小数|要缓存的序列号数。|
|LAST_NUMBER|小数|写入磁盘的上一个序列号。 如果序列使用缓存，写入磁盘的序列号是上一个放入序列缓存的序列号。 此序列号很可能大于上一个使用的序列号。|

## <a name="synonyms"></a>同义词

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|同义词的所有者。|
|SYNONYM_NAME|字符串|同义词的名称。|
|TABLE_OWNER|字符串|通过同义词引用的对象的所有者。|
|TABLE_NAME|字符串|通过同义词引用的对象的名称。|
|DB_LINK|字符串|所引用的数据库链接的名称（如果有）。|

## <a name="tables"></a>表

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|表的所有者。|
|TABLE_NAME|字符串|表的名称。|
|TYPE|字符串|表的类型。|

## <a name="users"></a>用户

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|名称|字符串|用户的名称。|
|ID|小数|用户的 ID 号。|
|CREATEDATE|DateTime|用户的创建日期。|

## <a name="views"></a>视图

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|视图的所有者。|
|VIEW_NAME|字符串|视图的名称。|
|TEXT_LENGTH|小数|视图文本的长度。|
|TEXT|String|视图文本。|
|TYPE_TEXT_LENGTH|小数|类型化视图的类型子句的长度。|
|TYPE_TEXT|字符串|类型化视图的类型子句。|
|OID_TEXT_LENGTH|小数|类型化视图的 WITH OID 子句的长度。|
|OID_TEXT|字符串|类型化视图的 WITH OID 子句。|
|VIEW_TYPE_OWNER|字符串|视图类型的所有者（如果视图是类型化视图）。|
|VIEW_TYPE|字符串|视图类型（如果视图是类型化视图）。|
|SUPERVIEW_NAME|字符串|超级视图的名称。|

## <a name="functions"></a>函数

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|对象的所有者。|
|OBJECT_NAME|字符串|对象的名称。|
|SUBOBJECT_NAME|字符串|子对象（例如分区）的名称。|
|OBJECT_ID|小数|对象的字典对象编号。|
|DATA_OBJECT_ID|小数|包含对象的段的字典对象编号。|
|Object_Type|字符串|对象的类型。|
|CREATED|DateTime|创建对象的日期。|
|LAST_DDL_TIME|DateTime|上次通过 DDL 命令修改对象（包括授予和吊销）的时间戳。|
|TIMESTAMP|字符串|指定对象（字符数据）的时间戳。|
|状态|字符串|对象的状态（VALID、INVALID 或 N/A）。|
|TEMPORARY|字符串|对象是否是临时对象（当前会话只能看到其放入此对象本身的数据）。|
|GENERATED|字符串|此对象的名称是否由系统生成？ &#124; N)  (。|
|SECONDARY|字符串|这是否是由 Oracle9i 数据磁带的 ODCIIndexCreate 方法创建的辅助对象 (Y &#124; N) 。|

## <a name="packages"></a>包

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|对象的所有者。|
|OBJECT_NAME|字符串|对象的名称。|
|SUBOBJECT_NAME|字符串|子对象（例如分区）的名称。|
|OBJECT_ID|小数|对象的字典对象编号。|
|DATA_OBJECT_ID|小数|包含对象的段的字典对象编号。|
|LAST_DDL_TIME|DateTime|上次通过 DDL 命令修改对象（包括授予和吊销）的时间戳。|
|TIMESTAMP|字符串|指定对象（字符数据）的时间戳。|
|状态|字符串|对象的状态（VALID、INVALID 或 N/A）。|
|TEMPORARY|字符串|对象是否是临时对象（当前会话只能看到其放入此对象本身的数据）。|
|GENERATED|字符串|此对象的名称是否由系统生成？ &#124; N)  (。|
|SECONDARY|字符串|这是否是由 Oracle9i 数据磁带的 ODCIIndexCreate 方法创建的辅助对象 (Y &#124; N) 。|
|CREATED|DateTime|创建对象的日期。|

## <a name="packagebodies"></a>PackageBodies

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|对象的所有者。|
|OBJECT_NAME|字符串|对象的名称。|
|SUBOBJECT_NAME|字符串|子对象（例如分区）的名称。|
|OBJECT_ID|小数|对象的字典对象编号。|
|DATA_OBJECT_ID|小数|包含对象的段的字典对象编号。|
|LAST_DDL_TIME|DateTime|上次通过 DDL 命令修改对象（包括授予和吊销）的时间戳。|
|TIMESTAMP|字符串|指定对象（字符数据）的时间戳。|
|状态|字符串|对象的状态（VALID、INVALID 或 N/A）。|
|TEMPORARY|字符串|对象是否是临时对象（当前会话只能看到其放入此对象本身的数据）。|
|GENERATED|字符串|此对象的名称是否由系统生成？ &#124; N)  (。|
|SECONDARY|字符串|这是否是由 Oracle9i 数据磁带的 ODCIIndexCreate 方法创建的辅助对象 (Y &#124; N) 。|
|CREATED|DateTime|创建对象的日期。|

## <a name="arguments"></a>参数

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|对象所有者的名称。|
|PACKAGE_NAME|字符串|包名称。|
|OBJECT_NAME|字符串|过程或函数的名称。|
|ARGUMENT_NAME|字符串|自变量的名称。|
|POSITION|小数|在自变量列表中的位置，对于函数返回值为 NULL。|
|SEQUENCE|小数|参数序列，包括所有嵌套级别。|
|DEFAULT_VALUE|字符串|自变量的默认值。|
|DEFAULT_LENGTH|小数|自变量的默认值的长度。|
|IN_OUT|字符串|自变量方向（IN、OUT 或 IN/OUT）。|
|DATA_LENGTH|小数|列的长度（字节数）。|
|DATA_PRECISION|小数|十进制位 (NUMBER) 或二进制位 (FLOAT) 的长度。|
|DATA_SCALE|小数|数字中小数点右侧的位数。|
|DATA_TYPE|字符串|参数的数据类型。|

## <a name="uniquekeys"></a>UniqueKeys

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|约束定义的所有者。|
|CONSTRAINT_NAME|字符串|约束定义的名称。|
|TABLE_NAME|字符串|与具有约束定义的表（或视图）关联的名称。|
|SEARCH_CONDITION|字符串|检查约束的搜索条件的文本。|
|R_OWNER|字符串|在引用约束中引用的表的所有者。|
|R_CONSTRAINT_NAME|字符串|所引用表的唯一约束定义的名称。|
|DELETE_RULE|字符串|删除引用约束的规则（CASCADE 或 NO ACTION）。|
|状态|字符串|约束的强制执行状态（ENABLED 或 DISABLED）。|
|DEFERRABLE|字符串|约束是否可以推迟。|
|VALIDATED|字符串|所有数据是否均遵循该约束（VALIDATED 或 NOT VALIDATED）。|
|GENERATED|字符串|约束名称是由用户还是由系统生成。|
|BAD|字符串|YES 值指示此约束以不明确的方式指定世纪。 为了避免因为这种不明确造成错误，使用 TO_DATE 函数重写该约束，包含一个四位的年份。|
|RELY|字符串|启用的约束强制执行还是非强制执行。|
|LAST_CHANGE|DateTime|上次启用或禁用约束的时间。|
|INDEX_OWNER|字符串|拥有索引的用户的名称。|
|INDEX_NAME|字符串|索引的名称。|

## <a name="primarykeys"></a>PrimaryKeys

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|约束定义的所有者。|
|CONSTRAINT_NAME|字符串|约束定义的名称。|
|TABLE_NAME|字符串|与具有约束定义的表（或视图）关联的名称。|
|SEARCH_CONDITION|字符串|检查约束的搜索条件的文本。|
|R_OWNER|字符串|在引用约束中引用的表的所有者。|
|R_CONSTRAINT_NAME|字符串|所引用表的唯一约束定义的名称。|
|DELETE_RULE|字符串|删除引用约束的规则（CASCADE 或 NO ACTION）。|
|状态|字符串|约束的强制执行状态（ENABLED 或 DISABLED）。|
|DEFERRABLE|字符串|约束是否可以推迟。|
|VALIDATED|字符串|所有数据是否均遵循该约束（VALIDATED 或 NOT VALIDATED）。|
|GENERATED|字符串|约束名称是由用户还是由系统生成。|
|BAD|字符串|YES 值指示此约束以不明确的方式指定世纪。 为了避免因为这种不明确造成错误，使用 TO_DATE 函数重写该约束，包含一个四位的年份。|
|RELY|字符串|启用的约束强制执行还是非强制执行。|
|LAST_CHANGE|DateTime|上次启用或禁用约束的时间。|
|INDEX_OWNER|字符串|拥有索引的用户的名称。|
|INDEX_NAME|字符串|索引的名称。|

## <a name="foreignkeys"></a>ForeignKeys

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|PRIMARY_KEY_CONSTRAINT_NAME|字符串|约束定义的名称。|
|PRIMARY_KEY_OWNER|字符串|约束定义的所有者。|
|PRIMARY_KEY_TABLE_NAME|字符串|与具有约束定义的表（或视图）关联的名称。|
|FOREIGN_KEY_OWNER|字符串|约束定义的所有者。|
|FOREIGN_KEY_CONSTRAINT_NAME|字符串|约束定义的名称。|
|FOREIGN_KEY_TABLE_NAME|字符串|与具有约束定义的表（或视图）关联的名称。|
|SEARCH_CONDITION|字符串|检查约束的搜索条件的文本。|
|R_OWNER|字符串|在引用约束中引用的表的所有者。|
|R_CONSTRAINT_NAME|字符串|所引用表的唯一约束定义的名称。|
|DELETE_RULE|字符串|删除引用约束的规则（CASCADE 或 NO ACTION）。|
|状态|字符串|约束的强制执行状态（ENABLED 或 DISABLED）。|
|VALIDATED|字符串|所有数据是否均遵循该约束（VALIDATED 或 NOT VALIDATED）。|
|GENERATED|字符串|约束名称是由用户还是由系统生成。|
|RELY|字符串|启用的约束强制执行还是非强制执行。|
|LAST_CHANGE|DateTime|上次启用或禁用约束的时间。|
|INDEX_OWNER|字符串|拥有索引的用户的名称。|
|INDEX_NAME|字符串|索引的名称。|

## <a name="foreignkeycolumns"></a>ForeignKeyColumns

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|约束定义的所有者。|
|CONSTRAINT_NAME|字符串|约束定义的名称。|
|TABLE_NAME|字符串|具有约束定义的表的名称。|
|COLUMN_NAME|字符串|约束定义中指定的对象类型列的列或属性的名称。|
|POSITION|小数|对象定义中列或属性的原始位置。|

## <a name="procedureparameters"></a>ProcedureParameters

|ColumnName|数据类型|说明|
|----------------|--------------|-----------------|
|OWNER|字符串|对象的所有者。|
|OBJECT_NAME|字符串|过程或函数的名称。|
|PACKAGE_NAME|字符串|过程或函数的名称。|
|OBJECT_ID|小数|对象的对象编号。|
|OVERLOAD|字符串|重载唯一标识符。|
|ARGUMENT_NAME|字符串|自变量的名称。|
|POSITION|小数|在自变量列表中的位置，对于函数返回值为 null。|
|SEQUENCE|小数|参数序列，包括所有嵌套级别。|
|DATA_LEVEL|小数|复合类型的参数的嵌套深度。|
|DATA_TYPE|字符串|参数的数据类型。|
|DEFAULT_VALUE|字符串|自变量的默认值。|
|DEFAULT_LENGTH|小数|参数的默认值的长度。|
|IN_OUT|字符串|自变量方向（IN、OUT 或 IN/OUT）。|
|DATA_LENGTH|小数|列的长度（字节数）。|
|DATA_PRECISION|小数|十进制位 (NUMBER) 或二进制位 (FLOAT) 的长度。|
|DATA_SCALE|小数|数字中小数点右侧的位数。|
|RADIX|小数|数字的参数基数。|
|CHARACTER_SET_NAME|字符串|自变量的字符集名称。|
|TYPE_OWNER|字符串|参数类型的所有者。|
|TYPE_NAME|字符串|参数类型的名称。 如果类型是包局部类型（即在包指定中声明），此列将显示包的名称。|
|TYPE_SUBNAME|字符串|只与包局部类型有关。 显示在 TYPE_NAME 列中标识的包中声明的类型名称。|
|TYPE_LINK|字符串|只有 TYPE_NAME 列中标识的包是远程包时，才与包局部类型有关。 此列显示用于引用远程包的数据库链接。|
|PLS_TYPE|字符串|对于数值参数，为参数的 PL/SQL 类型的名称。 否则为 Null。|
|CHAR_LENGTH|小数|字符串数据类型的字符限制。|
|CHAR_USED|字符串|指示字节限制 (B) 或字符限制 (C) 是否正式用于字符串。|

## <a name="see-also"></a>请参阅

- [ADO.NET 概述](ado-net-overview.md)
