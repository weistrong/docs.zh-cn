---
title: 从模拟到数字转换器读取值
description: 了解如何使用模拟到数字转换器读取可变电压值。
author: camsoper
ms.author: casoper
ms.date: 11/13/2020
ms.topic: tutorial
ms.prod: dotnet
ms.openlocfilehash: 509616e3423fbb83b74bfbb8ecec1a7df49f0a20
ms.sourcegitcommit: 9c589b25b005b9a7f87327646020eb85c3b6306f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2021
ms.locfileid: "102259730"
---
<!--markdownlint-disable DOCSMD011 -->
# <a name="read-values-from-an-analog-to-digital-converter"></a><span data-ttu-id="e8f81-103">从模拟到数字转换器读取值</span><span class="sxs-lookup"><span data-stu-id="e8f81-103">Read values from an analog-to-digital converter</span></span>

<span data-ttu-id="e8f81-104"> (ADC) 使用模拟到数字的转换器，它可以读取模拟输入电压值并将其转换为数字值。</span><span class="sxs-lookup"><span data-stu-id="e8f81-104">An analog-to-digital converter (ADC) is a device that can read an analog input voltage value and convert it into a digital value.</span></span> <span data-ttu-id="e8f81-105">ADCs 用于从 thermistors、potentiometers 和其他设备读取值，这些值根据某些条件更改抵抗。</span><span class="sxs-lookup"><span data-stu-id="e8f81-105">ADCs are used for reading values from thermistors, potentiometers, and other devices that change resistance based on certain conditions.</span></span>

<span data-ttu-id="e8f81-106">在本主题中，你将使用 .NET 从 ADC 读取值，因为使用 potentiometer 伯输入电压。</span><span class="sxs-lookup"><span data-stu-id="e8f81-106">In this topic, you will use .NET to read values from an ADC as you modulate the input voltage with a potentiometer.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e8f81-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="e8f81-107">Prerequisites</span></span>

