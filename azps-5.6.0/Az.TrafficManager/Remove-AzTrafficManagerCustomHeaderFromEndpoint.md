---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: f0d179c82292ffb9300791337f40436c4d4c5f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889849"
---
# <span data-ttu-id="b8c7e-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8c7e-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="b8c7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c7e-103">Remove informações de header personalizadas de um objeto de ponto de extremidade do Gerenciador de Tráfego local.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="b8c7e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8c7e-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8c7e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8c7e-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c7e-106">O cmdlet **Remove-AzTrafficManagerCustomHeaderFromEndpoint** remove informações de header personalizadas de um objeto de ponto de extremidade local do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="b8c7e-107">Você pode obter um ponto de extremidade usando o New-AzTrafficManagerEndpoint ou Get-AzTrafficManagerEndpoint cmdlets.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="b8c7e-108">Este cmdlet opera no objeto de ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="b8c7e-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="b8c7e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8c7e-110">EXAMPLES</span></span>

### <span data-ttu-id="b8c7e-111">Exemplo 1: Remover informações de sub-rede personalizadas de um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="b8c7e-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="b8c7e-112">O primeiro comando obtém o ponto de extremidade do Azure chamado contoso do perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="b8c7e-113">O segundo comando remove informações de header personalizadas do ponto de extremidade armazenado em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="b8c7e-114">O comando final atualiza o ponto de extremidade no Gerenciador de Tráfego para corresponder ao valor local em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="b8c7e-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8c7e-115">PARAMETERS</span></span>

### <span data-ttu-id="b8c7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c7e-116">-DefaultProfile</span></span>
<span data-ttu-id="b8c7e-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c7e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b8c7e-118">-Name</span></span>
<span data-ttu-id="b8c7e-119">Especifica o nome das informações de header personalizadas a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="b8c7e-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8c7e-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="b8c7e-121">Especifica um objeto **TrafficManagerEndpoint** local.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="b8c7e-122">Este cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="b8c7e-123">Para obter um **objeto TrafficManagerEndpoint,** use o Get-AzTrafficManagerEndpoint ou New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="b8c7e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8c7e-124">-Confirm</span></span>
<span data-ttu-id="b8c7e-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c7e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c7e-126">-WhatIf</span></span>
<span data-ttu-id="b8c7e-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8c7e-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c7e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c7e-129">CommonParameters</span></span>
<span data-ttu-id="b8c7e-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c7e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c7e-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c7e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c7e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8c7e-132">INPUTS</span></span>

### <span data-ttu-id="b8c7e-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8c7e-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="b8c7e-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8c7e-134">OUTPUTS</span></span>

### <span data-ttu-id="b8c7e-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8c7e-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="b8c7e-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8c7e-136">NOTES</span></span>

## <span data-ttu-id="b8c7e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8c7e-137">RELATED LINKS</span></span>

[<span data-ttu-id="b8c7e-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8c7e-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="b8c7e-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b8c7e-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b8c7e-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8c7e-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b8c7e-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8c7e-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
