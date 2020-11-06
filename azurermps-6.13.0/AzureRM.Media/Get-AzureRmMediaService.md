---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: 76705a699b814bf52d7c874ec86e067735764936
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429512"
---
# <span data-ttu-id="42b91-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="42b91-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="42b91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42b91-102">SYNOPSIS</span></span>
<span data-ttu-id="42b91-103">Obtém informações sobre um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="42b91-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42b91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42b91-104">SYNTAX</span></span>

### <span data-ttu-id="42b91-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="42b91-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42b91-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42b91-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42b91-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42b91-107">DESCRIPTION</span></span>
<span data-ttu-id="42b91-108">O cmdlet **Get-AzureRmMediaService** Obtém informações sobre um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="42b91-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="42b91-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42b91-109">EXAMPLES</span></span>

### <span data-ttu-id="42b91-110">Exemplo 1: obter todos os serviços de mídia em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="42b91-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="42b91-111">Esse comando obtém as propriedades de todos os serviços de mídia no grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="42b91-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="42b91-112">Exemplo 2: obter propriedades do serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="42b91-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="42b91-113">Esse comando obtém as propriedades do serviço de mídia chamado MediaService1 que pertence ao grupo de recursos chamado ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="42b91-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="42b91-114">OS</span><span class="sxs-lookup"><span data-stu-id="42b91-114">PARAMETERS</span></span>

### <span data-ttu-id="42b91-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="42b91-115">-AccountName</span></span>
<span data-ttu-id="42b91-116">Especifica o nome do serviço de mídia que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="42b91-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="42b91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b91-117">-DefaultProfile</span></span>
<span data-ttu-id="42b91-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="42b91-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b91-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42b91-119">-ResourceGroupName</span></span>
<span data-ttu-id="42b91-120">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="42b91-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="42b91-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b91-121">CommonParameters</span></span>
<span data-ttu-id="42b91-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b91-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b91-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42b91-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b91-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42b91-124">INPUTS</span></span>

### <span data-ttu-id="42b91-125">System. String</span><span class="sxs-lookup"><span data-stu-id="42b91-125">System.String</span></span>

## <span data-ttu-id="42b91-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42b91-126">OUTPUTS</span></span>

### <span data-ttu-id="42b91-127">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="42b91-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="42b91-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42b91-128">NOTES</span></span>

## <span data-ttu-id="42b91-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42b91-129">RELATED LINKS</span></span>

[<span data-ttu-id="42b91-130">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="42b91-130">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="42b91-131">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="42b91-131">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="42b91-132">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="42b91-132">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


