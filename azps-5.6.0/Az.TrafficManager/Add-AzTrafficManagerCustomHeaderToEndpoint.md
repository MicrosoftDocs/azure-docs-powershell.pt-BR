---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 4a24953dd763c54cba7454bf9e46bb9373b0f450
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889866"
---
# <span data-ttu-id="18163-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="18163-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="18163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18163-102">SYNOPSIS</span></span>
<span data-ttu-id="18163-103">Adiciona informações de header personalizadas a um objeto de ponto de extremidade do Gerenciador de Tráfego local.</span><span class="sxs-lookup"><span data-stu-id="18163-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="18163-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="18163-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18163-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="18163-105">DESCRIPTION</span></span>
<span data-ttu-id="18163-106">O cmdlet **Add-AzTrafficManagerCustomHeaderToEndpoint** adiciona informações de header personalizadas a um objeto de ponto de extremidade local do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="18163-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="18163-107">Você pode obter um ponto de extremidade usando o New-AzTrafficManagerEndpoint ou Get-AzTrafficManagerEndpoint cmdlets.</span><span class="sxs-lookup"><span data-stu-id="18163-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="18163-108">Este cmdlet opera no objeto de ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="18163-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="18163-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18163-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="18163-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18163-110">EXAMPLES</span></span>

### <span data-ttu-id="18163-111">Exemplo 1: Adicionar informações de header personalizadas a um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="18163-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="18163-112">O primeiro comando cria um ponto de extremidade do Gerenciador de Tráfego do Azure usando o cmdlet **New-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="18163-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="18163-113">O comando armazena o ponto de extremidade local na variável $TrafficManagerEndpoint local.</span><span class="sxs-lookup"><span data-stu-id="18163-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="18163-114">O segundo comando adiciona informações de header personalizadas ao ponto de extremidade armazenado $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="18163-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="18163-115">O comando final atualiza o ponto de extremidade no Gerenciador de Tráfego para corresponder ao valor local em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="18163-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="18163-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="18163-116">PARAMETERS</span></span>

### <span data-ttu-id="18163-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18163-117">-DefaultProfile</span></span>
<span data-ttu-id="18163-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="18163-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18163-119">-Name</span><span class="sxs-lookup"><span data-stu-id="18163-119">-Name</span></span>
<span data-ttu-id="18163-120">Especifica o nome das informações de header personalizadas a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="18163-120">Specifies the name of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18163-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="18163-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="18163-122">Especifica um objeto **TrafficManagerEndpoint** local.</span><span class="sxs-lookup"><span data-stu-id="18163-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="18163-123">Este cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="18163-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="18163-124">Para obter um **objeto TrafficManagerEndpoint,** use o Get-AzTrafficManagerEndpoint ou New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18163-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18163-125">-Value</span><span class="sxs-lookup"><span data-stu-id="18163-125">-Value</span></span>
<span data-ttu-id="18163-126">Especifica o valor das informações de header personalizadas a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="18163-126">Specifies the value of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18163-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18163-127">-Confirm</span></span>
<span data-ttu-id="18163-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18163-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18163-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18163-129">-WhatIf</span></span>
<span data-ttu-id="18163-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18163-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18163-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18163-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18163-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18163-132">CommonParameters</span></span>
<span data-ttu-id="18163-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18163-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18163-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18163-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18163-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18163-135">INPUTS</span></span>

### <span data-ttu-id="18163-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="18163-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="18163-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="18163-137">OUTPUTS</span></span>

### <span data-ttu-id="18163-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="18163-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="18163-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="18163-139">NOTES</span></span>

## <span data-ttu-id="18163-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18163-140">RELATED LINKS</span></span>

[<span data-ttu-id="18163-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="18163-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="18163-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="18163-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="18163-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="18163-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="18163-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="18163-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
