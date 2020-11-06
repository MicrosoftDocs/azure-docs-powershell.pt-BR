---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 6117bbae035653762d99096eb8735885c0554d0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603201"
---
# <span data-ttu-id="06580-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06580-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="06580-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06580-102">SYNOPSIS</span></span>
<span data-ttu-id="06580-103">Cria um ponto de extremidade em um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="06580-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06580-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06580-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06580-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06580-105">DESCRIPTION</span></span>
<span data-ttu-id="06580-106">O cmdlet **New-AzureRmTrafficManagerEndpoint** cria um ponto de extremidade em um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="06580-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="06580-107">Esse cmdlet confirma cada novo ponto de extremidade para o serviço do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="06580-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="06580-108">Para adicionar vários pontos de extremidade a um objeto de perfil do Gerenciador de tráfego local e confirmar as alterações em uma única operação, use o cmdlet Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="06580-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="06580-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06580-109">EXAMPLES</span></span>

### <span data-ttu-id="06580-110">Exemplo 1: criar um ponto de extremidade externo para um perfil</span><span class="sxs-lookup"><span data-stu-id="06580-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="06580-111">Esse comando cria um ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="06580-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="06580-112">Exemplo 2: criar um ponto de extremidade do Azure para um perfil</span><span class="sxs-lookup"><span data-stu-id="06580-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="06580-113">Esse comando cria um ponto de extremidade do Azure chamado contoso no perfil chamado ContosoProfile na ResouceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06580-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="06580-114">O ponto de extremidade do Azure aponta para o aplicativo Web do Azure cuja ID do Gerenciador de recursos do Azure é fornecida pelo caminho de URI no *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="06580-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="06580-115">O comando não especifica o parâmetro *EndpointLocation* porque o recurso do aplicativo Web fornece o local.</span><span class="sxs-lookup"><span data-stu-id="06580-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="06580-116">OS</span><span class="sxs-lookup"><span data-stu-id="06580-116">PARAMETERS</span></span>

### <span data-ttu-id="06580-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06580-117">-DefaultProfile</span></span>
<span data-ttu-id="06580-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06580-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06580-119">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="06580-119">-EndpointLocation</span></span>
<span data-ttu-id="06580-120">Especifica o local do ponto de extremidade a ser usado no método de roteamento de tráfego de desempenho.</span><span class="sxs-lookup"><span data-stu-id="06580-120">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="06580-121">Esse parâmetro é aplicável somente a pontos de extremidade do tipo ExternalEndpoints ou NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="06580-121">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="06580-122">Você deve especificar esse parâmetro quando o método de roteamento de tráfego de desempenho for usado.</span><span class="sxs-lookup"><span data-stu-id="06580-122">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="06580-123">Especifique um nome de região do Azure.</span><span class="sxs-lookup"><span data-stu-id="06580-123">Specify an Azure region name.</span></span>
<span data-ttu-id="06580-124">Para obter uma lista completa de regiões do Azure, consulte regiões do Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="06580-124">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06580-125">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="06580-125">-EndpointStatus</span></span>
<span data-ttu-id="06580-126">Especifica o status do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06580-126">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="06580-127">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="06580-127">Valid values are:</span></span> 

- <span data-ttu-id="06580-128">Possibilita</span><span class="sxs-lookup"><span data-stu-id="06580-128">Enabled</span></span> 
- <span data-ttu-id="06580-129">Ativo</span><span class="sxs-lookup"><span data-stu-id="06580-129">Disabled</span></span> 

<span data-ttu-id="06580-130">Se o status estiver habilitado, o ponto de extremidade será analisado para a integridade do ponto de extremidade e será incluído no método de roteamento de tráfego.</span><span class="sxs-lookup"><span data-stu-id="06580-130">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06580-131">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="06580-131">-GeoMapping</span></span>
<span data-ttu-id="06580-132">A lista de regiões mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego ' geográfico '.</span><span class="sxs-lookup"><span data-stu-id="06580-132">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="06580-133">Consulte a documentação do Gerenciador de tráfego para obter uma lista completa de valores aceitos.</span><span class="sxs-lookup"><span data-stu-id="06580-133">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="06580-134">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="06580-134">-MinChildEndpoints</span></span>
<span data-ttu-id="06580-135">Especifique um nome de região do Azure.</span><span class="sxs-lookup"><span data-stu-id="06580-135">Specify an Azure region name.</span></span>
<span data-ttu-id="06580-136">Para obter uma lista completa de regiões do Azure, consulte regiões do Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="06580-136">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06580-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="06580-137">-Name</span></span>
<span data-ttu-id="06580-138">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="06580-138">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06580-139">-Priority</span><span class="sxs-lookup"><span data-stu-id="06580-139">-Priority</span></span>
<span data-ttu-id="06580-140">Especifica a prioridade que o Gerenciador de tráfego atribui ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06580-140">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="06580-141">Esse parâmetro será usado somente se o perfil do Gerenciador de tráfego estiver configurado com o método para roteamento de tráfego prioritário.</span><span class="sxs-lookup"><span data-stu-id="06580-141">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="06580-142">Os valores válidos são inteiros de 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="06580-142">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="06580-143">Valores inferiores representam prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="06580-143">Lower values represent higher priority.</span></span>

