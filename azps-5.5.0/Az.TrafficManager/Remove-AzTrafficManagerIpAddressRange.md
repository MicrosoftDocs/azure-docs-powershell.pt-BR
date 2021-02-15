---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: bfeef76b700eb408da89561464bc5457f94cdd4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116275"
---
# <span data-ttu-id="0d51e-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="0d51e-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="0d51e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d51e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d51e-103">Remove um intervalo de endereços ou uma sub-rede de um objeto de ponto de extremidade do Gerenciador de Tráfego local.</span><span class="sxs-lookup"><span data-stu-id="0d51e-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="0d51e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d51e-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d51e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d51e-105">DESCRIPTION</span></span>
<span data-ttu-id="0d51e-106">O cmdlet **Remove-AzTrafficManagerIpAddressRange** remove um intervalo de endereços IP de um objeto local do Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="0d51e-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="0d51e-107">Você pode obter um ponto de extremidade usando os cmdlets New-AzTrafficManagerEndpoint ou Get-AzTrafficManagerEndpoint de extremidade.</span><span class="sxs-lookup"><span data-stu-id="0d51e-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="0d51e-108">Este cmdlet opera no objeto de ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="0d51e-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="0d51e-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d51e-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="0d51e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d51e-110">EXAMPLES</span></span>

### <span data-ttu-id="0d51e-111">Exemplo 1: Remover intervalos de endereços IP de um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="0d51e-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="0d51e-112">O primeiro comando obtém o ponto de extremidade do Azure chamado contoso do perfil contosoProfile no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0d51e-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="0d51e-113">O segundo comando remove um intervalo de endereços IP do ponto de extremidade armazenado no $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0d51e-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="0d51e-114">O comando final atualiza o ponto de extremidade no Gerenciador de Tráfego para corresponder ao valor local no $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0d51e-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="0d51e-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d51e-115">PARAMETERS</span></span>

### <span data-ttu-id="0d51e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d51e-116">-DefaultProfile</span></span>
<span data-ttu-id="0d51e-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0d51e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d51e-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d51e-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="0d51e-119">Especifica um objeto **Local TrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="0d51e-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="0d51e-120">Este cmdlet modifica este objeto local.</span><span class="sxs-lookup"><span data-stu-id="0d51e-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="0d51e-121">Para obter um **objeto TrafficManagerEndpoint,** use o Get-AzTrafficManagerEndpoint ou New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d51e-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="0d51e-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0d51e-122">-Confirm</span></span>
<span data-ttu-id="0d51e-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d51e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d51e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d51e-124">-WhatIf</span></span>
<span data-ttu-id="0d51e-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0d51e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d51e-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d51e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d51e-127">-First</span><span class="sxs-lookup"><span data-stu-id="0d51e-127">-First</span></span>
<span data-ttu-id="0d51e-128">Especifica o primeiro endereço IP no intervalo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="0d51e-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="0d51e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d51e-129">CommonParameters</span></span>
<span data-ttu-id="0d51e-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d51e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d51e-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d51e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d51e-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="0d51e-132">INPUTS</span></span>

### <span data-ttu-id="0d51e-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d51e-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="0d51e-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="0d51e-134">OUTPUTS</span></span>

### <span data-ttu-id="0d51e-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d51e-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="0d51e-136">Notas</span><span class="sxs-lookup"><span data-stu-id="0d51e-136">NOTES</span></span>

## <span data-ttu-id="0d51e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d51e-137">RELATED LINKS</span></span>

[<span data-ttu-id="0d51e-138">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="0d51e-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="0d51e-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0d51e-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0d51e-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d51e-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0d51e-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d51e-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
