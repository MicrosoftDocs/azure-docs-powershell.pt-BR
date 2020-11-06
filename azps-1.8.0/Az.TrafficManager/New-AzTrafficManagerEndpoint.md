---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 007fb7a309b9dd305f58d2f947d3d2dfc55078e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598402"
---
# <span data-ttu-id="9fbc5-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fbc5-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="9fbc5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fbc5-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbc5-103">Cria um ponto de extremidade em um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="9fbc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fbc5-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fbc5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fbc5-105">DESCRIPTION</span></span>
<span data-ttu-id="9fbc5-106">O cmdlet **New-AzTrafficManagerEndpoint** cria um ponto de extremidade em um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="9fbc5-107">Esse cmdlet confirma cada novo ponto de extremidade para o serviço do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="9fbc5-108">Para adicionar vários pontos de extremidade a um objeto de perfil do Gerenciador de tráfego local e confirmar as alterações em uma única operação, use o cmdlet Add-AzTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="9fbc5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fbc5-109">EXAMPLES</span></span>

### <span data-ttu-id="9fbc5-110">Exemplo 1: criar um ponto de extremidade externo para um perfil</span><span class="sxs-lookup"><span data-stu-id="9fbc5-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="9fbc5-111">Esse comando cria um ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="9fbc5-112">Exemplo 2: criar um ponto de extremidade do Azure para um perfil</span><span class="sxs-lookup"><span data-stu-id="9fbc5-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="9fbc5-113">Esse comando cria um ponto de extremidade do Azure chamado contoso no perfil chamado ContosoProfile na ResouceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="9fbc5-114">O ponto de extremidade do Azure aponta para o aplicativo Web do Azure cuja ID do Gerenciador de recursos do Azure é fornecida pelo caminho de URI no *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="9fbc5-115">O comando não especifica o parâmetro *EndpointLocation* porque o recurso do aplicativo Web fornece o local.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="9fbc5-116">OS</span><span class="sxs-lookup"><span data-stu-id="9fbc5-116">PARAMETERS</span></span>

### <span data-ttu-id="9fbc5-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="9fbc5-117">-CustomHeader</span></span>
<span data-ttu-id="9fbc5-118">Lista de pares de nome e valor do cabeçalho personalizado para solicitações de sondagem.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="9fbc5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbc5-119">-DefaultProfile</span></span>
<span data-ttu-id="9fbc5-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fbc5-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="9fbc5-121">-EndpointLocation</span></span>
<span data-ttu-id="9fbc5-122">Especifica o local do ponto de extremidade a ser usado no método de roteamento de tráfego de desempenho.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="9fbc5-123">Esse parâmetro é aplicável somente a pontos de extremidade do tipo ExternalEndpoints ou NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="9fbc5-124">Você deve especificar esse parâmetro quando o método de roteamento de tráfego de desempenho for usado.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="9fbc5-125">Especifique um nome de região do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-125">Specify an Azure region name.</span></span>
<span data-ttu-id="9fbc5-126">Para obter uma lista completa de regiões do Azure, consulte regiões do Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="9fbc5-126">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="9fbc5-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="9fbc5-127">-EndpointStatus</span></span>
<span data-ttu-id="9fbc5-128">Especifica o status do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="9fbc5-129">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="9fbc5-129">Valid values are:</span></span> 

- <span data-ttu-id="9fbc5-130">Possibilita</span><span class="sxs-lookup"><span data-stu-id="9fbc5-130">Enabled</span></span> 
- <span data-ttu-id="9fbc5-131">Ativo</span><span class="sxs-lookup"><span data-stu-id="9fbc5-131">Disabled</span></span> 

