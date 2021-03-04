---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: fcfd642ceaf2f371385ee1f09c99e1efa566941d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892480"
---
# <span data-ttu-id="e17f0-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e17f0-101">Get-AzMediaService</span></span>

## <span data-ttu-id="e17f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e17f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e17f0-103">Obtém informações sobre um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="e17f0-103">Gets information about a media service.</span></span>

## <span data-ttu-id="e17f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e17f0-104">SYNTAX</span></span>

### <span data-ttu-id="e17f0-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e17f0-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e17f0-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e17f0-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e17f0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e17f0-107">DESCRIPTION</span></span>
<span data-ttu-id="e17f0-108">O cmdlet **Get-AzMediaService** obtém informações sobre um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="e17f0-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="e17f0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e17f0-109">EXAMPLES</span></span>

### <span data-ttu-id="e17f0-110">Exemplo 1: Obter todos os serviços de mídia em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e17f0-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="e17f0-111">Este comando obtém propriedades para todos os serviços de mídia no grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="e17f0-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="e17f0-112">Exemplo 2: Obter propriedades de serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="e17f0-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="e17f0-113">Este comando obtém as propriedades do serviço de mídia chamado MediaService1 que pertence ao grupo de recursos chamado ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="e17f0-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="e17f0-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e17f0-114">PARAMETERS</span></span>

### <span data-ttu-id="e17f0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e17f0-115">-AccountName</span></span>
<span data-ttu-id="e17f0-116">Especifica o nome do serviço de mídia que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e17f0-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e17f0-117">-DefaultProfile</span></span>
<span data-ttu-id="e17f0-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e17f0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e17f0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e17f0-119">-ResourceGroupName</span></span>
<span data-ttu-id="e17f0-120">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="e17f0-120">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e17f0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17f0-121">CommonParameters</span></span>
<span data-ttu-id="e17f0-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e17f0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17f0-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e17f0-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17f0-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e17f0-124">INPUTS</span></span>

### <span data-ttu-id="e17f0-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e17f0-125">System.String</span></span>

## <span data-ttu-id="e17f0-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e17f0-126">OUTPUTS</span></span>

### <span data-ttu-id="e17f0-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="e17f0-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="e17f0-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="e17f0-128">NOTES</span></span>

## <span data-ttu-id="e17f0-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e17f0-129">RELATED LINKS</span></span>

[<span data-ttu-id="e17f0-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e17f0-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="e17f0-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e17f0-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="e17f0-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e17f0-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


