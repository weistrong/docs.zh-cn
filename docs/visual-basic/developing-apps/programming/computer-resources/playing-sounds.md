---
description: 详细了解：播放声音 (Visual Basic)
title: 播放声音
ms.date: 07/20/2015
helpviewer_keywords:
- system sounds, playing
- system sounds
- playing sounds, Visual Basic
- sound loops
- My.Computer.Audio object, tasks
- sounds, playing
- sounds, background
- playing sounds
ms.assetid: f0d9e4ab-57c7-47b6-86d3-99ff07078040
ms.openlocfilehash: 247af8274108ca8374cf87e53aa2aaad8e5e736c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99641507"
---
# <a name="playing-sounds-visual-basic"></a><span data-ttu-id="b2cb1-103">播放声音 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b2cb1-103">Playing Sounds (Visual Basic)</span></span>

<span data-ttu-id="b2cb1-104">`My.Computer.Audio` 对象提供用于播放声音的方法。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-104">The `My.Computer.Audio` object provides methods for playing sounds.</span></span>  
  
## <a name="playing-sounds"></a><span data-ttu-id="b2cb1-105">播放声音</span><span class="sxs-lookup"><span data-stu-id="b2cb1-105">Playing Sounds</span></span>  

 <span data-ttu-id="b2cb1-106">应用程序可通过背景播放在播放声音时执行其他代码。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-106">Background playing lets the application execute other code while the sound plays.</span></span> <span data-ttu-id="b2cb1-107">`My.Computer.Audio.Play` 方法允许应用程序一次仅播放一种背景声音；应用程序播放新背景声音时，会停止播放上一种背景声音。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-107">The `My.Computer.Audio.Play` method allows the application to play only one background sound at a time; when the application plays a new background sound, it stops playing the previous background sound.</span></span> <span data-ttu-id="b2cb1-108">你也可以播放一种声音并等待其播放完毕。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-108">You can also play a sound and wait for it to complete.</span></span>  
  
 <span data-ttu-id="b2cb1-109">下例中使用 `My.Computer.Audio.Play` 方法播放声音。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-109">In the following example, the `My.Computer.Audio.Play` method plays a sound.</span></span> <span data-ttu-id="b2cb1-110">指定 `AudioPlayMode.WaitToComplete` 时，`My.Computer.Audio.Play` 将等待声音播放完毕，然后再调用代码继续。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-110">When `AudioPlayMode.WaitToComplete` is specified, `My.Computer.Audio.Play` waits until the sound completes before calling code continues.</span></span> <span data-ttu-id="b2cb1-111">使用此示例时，应确保文件名可指代计算机中的 .wav 声音文件</span><span class="sxs-lookup"><span data-stu-id="b2cb1-111">When using this example, you should ensure that the file name refers to a .wav sound file that is on your computer</span></span>  
  
 [!code-vb[VbVbalrMyComputer#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class1.vb#15)]  
  
 <span data-ttu-id="b2cb1-112">下例中使用 `My.Computer.Audio.Play` 方法播放声音。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-112">In the following example, the `My.Computer.Audio.Play` method plays a sound.</span></span> <span data-ttu-id="b2cb1-113">使用此示例时，应确保应用程序资源包含名为 Waterfall 的 .wav 声音文件。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-113">When using this example, you should ensure that the application resources include a .wav sound file that is named Waterfall.</span></span>  
  
 [!code-vb[VbVbalrMyComputer#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class1.vb#16)]  
  
## <a name="playing-looping-sounds"></a><span data-ttu-id="b2cb1-114">播放循环声音</span><span class="sxs-lookup"><span data-stu-id="b2cb1-114">Playing Looping Sounds</span></span>  

 <span data-ttu-id="b2cb1-115">在下例中，指定 `PlayMode.BackgroundLoop` 时，`My.Computer.Audio.Play` 方法将播放指定的背景声音。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-115">In the following example, the `My.Computer.Audio.Play` method plays the specified sound in the background when `PlayMode.BackgroundLoop` is specified.</span></span> <span data-ttu-id="b2cb1-116">使用此示例时，应确保文件名可指代计算机中的 .wav 声音文件。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-116">When using this example, you should ensure that the file name refers to a .wav sound file that is on your computer.</span></span>  
  
 [!code-vb[VbVbalrMyComputer#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class1.vb#11)]  
  
 <span data-ttu-id="b2cb1-117">在下例中，指定 `PlayMode.BackgroundLoop` 时，`My.Computer.Audio.Play` 方法将播放指定的背景声音。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-117">In the following example, the `My.Computer.Audio.Play` method plays the specified sound in the background when `PlayMode.BackgroundLoop` is specified.</span></span> <span data-ttu-id="b2cb1-118">使用此示例时，应确保应用程序资源包含名为 Waterfall 的 .wav 声音文件。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-118">When using this example, you should ensure that the application resources include a .wav sound file that is named Waterfall.</span></span>  
  
 [!code-vb[VbVbalrMyComputer#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class1.vb#12)]  
  
 <span data-ttu-id="b2cb1-119">前面的代码示例也可作为 IntelliSense 代码片段。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-119">The preceding code example is also available as an IntelliSense code snippet.</span></span> <span data-ttu-id="b2cb1-120">在代码片段选取器中，它位于“Windows 窗体应用程序”>“声音”中。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-120">In the code snippet picker, it is located in **Windows Forms Applications > Sound**.</span></span> <span data-ttu-id="b2cb1-121">有关详细信息，请参阅[代码片段](/visualstudio/ide/code-snippets)。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-121">For more information, see [Code Snippets](/visualstudio/ide/code-snippets).</span></span>  
  
 <span data-ttu-id="b2cb1-122">一般情况下，应用程序播放循环声音时，声音最终将停止。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-122">In general, when an application plays a looping sound, it should eventually stop the sound.</span></span>  
  
## <a name="stopping-the-playing-of-sounds-in-the-background"></a><span data-ttu-id="b2cb1-123">停止播放背景声音</span><span class="sxs-lookup"><span data-stu-id="b2cb1-123">Stopping the Playing of Sounds in the Background</span></span>  

 <span data-ttu-id="b2cb1-124">使用 `My.Computer.Audio.Stop` 方法可停止应用程序当前播放的背景声音或循环声音。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-124">Use the `My.Computer.Audio.Stop` method to stop the application's currently playing background or looping sound.</span></span>  
  
 <span data-ttu-id="b2cb1-125">一般情况下，应用程序播放循环声音时，声音将在某个时间点停止。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-125">In general, when an application plays a looping sound, it should stop the sound at some point.</span></span>  
  
 <span data-ttu-id="b2cb1-126">下面的示例将停止播放背景声音。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-126">The following example stops a sound that is playing in the background.</span></span>  
  
 [!code-vb[VbVbalrMyComputer#18](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class1.vb#18)]  
  
 <span data-ttu-id="b2cb1-127">前面的代码示例也可作为 IntelliSense 代码片段。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-127">The preceding code example is also available as an IntelliSense code snippet.</span></span> <span data-ttu-id="b2cb1-128">在代码片段选取器中，它位于“Windows 窗体应用程序”>“声音”中。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-128">In the code snippet picker, it is located in **Windows Forms Applications > Sound**.</span></span> <span data-ttu-id="b2cb1-129">有关详细信息，请参阅[代码片段](/visualstudio/ide/code-snippets)。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-129">For more information, see [Code Snippets](/visualstudio/ide/code-snippets).</span></span>  
  
## <a name="playing-system-sounds"></a><span data-ttu-id="b2cb1-130">播放系统声音</span><span class="sxs-lookup"><span data-stu-id="b2cb1-130">Playing System Sounds</span></span>  

 <span data-ttu-id="b2cb1-131">使用 `My.Computer.Audio.PlaySystemSound` 方法可播放指定的系统声音。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-131">Use the `My.Computer.Audio.PlaySystemSound` method to play the specified system sound.</span></span>  
  
 <span data-ttu-id="b2cb1-132">`My.Computer.Audio.PlaySystemSound` 方法将作为 <xref:System.Media.SystemSound> 类中的共享成员之一的参数。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-132">The `My.Computer.Audio.PlaySystemSound` method takes as a parameter one of the shared members from the <xref:System.Media.SystemSound> class.</span></span> <span data-ttu-id="b2cb1-133">系统声音 <xref:System.Media.SystemSounds.Asterisk%2A> 通常表示错误。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-133">The system sound <xref:System.Media.SystemSounds.Asterisk%2A> generally denotes errors.</span></span>  
  
 <span data-ttu-id="b2cb1-134">下例使用 `My.Computer.Audio.PlaySystemSound` 方法播放系统声音。</span><span class="sxs-lookup"><span data-stu-id="b2cb1-134">The following example uses the `My.Computer.Audio.PlaySystemSound` method to play a system sound.</span></span>  
  
 [!code-vb[VbVbalrMyComputer#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class1.vb#17)]  
  
## <a name="see-also"></a><span data-ttu-id="b2cb1-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b2cb1-135">See also</span></span>

- <xref:Microsoft.VisualBasic.Devices.Audio>
- <xref:Microsoft.VisualBasic.Devices.Audio.Play%2A>
- <xref:Microsoft.VisualBasic.Devices.Audio.PlaySystemSound%2A>
- <xref:Microsoft.VisualBasic.Devices.Audio.Stop%2A>
- <xref:Microsoft.VisualBasic.AudioPlayMode>
