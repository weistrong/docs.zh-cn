---
description: 了解更多相关信息：必需的参数和重载组
title: 必需自变量和重载组
ms.date: 03/30/2017
ms.assetid: 4ca3ed06-b9af-4b85-8b70-88c2186aefa3
ms.openlocfilehash: 1eea77276ad976c81d891e45cfbe5217b298b4fd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99720028"
---
# <a name="required-arguments-and-overload-groups"></a><span data-ttu-id="c7201-103">必需自变量和重载组</span><span class="sxs-lookup"><span data-stu-id="c7201-103">Required Arguments and Overload Groups</span></span>

<span data-ttu-id="c7201-104">可以对活动进行配置，以便必须绑定某些参数才能有效执行该活动。</span><span class="sxs-lookup"><span data-stu-id="c7201-104">Activities can be configured so that certain arguments are required to be bound for the activity to be valid for execution.</span></span> <span data-ttu-id="c7201-105">`RequiredArgument` 特性用于指示活动中的某些自变量是必需自变量，`OverloadGroup` 特性用于将必需自变量的多个类别组合在一起。</span><span class="sxs-lookup"><span data-stu-id="c7201-105">The `RequiredArgument` attribute is used to indicate that certain arguments on an activity are required and the `OverloadGroup` attribute is used to group categories of required arguments together.</span></span> <span data-ttu-id="c7201-106">使用这些特性，活动作者可以提供简单或复杂的活动验证配置。</span><span class="sxs-lookup"><span data-stu-id="c7201-106">By using the attributes, activity authors can provide simple or complex activity validation configurations.</span></span>  
  
## <a name="using-required-arguments"></a><span data-ttu-id="c7201-107">使用必需参数</span><span class="sxs-lookup"><span data-stu-id="c7201-107">Using Required Arguments</span></span>  

 <span data-ttu-id="c7201-108">若要在活动中使用 `RequiredArgument` 特性，请使用 <xref:System.Activities.RequiredArgumentAttribute> 指示所需参数。</span><span class="sxs-lookup"><span data-stu-id="c7201-108">To use the `RequiredArgument` attribute in an activity, indicate the desired arguments using <xref:System.Activities.RequiredArgumentAttribute>.</span></span> <span data-ttu-id="c7201-109">下面的示例定义了一个含有两个必需自变量的 `Add` 活动。</span><span class="sxs-lookup"><span data-stu-id="c7201-109">In this example, an `Add` activity is defined that has two required arguments.</span></span>  
  
```csharp  
public sealed class Add : CodeActivity<int>  
{  
    [RequiredArgument]  
    public InArgument<int> Operand1 { get; set; }  
  
    [RequiredArgument]  
    public InArgument<int> Operand2 { get; set; }  
  
    protected override int Execute(CodeActivityContext context)  
    {  
        return Operand1.Get(context) + Operand2.Get(context);  
    }  
}  
```  
  
 <span data-ttu-id="c7201-110">在 XAML 中，也请使用 <xref:System.Activities.RequiredArgumentAttribute> 来指示所需参数。</span><span class="sxs-lookup"><span data-stu-id="c7201-110">In XAML, required arguments are also indicated by using <xref:System.Activities.RequiredArgumentAttribute>.</span></span> <span data-ttu-id="c7201-111">下面的示例通过使用三个参数定义了一个 `Add` 活动，并使用 <xref:System.Activities.Statements.Assign%601> 活动执行添加操作。</span><span class="sxs-lookup"><span data-stu-id="c7201-111">In this example the `Add` activity is defined by using three arguments and uses an <xref:System.Activities.Statements.Assign%601> activity to perform the add operation.</span></span>  
  
