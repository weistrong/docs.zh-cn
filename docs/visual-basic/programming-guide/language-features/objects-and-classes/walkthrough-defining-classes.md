---
description: '了解详细信息：演练：定义类 (Visual Basic) '
title: 定义类
ms.date: 07/20/2015
helpviewer_keywords:
- execution [Visual Basic], ending
- objects [Visual Basic], initializing
- Initialize event [Visual Basic]
- files [Visual Basic], closing
- programs [Visual Basic], quitting
- code, exiting
- objects [Visual Basic], creating
- program termination
- classes [Visual Basic], walkthroughs
- class modules, walkthroughs
- Terminate event [Visual Basic]
- execution [Visual Basic], stopping
ms.assetid: 07018828-2d49-4cf5-a44b-19fb15d9efea
ms.openlocfilehash: a97e04b92db3387966afa410d5697a05b482ae09
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100438783"
---
# <a name="walkthrough-defining-classes-visual-basic"></a><span data-ttu-id="dc894-103">演练：定义类 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dc894-103">Walkthrough: Defining Classes (Visual Basic)</span></span>

<span data-ttu-id="dc894-104">本演练演示如何定义类，然后可以使用这些类来创建对象。</span><span class="sxs-lookup"><span data-stu-id="dc894-104">This walkthrough demonstrates how to define classes, which you can then use to create objects.</span></span> <span data-ttu-id="dc894-105">它还演示了如何将属性和方法添加到新类，并演示了如何初始化对象。</span><span class="sxs-lookup"><span data-stu-id="dc894-105">It also shows you how to add properties and methods to the new class, and demonstrates how to initialize an object.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
## <a name="to-define-a-class"></a><span data-ttu-id="dc894-106">定义类</span><span class="sxs-lookup"><span data-stu-id="dc894-106">To define a class</span></span>
  
1. <span data-ttu-id="dc894-107">通过单击 "**文件**" 菜单上的 "**新建项目**" 来创建项目。</span><span class="sxs-lookup"><span data-stu-id="dc894-107">Create a project by clicking **New Project** on the **File** menu.</span></span> <span data-ttu-id="dc894-108">此时将出现“新建项目”  对话框。</span><span class="sxs-lookup"><span data-stu-id="dc894-108">The **New Project** dialog box appears.</span></span>  
  
2. <span data-ttu-id="dc894-109">从 Visual Basic 项目模板列表中选择 "Windows 应用程序" 以显示新项目。</span><span class="sxs-lookup"><span data-stu-id="dc894-109">Select Windows Application from the list of Visual Basic project templates to display the new project.</span></span>  
  
3. <span data-ttu-id="dc894-110">通过单击 "**项目**" 菜单上的 "**添加类**"，将新类添加到项目。</span><span class="sxs-lookup"><span data-stu-id="dc894-110">Add a new class to the project by clicking **Add Class** on the **Project** menu.</span></span> <span data-ttu-id="dc894-111">“添加新项”  对话框随即出现。</span><span class="sxs-lookup"><span data-stu-id="dc894-111">The **Add New Item** dialog box appears.</span></span>  
  
4. <span data-ttu-id="dc894-112">选择 " **类** " 模板。</span><span class="sxs-lookup"><span data-stu-id="dc894-112">Select the **Class** template.</span></span>  
  
