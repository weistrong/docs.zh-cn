---
description: 了解详细信息：如何：验证 DBML 和外部映射文件
title: 如何：验证 DBML 和外部映射文件
ms.date: 03/30/2017
ms.assetid: d9ea37f5-0a9e-4401-8fc3-1e6fd44c49f9
ms.openlocfilehash: 46e5c787bef8e152020fc97631ef8c1c4928fe74
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785778"
---
# <a name="how-to-validate-dbml-and-external-mapping-files"></a><span data-ttu-id="9b2de-103">如何：验证 DBML 和外部映射文件</span><span class="sxs-lookup"><span data-stu-id="9b2de-103">How to: Validate DBML and External Mapping Files</span></span>

<span data-ttu-id="9b2de-104">您修改的外部映射文件和 .dbml 文件必须通过其各自架构定义的验证。</span><span class="sxs-lookup"><span data-stu-id="9b2de-104">External mapping files and .dbml files that you modify must be validated against their respective schema definitions.</span></span> <span data-ttu-id="9b2de-105">本主题向 Visual Studio 用户提供实现验证过程的步骤。</span><span class="sxs-lookup"><span data-stu-id="9b2de-105">This topic provides Visual Studio users with the steps to implement the validation process.</span></span>

[!INCLUDE[note_settings_general](../../../../../../includes/note-settings-general-md.md)]

### <a name="to-validate-a-dbml-or-xml-file"></a><span data-ttu-id="9b2de-106">验证 .dbml 或 XML 文件</span><span class="sxs-lookup"><span data-stu-id="9b2de-106">To validate a .dbml or XML file</span></span>

1. <span data-ttu-id="9b2de-107">在 Visual Studio 的 " **文件** " 菜单上，指向 " **打开**"，然后单击 " **文件**"。</span><span class="sxs-lookup"><span data-stu-id="9b2de-107">On the Visual Studio **File** menu, point to **Open**, and then click **File**.</span></span>

2. <span data-ttu-id="9b2de-108">在 " **打开文件** " 对话框中，单击要验证的 .DBML 或 XML 映射文件。</span><span class="sxs-lookup"><span data-stu-id="9b2de-108">In the **Open File** dialog box, click the .dbml or XML mapping file that you want to validate.</span></span>

    <span data-ttu-id="9b2de-109">文件将在 **XML 编辑器** 中打开。</span><span class="sxs-lookup"><span data-stu-id="9b2de-109">The file opens in the **XML Editor**.</span></span>

3. <span data-ttu-id="9b2de-110">右键单击该窗口，然后单击 " **属性**"。</span><span class="sxs-lookup"><span data-stu-id="9b2de-110">Right-click the window, and then click **Properties**.</span></span>

4. <span data-ttu-id="9b2de-111">在 " **属性** " 窗口中，单击 " **架构** " 属性的省略号。</span><span class="sxs-lookup"><span data-stu-id="9b2de-111">In the **Properties** window, click the ellipsis for the **Schemas** property.</span></span>

    <span data-ttu-id="9b2de-112">" **XML 架构** " 对话框随即打开。</span><span class="sxs-lookup"><span data-stu-id="9b2de-112">The **XML Schemas** dialog box opens.</span></span>