```xaml  
<Activity x:Class="ValidationDemo.Add" ...>  
  <x:Members>  
    <x:Property Name="Operand1" Type="InArgument(x:Int32)">  
      <x:Property.Attributes>  
        <RequiredArgumentAttribute />  
      </x:Property.Attributes>  
    </x:Property>  
    <x:Property Name="Operand2" Type="InArgument(x:Int32)">  
      <x:Property.Attributes>  
        <RequiredArgumentAttribute />  
      </x:Property.Attributes>  
    </x:Property>  
    <x:Property Name="Result" Type="OutArgument(x:Int32)" />  
  </x:Members>  
  <Assign>  
    <Assign.To>  
      <OutArgument x:TypeArguments="x:Int32">[Result]</OutArgument>  
    </Assign.To>  
    <Assign.Value>  
      <InArgument x:TypeArguments="x:Int32">[Operand1 + Operand2]</InArgument>  
    </Assign.Value>  
  </Assign>  
</Activity>  
```  
  
 <span data-ttu-id="c7201-112">如果使用了该活动，但未绑定任何一个必需参数，则会返回以下验证错误。</span><span class="sxs-lookup"><span data-stu-id="c7201-112">If the activity is used and either of the required arguments is not bound the following validation error is returned.</span></span>  
  
 <span data-ttu-id="c7201-113">**未提供必需活动自变量“Operand1”的值。**</span><span class="sxs-lookup"><span data-stu-id="c7201-113">**Value for a required activity argument 'Operand1' was not supplied.**</span></span>  
> [!NOTE]
> <span data-ttu-id="c7201-114">有关检查和处理验证错误和警告的详细信息，请参阅 [调用活动验证](invoking-activity-validation.md)。</span><span class="sxs-lookup"><span data-stu-id="c7201-114">For more information about checking for and handling validation errors and warnings, see [Invoking Activity Validation](invoking-activity-validation.md).</span></span>  
  
## <a name="using-overload-groups"></a><span data-ttu-id="c7201-115">使用重载组</span><span class="sxs-lookup"><span data-stu-id="c7201-115">Using Overload Groups</span></span>

<span data-ttu-id="c7201-116">重载组提供了一种方法，指示哪些自变量组合在活动中有效。</span><span class="sxs-lookup"><span data-stu-id="c7201-116">Overload groups provide a method for indicating which combinations of arguments are valid in an activity.</span></span> <span data-ttu-id="c7201-117">使用 <xref:System.Activities.OverloadGroupAttribute> 将参数组合在一起。</span><span class="sxs-lookup"><span data-stu-id="c7201-117">Arguments are grouped together by using <xref:System.Activities.OverloadGroupAttribute>.</span></span> <span data-ttu-id="c7201-118">为每个组指定一个名称，该名称由指定 <xref:System.Activities.OverloadGroupAttribute> 。</span><span class="sxs-lookup"><span data-stu-id="c7201-118">Each group is given a name that is specified by the <xref:System.Activities.OverloadGroupAttribute>.</span></span> <span data-ttu-id="c7201-119">仅当绑定重载组中的一组参数时，该活动才有效。</span><span class="sxs-lookup"><span data-stu-id="c7201-119">The activity is valid when only one set of arguments in an overload group are bound.</span></span> <span data-ttu-id="c7201-120">下面的示例定义了一个 `CreateLocation` 类。</span><span class="sxs-lookup"><span data-stu-id="c7201-120">In the following example, a `CreateLocation` class is defined.</span></span>  
  
