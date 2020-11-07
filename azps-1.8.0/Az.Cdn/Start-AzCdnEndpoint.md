---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 8216d6404cb184767b03acd92f6549c2b8eda2e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771267"
---
# <span data-ttu-id="d3c81-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3c81-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="d3c81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3c81-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c81-103">Inicia um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="d3c81-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="d3c81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3c81-104">SYNTAX</span></span>

### <span data-ttu-id="d3c81-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d3c81-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3c81-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3c81-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3c81-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3c81-107">DESCRIPTION</span></span>
<span data-ttu-id="d3c81-108">O cmdlet **Start-AzCdnEndpoint** inicia um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c81-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d3c81-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3c81-109">EXAMPLES</span></span>

## <span data-ttu-id="d3c81-110">OS</span><span class="sxs-lookup"><span data-stu-id="d3c81-110">PARAMETERS</span></span>

### <span data-ttu-id="d3c81-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3c81-111">-CdnEndpoint</span></span>
<span data-ttu-id="d3c81-112">Especifica o ponto de extremidade que este cmdlet iniciará.</span><span class="sxs-lookup"><span data-stu-id="d3c81-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d3c81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c81-113">-DefaultProfile</span></span>
<span data-ttu-id="d3c81-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d3c81-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3c81-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d3c81-115">-EndpointName</span></span>
<span data-ttu-id="d3c81-116">Especifica o nome do ponto de extremidade que este cmdlet iniciará.</span><span class="sxs-lookup"><span data-stu-id="d3c81-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d3c81-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3c81-117">-PassThru</span></span>
<span data-ttu-id="d3c81-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d3c81-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d3c81-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d3c81-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3c81-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d3c81-120">-ProfileName</span></span>
<span data-ttu-id="d3c81-121">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="d3c81-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d3c81-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3c81-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3c81-123">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="d3c81-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d3c81-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d3c81-124">-Confirm</span></span>
<span data-ttu-id="d3c81-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3c81-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3c81-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3c81-126">-WhatIf</span></span>
<span data-ttu-id="d3c81-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3c81-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3c81-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3c81-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3c81-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c81-129">CommonParameters</span></span>
<span data-ttu-id="d3c81-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3c81-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c81-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c81-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c81-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3c81-132">INPUTS</span></span>

### <span data-ttu-id="d3c81-133">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3c81-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="d3c81-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d3c81-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d3c81-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3c81-135">OUTPUTS</span></span>

### <span data-ttu-id="d3c81-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3c81-136">System.Boolean</span></span>

## <span data-ttu-id="d3c81-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3c81-137">NOTES</span></span>

## <span data-ttu-id="d3c81-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3c81-138">RELATED LINKS</span></span>

[<span data-ttu-id="d3c81-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3c81-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="d3c81-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3c81-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="d3c81-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3c81-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="d3c81-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3c81-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="d3c81-143">Parar-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3c81-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


