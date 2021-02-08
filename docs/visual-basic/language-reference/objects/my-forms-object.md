---
description: 了解有关以下内容的详细信息： My Forms 对象
title: My.Forms 对象
ms.date: 07/20/2015
f1_keywords:
- My.Forms
- My.MyProject.Forms
helpviewer_keywords:
- My.Forms object
ms.assetid: f6bff4e6-6769-4294-956b-037aa6106d2a
ms.openlocfilehash: 18ef8ee475163ff7eb177dfee590d959a242a88e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99774403"
---
# <a name="myforms-object"></a><span data-ttu-id="76c8b-103">My.Forms 对象</span><span class="sxs-lookup"><span data-stu-id="76c8b-103">My.Forms Object</span></span>

<span data-ttu-id="76c8b-104">为访问在当前项目中声明的每个 Windows 窗体的实例提供属性。</span><span class="sxs-lookup"><span data-stu-id="76c8b-104">Provides properties for accessing an instance of each Windows form declared in the current project.</span></span>

## <a name="remarks"></a><span data-ttu-id="76c8b-105">备注</span><span class="sxs-lookup"><span data-stu-id="76c8b-105">Remarks</span></span>

<span data-ttu-id="76c8b-106">`My.Forms`对象为当前项目中的每个窗体提供一个实例。</span><span class="sxs-lookup"><span data-stu-id="76c8b-106">The `My.Forms` object provides an instance of each form in the current project.</span></span> <span data-ttu-id="76c8b-107">属性的名称与属性访问的窗体的名称相同。</span><span class="sxs-lookup"><span data-stu-id="76c8b-107">The name of the property is the same as the name of the form that the property accesses.</span></span>

<span data-ttu-id="76c8b-108">您可以 `My.Forms` 通过使用窗体的名称，而无需限定来访问由对象提供的窗体。</span><span class="sxs-lookup"><span data-stu-id="76c8b-108">You can access the forms provided by the `My.Forms` object by using the name of the form, without qualification.</span></span> <span data-ttu-id="76c8b-109">因为属性名称与窗体的类型名称相同，所以这允许你像访问默认实例一样访问窗体。</span><span class="sxs-lookup"><span data-stu-id="76c8b-109">Because the property name is the same as the form's type name, this allows you to access a form as if it had a default instance.</span></span> <span data-ttu-id="76c8b-110">例如，`My.Forms.Form1.Show` 等效于 `Form1.Show`。</span><span class="sxs-lookup"><span data-stu-id="76c8b-110">For example, `My.Forms.Form1.Show` is equivalent to `Form1.Show`.</span></span>

<span data-ttu-id="76c8b-111">`My.Forms`对象只公开与当前项目关联的窗体。</span><span class="sxs-lookup"><span data-stu-id="76c8b-111">The `My.Forms` object exposes only the forms associated with the current project.</span></span> <span data-ttu-id="76c8b-112">它不提供对引用 Dll 中声明的窗体的访问。</span><span class="sxs-lookup"><span data-stu-id="76c8b-112">It does not provide access to forms declared in referenced DLLs.</span></span> <span data-ttu-id="76c8b-113">若要访问 DLL 提供的窗体，必须使用以 *DllName* 形式编写的格式的限定名称。*FormName*。</span><span class="sxs-lookup"><span data-stu-id="76c8b-113">To access a form that a DLL provides, you must use the qualified name of the form, written as *DllName*.*FormName*.</span></span>

<span data-ttu-id="76c8b-114">您可以使用 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OpenForms%2A> 属性来获取应用程序的所有打开窗体的集合。</span><span class="sxs-lookup"><span data-stu-id="76c8b-114">You can use the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OpenForms%2A> property to get a collection of all the application's open forms.</span></span>

<span data-ttu-id="76c8b-115">对象及其属性仅适用于 Windows 应用程序。</span><span class="sxs-lookup"><span data-stu-id="76c8b-115">The object and its properties are available only for Windows applications.</span></span>

## <a name="properties"></a><span data-ttu-id="76c8b-116">属性</span><span class="sxs-lookup"><span data-stu-id="76c8b-116">Properties</span></span>

<span data-ttu-id="76c8b-117">对象的每个属性都 `My.Forms` 提供对当前项目中窗体的实例的访问。</span><span class="sxs-lookup"><span data-stu-id="76c8b-117">Each property of the `My.Forms` object provides access to an instance of a form in the current project.</span></span> <span data-ttu-id="76c8b-118">属性的名称与属性访问的窗体的名称相同，属性类型与窗体的类型相同。</span><span class="sxs-lookup"><span data-stu-id="76c8b-118">The name of the property is the same as the name of the form that the property accesses, and the property type is the same as the form's type.</span></span>