5. <span data-ttu-id="dc894-113">将新类命名为 `UserNameInfo.vb` ，然后单击 " **添加** " 以显示新类的代码。</span><span class="sxs-lookup"><span data-stu-id="dc894-113">Name the new class `UserNameInfo.vb`, and then click **Add** to display the code for the new class.</span></span>  
  
     [!code-vb[VbVbalrOOP#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#5)]
  
    > [!NOTE]
    > <span data-ttu-id="dc894-114">你可以使用 Visual Basic **代码编辑器** 将类添加到启动窗体中，方法是键入 `Class` 关键字，然后键入新类的名称。</span><span class="sxs-lookup"><span data-stu-id="dc894-114">You can use the Visual Basic **Code Editor** to add a class to your startup form by typing the `Class` keyword followed by the name of the new class.</span></span> <span data-ttu-id="dc894-115">**代码编辑器** 为您提供相应的 `End Class` 语句。</span><span class="sxs-lookup"><span data-stu-id="dc894-115">The **Code Editor** provides a corresponding `End Class` statement for you.</span></span>  
  
6. <span data-ttu-id="dc894-116">通过在和语句之间添加以下代码，为类定义私有字段 `Class` `End Class` ：</span><span class="sxs-lookup"><span data-stu-id="dc894-116">Define a private field for the class by adding the following code between the `Class` and `End Class` statements:</span></span>  
  
     [!code-vb[VbVbalrOOP#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#7)]
  
     <span data-ttu-id="dc894-117">将字段声明为 `Private` 意味着它只能在类中使用。</span><span class="sxs-lookup"><span data-stu-id="dc894-117">Declaring the field as `Private` means it can be used only within the class.</span></span> <span data-ttu-id="dc894-118">可以通过使用访问修饰符（如） `Public` 提供更多访问权限，使字段从类的外部可用。</span><span class="sxs-lookup"><span data-stu-id="dc894-118">You can make fields available from outside a class by using access modifiers such as `Public` that provide more access.</span></span> <span data-ttu-id="dc894-119">有关详细信息，请参阅 [Visual Basic 中的访问级别](../declared-elements/access-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="dc894-119">For more information, see [Access levels in Visual Basic](../declared-elements/access-levels.md).</span></span>  
  
7. <span data-ttu-id="dc894-120">通过添加以下代码来定义类的属性：</span><span class="sxs-lookup"><span data-stu-id="dc894-120">Define a property for the class by adding the following code:</span></span>  
  
     [!code-vb[VbVbalrOOP#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#8)]
  
8. <span data-ttu-id="dc894-121">通过添加以下代码为类定义方法：</span><span class="sxs-lookup"><span data-stu-id="dc894-121">Define a method for the class by adding the following code:</span></span>  
  
     [!code-vb[VbVbalrOOP#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#9)]
  
9. <span data-ttu-id="dc894-122">通过添加名为的过程为新类定义参数化构造函数 `Sub New` ：</span><span class="sxs-lookup"><span data-stu-id="dc894-122">Define a parameterized constructor for the new class by adding a procedure named `Sub New`:</span></span>  
  
     [!code-vb[VbVbalrOOP#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#10)]
  
     <span data-ttu-id="dc894-123">`Sub New`当创建基于此类的对象时，将自动调用构造函数。</span><span class="sxs-lookup"><span data-stu-id="dc894-123">The `Sub New` constructor is called automatically when an object based on this class is created.</span></span> <span data-ttu-id="dc894-124">此构造函数设置包含用户名的字段的值。</span><span class="sxs-lookup"><span data-stu-id="dc894-124">This constructor sets the value of the field that holds the user name.</span></span>  
  
## <a name="to-create-a-button-to-test-the-class"></a><span data-ttu-id="dc894-125">创建用于测试类的按钮</span><span class="sxs-lookup"><span data-stu-id="dc894-125">To create a button to test the class</span></span>
  
1. <span data-ttu-id="dc894-126">将启动窗体更改为设计模式，方法是在 **解决方案资源管理器** 中右键单击其名称，然后单击 " **视图设计器**"。</span><span class="sxs-lookup"><span data-stu-id="dc894-126">Change the startup form to design mode by right-clicking its name in **Solution Explorer** and then clicking **View Designer**.</span></span> <span data-ttu-id="dc894-127">默认情况下，Windows 应用程序项目的启动窗体命名为 "Form1"。</span><span class="sxs-lookup"><span data-stu-id="dc894-127">By default, the startup form for Windows Application projects is named Form1.vb.</span></span> <span data-ttu-id="dc894-128">然后，将显示主窗体。</span><span class="sxs-lookup"><span data-stu-id="dc894-128">The main form will then appear.</span></span>  
  
2. <span data-ttu-id="dc894-129">向主窗体添加一个按钮，然后双击它显示 `Button1_Click` 事件处理程序的代码。</span><span class="sxs-lookup"><span data-stu-id="dc894-129">Add a button to the main form and double-click it to display the code for the `Button1_Click` event handler.</span></span> <span data-ttu-id="dc894-130">添加以下代码来调用测试过程：</span><span class="sxs-lookup"><span data-stu-id="dc894-130">Add the following code to call the test procedure:</span></span>  
  
     [!code-vb[VbVbalrOOP#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#12)]
  
## <a name="to-run-your-application"></a><span data-ttu-id="dc894-131">运行应用程序</span><span class="sxs-lookup"><span data-stu-id="dc894-131">To run your application</span></span>
  
1. <span data-ttu-id="dc894-132">按 F5 运行应用程序。</span><span class="sxs-lookup"><span data-stu-id="dc894-132">Run your application by pressing F5.</span></span> <span data-ttu-id="dc894-133">单击窗体上的按钮以调用测试过程。</span><span class="sxs-lookup"><span data-stu-id="dc894-133">Click the button on the form to call the test procedure.</span></span> <span data-ttu-id="dc894-134">它将显示一条消息，指出原始 `UserName` 是 "尧，胡继"，因为过程调用了 `Capitalize` 对象的方法。</span><span class="sxs-lookup"><span data-stu-id="dc894-134">It displays a message stating that the original `UserName` is "MOORE, BOBBY", because the procedure called the `Capitalize` method of the object.</span></span>  
  
2. <span data-ttu-id="dc894-135">单击“确定”，关闭该消息框。</span><span class="sxs-lookup"><span data-stu-id="dc894-135">Click **OK** to dismiss the message box.</span></span> <span data-ttu-id="dc894-136">此 `Button1 Click` 过程将更改属性的值 `UserName` ，并显示一条消息，指出的新值 `UserName` 为 "Worden，Joe"。</span><span class="sxs-lookup"><span data-stu-id="dc894-136">The `Button1 Click` procedure changes the value of the `UserName` property and displays a message stating that the new value of `UserName` is "Worden, Joe".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc894-137">请参阅</span><span class="sxs-lookup"><span data-stu-id="dc894-137">See also</span></span>

- [<span data-ttu-id="dc894-138">面向对象的编程 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dc894-138">Object-Oriented Programming (Visual Basic)</span></span>](../../concepts/object-oriented-programming.md)
- [<span data-ttu-id="dc894-139">对象和类</span><span class="sxs-lookup"><span data-stu-id="dc894-139">Objects and Classes</span></span>](index.md)
