---
description: 了解详细信息：应用程序设置架构
title: 应用程序设置架构
ms.date: 03/30/2017
helpviewer_keywords:
- schema application settings
- application settings, schema [Windows Forms]
- Windows Forms, application settings schema
- configuration schema [.NET Framework], application settings
ms.assetid: 5797fcff-6081-4e8c-bebf-63d9c70cf14b
ms.openlocfilehash: 24c5771e9d98d07bbdc8dab5fce0f1535bc9b582
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99652895"
---
# <a name="application-settings-schema"></a><span data-ttu-id="9558d-103">应用程序设置架构</span><span class="sxs-lookup"><span data-stu-id="9558d-103">Application Settings schema</span></span>

<span data-ttu-id="9558d-104">应用程序设置允许 Windows 窗体或 ASP.NET 应用程序存储和检索应用程序范围的设置和用户范围的设置。</span><span class="sxs-lookup"><span data-stu-id="9558d-104">Application settings allow a Windows Forms or ASP.NET application to store and retrieve application-scoped and user-scoped settings.</span></span> <span data-ttu-id="9558d-105">在此上下文中， *设置* 是指特定于应用程序或特定于当前用户的任何信息，包括从数据库连接字符串到用户首选默认窗口大小的任何信息。</span><span class="sxs-lookup"><span data-stu-id="9558d-105">In this context, a *setting* is any piece of information that may be specific to the application or specific to the current user — anything from a database connection string to the user's preferred default window size.</span></span>

<span data-ttu-id="9558d-106">默认情况下，Windows 窗体应用程序中的应用程序设置使用 <xref:System.Configuration.LocalFileSettingsProvider> 类，该类使用 .net 配置系统将设置存储在 XML 配置文件中。</span><span class="sxs-lookup"><span data-stu-id="9558d-106">By default, application settings in a Windows Forms application uses the <xref:System.Configuration.LocalFileSettingsProvider> class, which uses the .NET configuration system to store settings in an XML configuration file.</span></span> <span data-ttu-id="9558d-107">有关应用程序设置使用的文件的详细信息，请参阅 [应用程序设置体系结构](/dotnet/desktop/winforms/advanced/application-settings-architecture)。</span><span class="sxs-lookup"><span data-stu-id="9558d-107">For more information about the files used by application settings, see [Application Settings Architecture](/dotnet/desktop/winforms/advanced/application-settings-architecture).</span></span>

<span data-ttu-id="9558d-108">应用程序设置将以下元素定义为它所使用的配置文件的一部分。</span><span class="sxs-lookup"><span data-stu-id="9558d-108">Application settings defines the following elements as part of the configuration files it uses.</span></span>

| <span data-ttu-id="9558d-109">元素</span><span class="sxs-lookup"><span data-stu-id="9558d-109">Element</span></span>                    | <span data-ttu-id="9558d-110">说明</span><span class="sxs-lookup"><span data-stu-id="9558d-110">Description</span></span>                                                                           |
| -------------------------- | ------------------------------------------------------------------------------------- |
| **\<applicationSettings>** | <span data-ttu-id="9558d-111">包含 **\<setting>** 应用程序特定的所有标记。</span><span class="sxs-lookup"><span data-stu-id="9558d-111">Contains all **\<setting>** tags specific to the application.</span></span>                         |
| **\<userSettings>**        | <span data-ttu-id="9558d-112">包含 **\<setting>** 特定于当前用户的所有标记。</span><span class="sxs-lookup"><span data-stu-id="9558d-112">Contains all **\<setting>** tags specific to the current user.</span></span>                        |
| **\<setting>**             | <span data-ttu-id="9558d-113">定义设置。</span><span class="sxs-lookup"><span data-stu-id="9558d-113">Defines a setting.</span></span> <span data-ttu-id="9558d-114">或的子级 **\<applicationSettings>** **\<userSettings>** 。</span><span class="sxs-lookup"><span data-stu-id="9558d-114">Child of either **\<applicationSettings>** or **\<userSettings>**.</span></span> |
| **\<value>**               | <span data-ttu-id="9558d-115">定义设置的值。</span><span class="sxs-lookup"><span data-stu-id="9558d-115">Defines a setting's value.</span></span> <span data-ttu-id="9558d-116">的子项 **\<setting>** 。</span><span class="sxs-lookup"><span data-stu-id="9558d-116">Child of **\<setting>**.</span></span>                                   |

