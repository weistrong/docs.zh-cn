---
description: 详细了解：操作说明：在 Visual Basic 中使用连接到串行端口的调制解调器拨号
title: 如何：使用连接到串行端口的调制解调器拨号
ms.date: 07/20/2015
helpviewer_keywords:
- modems [Visual Basic], dialing
- serial ports [Visual Basic], dialing
- My.Computer.Ports object
ms.assetid: 3834db40-f431-45f1-b671-dc91787164b6
ms.openlocfilehash: 016a3f768020c551c4f4ca7f5a097f4f1f9d07d7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797700"
---
# <a name="how-to-dial-modems-attached-to-serial-ports-in-visual-basic"></a>如何：在 Visual Basic 中使用连接到串行端口的调制解调器拨号

本主题介绍如何在 Visual Basic 中使用 `My.Computer.Ports` 进行调制解调器拨号。  
  
 通常，调制解调器连接到计算机的某个串行端口。 若要使应用程序与调制解调器通信，必须将命令发送到相应的串行端口。  
  
### <a name="to-dial-a-modem"></a>调制解调器拨号  
  
1. 确定调制解调器连接到的串行端口。 此示例假定调制解调器在 COM1 上。  
  
2. 使用 `My.Computer.Ports.OpenSerialPort` 方法获取对端口的引用。 有关详细信息，请参阅 <xref:Microsoft.VisualBasic.Devices.Ports.OpenSerialPort%2A>。  
  
     `Using` 块允许应用程序在即使会生成异常的情况下也关闭串行端口。 操作串行端口的所有代码都应出现在此块中，或者出现在 `Try...Catch...Finally` 块中。  
  
     [!code-vb[VbVbalrMyComputer#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#28)]  
  
3. 设置 `DtrEnable` 属性，指示计算机已准备好接受从调制解调器传入的传输。  
  
     [!code-vb[VbVbalrMyComputer#29](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#29)]  
  
4. 通过 <xref:System.IO.Ports.SerialPort.Write%2A> 方法将拨号命令和电话号码从串行端口发送到调制解调器。  
  
     [!code-vb[VbVbalrMyComputer#30](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#30)]  
  
## <a name="example"></a>示例  

 [!code-vb[VbVbalrMyComputer#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#27)]  
  
 此代码示例也可作为 IntelliSense 代码片段。 它位于代码片段选取器的“连接和网络”中。 有关详细信息，请参阅[代码片段](/visualstudio/ide/code-snippets)。  
  
## <a name="compiling-the-code"></a>编译代码  

 该示例需要引用 <xref:System?displayProperty=nameWithType> 命名空间。  
  
## <a name="robust-programming"></a>可靠编程  

 此示例假定调制解调器已连接 COM1。 建议使代码允许用户从可用端口列表中选择所需串行端口。 有关详细信息，请参阅[如何：显示可用的串行端口](how-to-show-available-serial-ports.md)。  
  
 本示例使用 `Using` 块来确保应用程序在即使会引发异常的情况下也关闭端口。 有关详细信息，请参阅 [Using 语句](../../../language-reference/statements/using-statement.md)。  
  
 在本例中，应用程序拨打调制解调器后断开了串行端口。 实际上，需要将数据传入和传出调制解调器。 有关详细信息，请参阅[如何：从串行端口接收字符串](how-to-receive-strings-from-serial-ports.md)。  
  
## <a name="see-also"></a>另请参阅

- <xref:Microsoft.VisualBasic.Devices.Ports>
- <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType>
- [如何：将字符串发送到串行端口](how-to-send-strings-to-serial-ports.md)
- [如何：从串行端口接收字符串](how-to-receive-strings-from-serial-ports.md)
- [如何：显示可用的串行端口](how-to-show-available-serial-ports.md)
