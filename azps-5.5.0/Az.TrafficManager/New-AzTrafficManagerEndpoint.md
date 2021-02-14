---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115595"
---
# <span data-ttu-id="06042-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06042-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="06042-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06042-102">SYNOPSIS</span></span>
<span data-ttu-id="06042-103">Cria um ponto de extremidade em um perfil do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="06042-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="06042-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06042-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06042-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="06042-105">DESCRIPTION</span></span>
<span data-ttu-id="06042-106">O cmdlet **New-AzTrafficManagerEndpoint** cria um ponto de extremidade em um perfil do Gerenciador de Tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="06042-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="06042-107">Este cmdlet confirma cada novo ponto de extremidade para o serviço gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="06042-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="06042-108">Para adicionar vários pontos de extremidade a um objeto de perfil local do Gerenciador de Tráfego e comprometer as alterações em uma única operação, use o cmdlet Add-AzTrafficManagerEndpointConfig controle.</span><span class="sxs-lookup"><span data-stu-id="06042-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="06042-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="06042-109">EXAMPLES</span></span>

### <span data-ttu-id="06042-110">Exemplo 1: Criar um ponto de extremidade externo para um perfil</span><span class="sxs-lookup"><span data-stu-id="06042-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="06042-111">Esse comando cria um ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="06042-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="06042-112">Exemplo 2: Criar um ponto de extremidade do Azure para um perfil</span><span class="sxs-lookup"><span data-stu-id="06042-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="06042-113">Esse comando cria um ponto de extremidade do Azure chamado contoso no perfil chamado ContosoProfile no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="06042-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="06042-114">O ponto de extremidade do Azure aponta para o Azure Web App cuja ID do Gerenciador de Recursos do Azure é dada pelo caminho do URI no *TargetResourceId.*</span><span class="sxs-lookup"><span data-stu-id="06042-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="06042-115">O comando não especifica o parâmetro *EndpointLocation* porque o recurso do Web App fornece o local.</span><span class="sxs-lookup"><span data-stu-id="06042-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="06042-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06042-116">PARAMETERS</span></span>

### <span data-ttu-id="06042-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="06042-117">-CustomHeader</span></span>
<span data-ttu-id="06042-118">Lista de nomes de cabeça personalizados e pares de valores para solicitações de solicitação de confirmação.</span><span class="sxs-lookup"><span data-stu-id="06042-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="06042-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06042-119">-DefaultProfile</span></span>
<span data-ttu-id="06042-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="06042-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06042-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="06042-121">-EndpointLocation</span></span>
<span data-ttu-id="06042-122">Especifica o local do ponto de extremidade a ser usado no método de roteamento de tráfego de desempenho.</span><span class="sxs-lookup"><span data-stu-id="06042-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="06042-123">Este parâmetro só é aplicável aos pontos de extremidade do tipo ExternalEndpoints ou Aninhados.</span><span class="sxs-lookup"><span data-stu-id="06042-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="06042-124">Você deve especificar esse parâmetro quando o método de roteamento de tráfego de desempenho for usado.</span><span class="sxs-lookup"><span data-stu-id="06042-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="06042-125">Especifique um nome de região do Azure.</span><span class="sxs-lookup"><span data-stu-id="06042-125">Specify an Azure region name.</span></span>
<span data-ttu-id="06042-126">Para ver uma lista completa de regiões do Azure, consulte Regiões do Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="06042-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="06042-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="06042-127">-EndpointStatus</span></span>
<span data-ttu-id="06042-128">Especifica o status do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06042-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="06042-129">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="06042-129">Valid values are:</span></span> 

- <span data-ttu-id="06042-130">Habilitado</span><span class="sxs-lookup"><span data-stu-id="06042-130">Enabled</span></span> 
- <span data-ttu-id="06042-131">Desativado</span><span class="sxs-lookup"><span data-stu-id="06042-131">Disabled</span></span> 

