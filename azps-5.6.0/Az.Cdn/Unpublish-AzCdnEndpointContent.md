---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: 403c91802c70d7d5e6cfb844909dee1ca6956847
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887590"
---
# <span data-ttu-id="b1775-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="b1775-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="b1775-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1775-102">SYNOPSIS</span></span>
<span data-ttu-id="b1775-103">Limpa um ponto de extremidade cdn.</span><span class="sxs-lookup"><span data-stu-id="b1775-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="b1775-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b1775-104">SYNTAX</span></span>

### <span data-ttu-id="b1775-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b1775-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1775-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1775-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1775-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b1775-107">DESCRIPTION</span></span>
<span data-ttu-id="b1775-108">O cmdlet **Unpublish-AzCdnEndpointContent** limpa o conteúdo de um ponto de extremidade cdn (Rede de Distribuição de Conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1775-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b1775-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1775-109">EXAMPLES</span></span>

## <span data-ttu-id="b1775-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b1775-110">PARAMETERS</span></span>

### <span data-ttu-id="b1775-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b1775-111">-CdnEndpoint</span></span>
<span data-ttu-id="b1775-112">Especifica o ponto de extremidade que esse cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="b1775-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="b1775-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1775-113">-DefaultProfile</span></span>
<span data-ttu-id="b1775-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b1775-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1775-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b1775-115">-EndpointName</span></span>
<span data-ttu-id="b1775-116">Especifica o nome do ponto de extremidade que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="b1775-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="b1775-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1775-117">-PassThru</span></span>
<span data-ttu-id="b1775-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b1775-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b1775-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b1775-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1775-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b1775-120">-ProfileName</span></span>
<span data-ttu-id="b1775-121">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="b1775-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b1775-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="b1775-122">-PurgeContent</span></span>
<span data-ttu-id="b1775-123">Especifica uma matriz de caminhos relativos para o conteúdo no servidor de origem que este cmdlet limpa.</span><span class="sxs-lookup"><span data-stu-id="b1775-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1775-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1775-124">-ResourceGroupName</span></span>
<span data-ttu-id="b1775-125">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="b1775-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b1775-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1775-126">-Confirm</span></span>
<span data-ttu-id="b1775-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1775-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1775-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1775-128">-WhatIf</span></span>
<span data-ttu-id="b1775-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1775-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1775-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1775-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1775-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1775-131">CommonParameters</span></span>
<span data-ttu-id="b1775-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1775-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1775-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1775-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1775-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1775-134">INPUTS</span></span>

### <span data-ttu-id="b1775-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b1775-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="b1775-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b1775-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b1775-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b1775-137">OUTPUTS</span></span>

### <span data-ttu-id="b1775-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1775-138">System.Boolean</span></span>

## <span data-ttu-id="b1775-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="b1775-139">NOTES</span></span>

## <span data-ttu-id="b1775-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1775-140">RELATED LINKS</span></span>

[<span data-ttu-id="b1775-141">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="b1775-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


