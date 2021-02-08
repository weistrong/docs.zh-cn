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
# <a name="find-private-key-tool-findprivatekeyexe"></a><span data-ttu-id="c883e-103">“查找私钥”工具 (FindPrivateKey.exe)</span><span class="sxs-lookup"><span data-stu-id="c883e-103">Find Private Key Tool (FindPrivateKey.exe)</span></span>

<span data-ttu-id="c883e-104">可以使用此命令行工具从证书存储区中检索私钥。</span><span class="sxs-lookup"><span data-stu-id="c883e-104">This command-line tool can be used to retrieve a private key from a certificate store.</span></span> <span data-ttu-id="c883e-105">例如， *FindPrivateKey.exe* 可用于查找与证书存储区中特定 x.509 证书关联的私钥文件的位置和名称。</span><span class="sxs-lookup"><span data-stu-id="c883e-105">For example, *FindPrivateKey.exe* can be used to find the location and name of the private key file associated with a specific X.509 certificate in the certificate store.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c883e-106">FindPrivateKey 工具附带作为一个 WCF 示例。</span><span class="sxs-lookup"><span data-stu-id="c883e-106">The FindPrivateKey tool is shipped as a WCF sample.</span></span> <span data-ttu-id="c883e-107">有关在何处查找示例以及如何生成示例的详细信息，请参阅 [FindPrivateKey](./samples/findprivatekey.md)。</span><span class="sxs-lookup"><span data-stu-id="c883e-107">For more information about where to find the sample and how to build it, see [FindPrivateKey](./samples/findprivatekey.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c883e-108">语法</span><span class="sxs-lookup"><span data-stu-id="c883e-108">Syntax</span></span>

```console
FindPrivateKey<storeName> <storeLocation> [{ {-n <subjectName>} | {-t <thumbprint>} } [-f | -d | -a]]
```

## <a name="remarks"></a><span data-ttu-id="c883e-109">备注</span><span class="sxs-lookup"><span data-stu-id="c883e-109">Remarks</span></span>

<span data-ttu-id="c883e-110">下表介绍了可用于“查找私钥”工具 (FindPrivateKey.exe) 的自变量和选项。</span><span class="sxs-lookup"><span data-stu-id="c883e-110">The following tables describe the arguments and the options that can be used with the Find Private Key tool (FindPrivateKey.exe).</span></span>

|<span data-ttu-id="c883e-111">参数</span><span class="sxs-lookup"><span data-stu-id="c883e-111">Argument</span></span>|<span data-ttu-id="c883e-112">说明</span><span class="sxs-lookup"><span data-stu-id="c883e-112">Description</span></span>|
|--------------|-----------------|
|`storeName`|<span data-ttu-id="c883e-113">证书存储区的名称。</span><span class="sxs-lookup"><span data-stu-id="c883e-113">Name of the certificate store.</span></span>|
|`storeLocation`|<span data-ttu-id="c883e-114">证书存储区的位置。</span><span class="sxs-lookup"><span data-stu-id="c883e-114">The location of the certificate store.</span></span>|

|<span data-ttu-id="c883e-115">选项</span><span class="sxs-lookup"><span data-stu-id="c883e-115">Option</span></span>|<span data-ttu-id="c883e-116">说明</span><span class="sxs-lookup"><span data-stu-id="c883e-116">Description</span></span>|
|------------|-----------------|
|<span data-ttu-id="c883e-117">`/n <`*subjectName*`>`</span><span class="sxs-lookup"><span data-stu-id="c883e-117">`/n <` *subjectName* `>`</span></span>|<span data-ttu-id="c883e-118">指定证书的主题名称。</span><span class="sxs-lookup"><span data-stu-id="c883e-118">Specifies the subject name of the certificate.</span></span>|
|<span data-ttu-id="c883e-119">`/t <`*指纹*`>`</span><span class="sxs-lookup"><span data-stu-id="c883e-119">`/t <` *thumbprint* `>`</span></span>|<span data-ttu-id="c883e-120">指定证书的指纹。</span><span class="sxs-lookup"><span data-stu-id="c883e-120">Specifies the thumbprint of the certificate.</span></span> <span data-ttu-id="c883e-121">使用 Certmgr.exe 来检索证书的指纹。</span><span class="sxs-lookup"><span data-stu-id="c883e-121">Use Certmgr.exe to retrieve the thumbprint of the certificate.</span></span>|
|`/f`|<span data-ttu-id="c883e-122">只输出文件名。</span><span class="sxs-lookup"><span data-stu-id="c883e-122">Outputs the file name only.</span></span>|
|`/d`|<span data-ttu-id="c883e-123">只输出目录。</span><span class="sxs-lookup"><span data-stu-id="c883e-123">Outputs the directory only.</span></span>|
|`/a`|<span data-ttu-id="c883e-124">输出绝对文件名。</span><span class="sxs-lookup"><span data-stu-id="c883e-124">Outputs the absolute file name.</span></span>|

## <a name="examples"></a><span data-ttu-id="c883e-125">示例</span><span class="sxs-lookup"><span data-stu-id="c883e-125">Examples</span></span>

<span data-ttu-id="c883e-126">以下命令检索 John Doe 的私钥：</span><span class="sxs-lookup"><span data-stu-id="c883e-126">The following command retrieves the private key for John Doe:</span></span>

```console
FindPrivateKey My CurrentUser -n "CN=John Doe"
```

<span data-ttu-id="c883e-127">以下命令检索本地计算机的私钥：</span><span class="sxs-lookup"><span data-stu-id="c883e-127">The following command retrieves the private key for the local machine:</span></span>

```console
FindPrivateKey My LocalMachine -t "03 33 98 63 d0 47 e7 48 71 33 62 64 76 5c 4c 9d 42 1d 6b 52" –a
```