<span data-ttu-id="06580-144">Se você especificar uma prioridade, deverá especificar prioridades em todos os pontos de extremidade do perfil, e nenhum dois pontos de extremidade poderá compartilhar o mesmo valor de prioridade.</span><span class="sxs-lookup"><span data-stu-id="06580-144">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="06580-145">Se você não especificar prioridades, o Gerenciador de tráfego atribuirá valores de prioridade padrão aos pontos de extremidade, começando com um (1), na ordem em que o perfil lista os pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06580-145">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06580-146">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="06580-146">-ProfileName</span></span>
<span data-ttu-id="06580-147">Especifica o nome de um perfil do Gerenciador de tráfego ao qual esse cmdlet adiciona um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06580-147">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="06580-148">Para obter um perfil, use os cmdlets New-AzureRmTrafficManagerProfile ou Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="06580-148">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06580-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06580-149">-ResourceGroupName</span></span>
<span data-ttu-id="06580-150">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06580-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="06580-151">Esse cmdlet cria um ponto de extremidade do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="06580-151">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06580-152">-Destino</span><span class="sxs-lookup"><span data-stu-id="06580-152">-Target</span></span>
<span data-ttu-id="06580-153">Especifica o nome DNS totalmente qualificado do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06580-153">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="06580-154">O Gerenciador de tráfego retorna esse valor em respostas DNS quando direciona o tráfego para esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06580-154">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="06580-155">Especifique esse parâmetro somente para o tipo de ponto de extremidade ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="06580-155">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="06580-156">Para outros tipos de ponto de extremidade, especifique o parâmetro *TargetResourceId* em vez disso.</span><span class="sxs-lookup"><span data-stu-id="06580-156">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06580-157">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="06580-157">-TargetResourceId</span></span>
<span data-ttu-id="06580-158">Especifica a ID do recurso do destino.</span><span class="sxs-lookup"><span data-stu-id="06580-158">Specifies resource ID of the target.</span></span>
<span data-ttu-id="06580-159">Especifique esse parâmetro somente para os tipos de ponto de extremidade AzureEndpoints e NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="06580-159">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="06580-160">Para o tipo de ponto de extremidade ExternalEndpoints, especifique o parâmetro de *destino* em vez disso.</span><span class="sxs-lookup"><span data-stu-id="06580-160">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06580-161">-Digite</span><span class="sxs-lookup"><span data-stu-id="06580-161">-Type</span></span>
<span data-ttu-id="06580-162">Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="06580-162">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="06580-163">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="06580-163">Valid values are:</span></span> 

- <span data-ttu-id="06580-164">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="06580-164">AzureEndpoints</span></span>
- <span data-ttu-id="06580-165">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="06580-165">ExternalEndpoints</span></span>
- <span data-ttu-id="06580-166">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="06580-166">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06580-167">-Weight</span><span class="sxs-lookup"><span data-stu-id="06580-167">-Weight</span></span>
<span data-ttu-id="06580-168">Especifica a espessura que o Gerenciador de tráfego atribui ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="06580-168">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="06580-169">Os valores válidos são inteiros de 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="06580-169">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="06580-170">O valor padrão é um (1).</span><span class="sxs-lookup"><span data-stu-id="06580-170">The default value is one (1).</span></span>
<span data-ttu-id="06580-171">Esse parâmetro será usado somente se o perfil do Gerenciador de tráfego estiver configurado com o método de direcionamento de tráfego ponderado.</span><span class="sxs-lookup"><span data-stu-id="06580-171">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06580-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06580-172">CommonParameters</span></span>
<span data-ttu-id="06580-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06580-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06580-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06580-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06580-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06580-175">INPUTS</span></span>

### <span data-ttu-id="06580-176">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="06580-176">None</span></span>
<span data-ttu-id="06580-177">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="06580-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06580-178">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06580-178">OUTPUTS</span></span>

### <span data-ttu-id="06580-179">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06580-179">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="06580-180">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06580-180">NOTES</span></span>

## <span data-ttu-id="06580-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06580-181">RELATED LINKS</span></span>

[<span data-ttu-id="06580-182">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06580-182">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="06580-183">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06580-183">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="06580-184">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06580-184">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="06580-185">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06580-185">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="06580-186">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06580-186">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="06580-187">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06580-187">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="06580-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06580-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


