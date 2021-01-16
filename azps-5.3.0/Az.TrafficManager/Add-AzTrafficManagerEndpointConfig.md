---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271267"
---
# <span data-ttu-id="dc37d-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="dc37d-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="dc37d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc37d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc37d-103">Adiciona um ponto de extremidade a um objeto de perfil do Gerenciador de tráfego local.</span><span class="sxs-lookup"><span data-stu-id="dc37d-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="dc37d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc37d-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc37d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc37d-105">DESCRIPTION</span></span>
<span data-ttu-id="dc37d-106">O cmdlet **Add-AzTrafficManagerEndpointConfig** adiciona um ponto de extremidade a um objeto de perfil do Azure Traffic Manager local.</span><span class="sxs-lookup"><span data-stu-id="dc37d-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="dc37d-107">Você pode obter um perfil usando os cmdlets New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dc37d-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="dc37d-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="dc37d-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="dc37d-109">Confirme as alterações no perfil do Gerenciador de tráfego usando o cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dc37d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="dc37d-110">Para criar um ponto de extremidade e confirmar a alteração em uma única operação, use o cmdlet New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dc37d-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="dc37d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc37d-111">EXAMPLES</span></span>

### <span data-ttu-id="dc37d-112">Exemplo 1: adicionar um ponto de extremidade a um perfil</span><span class="sxs-lookup"><span data-stu-id="dc37d-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="dc37d-113">O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="dc37d-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="dc37d-114">O comando armazena o perfil local na variável $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dc37d-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="dc37d-115">O segundo comando adiciona um ponto de extremidade chamado contoso ao perfil armazenado em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dc37d-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="dc37d-116">O comando inclui dados de configuração para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dc37d-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="dc37d-117">Esse comando altera somente o objeto local.</span><span class="sxs-lookup"><span data-stu-id="dc37d-117">This command changes only the local object.</span></span>

<span data-ttu-id="dc37d-118">O comando final atualiza o perfil do Gerenciador de tráfego no Azure para corresponder ao valor local em $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dc37d-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="dc37d-119">OS</span><span class="sxs-lookup"><span data-stu-id="dc37d-119">PARAMETERS</span></span>

### <span data-ttu-id="dc37d-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="dc37d-120">-CustomHeader</span></span>
<span data-ttu-id="dc37d-121">Lista de pares de nome e valor do cabeçalho personalizado para solicitações de sondagem.</span><span class="sxs-lookup"><span data-stu-id="dc37d-121">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc37d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc37d-122">-DefaultProfile</span></span>
<span data-ttu-id="dc37d-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc37d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc37d-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="dc37d-124">-EndpointLocation</span></span>
<span data-ttu-id="dc37d-125">Especifica o local do ponto de extremidade a ser usado no método de roteamento de tráfego de desempenho.</span><span class="sxs-lookup"><span data-stu-id="dc37d-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="dc37d-126">Esse parâmetro é aplicável somente a pontos de extremidade do tipo ExternalEndpoints ou NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="dc37d-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="dc37d-127">Você deve especificar esse parâmetro quando o método de roteamento de tráfego de desempenho for usado.</span><span class="sxs-lookup"><span data-stu-id="dc37d-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="dc37d-128">Especifique um nome de região do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc37d-128">Specify an Azure region name.</span></span>
<span data-ttu-id="dc37d-129">Para obter uma lista completa de regiões do Azure, consulte regiões do Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="dc37d-129">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="dc37d-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dc37d-130">-EndpointName</span></span>
<span data-ttu-id="dc37d-131">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que o cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="dc37d-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="dc37d-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="dc37d-132">-EndpointStatus</span></span>
<span data-ttu-id="dc37d-133">Especifica o status do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dc37d-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="dc37d-134">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dc37d-134">Valid values are:</span></span> 

- <span data-ttu-id="dc37d-135">Possibilita</span><span class="sxs-lookup"><span data-stu-id="dc37d-135">Enabled</span></span> 
- <span data-ttu-id="dc37d-136">Ativo</span><span class="sxs-lookup"><span data-stu-id="dc37d-136">Disabled</span></span> 

