---
description: 了解详细信息： TextFieldParser 不支持包含空格的注释标记
title: TextFieldParser 不支持包含空格的注释标记
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_WhitespaceInToken
ms.assetid: 55107656-270e-4bbb-841a-478904df8e07
ms.openlocfilehash: 27ca19f0a901ca1644d4b121951ed9fdf4d553bd
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100455335"
---
# <a name="textfieldparser-does-not-support-comment-tokens-that-contain-white-space"></a><span data-ttu-id="2e3d6-103">TextFieldParser 不支持包含空格的注释标记</span><span class="sxs-lookup"><span data-stu-id="2e3d6-103">TextFieldParser does not support comment tokens that contain white space</span></span>

<span data-ttu-id="2e3d6-104">提供了包含空格的注释标记。</span><span class="sxs-lookup"><span data-stu-id="2e3d6-104">A comment token that contains white space has been supplied.</span></span> <span data-ttu-id="2e3d6-105">`TextFieldParser` 不支持包含空格的注释标记，除非空格出现在标记的开头。</span><span class="sxs-lookup"><span data-stu-id="2e3d6-105">The `TextFieldParser` does not support comment tokens that contain white space unless the white space occurs at the beginning of the token.</span></span> <span data-ttu-id="2e3d6-106">出现在标记开头的空格将被忽略。</span><span class="sxs-lookup"><span data-stu-id="2e3d6-106">White space occurring at the beginning of a token is ignored.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="2e3d6-107">更正此错误</span><span class="sxs-lookup"><span data-stu-id="2e3d6-107">To correct this error</span></span>  
  
- <span data-ttu-id="2e3d6-108">提供正确的注释标记。</span><span class="sxs-lookup"><span data-stu-id="2e3d6-108">Supply a correct comment token.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e3d6-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="2e3d6-109">See also</span></span>

- [<span data-ttu-id="2e3d6-110">TextFieldParser.CommentTokens 属性</span><span class="sxs-lookup"><span data-stu-id="2e3d6-110">TextFieldParser.CommentTokens Property</span></span>](xref:Microsoft.VisualBasic.FileIO.TextFieldParser.CommentTokens%2A)
- [<span data-ttu-id="2e3d6-111">使用 TextFieldParser 对象分析文本文件</span><span class="sxs-lookup"><span data-stu-id="2e3d6-111">Parsing Text Files with the TextFieldParser Object</span></span>](../developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object.md)
- [<span data-ttu-id="2e3d6-112">TextFieldParser Object</span><span class="sxs-lookup"><span data-stu-id="2e3d6-112">TextFieldParser Object</span></span>](../language-reference/objects/textfieldparser-object.md)
