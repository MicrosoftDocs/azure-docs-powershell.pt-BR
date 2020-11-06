---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/start-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
ms.openlocfilehash: 4a6f7b86d16e5b82cf6bf9e869ed74f688fc5950
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431379"
---
# <span data-ttu-id="fc918-101">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc918-101">Start-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="fc918-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc918-102">SYNOPSIS</span></span>
<span data-ttu-id="fc918-103">Inicia um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="fc918-103">Starts a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc918-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc918-104">SYNTAX</span></span>

### <span data-ttu-id="fc918-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fc918-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc918-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc918-106">ByObjectParameterSet</span></span>
```
Start-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc918-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc918-107">DESCRIPTION</span></span>
<span data-ttu-id="fc918-108">O cmdlet **Start-AzureRmCdnEndpoint** inicia um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc918-108">The **Start-AzureRmCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="fc918-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc918-109">EXAMPLES</span></span>

## <span data-ttu-id="fc918-110">OS</span><span class="sxs-lookup"><span data-stu-id="fc918-110">PARAMETERS</span></span>

### <span data-ttu-id="fc918-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc918-111">-CdnEndpoint</span></span>
<span data-ttu-id="fc918-112">Especifica o ponto de extremidade que este cmdlet iniciará.</span><span class="sxs-lookup"><span data-stu-id="fc918-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="fc918-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc918-113">-DefaultProfile</span></span>
<span data-ttu-id="fc918-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fc918-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc918-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fc918-115">-EndpointName</span></span>
<span data-ttu-id="fc918-116">Especifica o nome do ponto de extremidade que este cmdlet iniciará.</span><span class="sxs-lookup"><span data-stu-id="fc918-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="fc918-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc918-117">-PassThru</span></span>
<span data-ttu-id="fc918-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="fc918-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fc918-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="fc918-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fc918-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fc918-120">-ProfileName</span></span>
<span data-ttu-id="fc918-121">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="fc918-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="fc918-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc918-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc918-123">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="fc918-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="fc918-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc918-124">-Confirm</span></span>
<span data-ttu-id="fc918-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc918-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc918-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc918-126">-WhatIf</span></span>
<span data-ttu-id="fc918-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc918-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc918-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc918-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc918-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc918-129">CommonParameters</span></span>
<span data-ttu-id="fc918-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc918-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc918-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc918-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc918-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc918-132">INPUTS</span></span>

### <span data-ttu-id="fc918-133">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc918-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="fc918-134">Parâmetros: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fc918-134">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="fc918-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fc918-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fc918-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc918-136">OUTPUTS</span></span>

### <span data-ttu-id="fc918-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc918-137">System.Boolean</span></span>

## <span data-ttu-id="fc918-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc918-138">NOTES</span></span>

## <span data-ttu-id="fc918-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc918-139">RELATED LINKS</span></span>

[<span data-ttu-id="fc918-140">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc918-140">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fc918-141">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc918-141">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fc918-142">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc918-142">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fc918-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc918-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fc918-144">Parar-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc918-144">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


