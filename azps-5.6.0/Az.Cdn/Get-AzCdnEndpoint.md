---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 21aead3d3dd17b380f466ffdeaf2e5c36c9b1235
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890879"
---
# <span data-ttu-id="fa657-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa657-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="fa657-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa657-102">SYNOPSIS</span></span>
<span data-ttu-id="fa657-103">Obtém um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="fa657-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="fa657-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fa657-104">SYNTAX</span></span>

### <span data-ttu-id="fa657-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fa657-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa657-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa657-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa657-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fa657-107">DESCRIPTION</span></span>
<span data-ttu-id="fa657-108">O cmdlet **Get-AzCdnEndpoint** obtém um ponto de extremidade cdn (Rede de Distribuição de Conteúdo) do Azure e seus dados de configuração associados.</span><span class="sxs-lookup"><span data-stu-id="fa657-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="fa657-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa657-109">EXAMPLES</span></span>

## <span data-ttu-id="fa657-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fa657-110">PARAMETERS</span></span>

### <span data-ttu-id="fa657-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="fa657-111">-CdnProfile</span></span>
<span data-ttu-id="fa657-112">Especifica o objeto de perfil CDN ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="fa657-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa657-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa657-113">-DefaultProfile</span></span>
<span data-ttu-id="fa657-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fa657-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa657-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fa657-115">-EndpointName</span></span>
<span data-ttu-id="fa657-116">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="fa657-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="fa657-117">O nome do ponto de extremidade não é o nome do host do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="fa657-117">The name of the endpoint is not the host name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa657-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fa657-118">-ProfileName</span></span>
<span data-ttu-id="fa657-119">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="fa657-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa657-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa657-120">-ResourceGroupName</span></span>
<span data-ttu-id="fa657-121">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="fa657-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa657-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa657-122">CommonParameters</span></span>
<span data-ttu-id="fa657-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa657-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa657-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa657-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa657-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa657-125">INPUTS</span></span>

### <span data-ttu-id="fa657-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="fa657-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="fa657-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fa657-127">OUTPUTS</span></span>

### <span data-ttu-id="fa657-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa657-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="fa657-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="fa657-129">NOTES</span></span>

## <span data-ttu-id="fa657-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa657-130">RELATED LINKS</span></span>

[<span data-ttu-id="fa657-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa657-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="fa657-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa657-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="fa657-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa657-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="fa657-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa657-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="fa657-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fa657-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