<span data-ttu-id="06042-132">Se o status estiver habilitado, o ponto de extremidade será substituído pela saúde do ponto de extremidade e será incluído no método de roteamento de tráfego.</span><span class="sxs-lookup"><span data-stu-id="06042-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="06042-133">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="06042-133">-GeoMapping</span></span>
<span data-ttu-id="06042-134">A lista de regiões mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego "Geográfico".</span><span class="sxs-lookup"><span data-stu-id="06042-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="06042-135">Consulte a documentação do Gerenciador de Tráfego para ver uma lista completa de valores aceitos.</span><span class="sxs-lookup"><span data-stu-id="06042-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="06042-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="06042-136">-MinChildEndpoints</span></span>
<span data-ttu-id="06042-137">Especifique um nome de região do Azure.</span><span class="sxs-lookup"><span data-stu-id="06042-137">Specify an Azure region name.</span></span>
<span data-ttu-id="06042-138">Para ver uma lista completa de regiões do Azure, consulte Regiões do Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="06042-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="06042-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="06042-139">-Name</span></span>
<span data-ttu-id="06042-140">Especifica o nome do ponto de extremidade do Gerenciador de Tráfego que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="06042-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="06042-141">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="06042-141">-Priority</span></span>
<span data-ttu-id="06042-142">Especifica a prioridade que o Gerenciador de Tráfego atribui ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06042-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="06042-143">Esse parâmetro será usado somente se o perfil do Gerenciador de Tráfego estiver configurado com o método de roteamento de tráfego de prioridade.</span><span class="sxs-lookup"><span data-stu-id="06042-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="06042-144">Os valores válidos são números inteiros de 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="06042-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="06042-145">Valores inferiores representam prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="06042-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="06042-146">Se você especificar uma prioridade, deverá especificar prioridades em todos os pontos de extremidade no perfil e nenhum dois pontos de extremidade poderá compartilhar o mesmo valor de prioridade.</span><span class="sxs-lookup"><span data-stu-id="06042-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="06042-147">Se você não especificar prioridades, o Gerenciador de Tráfego atribuirá valores de prioridade padrão aos pontos de extremidade, começando com um (1), na ordem em que o perfil lista os pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06042-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="06042-148">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="06042-148">-ProfileName</span></span>
<span data-ttu-id="06042-149">Especifica o nome de um perfil do Gerenciador de Tráfego ao qual este cmdlet adiciona um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06042-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="06042-150">Para obter um perfil, use os cmdlets New-AzTrafficManagerProfile ou Get-AzTrafficManagerProfile dados.</span><span class="sxs-lookup"><span data-stu-id="06042-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="06042-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06042-151">-ResourceGroupName</span></span>
<span data-ttu-id="06042-152">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06042-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="06042-153">Esse cmdlet cria um ponto de extremidade do Gerenciador de Tráfego no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="06042-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="06042-154">-Sub-RedeMapping</span><span class="sxs-lookup"><span data-stu-id="06042-154">-SubnetMapping</span></span>
<span data-ttu-id="06042-155">A lista de intervalos de endereços ou sub-redes mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego "Sub-rede".</span><span class="sxs-lookup"><span data-stu-id="06042-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="06042-156">-Destino</span><span class="sxs-lookup"><span data-stu-id="06042-156">-Target</span></span>
<span data-ttu-id="06042-157">Especifica o nome DNS totalmente qualificado do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06042-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="06042-158">O Gerenciador de Tráfego retorna esse valor em respostas DNS quando direciona o tráfego para esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06042-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="06042-159">Especifique esse parâmetro somente para o tipo de ponto de extremidade ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="06042-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="06042-160">Para outros tipos de ponto de extremidade, especifique o parâmetro *TargetResourceId.*</span><span class="sxs-lookup"><span data-stu-id="06042-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="06042-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="06042-161">-TargetResourceId</span></span>
<span data-ttu-id="06042-162">Especifica a ID de recurso do destino.</span><span class="sxs-lookup"><span data-stu-id="06042-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="06042-163">Especifique esse parâmetro somente para os tipos de pontos de extremidade AzureEndpoints e Aninhados.</span><span class="sxs-lookup"><span data-stu-id="06042-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="06042-164">Para o tipo de ponto de extremidade ExternalEndpoints, especifique o *parâmetro* Destino.</span><span class="sxs-lookup"><span data-stu-id="06042-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="06042-165">-Tipo</span><span class="sxs-lookup"><span data-stu-id="06042-165">-Type</span></span>
<span data-ttu-id="06042-166">Especifica o tipo de ponto de extremidade que esse cmdlet adiciona ao perfil do Gerenciador de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="06042-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="06042-167">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="06042-167">Valid values are:</span></span> 

- <span data-ttu-id="06042-168">Pontos do AzureEnd</span><span class="sxs-lookup"><span data-stu-id="06042-168">AzureEndpoints</span></span>
- <span data-ttu-id="06042-169">Pontos Externos</span><span class="sxs-lookup"><span data-stu-id="06042-169">ExternalEndpoints</span></span>
- <span data-ttu-id="06042-170">Pontos Aninhados</span><span class="sxs-lookup"><span data-stu-id="06042-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="06042-171">-Peso</span><span class="sxs-lookup"><span data-stu-id="06042-171">-Weight</span></span>
<span data-ttu-id="06042-172">Especifica a peso que o Gerenciador de Tráfego atribui ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06042-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="06042-173">Os valores válidos são números inteiros de 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="06042-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="06042-174">O valor padrão é um (1).</span><span class="sxs-lookup"><span data-stu-id="06042-174">The default value is one (1).</span></span>
<span data-ttu-id="06042-175">Esse parâmetro será usado somente se o perfil do Gerenciador de Tráfego estiver configurado com o método de roteamento de tráfego ponderado.</span><span class="sxs-lookup"><span data-stu-id="06042-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="06042-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06042-176">CommonParameters</span></span>
<span data-ttu-id="06042-177">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06042-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06042-178">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06042-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06042-179">Entradas</span><span class="sxs-lookup"><span data-stu-id="06042-179">INPUTS</span></span>

### <span data-ttu-id="06042-180">Nenhum</span><span class="sxs-lookup"><span data-stu-id="06042-180">None</span></span>

## <span data-ttu-id="06042-181">Saídas</span><span class="sxs-lookup"><span data-stu-id="06042-181">OUTPUTS</span></span>

### <span data-ttu-id="06042-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06042-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="06042-183">Notas</span><span class="sxs-lookup"><span data-stu-id="06042-183">NOTES</span></span>

## <span data-ttu-id="06042-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06042-184">RELATED LINKS</span></span>

[<span data-ttu-id="06042-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06042-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="06042-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06042-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="06042-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06042-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="06042-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06042-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="06042-189">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06042-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="06042-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06042-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="06042-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06042-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