```csharp  
class CreateLocation: Activity  
{  
    [RequiredArgument]  
    public InArgument<string> Name { get; set; }  
  
    public InArgument<string> Description { get; set; }  
  
    [RequiredArgument]  
    [OverloadGroup("G1")]  
    public InArgument<int> Latitude { get; set; }  
  
    [RequiredArgument]  
    [OverloadGroup("G1")]  
    public InArgument<int> Longitude { get; set; }  
  
    [RequiredArgument]  
    [OverloadGroup("G2")]  
    [OverloadGroup("G3")]  
    public InArgument<string> Street { get; set; }  
  
    [RequiredArgument]  
    [OverloadGroup("G2")]  
    public InArgument<string> City { get; set; }  
  
    [RequiredArgument]  
    [OverloadGroup("G2")]  
    public InArgument<string> State { get; set; }  
  
    [RequiredArgument]  
    [OverloadGroup("G3")]  
    public InArgument<int> Zip { get; set; }
}  
```  
  
 <span data-ttu-id="c7201-121">该活动的目的是指定美国的某个位置。</span><span class="sxs-lookup"><span data-stu-id="c7201-121">The objective of this activity is to specify a location in the US.</span></span> <span data-ttu-id="c7201-122">为此，活动用户可以使用三组参数中的一组来指定该位置。</span><span class="sxs-lookup"><span data-stu-id="c7201-122">To do this, the user of the activity can specify the location using one of three groups of arguments.</span></span> <span data-ttu-id="c7201-123">若要指定自变量的有效组合，请定义三个重载组。</span><span class="sxs-lookup"><span data-stu-id="c7201-123">To specify the valid combinations of arguments, three overload groups are defined.</span></span> <span data-ttu-id="c7201-124">`G1` 包含 `Latitude` 和 `Longitude` 自变量。</span><span class="sxs-lookup"><span data-stu-id="c7201-124">`G1` contains the `Latitude` and `Longitude` arguments.</span></span> <span data-ttu-id="c7201-125">`G2` 包含 `Street`、`City` 和 `State`。</span><span class="sxs-lookup"><span data-stu-id="c7201-125">`G2` contains `Street`, `City`, and `State`.</span></span> <span data-ttu-id="c7201-126">`G3` 包含 `Street` 和 `Zip`。</span><span class="sxs-lookup"><span data-stu-id="c7201-126">`G3` contains `Street` and `Zip`.</span></span> <span data-ttu-id="c7201-127">`Name` 也是一个必需的自变量，但它不是重载组的一部分。</span><span class="sxs-lookup"><span data-stu-id="c7201-127">`Name` is also a required argument, but it is not part of an overload group.</span></span> <span data-ttu-id="c7201-128">为使该活动有效，必须一起绑定 `Name` 和一个（且只有一个）重载组中的所有参数。</span><span class="sxs-lookup"><span data-stu-id="c7201-128">For this activity to be valid, `Name` would have to be bound together with all of the arguments from one and only one overload group.</span></span>  
  
 <span data-ttu-id="c7201-129">在下面的示例中，从 " [数据库访问" 活动](./samples/database-access-activities.md) 示例中，有两个重载组： `ConnectionString` 和 `ConfigFileSectionName` 。</span><span class="sxs-lookup"><span data-stu-id="c7201-129">In the following example, taken from the [Database Access Activities](./samples/database-access-activities.md) sample, there are two overload groups: `ConnectionString` and `ConfigFileSectionName`.</span></span> <span data-ttu-id="c7201-130">为使此活动有效，必须绑定 `ProviderName` 和 `ConnectionString` 自变量，或者绑定 `ConfigName` 自变量，但不能这些自变量一起绑定。</span><span class="sxs-lookup"><span data-stu-id="c7201-130">For this activity to be valid, either the `ProviderName` and `ConnectionString` arguments must be bound, or the `ConfigName` argument, but not both.</span></span>  
  
