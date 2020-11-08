---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 2cececec0610b813bf59a1ef8adac59e1fa8ddb2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115151"
---
# <span data-ttu-id="10116-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="10116-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="10116-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10116-102">SYNOPSIS</span></span>
<span data-ttu-id="10116-103">Adiciona uma sub-rede ou um intervalo de endereços a um objeto de ponto de extremidade do Gerenciador de tráfego local.</span><span class="sxs-lookup"><span data-stu-id="10116-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="10116-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10116-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10116-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10116-105">DESCRIPTION</span></span>
<span data-ttu-id="10116-106">O cmdlet **Add-AzTrafficManagerIpAddressRange** adiciona um intervalo de endereços IP a um objeto de ponto de extremidade do Azure Traffic Manager local.</span><span class="sxs-lookup"><span data-stu-id="10116-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="10116-107">Você pode obter um ponto de extremidade usando os cmdlets New-AzTrafficManagerEndpoint ou Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10116-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="10116-108">Este cmdlet opera no objeto ponto de extremidade local.</span><span class="sxs-lookup"><span data-stu-id="10116-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="10116-109">Confirme as alterações no ponto de extremidade do Gerenciador de tráfego usando o cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10116-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="10116-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10116-110">EXAMPLES</span></span>

### <span data-ttu-id="10116-111">Exemplo 1: Adicionar intervalos de endereços IP a um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="10116-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="10116-112">O primeiro comando cria um ponto de extremidade do Gerenciador de tráfego do Azure usando o cmdlet **New-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="10116-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="10116-113">O comando armazena o ponto de extremidade local na variável $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10116-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="10116-114">O segundo comando adiciona o intervalo de endereços IP 1.2.3.4 a 5.6.7.8 ao ponto de extremidade armazenado em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10116-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="10116-115">O terceiro comando adiciona o intervalo de endereços IP 9.10.11.0 ao 9.10.11.255 ao ponto de extremidade armazenado em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10116-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="10116-116">O quarto comando verifica se o escopo corresponde ao tamanho do intervalo e, em seguida, adiciona o intervalo de endereços IP 12.13.14.0 ao 12.13.14.31 ao ponto de extremidade armazenado em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10116-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="10116-117">O quinto comando adiciona o intervalo de endereços IP 15.16.17.18 ao 15.16.17.18 ao ponto de extremidade armazenado em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10116-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="10116-118">O comando final atualiza o ponto de extremidade no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10116-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="10116-119">OS</span><span class="sxs-lookup"><span data-stu-id="10116-119">PARAMETERS</span></span>

### <span data-ttu-id="10116-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10116-120">-DefaultProfile</span></span>
<span data-ttu-id="10116-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10116-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10116-122">-Último</span><span class="sxs-lookup"><span data-stu-id="10116-122">-Last</span></span>
<span data-ttu-id="10116-123">Especifica o último endereço IP no intervalo a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="10116-123">Specifies the last IP address in the range to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10116-124">-Escopo</span><span class="sxs-lookup"><span data-stu-id="10116-124">-Scope</span></span>
<span data-ttu-id="10116-125">Especifica o escopo do intervalo de endereços IP a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="10116-125">Specifies the scope of the IP address range to be added.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10116-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10116-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="10116-127">Especifica um objeto **TrafficManagerEndpoint** local.</span><span class="sxs-lookup"><span data-stu-id="10116-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="10116-128">Esse cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="10116-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="10116-129">Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzTrafficManagerEndpoint ou New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10116-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="10116-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="10116-130">-Confirm</span></span>
<span data-ttu-id="10116-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10116-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10116-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10116-132">-WhatIf</span></span>
<span data-ttu-id="10116-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10116-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10116-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10116-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10116-135">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="10116-135">-First</span></span>
<span data-ttu-id="10116-136">Especifica o primeiro endereço IP do intervalo a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="10116-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="10116-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10116-137">CommonParameters</span></span>
<span data-ttu-id="10116-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10116-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10116-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10116-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10116-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10116-140">INPUTS</span></span>

### <span data-ttu-id="10116-141">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10116-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="10116-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10116-142">OUTPUTS</span></span>

### <span data-ttu-id="10116-143">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10116-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="10116-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10116-144">NOTES</span></span>

## <span data-ttu-id="10116-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10116-145">RELATED LINKS</span></span>

[<span data-ttu-id="10116-146">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="10116-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="10116-147">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10116-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="10116-148">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10116-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="10116-149">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10116-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
