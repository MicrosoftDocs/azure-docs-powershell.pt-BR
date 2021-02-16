---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118513"
---
# <span data-ttu-id="75516-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="75516-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="75516-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75516-102">SYNOPSIS</span></span>
<span data-ttu-id="75516-103">Adiciona um ponto de extremidade a um objeto de perfil local do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="75516-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="75516-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75516-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75516-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="75516-105">DESCRIPTION</span></span>
<span data-ttu-id="75516-106">O **cmdlet Add-AzTrafficManagerEndpointConfig** adiciona um ponto de extremidade a um objeto de perfil local do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="75516-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="75516-107">Você pode obter um perfil usando os cmdlets New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="75516-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="75516-108">Este cmdlet opera no objeto de perfil local.</span><span class="sxs-lookup"><span data-stu-id="75516-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="75516-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75516-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="75516-110">Para criar um ponto de extremidade e comprometer a alteração em uma única operação, use New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75516-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="75516-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="75516-111">EXAMPLES</span></span>

### <span data-ttu-id="75516-112">Exemplo 1: Adicionar um ponto de extremidade a um perfil</span><span class="sxs-lookup"><span data-stu-id="75516-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="75516-113">O primeiro comando obtém um perfil do Gerenciador de Tráfego do Azure usando o cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="75516-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="75516-114">O comando armazena o perfil local na variável $TrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="75516-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="75516-115">O segundo comando adiciona um ponto de extremidade chamado contoso ao perfil armazenado $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="75516-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="75516-116">O comando inclui dados de configuração para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="75516-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="75516-117">Esse comando altera apenas o objeto local.</span><span class="sxs-lookup"><span data-stu-id="75516-117">This command changes only the local object.</span></span>

<span data-ttu-id="75516-118">O comando final atualiza o perfil do Gerenciador de Tráfego no Azure para corresponder ao valor local no $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="75516-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="75516-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75516-119">PARAMETERS</span></span>

### <span data-ttu-id="75516-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="75516-120">-CustomHeader</span></span>
<span data-ttu-id="75516-121">Lista de nomes de cabeça personalizados e pares de valores para solicitações de solicitação de confirmação.</span><span class="sxs-lookup"><span data-stu-id="75516-121">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="75516-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75516-122">-DefaultProfile</span></span>
<span data-ttu-id="75516-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="75516-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75516-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="75516-124">-EndpointLocation</span></span>
<span data-ttu-id="75516-125">Especifica o local do ponto de extremidade a ser usado no método de roteamento de tráfego de desempenho.</span><span class="sxs-lookup"><span data-stu-id="75516-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="75516-126">Este parâmetro só é aplicável aos pontos de extremidade dos Pontos Externos ou do tipo AninhadoEndpoints.</span><span class="sxs-lookup"><span data-stu-id="75516-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="75516-127">Você deve especificar esse parâmetro quando o método de roteamento de tráfego de desempenho for usado.</span><span class="sxs-lookup"><span data-stu-id="75516-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="75516-128">Especifique um nome de região do Azure.</span><span class="sxs-lookup"><span data-stu-id="75516-128">Specify an Azure region name.</span></span>
<span data-ttu-id="75516-129">Para ver uma lista completa de regiões do Azure, consulte Regiões do Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="75516-129">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="75516-130">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="75516-130">-EndpointName</span></span>
<span data-ttu-id="75516-131">Especifica o nome do ponto de extremidade do Gerenciador de Tráfego que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="75516-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="75516-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="75516-132">-EndpointStatus</span></span>
<span data-ttu-id="75516-133">Especifica o status do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="75516-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="75516-134">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="75516-134">Valid values are:</span></span> 

- <span data-ttu-id="75516-135">Habilitado</span><span class="sxs-lookup"><span data-stu-id="75516-135">Enabled</span></span> 
- <span data-ttu-id="75516-136">Desativado</span><span class="sxs-lookup"><span data-stu-id="75516-136">Disabled</span></span> 

<span data-ttu-id="75516-137">Se o status estiver habilitado, o ponto de extremidade será substituído pela saúde do ponto de extremidade e será incluído no método de roteamento de tráfego.</span><span class="sxs-lookup"><span data-stu-id="75516-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="75516-138">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="75516-138">-GeoMapping</span></span>
<span data-ttu-id="75516-139">A lista de regiões mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego "Geográfico".</span><span class="sxs-lookup"><span data-stu-id="75516-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="75516-140">Consulte a documentação do Gerenciador de Tráfego para ver uma [lista completa de valores aceitos.](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)</span><span class="sxs-lookup"><span data-stu-id="75516-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

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

### <span data-ttu-id="75516-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="75516-141">-MinChildEndpoints</span></span>
<span data-ttu-id="75516-142">O número mínimo de pontos de extremidade que devem estar disponíveis no perfil filho para que o Ponto de Extremidade Aninhado no perfil pai seja considerado disponível.</span><span class="sxs-lookup"><span data-stu-id="75516-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="75516-143">Aplicável somente ao ponto de extremidade do tipo "Aninhados".</span><span class="sxs-lookup"><span data-stu-id="75516-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

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

