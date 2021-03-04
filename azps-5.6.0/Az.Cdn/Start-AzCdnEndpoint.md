---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: a6b5a471b4f04ce36d20b72502894b41b8dade4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891508"
---
# <span data-ttu-id="63674-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="63674-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="63674-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63674-102">SYNOPSIS</span></span>
<span data-ttu-id="63674-103">Inicia um ponto de extremidade cdn.</span><span class="sxs-lookup"><span data-stu-id="63674-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="63674-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="63674-104">SYNTAX</span></span>

### <span data-ttu-id="63674-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="63674-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63674-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63674-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63674-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="63674-107">DESCRIPTION</span></span>
<span data-ttu-id="63674-108">O cmdlet **Start-AzCdnEndpoint** inicia um ponto de extremidade cdn (Rede de Distribuição de Conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="63674-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="63674-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63674-109">EXAMPLES</span></span>

## <span data-ttu-id="63674-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="63674-110">PARAMETERS</span></span>

### <span data-ttu-id="63674-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="63674-111">-CdnEndpoint</span></span>
<span data-ttu-id="63674-112">Especifica o ponto de extremidade que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="63674-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="63674-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63674-113">-DefaultProfile</span></span>
<span data-ttu-id="63674-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="63674-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63674-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="63674-115">-EndpointName</span></span>
<span data-ttu-id="63674-116">Especifica o nome do ponto de extremidade que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="63674-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="63674-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63674-117">-PassThru</span></span>
<span data-ttu-id="63674-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="63674-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="63674-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="63674-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="63674-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="63674-120">-ProfileName</span></span>
<span data-ttu-id="63674-121">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="63674-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="63674-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63674-122">-ResourceGroupName</span></span>
<span data-ttu-id="63674-123">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="63674-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="63674-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63674-124">-Confirm</span></span>
<span data-ttu-id="63674-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63674-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63674-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63674-126">-WhatIf</span></span>
<span data-ttu-id="63674-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="63674-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63674-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63674-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63674-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63674-129">CommonParameters</span></span>
<span data-ttu-id="63674-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63674-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63674-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63674-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63674-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63674-132">INPUTS</span></span>

### <span data-ttu-id="63674-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="63674-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="63674-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="63674-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="63674-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="63674-135">OUTPUTS</span></span>

### <span data-ttu-id="63674-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63674-136">System.Boolean</span></span>

## <span data-ttu-id="63674-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="63674-137">NOTES</span></span>

## <span data-ttu-id="63674-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63674-138">RELATED LINKS</span></span>

[<span data-ttu-id="63674-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="63674-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="63674-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="63674-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="63674-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="63674-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="63674-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="63674-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="63674-143">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="63674-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


