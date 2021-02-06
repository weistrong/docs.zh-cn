---
description: 了解详细信息： <section> element
title: <section> element
ms.date: 05/01/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/configSections/section
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/configSections/sectionGroup/section
helpviewer_keywords:
- section Element
- <section> Element
ms.assetid: ec7d4110-2403-47ac-8218-499bfe9d5ddb
ms.openlocfilehash: 7756f7ee3be2391a0d068708f3719083640b5595
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99639934"
---
# <a name="section-element"></a><span data-ttu-id="9341e-104">\<section> 元素</span><span class="sxs-lookup"><span data-stu-id="9341e-104">\<section> element</span></span>

<span data-ttu-id="9341e-105">包含配置节声明。</span><span class="sxs-lookup"><span data-stu-id="9341e-105">Contains a configuration section declaration.</span></span>

[**\<configuration>**](configuration-element.md)\
&nbsp;&nbsp;[**\<configSections>**](configsections-element-for-configuration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;**\<section>**

[**\<configuration>**](configuration-element.md)\
&nbsp;&nbsp;[**\<configSections>**](configsections-element-for-configuration.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<sectionGroup>**](sectiongroup-element-for-configsections.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<section>**

## <a name="syntax"></a><span data-ttu-id="9341e-106">语法</span><span class="sxs-lookup"><span data-stu-id="9341e-106">Syntax</span></span>

```xml
<section name="section name"
         type="configuration section handler class, assembly"
         allowDefinition="Everywhere|MachineOnly|MachineToApplication"
         allowLocation="true|false" />
```

## <a name="required-attributes"></a><span data-ttu-id="9341e-107">必需属性</span><span class="sxs-lookup"><span data-stu-id="9341e-107">Required attributes</span></span>

|           | <span data-ttu-id="9341e-108">说明</span><span class="sxs-lookup"><span data-stu-id="9341e-108">Description</span></span> |
| --------- | ----------- |
| <span data-ttu-id="9341e-109">**name**</span><span class="sxs-lookup"><span data-stu-id="9341e-109">**name**</span></span>  | <span data-ttu-id="9341e-110">指定配置节的名称。</span><span class="sxs-lookup"><span data-stu-id="9341e-110">Specifies the name of the configuration section.</span></span> |
| <span data-ttu-id="9341e-111">type </span><span class="sxs-lookup"><span data-stu-id="9341e-111">**type**</span></span>  | <span data-ttu-id="9341e-112">指定从配置文件读取节的配置节处理程序类的名称。</span><span class="sxs-lookup"><span data-stu-id="9341e-112">Specifies the name of the configuration section handler class that reads the section from the configuration file.</span></span> <span data-ttu-id="9341e-113">类型值具有语法 "完全限定的节-名称、简单程序集名称"。</span><span class="sxs-lookup"><span data-stu-id="9341e-113">The type value has the syntax "fully-qualified-section-handler-class-name, simple-assembly-name".</span></span> <span data-ttu-id="9341e-114">简单程序集名称是没有 *.dll* 文件扩展名的根文件名。</span><span class="sxs-lookup"><span data-stu-id="9341e-114">The simple assembly name is the root filename without the *.dll* file extension.</span></span> |

## <a name="optional-attributes"></a><span data-ttu-id="9341e-115">可选属性</span><span class="sxs-lookup"><span data-stu-id="9341e-115">Optional attributes</span></span>

<span data-ttu-id="9341e-116">以下属性仅适用于 ASP.NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="9341e-116">The following attributes are applicable only for ASP.NET applications.</span></span> <span data-ttu-id="9341e-117">对于其他应用程序类型，配置系统将忽略这些属性。</span><span class="sxs-lookup"><span data-stu-id="9341e-117">The configuration system ignores these attributes for other application types.</span></span>

|                     | <span data-ttu-id="9341e-118">说明</span><span class="sxs-lookup"><span data-stu-id="9341e-118">Description</span></span> |
| ------------------- | ----------- |
| <span data-ttu-id="9341e-119">**allowDefinition**</span><span class="sxs-lookup"><span data-stu-id="9341e-119">**allowDefinition**</span></span> | <span data-ttu-id="9341e-120">指定可在其中使用节的配置文件。</span><span class="sxs-lookup"><span data-stu-id="9341e-120">Specifies which configuration file the section can be used in.</span></span> <span data-ttu-id="9341e-121">使用以下值之一：</span><span class="sxs-lookup"><span data-stu-id="9341e-121">Use one of the following values:</span></span><br><br><span data-ttu-id="9341e-122">**无处不在**</span><span class="sxs-lookup"><span data-stu-id="9341e-122">**Everywhere**</span></span><br><span data-ttu-id="9341e-123">允许在任何配置文件中使用节。</span><span class="sxs-lookup"><span data-stu-id="9341e-123">Allows the section to be used in any configuration file.</span></span> <span data-ttu-id="9341e-124">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="9341e-124">This is the default.</span></span><br><span data-ttu-id="9341e-125">**MachineOnly**</span><span class="sxs-lookup"><span data-stu-id="9341e-125">**MachineOnly**</span></span><br><span data-ttu-id="9341e-126">允许部分仅在计算机配置文件中使用 (*Machine.config*) 。</span><span class="sxs-lookup"><span data-stu-id="9341e-126">Allows the section to be used only in the machine configuration file (*Machine.config*).</span></span><br><span data-ttu-id="9341e-127">**MachineToApplication**</span><span class="sxs-lookup"><span data-stu-id="9341e-127">**MachineToApplication**</span></span><br><span data-ttu-id="9341e-128">允许在计算机配置文件或应用程序配置文件中使用部分。</span><span class="sxs-lookup"><span data-stu-id="9341e-128">Allows the section to be used in the machine configuration file or the application configuration file.</span></span> |
| <span data-ttu-id="9341e-129">**allowLocation**</span><span class="sxs-lookup"><span data-stu-id="9341e-129">**allowLocation**</span></span>   | <span data-ttu-id="9341e-130">确定是否可以在元素中使用节 **\<location>** 。</span><span class="sxs-lookup"><span data-stu-id="9341e-130">Determines whether the section can be used within the **\<location>** element.</span></span> <span data-ttu-id="9341e-131">使用以下值之一：</span><span class="sxs-lookup"><span data-stu-id="9341e-131">Use one of the following values:</span></span><br><br><span data-ttu-id="9341e-132">true</span><span class="sxs-lookup"><span data-stu-id="9341e-132">**true**</span></span><br><span data-ttu-id="9341e-133">允许在元素中使用节 **\<location>** 。</span><span class="sxs-lookup"><span data-stu-id="9341e-133">Allows the section to be used within the **\<location>** element.</span></span> <span data-ttu-id="9341e-134">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="9341e-134">This is the default.</span></span><br><span data-ttu-id="9341e-135">**false**</span><span class="sxs-lookup"><span data-stu-id="9341e-135">**false**</span></span><br><span data-ttu-id="9341e-136">不允许在元素中使用节 **\<location>** 。</span><span class="sxs-lookup"><span data-stu-id="9341e-136">Does not allow the section to be used within the **\<location>** element.</span></span> |

## <a name="parent-elements"></a><span data-ttu-id="9341e-137">父元素</span><span class="sxs-lookup"><span data-stu-id="9341e-137">Parent elements</span></span>

|     | <span data-ttu-id="9341e-138">说明</span><span class="sxs-lookup"><span data-stu-id="9341e-138">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="9341e-139">**\<configSections>** 元素</span><span class="sxs-lookup"><span data-stu-id="9341e-139">**\<configSections>** Element</span></span>](configsections-element-for-configuration.md) | <span data-ttu-id="9341e-140">包含配置节和命名空间声明。</span><span class="sxs-lookup"><span data-stu-id="9341e-140">Contains configuration section and namespace declarations.</span></span> |
| [<span data-ttu-id="9341e-141">**\<sectionGroup>** Element</span><span class="sxs-lookup"><span data-stu-id="9341e-141">**\<sectionGroup>** Element</span></span>](sectiongroup-element-for-configsections.md) | <span data-ttu-id="9341e-142">定义配置节的命名空间。</span><span class="sxs-lookup"><span data-stu-id="9341e-142">Defines a namespace for configuration sections.</span></span> |

> [!NOTE]
> <span data-ttu-id="9341e-143">**\<section>** 元素是或中的子元素， **\<configSections>** **\<sectionGroup>** 而不是同时为两者。</span><span class="sxs-lookup"><span data-stu-id="9341e-143">A **\<section>** element is a child element of either **\<configSections>** or **\<sectionGroup>** but not both.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9341e-144">子元素</span><span class="sxs-lookup"><span data-stu-id="9341e-144">Child elements</span></span>

<span data-ttu-id="9341e-145">无</span><span class="sxs-lookup"><span data-stu-id="9341e-145">None</span></span>

## <a name="remarks"></a><span data-ttu-id="9341e-146">备注</span><span class="sxs-lookup"><span data-stu-id="9341e-146">Remarks</span></span>

<span data-ttu-id="9341e-147">声明配置节本质上定义了配置文件的新元素。</span><span class="sxs-lookup"><span data-stu-id="9341e-147">Declaring a configuration section essentially defines a new element for the configuration file.</span></span> <span data-ttu-id="9341e-148">新元素包含配置节处理程序 (的设置，即实现接口的类 <xref:System.Configuration.IConfigurationSectionHandler>) 读取。</span><span class="sxs-lookup"><span data-stu-id="9341e-148">The new element contains settings that a configuration section handler (that is, a class that implements the <xref:System.Configuration.IConfigurationSectionHandler> interface) reads.</span></span> <span data-ttu-id="9341e-149">你定义的节的特性和子元素取决于用于读取设置的部分处理程序。</span><span class="sxs-lookup"><span data-stu-id="9341e-149">The attributes and child elements of a section you define depend on the section handler you use to read your settings.</span></span>

<span data-ttu-id="9341e-150">通过在 *Machine.config* 文件中声明配置节处理程序，你可以使用该计算机上任何应用程序配置文件中的配置节，除非 **allowDefinition** 属性指定了其他。</span><span class="sxs-lookup"><span data-stu-id="9341e-150">Declaring a configuration section handler in the *Machine.config* file enables you to use the configuration section in any application configuration file on that computer, unless the **allowDefinition** attribute specifies otherwise.</span></span>

## <a name="example"></a><span data-ttu-id="9341e-151">示例</span><span class="sxs-lookup"><span data-stu-id="9341e-151">Example</span></span>

<span data-ttu-id="9341e-152">下面的示例演示如何定义配置节并定义该部分的设置：</span><span class="sxs-lookup"><span data-stu-id="9341e-152">The following example shows how to define a configuration section and define settings for that section:</span></span>

```xml
<configuration>
  <configSections>
    <section name="sampleSection"
             type="System.Configuration.SingleTagSectionHandler"
             allowLocation="false" />
  </configSections>
  <sampleSection setting1="Value1"
                 setting2="value two"
                 setting3="third value" />
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="9341e-153">配置文件</span><span class="sxs-lookup"><span data-stu-id="9341e-153">Configuration file</span></span>

<span data-ttu-id="9341e-154">此元素可用于应用程序配置文件、计算机配置文件 (*Machine.config*) 和 *Web.config* 不在应用程序目录级别的文件。</span><span class="sxs-lookup"><span data-stu-id="9341e-154">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="9341e-155">请参阅</span><span class="sxs-lookup"><span data-stu-id="9341e-155">See also</span></span>

- [<span data-ttu-id="9341e-156">.NET Framework 的配置文件架构</span><span class="sxs-lookup"><span data-stu-id="9341e-156">Configuration file schema for the .NET Framework</span></span>](index.md)
