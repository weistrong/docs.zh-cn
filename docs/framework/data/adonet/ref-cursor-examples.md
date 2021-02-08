---
description: 了解详细信息： REF CURSOR 示例
title: REF CURSOR 示例
ms.date: 03/30/2017
ms.assetid: c257da03-c6c9-4cf8-b591-b7740a962c40
ms.openlocfilehash: e7cb411778b325400d37511b082032e590b339c0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99773220"
---
# <a name="ref-cursor-examples"></a><span data-ttu-id="49dc1-103">REF CURSOR 示例</span><span class="sxs-lookup"><span data-stu-id="49dc1-103">REF CURSOR Examples</span></span>

<span data-ttu-id="49dc1-104">REF CURSOR 示例包括下列三个 Visual Basic 示例，演示如何使用 REF CURSOR。</span><span class="sxs-lookup"><span data-stu-id="49dc1-104">The REF CURSOR examples are comprised of the following three Microsoft Visual Basic examples that demonstrate using REF CURSORs.</span></span>  
  
|<span data-ttu-id="49dc1-105">示例</span><span class="sxs-lookup"><span data-stu-id="49dc1-105">Sample</span></span>|<span data-ttu-id="49dc1-106">说明</span><span class="sxs-lookup"><span data-stu-id="49dc1-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="49dc1-107">OracleDataReader 中的 REF CURSOR 参数</span><span class="sxs-lookup"><span data-stu-id="49dc1-107">REF CURSOR Parameters in an OracleDataReader</span></span>](ref-cursor-parameters-in-an-oracledatareader.md)|<span data-ttu-id="49dc1-108">此示例执行一个 PL/SQL 存储过程，返回 REF CURSOR 参数，并将值作为 <xref:System.Data.OracleClient.OracleDataReader> 读取。</span><span class="sxs-lookup"><span data-stu-id="49dc1-108">This example executes a PL/SQL stored procedure that returns a REF CURSOR parameter, and reads the value as an <xref:System.Data.OracleClient.OracleDataReader>.</span></span>|  
|[<span data-ttu-id="49dc1-109">使用 OracleDataReader 从多个 REF CURSOR 中检索数据</span><span class="sxs-lookup"><span data-stu-id="49dc1-109">Retrieving Data from Multiple REF CURSORs Using an OracleDataReader</span></span>](retrieving-data-from-multiple-ref-cursors.md)|<span data-ttu-id="49dc1-110">此示例执行一个 PL/SQL 存储过程，该存储过程返回两个 REF CURSOR 参数，并使用 **OracleDataReader** 读取值。</span><span class="sxs-lookup"><span data-stu-id="49dc1-110">This example executes a PL/SQL stored procedure that returns two REF CURSOR parameters, and reads the values using an **OracleDataReader**.</span></span>|  
|[<span data-ttu-id="49dc1-111">使用一个或多个 REF CURSOR 填充数据集</span><span class="sxs-lookup"><span data-stu-id="49dc1-111">Filling a DataSet Using One or More REF CURSORs</span></span>](filling-a-dataset-using-one-or-more-ref-cursors.md)|<span data-ttu-id="49dc1-112">此示例执行一个 PL/SQL 存储过程，返回两个 REF CURSOR 参数，并使用返回的行填充 <xref:System.Data.DataSet>。</span><span class="sxs-lookup"><span data-stu-id="49dc1-112">This example executes a PL/SQL stored procedure that returns two REF CURSOR parameters, and fills a <xref:System.Data.DataSet> with the rows that are returned.</span></span>|  
  
 <span data-ttu-id="49dc1-113">要使用这些示例，可能需要创建 Oracle 表，并且必须创建 PL/SQL 包和包正文。</span><span class="sxs-lookup"><span data-stu-id="49dc1-113">To use these examples, you may need to create the Oracle tables, and you must create a PL/SQL package and package body.</span></span>  
  