> [!NOTE]
> <span data-ttu-id="76c8b-119">如果存在名称冲突，则用于访问窗体的属性名称为 *RootNamespace* _ *命名空间* \_ *FormName*。</span><span class="sxs-lookup"><span data-stu-id="76c8b-119">If there is a name collision, the property name to access a form is *RootNamespace* _ *Namespace*\_*FormName*.</span></span> <span data-ttu-id="76c8b-120">例如，假设有两个名为的窗体： `Form1.` 如果其中一个窗体位于根命名空间 `WindowsApplication1` 和命名空间中 `Namespace1` ，则可以通过访问该窗体 `My.Forms.WindowsApplication1_Namespace1_Form1` 。</span><span class="sxs-lookup"><span data-stu-id="76c8b-120">For example, consider two forms named `Form1.`If one of these forms is in the root namespace `WindowsApplication1` and in the namespace `Namespace1`, you would access that form through `My.Forms.WindowsApplication1_Namespace1_Form1`.</span></span>

<span data-ttu-id="76c8b-121">`My.Forms`对象提供对启动时创建的应用程序主窗体实例的访问权限。</span><span class="sxs-lookup"><span data-stu-id="76c8b-121">The `My.Forms` object provides access to the instance of the application's main form that was created on startup.</span></span> <span data-ttu-id="76c8b-122">对于所有其他窗体， `My.Forms` 对象在被访问并存储时创建窗体的新实例。</span><span class="sxs-lookup"><span data-stu-id="76c8b-122">For all other forms, the `My.Forms` object creates a new instance of the form when it is accessed and stores it.</span></span> <span data-ttu-id="76c8b-123">后续尝试访问该属性将返回该窗体的实例。</span><span class="sxs-lookup"><span data-stu-id="76c8b-123">Subsequent attempts to access that property return that instance of the form.</span></span>

<span data-ttu-id="76c8b-124">您可以通过 `Nothing` 向窗体的属性分配来释放窗体。</span><span class="sxs-lookup"><span data-stu-id="76c8b-124">You can dispose of a form by assigning `Nothing` to the property for that form.</span></span> <span data-ttu-id="76c8b-125">属性 setter 调用 <xref:System.Windows.Forms.Form.Close%2A> 窗体的方法，然后将分配 `Nothing` 给存储的值。</span><span class="sxs-lookup"><span data-stu-id="76c8b-125">The property setter calls the <xref:System.Windows.Forms.Form.Close%2A> method of the form, and then assigns `Nothing` to the stored value.</span></span> <span data-ttu-id="76c8b-126">如果为属性分配除以外的任何值 `Nothing` ，则 setter 会引发 <xref:System.ArgumentException> 异常。</span><span class="sxs-lookup"><span data-stu-id="76c8b-126">If you assign any value other than `Nothing` to the property, the setter throws an <xref:System.ArgumentException> exception.</span></span>

<span data-ttu-id="76c8b-127">您可以 `My.Forms` 使用 or 运算符测试对象的属性是否存储窗体的实例 `Is` `IsNot` 。</span><span class="sxs-lookup"><span data-stu-id="76c8b-127">You can test whether a property of the `My.Forms` object stores an instance of the form by using the `Is` or `IsNot` operator.</span></span> <span data-ttu-id="76c8b-128">您可以使用这些运算符来检查属性的值是否为 `Nothing` 。</span><span class="sxs-lookup"><span data-stu-id="76c8b-128">You can use those operators to check if the value of the property is `Nothing`.</span></span>

> [!NOTE]
> <span data-ttu-id="76c8b-129">通常， `Is` 或 `IsNot` 运算符必须读取属性的值才能执行比较。</span><span class="sxs-lookup"><span data-stu-id="76c8b-129">Typically, the `Is` or `IsNot` operator has to read the value of the property to perform the comparison.</span></span> <span data-ttu-id="76c8b-130">但是，如果属性当前存储 `Nothing` ，则属性创建窗体的新实例，然后返回该实例。</span><span class="sxs-lookup"><span data-stu-id="76c8b-130">However, if the property currently stores `Nothing`, the property creates a new instance of the form and then returns that instance.</span></span> <span data-ttu-id="76c8b-131">不过，Visual Basic 编译器 `My.Forms` 会以不同的方式处理对象的属性，并允许 `Is` 或 `IsNot` 运算符检查属性的状态，而无需更改其值。</span><span class="sxs-lookup"><span data-stu-id="76c8b-131">However, the Visual Basic compiler treats the properties of the `My.Forms` object differently and allows the `Is` or `IsNot` operator to check the status of the property without altering its value.</span></span>

## <a name="example"></a><span data-ttu-id="76c8b-132">示例</span><span class="sxs-lookup"><span data-stu-id="76c8b-132">Example</span></span>