## <a name="applicationsettings-element"></a><span data-ttu-id="9558d-117">\<applicationSettings> 元素</span><span class="sxs-lookup"><span data-stu-id="9558d-117">\<applicationSettings> element</span></span>

<span data-ttu-id="9558d-118">此元素包含 **\<setting>** 特定于客户端计算机上的应用程序实例的所有标记。</span><span class="sxs-lookup"><span data-stu-id="9558d-118">This element contains all **\<setting>** tags that are specific to an instance of the application on a client computer.</span></span> <span data-ttu-id="9558d-119">未定义任何属性。</span><span class="sxs-lookup"><span data-stu-id="9558d-119">It defines no attributes.</span></span>

## <a name="usersettings-element"></a><span data-ttu-id="9558d-120">\<userSettings> 元素</span><span class="sxs-lookup"><span data-stu-id="9558d-120">\<userSettings> element</span></span>

<span data-ttu-id="9558d-121">此元素包含 **\<setting>** 特定于当前正在使用应用程序的用户的所有标记。</span><span class="sxs-lookup"><span data-stu-id="9558d-121">This element contains all **\<setting>** tags that are specific to the user who is currently using the application.</span></span> <span data-ttu-id="9558d-122">未定义任何属性。</span><span class="sxs-lookup"><span data-stu-id="9558d-122">It defines no attributes.</span></span>

## <a name="setting-element"></a><span data-ttu-id="9558d-123">\<setting> 元素</span><span class="sxs-lookup"><span data-stu-id="9558d-123">\<setting> element</span></span>

<span data-ttu-id="9558d-124">此元素定义一个设置。</span><span class="sxs-lookup"><span data-stu-id="9558d-124">This element defines a setting.</span></span> <span data-ttu-id="9558d-125">它具有以下属性。</span><span class="sxs-lookup"><span data-stu-id="9558d-125">It has the following attributes.</span></span>

| <span data-ttu-id="9558d-126">Attribute</span><span class="sxs-lookup"><span data-stu-id="9558d-126">Attribute</span></span>        | <span data-ttu-id="9558d-127">说明</span><span class="sxs-lookup"><span data-stu-id="9558d-127">Description</span></span> |
| ---------------- | ----------- |
| <span data-ttu-id="9558d-128">name</span><span class="sxs-lookup"><span data-stu-id="9558d-128">**name**</span></span>         | <span data-ttu-id="9558d-129">必需。</span><span class="sxs-lookup"><span data-stu-id="9558d-129">Required.</span></span> <span data-ttu-id="9558d-130">设置的唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="9558d-130">The unique ID of the setting.</span></span> <span data-ttu-id="9558d-131">使用名称保存通过 Visual Studio 创建的设置 `ProjectName.Properties.Settings` 。</span><span class="sxs-lookup"><span data-stu-id="9558d-131">Settings created through Visual Studio are saved with the name `ProjectName.Properties.Settings`.</span></span> |
| <span data-ttu-id="9558d-132">**serializeAs**</span><span class="sxs-lookup"><span data-stu-id="9558d-132">**serializeAs**</span></span> | <span data-ttu-id="9558d-133">必需。</span><span class="sxs-lookup"><span data-stu-id="9558d-133">Required.</span></span> <span data-ttu-id="9558d-134">将值序列化为文本时要使用的格式。</span><span class="sxs-lookup"><span data-stu-id="9558d-134">The format to use for serializing the value to text.</span></span> <span data-ttu-id="9558d-135">有效值是：</span><span class="sxs-lookup"><span data-stu-id="9558d-135">Valid values are:</span></span><br><br><span data-ttu-id="9558d-136">- `string`.</span><span class="sxs-lookup"><span data-stu-id="9558d-136">- `string`.</span></span> <span data-ttu-id="9558d-137">该值使用来序列化为字符串 <xref:System.ComponentModel.TypeConverter> 。</span><span class="sxs-lookup"><span data-stu-id="9558d-137">The value is serialized as a string using a <xref:System.ComponentModel.TypeConverter>.</span></span><br><span data-ttu-id="9558d-138">- `xml`.</span><span class="sxs-lookup"><span data-stu-id="9558d-138">- `xml`.</span></span> <span data-ttu-id="9558d-139">使用 XML 序列化对值进行序列化。</span><span class="sxs-lookup"><span data-stu-id="9558d-139">The value is serialized using XML serialization.</span></span><br><span data-ttu-id="9558d-140">- `binary`.</span><span class="sxs-lookup"><span data-stu-id="9558d-140">- `binary`.</span></span> <span data-ttu-id="9558d-141">使用二进制序列化将值作为文本编码的二进制序列化。</span><span class="sxs-lookup"><span data-stu-id="9558d-141">The value is serialized as text-encoded binary using binary serialization.</span></span><br /><span data-ttu-id="9558d-142">- `custom`.</span><span class="sxs-lookup"><span data-stu-id="9558d-142">- `custom`.</span></span> <span data-ttu-id="9558d-143">设置提供程序具有此设置的固有知识，并对其进行序列化和反序列化。</span><span class="sxs-lookup"><span data-stu-id="9558d-143">The settings provider has inherent knowledge of this setting and serializes and de-serializes it.</span></span> |