5. <span data-ttu-id="9b2de-113">请注意符合您需要的相应架构定义。</span><span class="sxs-lookup"><span data-stu-id="9b2de-113">Note the appropriate schema definition for your purpose.</span></span>

    - <span data-ttu-id="9b2de-114">DbmlSchema.xsd 是用于验证 .dbml 文件的架构定义。</span><span class="sxs-lookup"><span data-stu-id="9b2de-114">DbmlSchema.xsd is the schema definition for validating a .dbml file.</span></span> <span data-ttu-id="9b2de-115">有关详细信息，请参阅 [LINQ to SQL 中的代码生成](code-generation-in-linq-to-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="9b2de-115">For more information, see [Code Generation in LINQ to SQL](code-generation-in-linq-to-sql.md).</span></span>

    - <span data-ttu-id="9b2de-116">LinqToSqlMapping.xsd 是用于验证外部 XML 映射文件的架构定义。</span><span class="sxs-lookup"><span data-stu-id="9b2de-116">LinqToSqlMapping.xsd is the schema definition for validating an external XML mapping file.</span></span> <span data-ttu-id="9b2de-117">有关详细信息，请参阅 [外部映射](external-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="9b2de-117">For more information, see [External Mapping](external-mapping.md).</span></span>

6. <span data-ttu-id="9b2de-118">在 "所需的架构定义" 行的 " **使用** " 列中，单击 "打开" 下拉框，然后单击 " **使用此架构**"。</span><span class="sxs-lookup"><span data-stu-id="9b2de-118">In the **Use** column of the desired schema definition row, click to open the drop-down box, and then click **Use this schema**.</span></span>

    <span data-ttu-id="9b2de-119">此架构定义文件现在即与您的 DBML 或 XML 映射文件关联。</span><span class="sxs-lookup"><span data-stu-id="9b2de-119">The schema definition file is now associated with your DBML or XML mapping file.</span></span>

    <span data-ttu-id="9b2de-120">请确保未选择其他架构定义。</span><span class="sxs-lookup"><span data-stu-id="9b2de-120">Make sure no other schema definitions are selected.</span></span>

7. <span data-ttu-id="9b2de-121">在 **“视图”** 菜单上单击 **“错误列表”** 。</span><span class="sxs-lookup"><span data-stu-id="9b2de-121">On the **View** menu, click **Error List**.</span></span>

    <span data-ttu-id="9b2de-122">确定是否已生成了错误、警告或消息。</span><span class="sxs-lookup"><span data-stu-id="9b2de-122">Determine whether errors, warnings, or messages have been generated.</span></span> <span data-ttu-id="9b2de-123">如果未生成，则说明此 XML 文件对此架构定义有效。</span><span class="sxs-lookup"><span data-stu-id="9b2de-123">If not, the XML file is valid against the schema definition.</span></span>

## <a name="alternate-method-for-supplying-schema-definition"></a><span data-ttu-id="9b2de-124">提供架构定义的另一种方法</span><span class="sxs-lookup"><span data-stu-id="9b2de-124">Alternate Method for Supplying Schema Definition</span></span>

<span data-ttu-id="9b2de-125">如果由于某种原因相应的 .xsd 文件未出现在 " **XML 架构** " 对话框中，您可以从 "帮助" 主题下载 .xsd 文件。</span><span class="sxs-lookup"><span data-stu-id="9b2de-125">If for some reason the appropriate .xsd file does not appear in the **XML Schemas** dialog box, you can download the .xsd file from a Help topic.</span></span> <span data-ttu-id="9b2de-126">以下步骤可帮助你以 Visual Studio XML 编辑器所需的 Unicode 格式保存下载的文件。</span><span class="sxs-lookup"><span data-stu-id="9b2de-126">The following steps help you save the downloaded file in the Unicode format required by the Visual Studio XML Editor.</span></span>

#### <a name="to-copy-a-schema-definition-file-from-a-help-topic"></a><span data-ttu-id="9b2de-127">从帮助主题中复制架构定义文件</span><span class="sxs-lookup"><span data-stu-id="9b2de-127">To copy a schema definition file from a Help topic</span></span>

1. <span data-ttu-id="9b2de-128">找到包含本主题前面部分所述架构定义的帮助主题。</span><span class="sxs-lookup"><span data-stu-id="9b2de-128">Locate the Help topic that contains the schema definition as described earlier in this topic.</span></span>

    - <span data-ttu-id="9b2de-129">对于 .dbml 文件，请参阅 [LINQ to SQL 中的代码生成](code-generation-in-linq-to-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="9b2de-129">For .dbml files, see [Code Generation in LINQ to SQL](code-generation-in-linq-to-sql.md).</span></span>

    - <span data-ttu-id="9b2de-130">有关外部映射文件，请参阅 [外部映射](external-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="9b2de-130">For external mapping files, see [External Mapping](external-mapping.md).</span></span>

2. <span data-ttu-id="9b2de-131">单击 " **复制代码** "，将代码文件复制到剪贴板。</span><span class="sxs-lookup"><span data-stu-id="9b2de-131">Click **Copy Code** to copy the code file to the Clipboard.</span></span>

3. <span data-ttu-id="9b2de-132">启动记事本以创建一个新文件。</span><span class="sxs-lookup"><span data-stu-id="9b2de-132">Start Notepad to create a new file.</span></span>

4. <span data-ttu-id="9b2de-133">将剪贴板中的代码粘贴到记事本文件中。</span><span class="sxs-lookup"><span data-stu-id="9b2de-133">Paste the code from the clipboard into Notepad file.</span></span>

5. <span data-ttu-id="9b2de-134">在记事本的 " **文件** " 菜单上，单击 " **另存为**"。</span><span class="sxs-lookup"><span data-stu-id="9b2de-134">On the Notepad **File** menu, click **Save As**.</span></span>

6. <span data-ttu-id="9b2de-135">在 " **编码** " 框中，选择 " **Unicode**"。</span><span class="sxs-lookup"><span data-stu-id="9b2de-135">In the **Encoding** box, select **Unicode**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="9b2de-136">这样选择可保证在此文本文件前面加上 Unicode 16 字节顺序标记 (`FFFE`)。</span><span class="sxs-lookup"><span data-stu-id="9b2de-136">This selection guarantees that the Unicode-16 byte-order marker (`FFFE`) is prepended to the text file.</span></span>

7. <span data-ttu-id="9b2de-137">在 " **文件名" 框中** ，创建具有 .xsd 扩展名的文件名。</span><span class="sxs-lookup"><span data-stu-id="9b2de-137">In the **File name** box, create a file name with an .xsd extension.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b2de-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="9b2de-138">See also</span></span>

- [<span data-ttu-id="9b2de-139">引用</span><span class="sxs-lookup"><span data-stu-id="9b2de-139">Reference</span></span>](reference.md)