<span data-ttu-id="76c8b-133">此示例更改默认窗体的标题 `SidebarMenu` 。</span><span class="sxs-lookup"><span data-stu-id="76c8b-133">This example changes the title of the default `SidebarMenu` form.</span></span>

[!code-vb[VbVbalrMyForms#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyForms/VB/Class1.vb#2)]

<span data-ttu-id="76c8b-134">要使此示例正常运行，你的项目必须具有名为的窗体 `SidebarMenu` 。</span><span class="sxs-lookup"><span data-stu-id="76c8b-134">For this example to work, your project must have a form named `SidebarMenu`.</span></span>

<span data-ttu-id="76c8b-135">此代码仅适用于 Windows 应用程序项目。</span><span class="sxs-lookup"><span data-stu-id="76c8b-135">This code will work only in a Windows Application project.</span></span>

## <a name="requirements"></a><span data-ttu-id="76c8b-136">要求</span><span class="sxs-lookup"><span data-stu-id="76c8b-136">Requirements</span></span>

### <a name="availability-by-project-type"></a><span data-ttu-id="76c8b-137">按项目类型的可用性</span><span class="sxs-lookup"><span data-stu-id="76c8b-137">Availability by Project Type</span></span>

|<span data-ttu-id="76c8b-138">项目类型</span><span class="sxs-lookup"><span data-stu-id="76c8b-138">Project type</span></span>|<span data-ttu-id="76c8b-139">可用</span><span class="sxs-lookup"><span data-stu-id="76c8b-139">Available</span></span>|
|---|---|
|<span data-ttu-id="76c8b-140">Windows 应用程序</span><span class="sxs-lookup"><span data-stu-id="76c8b-140">Windows Application</span></span>|<span data-ttu-id="76c8b-141">**是**</span><span class="sxs-lookup"><span data-stu-id="76c8b-141">**Yes**</span></span>|
|<span data-ttu-id="76c8b-142">类库</span><span class="sxs-lookup"><span data-stu-id="76c8b-142">Class Library</span></span>|<span data-ttu-id="76c8b-143">否</span><span class="sxs-lookup"><span data-stu-id="76c8b-143">No</span></span>|
|<span data-ttu-id="76c8b-144">控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="76c8b-144">Console Application</span></span>|<span data-ttu-id="76c8b-145">否</span><span class="sxs-lookup"><span data-stu-id="76c8b-145">No</span></span>|
|<span data-ttu-id="76c8b-146">Windows 控件库</span><span class="sxs-lookup"><span data-stu-id="76c8b-146">Windows Control Library</span></span>|<span data-ttu-id="76c8b-147">否</span><span class="sxs-lookup"><span data-stu-id="76c8b-147">No</span></span>|
|<span data-ttu-id="76c8b-148">Web 控件库</span><span class="sxs-lookup"><span data-stu-id="76c8b-148">Web Control Library</span></span>|<span data-ttu-id="76c8b-149">否</span><span class="sxs-lookup"><span data-stu-id="76c8b-149">No</span></span>|
|<span data-ttu-id="76c8b-150">Windows 服务</span><span class="sxs-lookup"><span data-stu-id="76c8b-150">Windows Service</span></span>|<span data-ttu-id="76c8b-151">否</span><span class="sxs-lookup"><span data-stu-id="76c8b-151">No</span></span>|
|<span data-ttu-id="76c8b-152">网站</span><span class="sxs-lookup"><span data-stu-id="76c8b-152">Web Site</span></span>|<span data-ttu-id="76c8b-153">否</span><span class="sxs-lookup"><span data-stu-id="76c8b-153">No</span></span>|

## <a name="see-also"></a><span data-ttu-id="76c8b-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="76c8b-154">See also</span></span>

- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OpenForms%2A>
- <xref:System.Windows.Forms.Form>
- <xref:System.Windows.Forms.Form.Close%2A>
- [<span data-ttu-id="76c8b-155">对象</span><span class="sxs-lookup"><span data-stu-id="76c8b-155">Objects</span></span>](index.md)
- [<span data-ttu-id="76c8b-156">Is 运算符</span><span class="sxs-lookup"><span data-stu-id="76c8b-156">Is Operator</span></span>](../operators/is-operator.md)
- [<span data-ttu-id="76c8b-157">IsNot 运算符</span><span class="sxs-lookup"><span data-stu-id="76c8b-157">IsNot Operator</span></span>](../operators/isnot-operator.md)
- [<span data-ttu-id="76c8b-158">访问应用程序窗体</span><span class="sxs-lookup"><span data-stu-id="76c8b-158">Accessing Application Forms</span></span>](../../developing-apps/programming/accessing-application-forms.md)