- [!INCLUDE [prereq-rpi](../includes/prereq-rpi.md)]
- <span data-ttu-id="e8f81-108">[MCP3008](https://www.microchip.com/wwwproducts/MCP3008) 的模拟到数字转换器</span><span class="sxs-lookup"><span data-stu-id="e8f81-108">[MCP3008](https://www.microchip.com/wwwproducts/MCP3008) analog-to-digital converter</span></span>
- <span data-ttu-id="e8f81-109">三针 potentiometer</span><span class="sxs-lookup"><span data-stu-id="e8f81-109">Three-pin potentiometer</span></span>
- <span data-ttu-id="e8f81-110">试验板</span><span class="sxs-lookup"><span data-stu-id="e8f81-110">Breadboard</span></span>
- <span data-ttu-id="e8f81-111">跳线</span><span class="sxs-lookup"><span data-stu-id="e8f81-111">Jumper wires</span></span>
- <span data-ttu-id="e8f81-112">Raspberry Pi GPIO (可选/推荐的) </span><span class="sxs-lookup"><span data-stu-id="e8f81-112">Raspberry Pi GPIO breakout board (optional/recommended)</span></span>
- [!INCLUDE [tutorial-prereq-dotnet](../includes/tutorial-prereq-dotnet.md)]

[!INCLUDE [prepare-pi-spi](../includes/prepare-pi-spi.md)]

## <a name="prepare-the-hardware"></a><span data-ttu-id="e8f81-113">准备硬件</span><span class="sxs-lookup"><span data-stu-id="e8f81-113">Prepare the hardware</span></span>

<span data-ttu-id="e8f81-114">按照下图所示，使用硬件组件构建线路：</span><span class="sxs-lookup"><span data-stu-id="e8f81-114">Use the hardware components to build the circuit as depicted in the following diagram:</span></span>

:::image type="content" source="../media/rpi-trimpot_spi-thumb.png" alt-text="显示具有 MCP3008 ADC 和 potentiometer 的线路的 Fritzing 关系图" lightbox="../media/rpi-trimpot_spi.png":::

<span data-ttu-id="e8f81-116">MCP3008 使用串行外围设备接口 (SPI) 进行通信。</span><span class="sxs-lookup"><span data-stu-id="e8f81-116">The MCP3008 uses Serial Peripheral Interface (SPI) to communicate.</span></span> <span data-ttu-id="e8f81-117">下面是从 MCP3008 到 Raspberry Pi 和 potentiometer 的连接：</span><span class="sxs-lookup"><span data-stu-id="e8f81-117">The following are the connections from the MCP3008 to the Raspberry Pi and potentiometer:</span></span>

- <span data-ttu-id="e8f81-118">从<sub>DD</sub> 到 3.3 v (显示为红色) </span><span class="sxs-lookup"><span data-stu-id="e8f81-118">V<sub>DD</sub> to 3.3V (shown in red)</span></span>
- <span data-ttu-id="e8f81-119">指向 3.3 V 的 v<sub>引用</sub> (红色) </span><span class="sxs-lookup"><span data-stu-id="e8f81-119">V<sub>REF</sub> to 3.3V (red)</span></span>
- <span data-ttu-id="e8f81-120">AGND 到地面 (黑色) </span><span class="sxs-lookup"><span data-stu-id="e8f81-120">AGND to ground (black)</span></span>
- <span data-ttu-id="e8f81-121">CLK SCLK (橙色) </span><span class="sxs-lookup"><span data-stu-id="e8f81-121">CLK to SCLK (orange)</span></span>
- <span data-ttu-id="e8f81-122">D<sub>MISO</sub> (橙色) </span><span class="sxs-lookup"><span data-stu-id="e8f81-122">D<sub>OUT</sub> to MISO (orange)</span></span>
- <span data-ttu-id="e8f81-123">D<sub>中的</sub> MOSI (橙色) </span><span class="sxs-lookup"><span data-stu-id="e8f81-123">D<sub>IN</sub> to MOSI (orange)</span></span>
- <span data-ttu-id="e8f81-124">CS/SHDN to CE0 (绿色) </span><span class="sxs-lookup"><span data-stu-id="e8f81-124">CS/SHDN to CE0 (green)</span></span>
- <span data-ttu-id="e8f81-125">DGND 到地面 (黑色) </span><span class="sxs-lookup"><span data-stu-id="e8f81-125">DGND to ground (black)</span></span>
- <span data-ttu-id="e8f81-126">CH0 到 potentiometer (黄色的变量 (中间) 固定) </span><span class="sxs-lookup"><span data-stu-id="e8f81-126">CH0 to variable (middle) pin on potentiometer (yellow)</span></span>

<span data-ttu-id="e8f81-127">向 potentiometer 上的外部针脚提供 3.3 V 和接地。</span><span class="sxs-lookup"><span data-stu-id="e8f81-127">Supply 3.3V and ground to the outer pins on the potentiometer.</span></span> <span data-ttu-id="e8f81-128">顺序并不重要。</span><span class="sxs-lookup"><span data-stu-id="e8f81-128">Order is unimportant.</span></span>

<span data-ttu-id="e8f81-129">根据需要，请参阅以下引出线关系图：</span><span class="sxs-lookup"><span data-stu-id="e8f81-129">Refer to the following pinout diagrams as needed:</span></span>

| <span data-ttu-id="e8f81-130">MCP3008</span><span class="sxs-lookup"><span data-stu-id="e8f81-130">MCP3008</span></span>  | <span data-ttu-id="e8f81-131">Raspberry Pi GPIO</span><span class="sxs-lookup"><span data-stu-id="e8f81-131">Raspberry Pi GPIO</span></span> |
|----------|-------------------|
| :::image type="content" source="../media/mcp3008-diagram-thumb.png" alt-text="显示 MCP3008 引线的示意图" lightbox="../media/mcp3008-diagram.png"::: | :::image type="content" source="../media/gpio-pinout-diagram-thumb.png" alt-text="显示 Raspberry Pi GPIO 标头引线的关系图。Image 礼节性 Raspberry Pi Foundation。" lightbox="../media/gpio-pinout-diagram.png":::<br /><span data-ttu-id="e8f81-134">[Image 礼节性 Raspberry Pi Foundation](https://www.raspberrypi.org/documentation/usage/gpio/)。</span><span class="sxs-lookup"><span data-stu-id="e8f81-134">[Image courtesy Raspberry Pi Foundation](https://www.raspberrypi.org/documentation/usage/gpio/).</span></span>
 |

[!INCLUDE [gpio-breakout](../includes/gpio-breakout.md)]

## <a name="create-the-app"></a><span data-ttu-id="e8f81-135">创建应用</span><span class="sxs-lookup"><span data-stu-id="e8f81-135">Create the app</span></span>

<span data-ttu-id="e8f81-136">在首选开发环境中完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="e8f81-136">Complete the following steps in your preferred development environment:</span></span>

1. <span data-ttu-id="e8f81-137">使用 [.NET CLI](../../core/tools/dotnet-new.md) 或 [Visual Studio](../../core/tutorials/with-visual-studio.md)创建一个新的 .net 控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="e8f81-137">Create a new .NET Console App using either the [.NET CLI](../../core/tools/dotnet-new.md) or [Visual Studio](../../core/tutorials/with-visual-studio.md).</span></span> <span data-ttu-id="e8f81-138">将其命名为 *AdcTutorial*。</span><span class="sxs-lookup"><span data-stu-id="e8f81-138">Name it *AdcTutorial*.</span></span>

    ```dotnetcli
    dotnet new console -o AdcTutorial
    ```

1. [!INCLUDE [tutorial-add-packages](../includes/tutorial-add-packages.md)]
1. <span data-ttu-id="e8f81-139">将 Program.cs 的内容替换为以下代码：</span><span class="sxs-lookup"><span data-stu-id="e8f81-139">Replace the contents of *Program.cs* with the following code:</span></span>

    :::code language="csharp" source="~/iot-samples/tutorials/AdcTutorial/Program.cs" :::

    <span data-ttu-id="e8f81-140">在上述代码中：</span><span class="sxs-lookup"><span data-stu-id="e8f81-140">In the preceding code:</span></span>

    - <span data-ttu-id="e8f81-141">`hardwareSpiSettings` 设置为的新实例 `SpiConnectionSettings` 。</span><span class="sxs-lookup"><span data-stu-id="e8f81-141">`hardwareSpiSettings` is set to a new instance of `SpiConnectionSettings`.</span></span> <span data-ttu-id="e8f81-142">构造函数将 `busId` 参数设置为0，将 `chipSelectLine` 参数设置为0。</span><span class="sxs-lookup"><span data-stu-id="e8f81-142">The constructor sets the `busId` parameter to 0 and the `chipSelectLine` parameter to 0.</span></span>
    - <span data-ttu-id="e8f81-143">[Using 声明](../../csharp/whats-new/csharp-8.md#using-declarations) `SpiDevice` 通过调用并传入来创建的实例 `SpiDevice.Create` `hardwareSpiSettings` 。</span><span class="sxs-lookup"><span data-stu-id="e8f81-143">A [using declaration](../../csharp/whats-new/csharp-8.md#using-declarations) creates an instance of `SpiDevice` by calling `SpiDevice.Create` and passing in `hardwareSpiSettings`.</span></span> <span data-ttu-id="e8f81-144">这 `SpiDevice` 表示 SPI 总线。</span><span class="sxs-lookup"><span data-stu-id="e8f81-144">This `SpiDevice` represents the SPI bus.</span></span> <span data-ttu-id="e8f81-145">`using`声明可确保释放对象并正确释放硬件资源。</span><span class="sxs-lookup"><span data-stu-id="e8f81-145">The `using` declaration ensures the object is disposed and hardware resources are released properly.</span></span>
    - <span data-ttu-id="e8f81-146">其他 `using` 声明将创建的实例 `Mcp3008` ，并将传递 `SpiDevice` 到构造函数中。</span><span class="sxs-lookup"><span data-stu-id="e8f81-146">Another `using` declaration creates an instance of `Mcp3008` and passes the `SpiDevice` into the constructor.</span></span>
    - <span data-ttu-id="e8f81-147">`while`循环会无限期运行。</span><span class="sxs-lookup"><span data-stu-id="e8f81-147">A `while` loop runs indefinitely.</span></span> <span data-ttu-id="e8f81-148">每次迭代：</span><span class="sxs-lookup"><span data-stu-id="e8f81-148">Each iteration:</span></span>
        1. <span data-ttu-id="e8f81-149">通过调用读取 ADC 上 CH0 的值 `mcp.Read(0)` 。</span><span class="sxs-lookup"><span data-stu-id="e8f81-149">Reads the value of CH0 on the ADC by calling `mcp.Read(0)`.</span></span>
        1. <span data-ttu-id="e8f81-150">值除以10.24。</span><span class="sxs-lookup"><span data-stu-id="e8f81-150">Divides the value by 10.24.</span></span> <span data-ttu-id="e8f81-151">MCP3008 是一个10位 ADC，这意味着它将返回1024的可能值，范围为0-1023。</span><span class="sxs-lookup"><span data-stu-id="e8f81-151">The MCP3008 is a 10-bit ADC, which means it returns 1024 possible values ranging 0-1023.</span></span> <span data-ttu-id="e8f81-152">将值除以10.24 表示百分比形式的值。</span><span class="sxs-lookup"><span data-stu-id="e8f81-152">Dividing the value by 10.24 represents the value as a percentage.</span></span>
        1. <span data-ttu-id="e8f81-153">将值舍入到最接近的整数。</span><span class="sxs-lookup"><span data-stu-id="e8f81-153">Rounds the value to the nearest integer.</span></span>
        1. <span data-ttu-id="e8f81-154">将值写入格式为百分比的控制台。</span><span class="sxs-lookup"><span data-stu-id="e8f81-154">Writes the value to the console formatted as a percentage.</span></span>
        1. <span data-ttu-id="e8f81-155">睡眠500毫秒。</span><span class="sxs-lookup"><span data-stu-id="e8f81-155">Sleeps 500 ms.</span></span>

1. [!INCLUDE [tutorial-build](../includes/tutorial-build.md)]
1. [!INCLUDE [tutorial-deploy](../includes/tutorial-deploy.md)]
1. <span data-ttu-id="e8f81-156">通过切换到部署目录并运行可执行文件，在 Raspberry Pi 上运行该应用。</span><span class="sxs-lookup"><span data-stu-id="e8f81-156">Run the app on the Raspberry Pi by switching to the deployment directory and running the executable.</span></span>

    ```bash
    ./AdcTutorial
    ```

    <span data-ttu-id="e8f81-157">旋转 potentiometer 时观察输出。</span><span class="sxs-lookup"><span data-stu-id="e8f81-157">Observe the output as you rotate the potentiometer dial.</span></span> <span data-ttu-id="e8f81-158">这是因为 potentiometer 会将在 ADC 上提供给 CH0 的电压改变。</span><span class="sxs-lookup"><span data-stu-id="e8f81-158">This is due to the potentiometer varying the voltage supplied to CH0 on the ADC.</span></span> <span data-ttu-id="e8f81-159">ADC 比较了 CH0 上的输入电压与 V<sub>REF</sub> 提供的参考电压，以生成值。</span><span class="sxs-lookup"><span data-stu-id="e8f81-159">The ADC compares the input voltage on CH0 to the reference voltage supplied to V<sub>REF</sub> to generate a value.</span></span>

1. <span data-ttu-id="e8f81-160">通过按 <kbd>Ctrl + C</kbd>终止节目。</span><span class="sxs-lookup"><span data-stu-id="e8f81-160">Terminate the program by pressing <kbd>Ctrl+C</kbd>.</span></span>

<span data-ttu-id="e8f81-161">祝贺你！</span><span class="sxs-lookup"><span data-stu-id="e8f81-161">Congratulations!</span></span> <span data-ttu-id="e8f81-162">已使用 SPI 从模拟到数字转换器读取值。</span><span class="sxs-lookup"><span data-stu-id="e8f81-162">You've used SPI to read values from an analog-to-digital converter.</span></span>

## <a name="get-the-source-code"></a><span data-ttu-id="e8f81-163">获取源代码</span><span class="sxs-lookup"><span data-stu-id="e8f81-163">Get the source code</span></span>

<span data-ttu-id="e8f81-164">[GitHub 上提供](https://github.com/MicrosoftDocs/dotnet-iot-assets/tree/master/tutorials/AdcTutorial)了本教程的源。</span><span class="sxs-lookup"><span data-stu-id="e8f81-164">The source for this tutorial is [available on GitHub](https://github.com/MicrosoftDocs/dotnet-iot-assets/tree/master/tutorials/AdcTutorial).</span></span>

## <a name="next-steps"></a><span data-ttu-id="e8f81-165">后续步骤</span><span class="sxs-lookup"><span data-stu-id="e8f81-165">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="e8f81-166">了解如何使用常规用途输入/输出使 LED 闪烁</span><span class="sxs-lookup"><span data-stu-id="e8f81-166">Learn to use General Purpose Input/Output to blink an LED</span></span>](../tutorials/blink-led.md)
