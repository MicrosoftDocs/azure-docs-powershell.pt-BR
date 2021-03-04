---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: 5c2aa677bd2f197cfae262ed54372d5172fe2a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892810"
---
# <span data-ttu-id="87111-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="87111-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="87111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87111-102">SYNOPSIS</span></span>
<span data-ttu-id="87111-103">Obtém um servidor de origem cdn.</span><span class="sxs-lookup"><span data-stu-id="87111-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="87111-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="87111-104">SYNTAX</span></span>

### <span data-ttu-id="87111-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="87111-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87111-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87111-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87111-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87111-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87111-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="87111-108">DESCRIPTION</span></span>
<span data-ttu-id="87111-109">O cmdlet **Get-AzCdnOrigin** obtém um servidor de origem da Rede de Distribuição de Conteúdo (CDN) do Azure e seus dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="87111-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="87111-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87111-110">EXAMPLES</span></span>

## <span data-ttu-id="87111-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="87111-111">PARAMETERS</span></span>

### <span data-ttu-id="87111-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="87111-112">-CdnEndpoint</span></span>
<span data-ttu-id="87111-113">Especifica o objeto de ponto de extremidade CDN ao qual a origem pertence.</span><span class="sxs-lookup"><span data-stu-id="87111-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87111-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87111-114">-DefaultProfile</span></span>
<span data-ttu-id="87111-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="87111-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87111-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="87111-116">-EndpointName</span></span>
<span data-ttu-id="87111-117">Especifica o nome do ponto de extremidade ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="87111-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="87111-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="87111-118">-OriginName</span></span>
<span data-ttu-id="87111-119">Especifica o nome do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="87111-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="87111-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="87111-120">-ProfileName</span></span>
<span data-ttu-id="87111-121">Especifica o nome do perfil ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="87111-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="87111-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87111-122">-ResourceGroupName</span></span>
<span data-ttu-id="87111-123">Especifica o nome do grupo de recursos ao qual o servidor de origem pertence.</span><span class="sxs-lookup"><span data-stu-id="87111-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="87111-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87111-124">-ResourceId</span></span>
<span data-ttu-id="87111-125">A id de recurso da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="87111-125">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87111-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87111-126">CommonParameters</span></span>
<span data-ttu-id="87111-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87111-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87111-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87111-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87111-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87111-129">INPUTS</span></span>

### <span data-ttu-id="87111-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="87111-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="87111-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="87111-131">OUTPUTS</span></span>

### <span data-ttu-id="87111-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="87111-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="87111-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="87111-133">NOTES</span></span>

## <span data-ttu-id="87111-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87111-134">RELATED LINKS</span></span>

[<span data-ttu-id="87111-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="87111-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


