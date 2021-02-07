---
description: 了解有关详细信息，请参阅 OracleDataReader 中的 REF CURSOR 参数
title: OracleDataReader 中的 REF CURSOR 参数
ms.date: 03/30/2017
dev_langs:
- vb
ms.assetid: 801dff0f-2508-45aa-9416-f45d6887740c
ms.openlocfilehash: 94c4e1fe6eb6c065b8551e09c49b322b4728abeb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739152"
---
# <a name="ref-cursor-parameters-in-an-oracledatareader"></a><span data-ttu-id="8963f-103">OracleDataReader 中的 REF CURSOR 参数</span><span class="sxs-lookup"><span data-stu-id="8963f-103">REF CURSOR Parameters in an OracleDataReader</span></span>

<span data-ttu-id="8963f-104">此 Microsoft Visual Basic 示例执行一个 PL/SQL 存储过程，返回 REF CURSOR 参数，并将值作为 <xref:System.Data.OracleClient.OracleDataReader> 读取。</span><span class="sxs-lookup"><span data-stu-id="8963f-104">This Microsoft Visual Basic example executes a PL/SQL stored procedure that returns a REF CURSOR parameter, and reads the value as an <xref:System.Data.OracleClient.OracleDataReader>.</span></span>

```vb
Private Sub Button1_Click(ByVal sender As Object, _
  ByVal e As System.EventArgs) Handles Button1.Click

  Dim connString As New String(_
      "Data Source=Oracle9i;User ID=scott;Password=[PLACEHOLDER];")
  Using conn As New OracleConnection(connString)
    Dim cmd As New OracleCommand()
    Dim rdr As OracleDataReader

    conn.Open()
    cmd.Connection = conn
    cmd.CommandText = "CURSPKG.OPEN_ONE_CURSOR"
    cmd.CommandType = CommandType.StoredProcedure
    cmd.Parameters.Add(New OracleParameter(
      "N_EMPNO", OracleType.Number)).Value = 7369
    cmd.Parameters.Add(New OracleParameter(
      "IO_CURSOR", OracleType.Cursor)).Direction = ParameterDirection.Output

    rdr = cmd.ExecuteReader()
    While (rdr.Read())
        REM do something with the values
    End While

    rdr.Close()
  End Using
End Sub
```

## <a name="see-also"></a><span data-ttu-id="8963f-105">请参阅</span><span class="sxs-lookup"><span data-stu-id="8963f-105">See also</span></span>

- [<span data-ttu-id="8963f-106">Oracle REF CURSOR</span><span class="sxs-lookup"><span data-stu-id="8963f-106">Oracle REF CURSORs</span></span>](oracle-ref-cursors.md)
- [<span data-ttu-id="8963f-107">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="8963f-107">ADO.NET Overview</span></span>](ado-net-overview.md)
