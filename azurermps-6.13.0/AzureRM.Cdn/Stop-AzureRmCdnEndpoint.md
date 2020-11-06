---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 20206ebf99d597a2961804bf3062cd4c049f8017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609413"
---
# <span data-ttu-id="9e2d5-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e2d5-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="9e2d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e2d5-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2d5-103">Para o ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e2d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e2d5-104">SYNTAX</span></span>

### <span data-ttu-id="9e2d5-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="9e2d5-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e2d5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e2d5-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e2d5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e2d5-107">DESCRIPTION</span></span>
<span data-ttu-id="9e2d5-108">O cmdlet **Stop-AzureRmCdnEndpoint** interrompe o ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="9e2d5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e2d5-109">EXAMPLES</span></span>

## <span data-ttu-id="9e2d5-110">OS</span><span class="sxs-lookup"><span data-stu-id="9e2d5-110">PARAMETERS</span></span>

### <span data-ttu-id="9e2d5-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e2d5-111">-CdnEndpoint</span></span>
<span data-ttu-id="9e2d5-112">Especifica o objeto de ponto de extremidade para o qual este cmdlet é interrompido.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="9e2d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2d5-113">-DefaultProfile</span></span>
<span data-ttu-id="9e2d5-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9e2d5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e2d5-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9e2d5-115">-EndpointName</span></span>
<span data-ttu-id="9e2d5-116">Especifica o nome do ponto de extremidade que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="9e2d5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e2d5-117">-PassThru</span></span>
<span data-ttu-id="9e2d5-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9e2d5-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9e2d5-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9e2d5-120">-ProfileName</span></span>
<span data-ttu-id="9e2d5-121">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="9e2d5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e2d5-122">-ResourceGroupName</span></span>
<span data-ttu-id="9e2d5-123">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="9e2d5-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9e2d5-124">-Confirm</span></span>
<span data-ttu-id="9e2d5-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e2d5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e2d5-126">-WhatIf</span></span>
<span data-ttu-id="9e2d5-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e2d5-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e2d5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2d5-129">CommonParameters</span></span>
<span data-ttu-id="9e2d5-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e2d5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2d5-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e2d5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2d5-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e2d5-132">INPUTS</span></span>

### <span data-ttu-id="9e2d5-133">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e2d5-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="9e2d5-134">Parâmetros: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9e2d5-134">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="9e2d5-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9e2d5-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9e2d5-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e2d5-136">OUTPUTS</span></span>

### <span data-ttu-id="9e2d5-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e2d5-137">System.Boolean</span></span>

## <span data-ttu-id="9e2d5-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e2d5-138">NOTES</span></span>

## <span data-ttu-id="9e2d5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e2d5-139">RELATED LINKS</span></span>

[<span data-ttu-id="9e2d5-140">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e2d5-140">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9e2d5-141">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e2d5-141">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9e2d5-142">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e2d5-142">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9e2d5-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e2d5-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="9e2d5-144">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e2d5-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


