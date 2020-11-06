---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
ms.openlocfilehash: 742fe2795f16ed0a626e071520977ead66a491f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431129"
---
# <span data-ttu-id="539cf-101">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="539cf-101">Start-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="539cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="539cf-102">SYNOPSIS</span></span>
<span data-ttu-id="539cf-103">Inicia um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="539cf-103">Starts a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="539cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="539cf-104">SYNTAX</span></span>

### <span data-ttu-id="539cf-105">Conjunto de parâmetros para parâmetros de campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="539cf-105">Parameter Set for fields parameters (Default)</span></span>
```
Start-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="539cf-106">Conjunto de parâmetros para parâmetros de objeto</span><span class="sxs-lookup"><span data-stu-id="539cf-106">Parameter Set for object parameters</span></span>
```
Start-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="539cf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="539cf-107">DESCRIPTION</span></span>
<span data-ttu-id="539cf-108">O cmdlet **Start-AzureRmCdnEndpoint** inicia um ponto de extremidade da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="539cf-108">The **Start-AzureRmCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="539cf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="539cf-109">EXAMPLES</span></span>

## <span data-ttu-id="539cf-110">OS</span><span class="sxs-lookup"><span data-stu-id="539cf-110">PARAMETERS</span></span>

### <span data-ttu-id="539cf-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="539cf-111">-CdnEndpoint</span></span>
<span data-ttu-id="539cf-112">Especifica o ponto de extremidade que este cmdlet iniciará.</span><span class="sxs-lookup"><span data-stu-id="539cf-112">Specifies the endpoint that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="539cf-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="539cf-113">-EndpointName</span></span>
<span data-ttu-id="539cf-114">Especifica o nome do ponto de extremidade que este cmdlet iniciará.</span><span class="sxs-lookup"><span data-stu-id="539cf-114">Specifies the name of the endpoint that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539cf-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="539cf-115">-PassThru</span></span>
<span data-ttu-id="539cf-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="539cf-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="539cf-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="539cf-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="539cf-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="539cf-118">-ProfileName</span></span>
<span data-ttu-id="539cf-119">Especifica o nome do perfil ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="539cf-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="539cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="539cf-121">Especifica o nome do grupo de recursos ao qual o ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="539cf-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539cf-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="539cf-122">-Confirm</span></span>
<span data-ttu-id="539cf-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="539cf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="539cf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="539cf-124">-WhatIf</span></span>
<span data-ttu-id="539cf-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="539cf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="539cf-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="539cf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="539cf-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539cf-127">-DefaultProfile</span></span>
<span data-ttu-id="539cf-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="539cf-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="539cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539cf-129">CommonParameters</span></span>
<span data-ttu-id="539cf-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="539cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539cf-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="539cf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539cf-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="539cf-132">INPUTS</span></span>

### <span data-ttu-id="539cf-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="539cf-133">PSEndpoint</span></span>
<span data-ttu-id="539cf-134">O parâmetro ' CdnEndpoint ' aceita o valor do tipo ' PSEndpoint ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="539cf-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="539cf-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="539cf-135">OUTPUTS</span></span>

### <span data-ttu-id="539cf-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="539cf-136">System.Boolean</span></span>

## <span data-ttu-id="539cf-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="539cf-137">NOTES</span></span>

## <span data-ttu-id="539cf-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="539cf-138">RELATED LINKS</span></span>

[<span data-ttu-id="539cf-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="539cf-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="539cf-140">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="539cf-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="539cf-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="539cf-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="539cf-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="539cf-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="539cf-143">Parar-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="539cf-143">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


