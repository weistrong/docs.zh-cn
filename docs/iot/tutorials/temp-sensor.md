---
title: 从传感器读取环境条件
description: 了解如何通过 .NET IoT 库读取 termperature、大气压力和湿度。
author: camsoper
ms.author: casoper
ms.date: 11/14/2020
ms.topic: tutorial
ms.prod: dotnet
ms.openlocfilehash: bc5c2b9f0876603c152da859547c58b83826969c
ms.sourcegitcommit: 9c589b25b005b9a7f87327646020eb85c3b6306f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2021
ms.locfileid: "102259832"
---
# <a name="read-environmental-conditions-from-a-sensor"></a><span data-ttu-id="18bd1-103">从传感器读取环境条件</span><span class="sxs-lookup"><span data-stu-id="18bd1-103">Read environmental conditions from a sensor</span></span>

<span data-ttu-id="18bd1-104">IoT 设备的最常见方案之一就是检测环境情况。</span><span class="sxs-lookup"><span data-stu-id="18bd1-104">One of the most common scenarios for IoT devices is detection of environmental conditions.</span></span> <span data-ttu-id="18bd1-105">有多种传感器可用于监视温度、湿度、大气压力等。</span><span class="sxs-lookup"><span data-stu-id="18bd1-105">A variety of sensors are available to monitor temperature, humidity, barometric pressure, and more.</span></span>

<span data-ttu-id="18bd1-106">在本主题中，你将使用 .NET 从传感器读取环境条件。</span><span class="sxs-lookup"><span data-stu-id="18bd1-106">In this topic, you will use .NET to read environmental conditions from a sensor.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="18bd1-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="18bd1-107">Prerequisites</span></span>