## <a name="creating-the-oracle-tables"></a><span data-ttu-id="49dc1-114">创建 Oracle 表</span><span class="sxs-lookup"><span data-stu-id="49dc1-114">Creating the Oracle Tables</span></span>  

 <span data-ttu-id="49dc1-115">这些示例使用 Oracle Scott/Tiger 架构中定义的表。</span><span class="sxs-lookup"><span data-stu-id="49dc1-115">These examples use tables that are defined in the Oracle Scott/Tiger schema.</span></span> <span data-ttu-id="49dc1-116">大多数 Oracle 安装均包括 Oracle Scott/Tiger 架构。</span><span class="sxs-lookup"><span data-stu-id="49dc1-116">The Oracle Scott/Tiger schema is included with most Oracle installations.</span></span> <span data-ttu-id="49dc1-117">如果此架构不存在，可以使用 {OracleHome}\rdbms\admin\scott.sql 中的 SQL 命令文件创建供这些示例使用的表和索引。</span><span class="sxs-lookup"><span data-stu-id="49dc1-117">If this schema does not exist, you can use the SQL commands file in {OracleHome}\rdbms\admin\scott.sql to create the tables and indexes used by these examples.</span></span>  
  
## <a name="creating-the-oracle-package-and-package-body"></a><span data-ttu-id="49dc1-118">创建 Oracle 包和包正文</span><span class="sxs-lookup"><span data-stu-id="49dc1-118">Creating the Oracle Package and Package Body</span></span>  

 <span data-ttu-id="49dc1-119">这些示例要求服务器上存在以下 PL/SQL 包和包正文。</span><span class="sxs-lookup"><span data-stu-id="49dc1-119">These examples require the following PL/SQL package and package body on your server.</span></span> <span data-ttu-id="49dc1-120">在 Oracle 服务器上创建以下 Oracle 包。</span><span class="sxs-lookup"><span data-stu-id="49dc1-120">Create the following Oracle package on the Oracle server.</span></span>  
  
```sql
CREATE OR REPLACE PACKAGE CURSPKG AS
    TYPE T_CURSOR IS REF CURSOR;
    PROCEDURE OPEN_ONE_CURSOR (N_EMPNO IN NUMBER,
                               IO_CURSOR IN OUT T_CURSOR);
    PROCEDURE OPEN_TWO_CURSORS (EMPCURSOR OUT T_CURSOR,
                                DEPTCURSOR OUT T_CURSOR);  
END CURSPKG;  
/
```  
  
 <span data-ttu-id="49dc1-121">在 Oracle 服务器上创建下面的 Oracle 包正文。</span><span class="sxs-lookup"><span data-stu-id="49dc1-121">Create the following Oracle package body on the Oracle server.</span></span>  
  
```sql
CREATE OR REPLACE PACKAGE BODY CURSPKG AS  
    PROCEDURE OPEN_ONE_CURSOR (N_EMPNO IN NUMBER,  
                               IO_CURSOR IN OUT T_CURSOR)  
    IS
        V_CURSOR T_CURSOR;
    BEGIN
        IF N_EMPNO <> 0
        THEN  
             OPEN V_CURSOR FOR
             SELECT EMP.EMPNO, EMP.ENAME, DEPT.DEPTNO, DEPT.DNAME
                  FROM EMP, DEPT
                  WHERE EMP.DEPTNO = DEPT.DEPTNO
                  AND EMP.EMPNO = N_EMPNO;  
  
        ELSE
             OPEN V_CURSOR FOR
             SELECT EMP.EMPNO, EMP.ENAME, DEPT.DEPTNO, DEPT.DNAME
                  FROM EMP, DEPT
                  WHERE EMP.DEPTNO = DEPT.DEPTNO;  
  
        END IF;  
        IO_CURSOR := V_CURSOR;
    END OPEN_ONE_CURSOR;
  
    PROCEDURE OPEN_TWO_CURSORS (EMPCURSOR OUT T_CURSOR,  
                                DEPTCURSOR OUT T_CURSOR)  
    IS
        V_CURSOR1 T_CURSOR;
        V_CURSOR2 T_CURSOR;
    BEGIN
        OPEN V_CURSOR1 FOR SELECT * FROM EMP;  
        OPEN V_CURSOR2 FOR SELECT * FROM DEPT;  
        EMPCURSOR  := V_CURSOR1;
        DEPTCURSOR := V_CURSOR2;
    END OPEN_TWO_CURSORS;
END CURSPKG;  
/  
```  
  
## <a name="see-also"></a><span data-ttu-id="49dc1-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="49dc1-122">See also</span></span>

- [<span data-ttu-id="49dc1-123">Oracle REF CURSOR</span><span class="sxs-lookup"><span data-stu-id="49dc1-123">Oracle REF CURSORs</span></span>](oracle-ref-cursors.md)
- [<span data-ttu-id="49dc1-124">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="49dc1-124">ADO.NET Overview</span></span>](ado-net-overview.md)
