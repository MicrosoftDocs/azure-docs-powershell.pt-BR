---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126028"
---
# <span data-ttu-id="1c2b6-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1c2b6-101">Get-AzMediaService</span></span>

## <span data-ttu-id="1c2b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c2b6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2b6-103">Obtém informações sobre um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="1c2b6-103">Gets information about a media service.</span></span>

## <span data-ttu-id="1c2b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c2b6-104">SYNTAX</span></span>

### <span data-ttu-id="1c2b6-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c2b6-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c2b6-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c2b6-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c2b6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c2b6-107">DESCRIPTION</span></span>
<span data-ttu-id="1c2b6-108">O cmdlet **Get-AzMediaService** Obtém informações sobre um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="1c2b6-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="1c2b6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c2b6-109">EXAMPLES</span></span>

### <span data-ttu-id="1c2b6-110">Exemplo 1: obter todos os serviços de mídia em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1c2b6-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="1c2b6-111">Esse comando obtém as propriedades de todos os serviços de mídia no grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="1c2b6-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="1c2b6-112">Exemplo 2: obter propriedades do serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="1c2b6-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="1c2b6-113">Esse comando obtém as propriedades do serviço de mídia chamado MediaService1 que pertence ao grupo de recursos chamado ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="1c2b6-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="1c2b6-114">OS</span><span class="sxs-lookup"><span data-stu-id="1c2b6-114">PARAMETERS</span></span>

### <span data-ttu-id="1c2b6-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1c2b6-115">-AccountName</span></span>
<span data-ttu-id="1c2b6-116">Especifica o nome do serviço de mídia que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="1c2b6-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1c2b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2b6-117">-DefaultProfile</span></span>
<span data-ttu-id="1c2b6-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1c2b6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c2b6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c2b6-119">-ResourceGroupName</span></span>
<span data-ttu-id="1c2b6-120">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="1c2b6-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="1c2b6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2b6-121">CommonParameters</span></span>
<span data-ttu-id="1c2b6-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c2b6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2b6-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c2b6-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2b6-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c2b6-124">INPUTS</span></span>

### <span data-ttu-id="1c2b6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1c2b6-125">System.String</span></span>

## <span data-ttu-id="1c2b6-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c2b6-126">OUTPUTS</span></span>

### <span data-ttu-id="1c2b6-127">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="1c2b6-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="1c2b6-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c2b6-128">NOTES</span></span>

## <span data-ttu-id="1c2b6-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c2b6-129">RELATED LINKS</span></span>

[<span data-ttu-id="1c2b6-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1c2b6-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="1c2b6-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1c2b6-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="1c2b6-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1c2b6-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