```csharp  
public class DbUpdate: AsyncCodeActivity  
{  
    [RequiredArgument]  
    [OverloadGroup("ConnectionString")]  
    [DefaultValue(null)]  
    public InArgument<string> ProviderName { get; set; }  
  
    [RequiredArgument]  
    [OverloadGroup("ConnectionString")]  
    [DependsOn("ProviderName")]  
    [DefaultValue(null)]  
    public InArgument<string> ConnectionString { get; set; }  
  
    [RequiredArgument]  
    [OverloadGroup("ConfigFileSectionName")]  
    [DefaultValue(null)]  
    public InArgument<string> ConfigName { get; set; }  
  
    [DefaultValue(null)]  
    public CommandType CommandType { get; set; }  
  
    [RequiredArgument]  
    public InArgument<string> Sql { get; set; }  
  
    [DependsOn("Sql")]  
    [DefaultValue(null)]  
    public IDictionary<string, Argument> Parameters { get; }  
  
    [DependsOn("Parameters")]  
    public OutArgument<int> AffectedRecords { get; set; }
}  
```  
  
 <span data-ttu-id="c7201-131">定义重载组时：</span><span class="sxs-lookup"><span data-stu-id="c7201-131">When defining an overload group:</span></span>  
  
- <span data-ttu-id="c7201-132">重载组不能为另一个重载组的子集或等价集。</span><span class="sxs-lookup"><span data-stu-id="c7201-132">An overload group cannot be a subset or an equivalent set of another overload group.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="c7201-133">此规则有一个例外。</span><span class="sxs-lookup"><span data-stu-id="c7201-133">There is one exception to this rule.</span></span> <span data-ttu-id="c7201-134">如果某个重载组是另一重载组的子集，并且该子集仅包含 `RequiredArgument` 为 `false` 的参数，则该重载集有效。</span><span class="sxs-lookup"><span data-stu-id="c7201-134">If an overload group is a subset of another overload group, and the subset contains only arguments where `RequiredArgument` is `false`, then the overload group is valid.</span></span>  
  
- <span data-ttu-id="c7201-135">重载组可以重叠，但如果组的交集包含一个或两个重载组的所有必需自变量，则会出错。</span><span class="sxs-lookup"><span data-stu-id="c7201-135">Overload groups can overlap but it is an error if the intersection of the groups contains all the required arguments of one or both of the overload groups.</span></span> <span data-ttu-id="c7201-136">在前面的示例中，`G2` 和 `G3` 重载组重叠，但因为交集不包含一个或两个组的所有自变量，所以这是有效的。</span><span class="sxs-lookup"><span data-stu-id="c7201-136">In the previous example the `G2` and `G3` overload groups overlapped, but because the intersection did not contain all the arguments of one or both of the groups this was valid.</span></span>  
  
 <span data-ttu-id="c7201-137">在重载组中绑定自变量时：</span><span class="sxs-lookup"><span data-stu-id="c7201-137">When binding arguments in an overload group:</span></span>  
  
- <span data-ttu-id="c7201-138">如果重载组中的所有 `RequiredArgument` 参数均被绑定，则该组将被视为绑定的重载组。</span><span class="sxs-lookup"><span data-stu-id="c7201-138">An overload group is considered bound if all the `RequiredArgument` arguments in the group are bound.</span></span>  
  
- <span data-ttu-id="c7201-139">如果一个组具有零个 `RequiredArgument` 自变量且至少有一个自变量被绑定，则该组将被视为绑定的组。</span><span class="sxs-lookup"><span data-stu-id="c7201-139">If a group has zero `RequiredArgument` arguments and at least one argument bound, then the group is considered bound.</span></span>  
  
- <span data-ttu-id="c7201-140">如果没有绑定任何重载组，除非其中的一个重载组中未包含任何 `RequiredArgument` 参数，否则它是一个验证错误。</span><span class="sxs-lookup"><span data-stu-id="c7201-140">It is a validation error if no overload groups are bound unless one overload group has no `RequiredArgument` arguments in it.</span></span>  
  
- <span data-ttu-id="c7201-141">绑定多个重载组（即，绑定一个重载组中的所有必需参数，并同时绑定另一个重载组中的所有参数）的做法是错误的。</span><span class="sxs-lookup"><span data-stu-id="c7201-141">It is an error to have more than one overload group bound, that is, all required arguments in one overload group are bound and any argument in another overload group is also bound.</span></span>
