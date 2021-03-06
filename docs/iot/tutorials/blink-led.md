---
title: 闪烁 LED
description: 了解如何使用 .NET IoT 库闪烁 LED。
author: camsoper
ms.author: casoper
ms.date: 11/13/2020
ms.topic: tutorial
ms.prod: dotnet
ms.openlocfilehash: 0d5db19faac0293b9982731f26dfd85d6ce07b3a
ms.sourcegitcommit: 9c589b25b005b9a7f87327646020eb85c3b6306f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2021
ms.locfileid: "102259007"
---
# <a name="blink-an-led"></a><span data-ttu-id="37234-103">闪烁 LED</span><span class="sxs-lookup"><span data-stu-id="37234-103">Blink an LED</span></span>

<span data-ttu-id="37234-104">可以单独控制常规用途 i/o (GPIO) pin。</span><span class="sxs-lookup"><span data-stu-id="37234-104">General-purpose I/O (GPIO) pins can be controlled individually.</span></span> <span data-ttu-id="37234-105">这适用于控制 Led、中继和其他有状态设备。</span><span class="sxs-lookup"><span data-stu-id="37234-105">This is useful for controlling LEDs, relays, and other stateful devices.</span></span> <span data-ttu-id="37234-106">在本主题中，你将使用 .NET 和 Raspberry Pi 的 GPIO pin 来使 LED 通电，并重复闪烁。</span><span class="sxs-lookup"><span data-stu-id="37234-106">In this topic, you will use .NET and your Raspberry Pi's GPIO pins to power an LED and blink it repeatedly.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="37234-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="37234-107">Prerequisites</span></span>

- [!INCLUDE [prereq-rpi](../includes/prereq-rpi.md)]
- <span data-ttu-id="37234-108">5 mm LED</span><span class="sxs-lookup"><span data-stu-id="37234-108">5 mm LED</span></span>
- <span data-ttu-id="37234-109">330Ω电阻器</span><span class="sxs-lookup"><span data-stu-id="37234-109">330 Ω resistor</span></span>
- <span data-ttu-id="37234-110">试验板</span><span class="sxs-lookup"><span data-stu-id="37234-110">Breadboard</span></span>
- <span data-ttu-id="37234-111">跳线</span><span class="sxs-lookup"><span data-stu-id="37234-111">Jumper wires</span></span>
- <span data-ttu-id="37234-112">Raspberry Pi GPIO (可选/推荐的) </span><span class="sxs-lookup"><span data-stu-id="37234-112">Raspberry Pi GPIO breakout board (optional/recommended)</span></span>
- [!INCLUDE [tutorial-prereq-dotnet](../includes/tutorial-prereq-dotnet.md)]

[!INCLUDE [ensure-ssh](../includes/ensure-ssh.md)]

## <a name="prepare-the-hardware"></a><span data-ttu-id="37234-113">准备硬件</span><span class="sxs-lookup"><span data-stu-id="37234-113">Prepare the hardware</span></span>

<span data-ttu-id="37234-114">按照下图所示，使用硬件组件构建线路：</span><span class="sxs-lookup"><span data-stu-id="37234-114">Use the hardware components to build the circuit as depicted in the following diagram:</span></span>

:::image type="content" source="../media/rpi-led_bb-thumb.png" alt-text="显示具有 LED 和电阻器的线路的 Fritzing 图" lightbox="../media/rpi-led_bb.png":::

<span data-ttu-id="37234-116">上图描述了下列连接：</span><span class="sxs-lookup"><span data-stu-id="37234-116">The image above depicts the following connections:</span></span>

- <span data-ttu-id="37234-117">GPIO 18 到 LED 阳极 (更长的正面) </span><span class="sxs-lookup"><span data-stu-id="37234-117">GPIO 18 to LED anode (longer, positive lead)</span></span>
- <span data-ttu-id="37234-118">LED (较短、负面的潜在顾客) 到330Ω电阻器 (要么结束) </span><span class="sxs-lookup"><span data-stu-id="37234-118">LED cathode (shorter, negative lead) to 330 Ω resistor (either end)</span></span>
- <span data-ttu-id="37234-119">330Ω电阻器 (其他端) 到地面</span><span class="sxs-lookup"><span data-stu-id="37234-119">330 Ω resistor (other end) to ground</span></span>

[!INCLUDE [tutorial-rpi-gpio](../includes/tutorial-rpi-gpio.md)]

[!INCLUDE [gpio-breakout](../includes/gpio-breakout.md)]

## <a name="create-the-app"></a><span data-ttu-id="37234-120">创建应用</span><span class="sxs-lookup"><span data-stu-id="37234-120">Create the app</span></span>

<span data-ttu-id="37234-121">在首选开发环境中完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="37234-121">Complete the following steps in your preferred development environment:</span></span>

1. <span data-ttu-id="37234-122">使用 [.NET CLI](../../core/tools/dotnet-new.md) 或 [Visual Studio](../../core/tutorials/with-visual-studio.md)创建一个新的 .net 控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="37234-122">Create a new .NET Console App using either the [.NET CLI](../../core/tools/dotnet-new.md) or [Visual Studio](../../core/tutorials/with-visual-studio.md).</span></span> <span data-ttu-id="37234-123">将其命名为 *BlinkTutorial*。</span><span class="sxs-lookup"><span data-stu-id="37234-123">Name it *BlinkTutorial*.</span></span>

    ```dotnetcli
    dotnet new console -o BlinkTutorial
    ```

