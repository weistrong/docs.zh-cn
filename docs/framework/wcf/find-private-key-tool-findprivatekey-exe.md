---
description: '了解详细信息：查找私钥工具 ( # A0) '
title: “查找私钥”工具 (FindPrivateKey.exe)
ms.date: 09/11/2017
ms.assetid: b8846a95-3fcc-4e8c-b9c0-128d975a6307
ms.openlocfilehash: 1d87d19e17c1de89c13db6d7ca092eedf630e6ca
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99793280"
---
# <a name="find-private-key-tool-findprivatekeyexe"></a>“查找私钥”工具 (FindPrivateKey.exe)

可以使用此命令行工具从证书存储区中检索私钥。 例如， *FindPrivateKey.exe* 可用于查找与证书存储区中特定 x.509 证书关联的私钥文件的位置和名称。

> [!IMPORTANT]
> FindPrivateKey 工具附带作为一个 WCF 示例。 有关在何处查找示例以及如何生成示例的详细信息，请参阅 [FindPrivateKey](./samples/findprivatekey.md)。

## <a name="syntax"></a>语法

```console
FindPrivateKey<storeName> <storeLocation> [{ {-n <subjectName>} | {-t <thumbprint>} } [-f | -d | -a]]
```

## <a name="remarks"></a>备注

下表介绍了可用于“查找私钥”工具 (FindPrivateKey.exe) 的自变量和选项。

|参数|说明|
|--------------|-----------------|
|`storeName`|证书存储区的名称。|
|`storeLocation`|证书存储区的位置。|

|选项|说明|
|------------|-----------------|
|`/n <`*subjectName*`>`|指定证书的主题名称。|
|`/t <`*指纹*`>`|指定证书的指纹。 使用 Certmgr.exe 来检索证书的指纹。|
|`/f`|只输出文件名。|
|`/d`|只输出目录。|
|`/a`|输出绝对文件名。|

## <a name="examples"></a>示例

以下命令检索 John Doe 的私钥：

```console
FindPrivateKey My CurrentUser -n "CN=John Doe"
```

以下命令检索本地计算机的私钥：

```console
FindPrivateKey My LocalMachine -t "03 33 98 63 d0 47 e7 48 71 33 62 64 76 5c 4c 9d 42 1d 6b 52" –a
```
