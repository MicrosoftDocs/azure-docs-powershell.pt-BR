---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 9a1be7c45c507746ae3b8c97f883a61de0da78db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118518"
---
# <span data-ttu-id="e26f9-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="e26f9-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="e26f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e26f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e26f9-103">Adiciona informações de header personalizadas a um objeto de ponto de extremidade do Gerenciador de Tráfego local.</span><span class="sxs-lookup"><span data-stu-id="e26f9-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="e26f9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e26f9-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e26f9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e26f9-105">DESCRIPTION</span></span>
<span data-ttu-id="e26f9-106">O cmdlet **Add-AzTrafficManagerCusagerCustomHeaderToEndpoint** adiciona informações de header personalizadas a um objeto de ponto de extremidade local do Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="e26f9-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="e26f9-107">Você pode obter um ponto de extremidade usando os cmdlets New-AzTrafficManagerEndpoint ou Get-AzTrafficManagerEndpoint de extremidade.</span><span class="sxs-lookup"><span data-stu-id="e26f9-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="e26f9-108">Este cmdlet opera no objeto de ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="e26f9-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="e26f9-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e26f9-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="e26f9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e26f9-110">EXAMPLES</span></span>

### <span data-ttu-id="e26f9-111">Exemplo 1: Adicionar informações personalizadas de um header a um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="e26f9-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="e26f9-112">O primeiro comando cria um ponto de extremidade do Gerenciador de Tráfego do Azure usando o cmdlet **New-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="e26f9-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="e26f9-113">O comando armazena o ponto de extremidade local na variável $TrafficManagerEndpoint local.</span><span class="sxs-lookup"><span data-stu-id="e26f9-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="e26f9-114">O segundo comando adiciona informações personalizadas ao ponto de extremidade armazenado $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e26f9-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="e26f9-115">O comando final atualiza o ponto de extremidade no Gerenciador de Tráfego para corresponder ao valor local no $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e26f9-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="e26f9-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e26f9-116">PARAMETERS</span></span>

### <span data-ttu-id="e26f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26f9-117">-DefaultProfile</span></span>
<span data-ttu-id="e26f9-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e26f9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e26f9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e26f9-119">-Name</span></span>
<span data-ttu-id="e26f9-120">Especifica o nome das informações de header personalizadas a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="e26f9-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="e26f9-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e26f9-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e26f9-122">Especifica um objeto **Local TrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="e26f9-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="e26f9-123">Este cmdlet modifica este objeto local.</span><span class="sxs-lookup"><span data-stu-id="e26f9-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e26f9-124">Para obter um **objeto TrafficManagerEndpoint,** use o Get-AzTrafficManagerEndpoint ou New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e26f9-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="e26f9-125">-Valor</span><span class="sxs-lookup"><span data-stu-id="e26f9-125">-Value</span></span>
<span data-ttu-id="e26f9-126">Especifica o valor das informações de header personalizadas a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="e26f9-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="e26f9-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e26f9-127">-Confirm</span></span>
<span data-ttu-id="e26f9-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e26f9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e26f9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e26f9-129">-WhatIf</span></span>
<span data-ttu-id="e26f9-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e26f9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e26f9-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e26f9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e26f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26f9-132">CommonParameters</span></span>
<span data-ttu-id="e26f9-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e26f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e26f9-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e26f9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26f9-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="e26f9-135">INPUTS</span></span>

### <span data-ttu-id="e26f9-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e26f9-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="e26f9-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="e26f9-137">OUTPUTS</span></span>

### <span data-ttu-id="e26f9-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e26f9-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="e26f9-139">Notas</span><span class="sxs-lookup"><span data-stu-id="e26f9-139">NOTES</span></span>

## <span data-ttu-id="e26f9-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e26f9-140">RELATED LINKS</span></span>

[<span data-ttu-id="e26f9-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="e26f9-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="e26f9-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e26f9-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e26f9-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e26f9-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e26f9-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e26f9-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