<span data-ttu-id="dc37d-137">Se o status estiver habilitado, o ponto de extremidade será analisado para a integridade do ponto de extremidade e será incluído no método de roteamento de tráfego.</span><span class="sxs-lookup"><span data-stu-id="dc37d-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc37d-138">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="dc37d-138">-GeoMapping</span></span>
<span data-ttu-id="dc37d-139">A lista de regiões mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego ' geográfico '.</span><span class="sxs-lookup"><span data-stu-id="dc37d-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="dc37d-140">Consulte a documentação do Gerenciador de tráfego para obter uma [lista completa de valores aceitos](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span><span class="sxs-lookup"><span data-stu-id="dc37d-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc37d-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="dc37d-141">-MinChildEndpoints</span></span>
<span data-ttu-id="dc37d-142">O número mínimo de pontos de extremidade que devem estar disponíveis no perfil filho para que o ponto de extremidade aninhado no perfil pai seja considerado disponível.</span><span class="sxs-lookup"><span data-stu-id="dc37d-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="dc37d-143">Aplicável somente ao ponto de extremidade do tipo ' NestedEndpoints '.</span><span class="sxs-lookup"><span data-stu-id="dc37d-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc37d-144">-Priority</span><span class="sxs-lookup"><span data-stu-id="dc37d-144">-Priority</span></span>
<span data-ttu-id="dc37d-145">Especifica a prioridade que o Gerenciador de tráfego atribui ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dc37d-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="dc37d-146">Esse parâmetro será usado somente se o perfil do Gerenciador de tráfego estiver configurado com o método para roteamento de tráfego prioritário.</span><span class="sxs-lookup"><span data-stu-id="dc37d-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="dc37d-147">Os valores válidos são inteiros de 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="dc37d-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="dc37d-148">Valores inferiores representam prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="dc37d-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="dc37d-149">Se você especificar uma prioridade, deverá especificar prioridades em todos os pontos de extremidade do perfil, e nenhum dois pontos de extremidade poderá compartilhar o mesmo valor de prioridade.</span><span class="sxs-lookup"><span data-stu-id="dc37d-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="dc37d-150">Se você não especificar prioridades, o Gerenciador de tráfego atribuirá valores de prioridade padrão aos pontos de extremidade, começando com um (1), na ordem em que o perfil lista os pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dc37d-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc37d-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="dc37d-151">-SubnetMapping</span></span>
<span data-ttu-id="dc37d-152">A lista de intervalos de endereços ou sub-redes mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego "sub-rede".</span><span class="sxs-lookup"><span data-stu-id="dc37d-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc37d-153">-Destino</span><span class="sxs-lookup"><span data-stu-id="dc37d-153">-Target</span></span>
<span data-ttu-id="dc37d-154">Especifica o nome DNS totalmente qualificado do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dc37d-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="dc37d-155">O Gerenciador de tráfego retorna esse valor em respostas DNS quando direciona o tráfego para esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dc37d-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="dc37d-156">Especifique esse parâmetro somente para o tipo de ponto de extremidade ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="dc37d-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="dc37d-157">Para outros tipos de ponto de extremidade, especifique o parâmetro *TargetResourceId* em vez disso.</span><span class="sxs-lookup"><span data-stu-id="dc37d-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="dc37d-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="dc37d-158">-TargetResourceId</span></span>
<span data-ttu-id="dc37d-159">Especifica a ID do recurso do destino.</span><span class="sxs-lookup"><span data-stu-id="dc37d-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="dc37d-160">Especifique esse parâmetro somente para os tipos de ponto de extremidade AzureEndpoints e NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="dc37d-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="dc37d-161">Para o tipo de ponto de extremidade ExternalEndpoints, especifique o parâmetro de *destino* em vez disso.</span><span class="sxs-lookup"><span data-stu-id="dc37d-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="dc37d-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dc37d-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="dc37d-163">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="dc37d-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="dc37d-164">Esse cmdlet modifica esse objeto local.</span><span class="sxs-lookup"><span data-stu-id="dc37d-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="dc37d-165">Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dc37d-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc37d-166">-Digite</span><span class="sxs-lookup"><span data-stu-id="dc37d-166">-Type</span></span>
<span data-ttu-id="dc37d-167">Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc37d-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="dc37d-168">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dc37d-168">Valid values are:</span></span> 

- <span data-ttu-id="dc37d-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="dc37d-169">AzureEndpoints</span></span>
- <span data-ttu-id="dc37d-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="dc37d-170">ExternalEndpoints</span></span>
- <span data-ttu-id="dc37d-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="dc37d-171">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc37d-172">-Weight</span><span class="sxs-lookup"><span data-stu-id="dc37d-172">-Weight</span></span>
<span data-ttu-id="dc37d-173">Especifica a espessura que o Gerenciador de tráfego atribui ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dc37d-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="dc37d-174">Os valores válidos são inteiros de 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="dc37d-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="dc37d-175">O valor padrão é um (1).</span><span class="sxs-lookup"><span data-stu-id="dc37d-175">The default value is one (1).</span></span>
<span data-ttu-id="dc37d-176">Esse parâmetro será usado somente se o perfil do Gerenciador de tráfego estiver configurado com o método de direcionamento de tráfego ponderado.</span><span class="sxs-lookup"><span data-stu-id="dc37d-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc37d-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc37d-177">CommonParameters</span></span>
<span data-ttu-id="dc37d-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc37d-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc37d-179">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc37d-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc37d-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc37d-180">INPUTS</span></span>

### <span data-ttu-id="dc37d-181">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dc37d-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="dc37d-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc37d-182">OUTPUTS</span></span>

### <span data-ttu-id="dc37d-183">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dc37d-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="dc37d-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc37d-184">NOTES</span></span>

## <span data-ttu-id="dc37d-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc37d-185">RELATED LINKS</span></span>

[<span data-ttu-id="dc37d-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dc37d-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="dc37d-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dc37d-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="dc37d-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="dc37d-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="dc37d-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dc37d-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