- [!INCLUDE [prereq-rpi](../includes/prereq-rpi.md)]
- <span data-ttu-id="18bd1-108">[BME280](https://learn.adafruit.com/adafruit-bme280-humidity-barometric-pressure-temperature-sensor-breakout) 湿度/大气压力/温度传感器分类</span><span class="sxs-lookup"><span data-stu-id="18bd1-108">[BME280](https://learn.adafruit.com/adafruit-bme280-humidity-barometric-pressure-temperature-sensor-breakout) humidity/barometric pressure/temperature sensor breakout</span></span>
- <span data-ttu-id="18bd1-109">跳线</span><span class="sxs-lookup"><span data-stu-id="18bd1-109">Jumper wires</span></span>
- <span data-ttu-id="18bd1-110">试验板 (可选) </span><span class="sxs-lookup"><span data-stu-id="18bd1-110">Breadboard (optional)</span></span>
- <span data-ttu-id="18bd1-111">Raspberry Pi GPIO (可选) </span><span class="sxs-lookup"><span data-stu-id="18bd1-111">Raspberry Pi GPIO breakout board (optional)</span></span>
- [!INCLUDE [tutorial-prereq-dotnet](../includes/tutorial-prereq-dotnet.md)]

> [!IMPORTANT]
> <span data-ttu-id="18bd1-112">有很多 BME280 取得突破的制造商。</span><span class="sxs-lookup"><span data-stu-id="18bd1-112">There are many manufacturers of BME280 breakouts.</span></span> <span data-ttu-id="18bd1-113">大多数设计都是类似的，并且制造商不应对功能产生任何影响。</span><span class="sxs-lookup"><span data-stu-id="18bd1-113">Most designs are similar, and the manufacturer shouldn't make any difference to the functionality.</span></span> <span data-ttu-id="18bd1-114">本教程尝试考虑变体。</span><span class="sxs-lookup"><span data-stu-id="18bd1-114">This tutorial attempts to account for variations.</span></span> <span data-ttu-id="18bd1-115">确保 BME280 的 Inter-Integrated 线路 (I2C) 接口。</span><span class="sxs-lookup"><span data-stu-id="18bd1-115">Ensure your BME280 breakout includes an Inter-Integrated Circuit (I2C) interface.</span></span>

[!INCLUDE [prepare-pi-i2c](../includes/prepare-pi-i2c.md)]

## <a name="prepare-the-hardware"></a><span data-ttu-id="18bd1-116">准备硬件</span><span class="sxs-lookup"><span data-stu-id="18bd1-116">Prepare the hardware</span></span>

<span data-ttu-id="18bd1-117">按照下图所示，使用硬件组件构建线路：</span><span class="sxs-lookup"><span data-stu-id="18bd1-117">Use the hardware components to build the circuit as depicted in the following diagram:</span></span>

:::image type="content" source="../media/rpi-bmp280_i2c-thumb.png" alt-text="显示从 Raspberry Pi 到 BME280 出局的连接的 Fritzing 关系图" lightbox="../media/rpi-bmp280_i2c.png":::

<span data-ttu-id="18bd1-119">下面是从 Raspberry Pi 到 BME280 的连接：</span><span class="sxs-lookup"><span data-stu-id="18bd1-119">The following are the connections from the Raspberry Pi to the BME280 breakout:</span></span>

- <span data-ttu-id="18bd1-120">3.3 v 到 VIN *或* 3V3 (显示为红色) </span><span class="sxs-lookup"><span data-stu-id="18bd1-120">3.3V to VIN *OR* 3V3 (shown in red)</span></span>
- <span data-ttu-id="18bd1-121">与 GND 的地面 (黑色) </span><span class="sxs-lookup"><span data-stu-id="18bd1-121">Ground to GND (black)</span></span>
- <span data-ttu-id="18bd1-122">SDA (GPIO 2) 到 SDI *或* SDA (blue) </span><span class="sxs-lookup"><span data-stu-id="18bd1-122">SDA (GPIO 2) to SDI *OR* SDA (blue)</span></span>
- <span data-ttu-id="18bd1-123">SCL (GPIO 3) 到 SCK *或* scl (橙色) </span><span class="sxs-lookup"><span data-stu-id="18bd1-123">SCL (GPIO 3) to SCK *OR* SCL (orange)</span></span>

[!INCLUDE [tutorial-rpi-gpio](../includes/tutorial-rpi-gpio.md)]

[!INCLUDE [gpio-breakout](../includes/gpio-breakout.md)]

## <a name="create-the-app"></a><span data-ttu-id="18bd1-124">创建应用</span><span class="sxs-lookup"><span data-stu-id="18bd1-124">Create the app</span></span>

<span data-ttu-id="18bd1-125">在首选开发环境中完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="18bd1-125">Complete the following steps in your preferred development environment:</span></span>

1. <span data-ttu-id="18bd1-126">使用 [.NET CLI](../../core/tools/dotnet-new.md) 或 [Visual Studio](../../core/tutorials/with-visual-studio.md)创建一个新的 .net 控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="18bd1-126">Create a new .NET Console App using either the [.NET CLI](../../core/tools/dotnet-new.md) or [Visual Studio](../../core/tutorials/with-visual-studio.md).</span></span> <span data-ttu-id="18bd1-127">将其命名为 *SensorTutorial*。</span><span class="sxs-lookup"><span data-stu-id="18bd1-127">Name it *SensorTutorial*.</span></span>

    ```dotnetcli
    dotnet new console -o SensorTutorial
    ```

1. [!INCLUDE [tutorial-add-packages](../includes/tutorial-add-packages.md)]
1. <span data-ttu-id="18bd1-128">将 Program.cs 的内容替换为以下代码：</span><span class="sxs-lookup"><span data-stu-id="18bd1-128">Replace the contents of *Program.cs* with the following code:</span></span>

    :::code language="csharp" source="~/iot-samples/tutorials/SensorTutorial/Program.cs" :::

    <span data-ttu-id="18bd1-129">在上述代码中：</span><span class="sxs-lookup"><span data-stu-id="18bd1-129">In the preceding code:</span></span>

    - <span data-ttu-id="18bd1-130">`i2cSettings` 设置为的新实例 `I2cConnectionSettings` 。</span><span class="sxs-lookup"><span data-stu-id="18bd1-130">`i2cSettings` is set to a new instance of `I2cConnectionSettings`.</span></span> <span data-ttu-id="18bd1-131">构造函数将 `busId` 参数设置为1，并将 `deviceAddress` 参数设置为 `Bme280.DefaultI2cAddress` 。</span><span class="sxs-lookup"><span data-stu-id="18bd1-131">The constructor sets the `busId` parameter to 1 and the `deviceAddress` parameter to `Bme280.DefaultI2cAddress`.</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="18bd1-132">某些 BME280 的专题讨论会使用辅助地址值。</span><span class="sxs-lookup"><span data-stu-id="18bd1-132">Some BME280 breakout manufacturers use the secondary address value.</span></span> <span data-ttu-id="18bd1-133">对于这些设备，请使用 `Bme280.SecondaryI2cAddress` 。</span><span class="sxs-lookup"><span data-stu-id="18bd1-133">For those devices, use `Bme280.SecondaryI2cAddress`.</span></span>

    - <span data-ttu-id="18bd1-134">[Using 声明](../../csharp/whats-new/csharp-8.md#using-declarations) `I2cDevice` 通过调用并传入来创建的实例 `I2cDevice.Create` `i2cSettings` 。</span><span class="sxs-lookup"><span data-stu-id="18bd1-134">A [using declaration](../../csharp/whats-new/csharp-8.md#using-declarations) creates an instance of `I2cDevice` by calling `I2cDevice.Create` and passing in `i2cSettings`.</span></span> <span data-ttu-id="18bd1-135">这 `I2cDevice` 表示 I2C 总线。</span><span class="sxs-lookup"><span data-stu-id="18bd1-135">This `I2cDevice` represents the I2C bus.</span></span> <span data-ttu-id="18bd1-136">`using`声明可确保释放对象并正确释放硬件资源。</span><span class="sxs-lookup"><span data-stu-id="18bd1-136">The `using` declaration ensures the object is disposed and hardware resources are released properly.</span></span>
    - <span data-ttu-id="18bd1-137">另一个 `using` 声明创建 `Bme280` 用于表示传感器的的实例。</span><span class="sxs-lookup"><span data-stu-id="18bd1-137">Another `using` declaration creates an instance of `Bme280` to represent the sensor.</span></span> <span data-ttu-id="18bd1-138">在 `I2cDevice` 构造函数中传递。</span><span class="sxs-lookup"><span data-stu-id="18bd1-138">The `I2cDevice` is passed in the constructor.</span></span>
    - <span data-ttu-id="18bd1-139">芯片使用芯片的当前 (默认值进行度量所需的时间) 设置通过调用来检索 `GetMeasurementDuration` 。</span><span class="sxs-lookup"><span data-stu-id="18bd1-139">The time required for the chip to take measurements with the chip's current (default) settings is retrieved by calling `GetMeasurementDuration`.</span></span>
    - <span data-ttu-id="18bd1-140">`while`循环会无限期运行。</span><span class="sxs-lookup"><span data-stu-id="18bd1-140">A `while` loop runs indefinitely.</span></span> <span data-ttu-id="18bd1-141">每次迭代：</span><span class="sxs-lookup"><span data-stu-id="18bd1-141">Each iteration:</span></span>
        1. <span data-ttu-id="18bd1-142">清除控制台。</span><span class="sxs-lookup"><span data-stu-id="18bd1-142">Clears the console.</span></span>
        1. <span data-ttu-id="18bd1-143">将电源模式设置为 `Bmx280PowerMode.Forced` 。</span><span class="sxs-lookup"><span data-stu-id="18bd1-143">Sets the power mode to `Bmx280PowerMode.Forced`.</span></span> <span data-ttu-id="18bd1-144">这会强制芯片执行一个测量，存储结果，然后进入睡眠状态。</span><span class="sxs-lookup"><span data-stu-id="18bd1-144">This forces the chip to perform one measurement, store the results, and then sleep.</span></span>
        1. <span data-ttu-id="18bd1-145">读取温度、压力、湿度和海拔量的值。</span><span class="sxs-lookup"><span data-stu-id="18bd1-145">Reads the values for temperature, pressure, humidity, and altitude.</span></span>

            > [!NOTE]
            > <span data-ttu-id="18bd1-146">海拔由设备绑定计算。</span><span class="sxs-lookup"><span data-stu-id="18bd1-146">Altitude is calculated by the device binding.</span></span> <span data-ttu-id="18bd1-147">此重载 `TryReadAltitude` 使用平均海平面级压力来生成估算。</span><span class="sxs-lookup"><span data-stu-id="18bd1-147">This overload of `TryReadAltitude` uses mean sea level pressure to generate an estimate.</span></span>

        1. <span data-ttu-id="18bd1-148">将当前环境条件写入控制台。</span><span class="sxs-lookup"><span data-stu-id="18bd1-148">Writes the current environmental conditions to the console.</span></span>
        1. <span data-ttu-id="18bd1-149">睡眠1000毫秒。</span><span class="sxs-lookup"><span data-stu-id="18bd1-149">Sleeps 1000 ms.</span></span>

1. [!INCLUDE [tutorial-build](../includes/tutorial-build.md)]
1. [!INCLUDE [tutorial-deploy](../includes/tutorial-deploy.md)]
1. <span data-ttu-id="18bd1-150">通过切换到部署目录并运行可执行文件，在 Raspberry Pi 上运行该应用。</span><span class="sxs-lookup"><span data-stu-id="18bd1-150">Run the app on the Raspberry Pi by switching to the deployment directory and running the executable.</span></span>

    ```bash
    ./SensorTutorial
    ```

    <span data-ttu-id="18bd1-151">在控制台中查看传感器输出。</span><span class="sxs-lookup"><span data-stu-id="18bd1-151">Observe the sensor output in the console.</span></span>

1. <span data-ttu-id="18bd1-152">通过按 <kbd>Ctrl + C</kbd>终止节目。</span><span class="sxs-lookup"><span data-stu-id="18bd1-152">Terminate the program by pressing <kbd>Ctrl+C</kbd>.</span></span>

<span data-ttu-id="18bd1-153">祝贺你！</span><span class="sxs-lookup"><span data-stu-id="18bd1-153">Congratulations!</span></span> <span data-ttu-id="18bd1-154">你已使用 I2C 读取温度/湿度/大气压力传感器的值！</span><span class="sxs-lookup"><span data-stu-id="18bd1-154">You've used I2C to read values from a temperature/humidity/barometric pressure sensor!</span></span>

## <a name="get-the-source-code"></a><span data-ttu-id="18bd1-155">获取源代码</span><span class="sxs-lookup"><span data-stu-id="18bd1-155">Get the source code</span></span>

<span data-ttu-id="18bd1-156">[GitHub 上提供](https://github.com/MicrosoftDocs/dotnet-iot-assets/tree/master/tutorials/SensorTutorial)了本教程的源。</span><span class="sxs-lookup"><span data-stu-id="18bd1-156">The source for this tutorial is [available on GitHub](https://github.com/MicrosoftDocs/dotnet-iot-assets/tree/master/tutorials/SensorTutorial).</span></span>

## <a name="next-steps"></a><span data-ttu-id="18bd1-157">后续步骤</span><span class="sxs-lookup"><span data-stu-id="18bd1-157">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="18bd1-158">了解如何在液晶屏上显示文本</span><span class="sxs-lookup"><span data-stu-id="18bd1-158">Learn how to display text on an LCD</span></span>](../tutorials/lcd-display.md)
