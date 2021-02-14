---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111182"
---
# <span data-ttu-id="7468f-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7468f-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="7468f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7468f-102">SYNOPSIS</span></span>
<span data-ttu-id="7468f-103">Inicia um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="7468f-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="7468f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7468f-104">SYNTAX</span></span>

### <span data-ttu-id="7468f-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7468f-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7468f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7468f-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7468f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7468f-107">DESCRIPTION</span></span>
<span data-ttu-id="7468f-108">O cmdlet **Start-AzCdnEndpoint** inicia um ponto de extremidade de Rede de Distribuição de Conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="7468f-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7468f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7468f-109">EXAMPLES</span></span>

## <span data-ttu-id="7468f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7468f-110">PARAMETERS</span></span>

### <span data-ttu-id="7468f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7468f-111">-CdnEndpoint</span></span>
<span data-ttu-id="7468f-112">Especifica o ponto de extremidade que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="7468f-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="7468f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7468f-113">-DefaultProfile</span></span>
<span data-ttu-id="7468f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7468f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7468f-115">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="7468f-115">-EndpointName</span></span>
<span data-ttu-id="7468f-116">Especifica o nome do ponto de extremidade que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="7468f-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="7468f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7468f-117">-PassThru</span></span>
<span data-ttu-id="7468f-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="7468f-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7468f-119">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="7468f-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7468f-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7468f-120">-ProfileName</span></span>
<span data-ttu-id="7468f-121">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="7468f-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="7468f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7468f-122">-ResourceGroupName</span></span>
<span data-ttu-id="7468f-123">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="7468f-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="7468f-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7468f-124">-Confirm</span></span>
<span data-ttu-id="7468f-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7468f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7468f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7468f-126">-WhatIf</span></span>
<span data-ttu-id="7468f-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7468f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7468f-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7468f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7468f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7468f-129">CommonParameters</span></span>
<span data-ttu-id="7468f-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7468f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7468f-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7468f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7468f-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="7468f-132">INPUTS</span></span>

### <span data-ttu-id="7468f-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7468f-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="7468f-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7468f-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7468f-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="7468f-135">OUTPUTS</span></span>

### <span data-ttu-id="7468f-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7468f-136">System.Boolean</span></span>

## <span data-ttu-id="7468f-137">Notas</span><span class="sxs-lookup"><span data-stu-id="7468f-137">NOTES</span></span>

## <span data-ttu-id="7468f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7468f-138">RELATED LINKS</span></span>

[<span data-ttu-id="7468f-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7468f-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="7468f-140">Novo-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7468f-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="7468f-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7468f-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="7468f-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7468f-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="7468f-143">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7468f-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


