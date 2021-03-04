---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 51dd39f18874fc1888fb37277f5de0557cf3553b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888887"
---
# <span data-ttu-id="c70d4-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="c70d4-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="c70d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c70d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c70d4-103">Obtém um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="c70d4-103">Gets a log profile.</span></span>

## <span data-ttu-id="c70d4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c70d4-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c70d4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c70d4-105">DESCRIPTION</span></span>
<span data-ttu-id="c70d4-106">O cmdlet **Get-AzLogProfile** obtém um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="c70d4-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="c70d4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c70d4-107">EXAMPLES</span></span>

## <span data-ttu-id="c70d4-108">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c70d4-108">PARAMETERS</span></span>

### <span data-ttu-id="c70d4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c70d4-109">-DefaultProfile</span></span>
<span data-ttu-id="c70d4-110">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c70d4-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c70d4-111">-Name</span><span class="sxs-lookup"><span data-stu-id="c70d4-111">-Name</span></span>
<span data-ttu-id="c70d4-112">Especifica o nome do perfil de log a ser obter.</span><span class="sxs-lookup"><span data-stu-id="c70d4-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c70d4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c70d4-113">CommonParameters</span></span>
<span data-ttu-id="c70d4-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c70d4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c70d4-115">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c70d4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c70d4-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c70d4-116">INPUTS</span></span>

### <span data-ttu-id="c70d4-117">System.String</span><span class="sxs-lookup"><span data-stu-id="c70d4-117">System.String</span></span>

## <span data-ttu-id="c70d4-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c70d4-118">OUTPUTS</span></span>

### <span data-ttu-id="c70d4-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="c70d4-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="c70d4-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="c70d4-120">NOTES</span></span>

## <span data-ttu-id="c70d4-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c70d4-121">RELATED LINKS</span></span>

[<span data-ttu-id="c70d4-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="c70d4-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="c70d4-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="c70d4-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