<span data-ttu-id="9fbc5-132">Se o status estiver habilitado, o ponto de extremidade será analisado para a integridade do ponto de extremidade e será incluído no método de roteamento de tráfego.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="9fbc5-133">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="9fbc5-133">-GeoMapping</span></span>
<span data-ttu-id="9fbc5-134">A lista de regiões mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego ' geográfico '.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="9fbc5-135">Consulte a documentação do Gerenciador de tráfego para obter uma lista completa de valores aceitos.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="9fbc5-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="9fbc5-136">-MinChildEndpoints</span></span>
<span data-ttu-id="9fbc5-137">Especifique um nome de região do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-137">Specify an Azure region name.</span></span>
<span data-ttu-id="9fbc5-138">Para obter uma lista completa de regiões do Azure, consulte regiões do Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="9fbc5-138">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="9fbc5-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="9fbc5-139">-Name</span></span>
<span data-ttu-id="9fbc5-140">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9fbc5-141">-Priority</span><span class="sxs-lookup"><span data-stu-id="9fbc5-141">-Priority</span></span>
<span data-ttu-id="9fbc5-142">Especifica a prioridade que o Gerenciador de tráfego atribui ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="9fbc5-143">Esse parâmetro será usado somente se o perfil do Gerenciador de tráfego estiver configurado com o método para roteamento de tráfego prioritário.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="9fbc5-144">Os valores válidos são inteiros de 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="9fbc5-145">Valores inferiores representam prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="9fbc5-146">Se você especificar uma prioridade, deverá especificar prioridades em todos os pontos de extremidade do perfil, e nenhum dois pontos de extremidade poderá compartilhar o mesmo valor de prioridade.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="9fbc5-147">Se você não especificar prioridades, o Gerenciador de tráfego atribuirá valores de prioridade padrão aos pontos de extremidade, começando com um (1), na ordem em que o perfil lista os pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="9fbc5-148">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9fbc5-148">-ProfileName</span></span>
<span data-ttu-id="9fbc5-149">Especifica o nome de um perfil do Gerenciador de tráfego ao qual esse cmdlet adiciona um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="9fbc5-150">Para obter um perfil, use os cmdlets New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="9fbc5-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fbc5-151">-ResourceGroupName</span></span>
<span data-ttu-id="9fbc5-152">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9fbc5-153">Esse cmdlet cria um ponto de extremidade do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9fbc5-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="9fbc5-154">-SubnetMapping</span></span>
<span data-ttu-id="9fbc5-155">A lista de intervalos de endereços ou sub-redes mapeadas para esse ponto de extremidade usando o método de roteamento de tráfego de â € ̃Subnetâ €™.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-155">The list of address ranges or subnets mapped to this endpoint when using the â€˜Subnetâ€™ traffic routing method.</span></span>

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

### <span data-ttu-id="9fbc5-156">-Destino</span><span class="sxs-lookup"><span data-stu-id="9fbc5-156">-Target</span></span>
<span data-ttu-id="9fbc5-157">Especifica o nome DNS totalmente qualificado do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="9fbc5-158">O Gerenciador de tráfego retorna esse valor em respostas DNS quando direciona o tráfego para esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="9fbc5-159">Especifique esse parâmetro somente para o tipo de ponto de extremidade ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="9fbc5-160">Para outros tipos de ponto de extremidade, especifique o parâmetro *TargetResourceId* em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="9fbc5-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9fbc5-161">-TargetResourceId</span></span>
<span data-ttu-id="9fbc5-162">Especifica a ID do recurso do destino.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="9fbc5-163">Especifique esse parâmetro somente para os tipos de ponto de extremidade AzureEndpoints e NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="9fbc5-164">Para o tipo de ponto de extremidade ExternalEndpoints, especifique o parâmetro de *destino* em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="9fbc5-165">-Digite</span><span class="sxs-lookup"><span data-stu-id="9fbc5-165">-Type</span></span>
<span data-ttu-id="9fbc5-166">Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="9fbc5-167">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="9fbc5-167">Valid values are:</span></span> 

- <span data-ttu-id="9fbc5-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="9fbc5-168">AzureEndpoints</span></span>
- <span data-ttu-id="9fbc5-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="9fbc5-169">ExternalEndpoints</span></span>
- <span data-ttu-id="9fbc5-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="9fbc5-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="9fbc5-171">-Weight</span><span class="sxs-lookup"><span data-stu-id="9fbc5-171">-Weight</span></span>
<span data-ttu-id="9fbc5-172">Especifica a espessura que o Gerenciador de tráfego atribui ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="9fbc5-173">Os valores válidos são inteiros de 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="9fbc5-174">O valor padrão é um (1).</span><span class="sxs-lookup"><span data-stu-id="9fbc5-174">The default value is one (1).</span></span>
<span data-ttu-id="9fbc5-175">Esse parâmetro será usado somente se o perfil do Gerenciador de tráfego estiver configurado com o método de direcionamento de tráfego ponderado.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="9fbc5-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbc5-176">CommonParameters</span></span>
<span data-ttu-id="9fbc5-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fbc5-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbc5-178">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fbc5-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbc5-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fbc5-179">INPUTS</span></span>

### <span data-ttu-id="9fbc5-180">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9fbc5-180">None</span></span>

## <span data-ttu-id="9fbc5-181">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fbc5-181">OUTPUTS</span></span>

### <span data-ttu-id="9fbc5-182">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fbc5-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9fbc5-183">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fbc5-183">NOTES</span></span>

## <span data-ttu-id="9fbc5-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fbc5-184">RELATED LINKS</span></span>

[<span data-ttu-id="9fbc5-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fbc5-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9fbc5-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fbc5-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9fbc5-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fbc5-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9fbc5-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9fbc5-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="9fbc5-189">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9fbc5-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="9fbc5-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fbc5-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9fbc5-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9fbc5-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


