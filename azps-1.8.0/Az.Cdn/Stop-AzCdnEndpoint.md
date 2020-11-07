---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: a606bbcb630ab4868e64221b9bcaa8f471327977
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771265"
---
# <span data-ttu-id="72c07-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="72c07-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="72c07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72c07-102">SYNOPSIS</span></span>
<span data-ttu-id="72c07-103">Para o ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="72c07-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="72c07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72c07-104">SYNTAX</span></span>

### <span data-ttu-id="72c07-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="72c07-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72c07-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72c07-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72c07-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72c07-107">DESCRIPTION</span></span>
<span data-ttu-id="72c07-108">O cmdlet **Stop-AzCdnEndpoint** interrompe o ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="72c07-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="72c07-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72c07-109">EXAMPLES</span></span>

## <span data-ttu-id="72c07-110">OS</span><span class="sxs-lookup"><span data-stu-id="72c07-110">PARAMETERS</span></span>

### <span data-ttu-id="72c07-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="72c07-111">-CdnEndpoint</span></span>
<span data-ttu-id="72c07-112">Especifica o objeto de ponto de extremidade para o qual este cmdlet é interrompido.</span><span class="sxs-lookup"><span data-stu-id="72c07-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="72c07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c07-113">-DefaultProfile</span></span>
<span data-ttu-id="72c07-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="72c07-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72c07-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="72c07-115">-EndpointName</span></span>
<span data-ttu-id="72c07-116">Especifica o nome do ponto de extremidade que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="72c07-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="72c07-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72c07-117">-PassThru</span></span>
<span data-ttu-id="72c07-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="72c07-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="72c07-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="72c07-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="72c07-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="72c07-120">-ProfileName</span></span>
<span data-ttu-id="72c07-121">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="72c07-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="72c07-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72c07-122">-ResourceGroupName</span></span>
<span data-ttu-id="72c07-123">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="72c07-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="72c07-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="72c07-124">-Confirm</span></span>
<span data-ttu-id="72c07-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72c07-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72c07-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72c07-126">-WhatIf</span></span>
<span data-ttu-id="72c07-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="72c07-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72c07-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="72c07-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72c07-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c07-129">CommonParameters</span></span>
<span data-ttu-id="72c07-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72c07-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c07-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72c07-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c07-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72c07-132">INPUTS</span></span>

### <span data-ttu-id="72c07-133">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="72c07-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="72c07-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="72c07-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="72c07-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72c07-135">OUTPUTS</span></span>

### <span data-ttu-id="72c07-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72c07-136">System.Boolean</span></span>

## <span data-ttu-id="72c07-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72c07-137">NOTES</span></span>

## <span data-ttu-id="72c07-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72c07-138">RELATED LINKS</span></span>

[<span data-ttu-id="72c07-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="72c07-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="72c07-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="72c07-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="72c07-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="72c07-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="72c07-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="72c07-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="72c07-143">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="72c07-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


