---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 5bb661dbc5a65b9a245fcfa35cdc194bbcded1eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427101"
---
# <span data-ttu-id="e28f4-101">Remove-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="e28f4-101">Remove-AzureRmTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="e28f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e28f4-102">SYNOPSIS</span></span>
<span data-ttu-id="e28f4-103">Remove uma sub-rede ou um intervalo de endereços de um objeto de ponto de extremidade do Gerenciador de tráfego local.</span><span class="sxs-lookup"><span data-stu-id="e28f4-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e28f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e28f4-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e28f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e28f4-105">DESCRIPTION</span></span>
<span data-ttu-id="e28f4-106">O cmdlet **Remove-AzureRmTrafficManagerIpAddressRange** remove um intervalo de endereços IP de um objeto de ponto de extremidade do Azure Traffic Manager local.</span><span class="sxs-lookup"><span data-stu-id="e28f4-106">The **Remove-AzureRmTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="e28f4-107">Você pode obter um ponto de extremidade usando os cmdlets New-AzureRmTrafficManagerEndpoint ou Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e28f4-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="e28f4-108">Este cmdlet opera no objeto ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="e28f4-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="e28f4-109">Confirme as alterações no ponto de extremidade do Gerenciador de tráfego usando o cmdlet Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e28f4-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="e28f4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e28f4-110">EXAMPLES</span></span>

### <span data-ttu-id="e28f4-111">Exemplo 1: remover intervalos de endereços IP de um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="e28f4-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="e28f4-112">O primeiro comando obtém o ponto de extremidade do Azure chamado contoso do perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e28f4-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="e28f4-113">O segundo comando Remove um intervalo de endereços IP do ponto de extremidade armazenado no $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e28f4-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="e28f4-114">O comando final atualiza o ponto de extremidade no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e28f4-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="e28f4-115">OS</span><span class="sxs-lookup"><span data-stu-id="e28f4-115">PARAMETERS</span></span>

### <span data-ttu-id="e28f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e28f4-116">-DefaultProfile</span></span>
<span data-ttu-id="e28f4-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e28f4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e28f4-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e28f4-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e28f4-119">Especifica um objeto **TrafficManagerEndpoint** local.</span><span class="sxs-lookup"><span data-stu-id="e28f4-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="e28f4-120">Esse cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="e28f4-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e28f4-121">Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzureRmTrafficManagerEndpoint ou New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e28f4-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="e28f4-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e28f4-122">-Confirm</span></span>
<span data-ttu-id="e28f4-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e28f4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e28f4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e28f4-124">-WhatIf</span></span>
<span data-ttu-id="e28f4-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e28f4-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e28f4-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e28f4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e28f4-127">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="e28f4-127">-First</span></span>
<span data-ttu-id="e28f4-128">Especifica o primeiro endereço IP do intervalo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e28f4-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="e28f4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e28f4-129">CommonParameters</span></span>
<span data-ttu-id="e28f4-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e28f4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e28f4-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e28f4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e28f4-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e28f4-132">INPUTS</span></span>

### <span data-ttu-id="e28f4-133">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e28f4-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="e28f4-134">Este cmdlet aceita um objeto **TrafficManagerEndpoint** para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e28f4-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="e28f4-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e28f4-135">OUTPUTS</span></span>

### <span data-ttu-id="e28f4-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e28f4-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="e28f4-137">Esse cmdlet retorna um objeto TrafficManagerEndpoint modificado.</span><span class="sxs-lookup"><span data-stu-id="e28f4-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="e28f4-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e28f4-138">NOTES</span></span>

## <span data-ttu-id="e28f4-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e28f4-139">RELATED LINKS</span></span>

[<span data-ttu-id="e28f4-140">Add-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="e28f4-140">Add-AzureRmTrafficManagerIpAddressRange</span></span>](./Add-AzureRmTrafficManagerIpAddressRange.md)

[<span data-ttu-id="e28f4-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e28f4-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e28f4-142">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e28f4-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e28f4-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e28f4-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