### <span data-ttu-id="75516-144">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="75516-144">-Priority</span></span>
<span data-ttu-id="75516-145">Especifica a prioridade que o Gerenciador de Tráfego atribui ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="75516-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="75516-146">Esse parâmetro será usado somente se o perfil do Gerenciador de Tráfego estiver configurado com o método de roteamento de tráfego de prioridade.</span><span class="sxs-lookup"><span data-stu-id="75516-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="75516-147">Os valores válidos são números inteiros de 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="75516-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="75516-148">Valores inferiores representam prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="75516-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="75516-149">Se você especificar uma prioridade, deverá especificar prioridades em todos os pontos de extremidade no perfil e nenhum dois pontos de extremidade poderá compartilhar o mesmo valor de prioridade.</span><span class="sxs-lookup"><span data-stu-id="75516-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="75516-150">Se você não especificar prioridades, o Gerenciador de Tráfego atribuirá valores de prioridade padrão aos pontos de extremidade, começando com um (1), na ordem em que o perfil lista os pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="75516-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="75516-151">-Sub-RedeMapping</span><span class="sxs-lookup"><span data-stu-id="75516-151">-SubnetMapping</span></span>
<span data-ttu-id="75516-152">A lista de intervalos de endereços ou sub-redes mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego "Sub-rede".</span><span class="sxs-lookup"><span data-stu-id="75516-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="75516-153">-Destino</span><span class="sxs-lookup"><span data-stu-id="75516-153">-Target</span></span>
<span data-ttu-id="75516-154">Especifica o nome DNS totalmente qualificado do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="75516-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="75516-155">O Gerenciador de Tráfego retorna esse valor em respostas DNS quando direciona o tráfego para esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="75516-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="75516-156">Especifique esse parâmetro somente para o tipo de ponto de extremidade ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="75516-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="75516-157">Para outros tipos de ponto de extremidade, especifique o parâmetro *TargetResourceId.*</span><span class="sxs-lookup"><span data-stu-id="75516-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="75516-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="75516-158">-TargetResourceId</span></span>
<span data-ttu-id="75516-159">Especifica a ID de recurso do destino.</span><span class="sxs-lookup"><span data-stu-id="75516-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="75516-160">Especifique esse parâmetro somente para os tipos de pontos de extremidade AzureEndpoints e Aninhados.</span><span class="sxs-lookup"><span data-stu-id="75516-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="75516-161">Para o tipo de ponto de extremidade ExternalEndpoints, especifique o *parâmetro* Destino.</span><span class="sxs-lookup"><span data-stu-id="75516-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="75516-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="75516-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="75516-163">Especifica um objeto **TrafficManagerProfile** local.</span><span class="sxs-lookup"><span data-stu-id="75516-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="75516-164">Este cmdlet modifica este objeto local.</span><span class="sxs-lookup"><span data-stu-id="75516-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="75516-165">Para obter um **objeto TrafficManagerProfile,** use o cmdlet Get-AzTrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="75516-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="75516-166">-Tipo</span><span class="sxs-lookup"><span data-stu-id="75516-166">-Type</span></span>
<span data-ttu-id="75516-167">Especifica o tipo de ponto de extremidade que esse cmdlet adiciona ao perfil do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="75516-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="75516-168">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="75516-168">Valid values are:</span></span> 

- <span data-ttu-id="75516-169">Pontos do AzureEnd</span><span class="sxs-lookup"><span data-stu-id="75516-169">AzureEndpoints</span></span>
- <span data-ttu-id="75516-170">Pontos Externos</span><span class="sxs-lookup"><span data-stu-id="75516-170">ExternalEndpoints</span></span>
- <span data-ttu-id="75516-171">Pontos aninhados</span><span class="sxs-lookup"><span data-stu-id="75516-171">NestedEndpoints</span></span>

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

### <span data-ttu-id="75516-172">-Peso</span><span class="sxs-lookup"><span data-stu-id="75516-172">-Weight</span></span>
<span data-ttu-id="75516-173">Especifica a peso que o Gerenciador de Tráfego atribui ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="75516-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="75516-174">Os valores válidos são números inteiros de 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="75516-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="75516-175">O valor padrão é um (1).</span><span class="sxs-lookup"><span data-stu-id="75516-175">The default value is one (1).</span></span>
<span data-ttu-id="75516-176">Esse parâmetro será usado somente se o perfil do Gerenciador de Tráfego estiver configurado com o método de roteamento de tráfego ponderado.</span><span class="sxs-lookup"><span data-stu-id="75516-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="75516-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75516-177">CommonParameters</span></span>
<span data-ttu-id="75516-178">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75516-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75516-179">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75516-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75516-180">Entradas</span><span class="sxs-lookup"><span data-stu-id="75516-180">INPUTS</span></span>

### <span data-ttu-id="75516-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="75516-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="75516-182">Saídas</span><span class="sxs-lookup"><span data-stu-id="75516-182">OUTPUTS</span></span>

### <span data-ttu-id="75516-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="75516-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="75516-184">Notas</span><span class="sxs-lookup"><span data-stu-id="75516-184">NOTES</span></span>

## <span data-ttu-id="75516-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75516-185">RELATED LINKS</span></span>

[<span data-ttu-id="75516-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="75516-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="75516-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="75516-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="75516-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="75516-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="75516-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="75516-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