## <a name="value-element"></a><span data-ttu-id="9558d-144">\<value> 元素</span><span class="sxs-lookup"><span data-stu-id="9558d-144">\<value> element</span></span>

<span data-ttu-id="9558d-145">此元素包含设置的值。</span><span class="sxs-lookup"><span data-stu-id="9558d-145">This element contains the value of a setting.</span></span>

## <a name="example"></a><span data-ttu-id="9558d-146">示例</span><span class="sxs-lookup"><span data-stu-id="9558d-146">Example</span></span>

<span data-ttu-id="9558d-147">以下示例显示了一个应用程序设置文件，该文件定义了两个应用程序范围的设置和两个用户范围的设置：</span><span class="sxs-lookup"><span data-stu-id="9558d-147">The following example shows an application settings file that defines two application-scoped settings and two user-scoped settings:</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <configSections>
    <sectionGroup name="applicationSettings" type="System.Configuration.ApplicationSettingsGroup, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">
      <section name="WindowsApplication1.Properties.Settings" type="System.Configuration.ClientSettingsSection, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" />
    </sectionGroup>
    <sectionGroup name="userSettings" type="System.Configuration.UserSettingsGroup, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089">
      <section name="WindowsApplication1.Properties.Settings" type="System.Configuration.ClientSettingsSection, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" allowExeDefinition="MachineToLocalUser" />
    </sectionGroup>
  </configSections>
  <applicationSettings>
    <WindowsApplication1.Properties.Settings>
      <setting name="Cursor" serializeAs="String">
        <value>Default</value>
      </setting>
      <setting name="DoubleBuffering" serializeAs="String">
        <value>False</value>
      </setting>
    </WindowsApplication1.Properties.Settings>
  </applicationSettings>
  <userSettings>
    <WindowsApplication1.Properties.Settings>
      <setting name="FormTitle" serializeAs="String">
        <value>Form1</value>
      </setting>
      <setting name="FormSize" serializeAs="String">
        <value>595, 536</value>
      </setting>
    </WindowsApplication1.Properties.Settings>
  </userSettings>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="9558d-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="9558d-148">See also</span></span>

- [<span data-ttu-id="9558d-149">应用程序设置概述</span><span class="sxs-lookup"><span data-stu-id="9558d-149">Application Settings Overview</span></span>](/dotnet/desktop/winforms/advanced/application-settings-overview)
- [<span data-ttu-id="9558d-150">应用程序设置体系结构</span><span class="sxs-lookup"><span data-stu-id="9558d-150">Application Settings Architecture</span></span>](/dotnet/desktop/winforms/advanced/application-settings-architecture)