1. [!INCLUDE [tutorial-add-packages](../includes/tutorial-add-packages.md)]
1. <span data-ttu-id="37234-124">将 Program.cs 的内容替换为以下代码：</span><span class="sxs-lookup"><span data-stu-id="37234-124">Replace the contents of *Program.cs* with the following code:</span></span>

    :::code language="csharp" source="~/iot-samples/tutorials/BlinkTutorial/Program.cs" :::

    <span data-ttu-id="37234-125">在上述代码中：</span><span class="sxs-lookup"><span data-stu-id="37234-125">In the preceding code:</span></span>

    - <span data-ttu-id="37234-126">[Using 声明](../../csharp/whats-new/csharp-8.md#using-declarations)创建的实例 `GpioController` 。</span><span class="sxs-lookup"><span data-stu-id="37234-126">A [using declaration](../../csharp/whats-new/csharp-8.md#using-declarations) creates an instance of `GpioController`.</span></span> <span data-ttu-id="37234-127">`using`声明可确保释放对象并正确释放硬件资源。</span><span class="sxs-lookup"><span data-stu-id="37234-127">The `using` declaration ensures the object is disposed and hardware resources are released properly.</span></span>
    - <span data-ttu-id="37234-128">为输出打开 GPIO 引脚18</span><span class="sxs-lookup"><span data-stu-id="37234-128">GPIO pin 18 is opened for output</span></span>
    - <span data-ttu-id="37234-129">`while`循环会无限期运行。</span><span class="sxs-lookup"><span data-stu-id="37234-129">A `while` loop runs indefinitely.</span></span> <span data-ttu-id="37234-130">每次迭代：</span><span class="sxs-lookup"><span data-stu-id="37234-130">Each iteration:</span></span>
        1. <span data-ttu-id="37234-131">向 GPIO 引脚18写入值。</span><span class="sxs-lookup"><span data-stu-id="37234-131">Writes a value to GPIO pin 18.</span></span> <span data-ttu-id="37234-132">如果 `ledOn` 为 true，则它 `PinValue.High` 在) 上写入 (。</span><span class="sxs-lookup"><span data-stu-id="37234-132">If `ledOn` is true, it writes `PinValue.High` (on).</span></span> <span data-ttu-id="37234-133">否则，将写入 `PinValue.Low` 。</span><span class="sxs-lookup"><span data-stu-id="37234-133">Otherwise, it writes `PinValue.Low`.</span></span>
        1. <span data-ttu-id="37234-134">睡眠1000毫秒。</span><span class="sxs-lookup"><span data-stu-id="37234-134">Sleeps 1000 ms.</span></span>
        1. <span data-ttu-id="37234-135">切换的值 `ledOn` 。</span><span class="sxs-lookup"><span data-stu-id="37234-135">Toggles the value of `ledOn`.</span></span>

1. [!INCLUDE [tutorial-build](../includes/tutorial-build.md)]
1. [!INCLUDE [tutorial-deploy](../includes/tutorial-deploy.md)]
1. <span data-ttu-id="37234-136">通过切换到部署目录并运行可执行文件，在 Raspberry Pi 上运行该应用。</span><span class="sxs-lookup"><span data-stu-id="37234-136">Run the app on the Raspberry Pi by switching to the deployment directory and running the executable.</span></span>

    ```bash
    ./BlinkTutorial
    ```

    <span data-ttu-id="37234-137">LED 闪烁，每秒闪烁一次。</span><span class="sxs-lookup"><span data-stu-id="37234-137">The LED blinks off and on every second.</span></span>

1. <span data-ttu-id="37234-138">通过按 <kbd>Ctrl + C</kbd>终止节目。</span><span class="sxs-lookup"><span data-stu-id="37234-138">Terminate the program by pressing <kbd>Ctrl+C</kbd>.</span></span>

<span data-ttu-id="37234-139">祝贺你！</span><span class="sxs-lookup"><span data-stu-id="37234-139">Congratulations!</span></span> <span data-ttu-id="37234-140">已使用 GPIO 闪烁 LED。</span><span class="sxs-lookup"><span data-stu-id="37234-140">You've used GPIO to blink an LED.</span></span>

## <a name="get-the-source-code"></a><span data-ttu-id="37234-141">获取源代码</span><span class="sxs-lookup"><span data-stu-id="37234-141">Get the source code</span></span>

<span data-ttu-id="37234-142">[GitHub 上提供](https://github.com/MicrosoftDocs/dotnet-iot-assets/tree/master/tutorials/BlinkTutorial)了本教程的源。</span><span class="sxs-lookup"><span data-stu-id="37234-142">The source for this tutorial is [available on GitHub](https://github.com/MicrosoftDocs/dotnet-iot-assets/tree/master/tutorials/BlinkTutorial).</span></span>

## <a name="next-steps"></a><span data-ttu-id="37234-143">后续步骤</span><span class="sxs-lookup"><span data-stu-id="37234-143">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="37234-144">了解如何从传感器读取环境条件</span><span class="sxs-lookup"><span data-stu-id="37234-144">Learn how to read environmental conditions from a sensor</span></span>](../tutorials/temp-sensor.md)
