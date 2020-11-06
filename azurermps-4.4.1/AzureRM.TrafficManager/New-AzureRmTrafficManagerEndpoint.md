---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 7eaadd8c80fff6491983a3e1d9c750227eba43cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426877"
---
# <span data-ttu-id="dbf7b-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dbf7b-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="dbf7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbf7b-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf7b-103">Cria um ponto de extremidade em um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbf7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbf7b-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbf7b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dbf7b-105">DESCRIPTION</span></span>
<span data-ttu-id="dbf7b-106">O cmdlet **New-AzureRmTrafficManagerEndpoint** cria um ponto de extremidade em um perfil do Gerenciador de tráfego do Azure.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="dbf7b-107">Esse cmdlet confirma cada novo ponto de extremidade para o serviço do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="dbf7b-108">Para adicionar vários pontos de extremidade a um objeto de perfil do Gerenciador de tráfego local e confirmar as alterações em uma única operação, use o cmdlet Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="dbf7b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbf7b-109">EXAMPLES</span></span>

### <span data-ttu-id="dbf7b-110">Exemplo 1: criar um ponto de extremidade externo para um perfil</span><span class="sxs-lookup"><span data-stu-id="dbf7b-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="dbf7b-111">Esse comando cria um ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile no grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="dbf7b-112">Exemplo 2: criar um ponto de extremidade do Azure para um perfil</span><span class="sxs-lookup"><span data-stu-id="dbf7b-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="dbf7b-113">Esse comando cria um ponto de extremidade do Azure chamado contoso no perfil chamado ContosoProfile na ResouceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="dbf7b-114">O ponto de extremidade do Azure aponta para o aplicativo Web do Azure cuja ID do Gerenciador de recursos do Azure é fornecida pelo caminho de URI no *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="dbf7b-115">O comando não especifica o parâmetro *EndpointLocation* porque o recurso do aplicativo Web fornece o local.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="dbf7b-116">OS</span><span class="sxs-lookup"><span data-stu-id="dbf7b-116">PARAMETERS</span></span>

### <span data-ttu-id="dbf7b-117">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="dbf7b-117">-EndpointLocation</span></span>
<span data-ttu-id="dbf7b-118">Especifica o local do ponto de extremidade a ser usado no método de roteamento de tráfego de desempenho.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-118">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="dbf7b-119">Esse parâmetro é aplicável somente a pontos de extremidade do tipo ExternalEndpoints ou NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-119">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="dbf7b-120">Você deve especificar esse parâmetro quando o método de roteamento de tráfego de desempenho for usado.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-120">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="dbf7b-121">Especifique um nome de região do Azure.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-121">Specify an Azure region name.</span></span>
<span data-ttu-id="dbf7b-122">Para obter uma lista completa de regiões do Azure, consulte regiões do Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="dbf7b-122">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="dbf7b-123">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="dbf7b-123">-EndpointStatus</span></span>
<span data-ttu-id="dbf7b-124">Especifica o status do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-124">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="dbf7b-125">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dbf7b-125">Valid values are:</span></span> 

- <span data-ttu-id="dbf7b-126">Possibilita</span><span class="sxs-lookup"><span data-stu-id="dbf7b-126">Enabled</span></span> 
- <span data-ttu-id="dbf7b-127">Ativo</span><span class="sxs-lookup"><span data-stu-id="dbf7b-127">Disabled</span></span> 

<span data-ttu-id="dbf7b-128">Se o status estiver habilitado, o ponto de extremidade será analisado para a integridade do ponto de extremidade e será incluído no método de roteamento de tráfego.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-128">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="dbf7b-129">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="dbf7b-129">-GeoMapping</span></span>
<span data-ttu-id="dbf7b-130">A lista de regiões mapeadas para esse ponto de extremidade ao usar o método de roteamento de tráfego ' geográfico '.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-130">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="dbf7b-131">Consulte a documentação do Gerenciador de tráfego para obter uma lista completa de valores aceitos.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-131">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="dbf7b-132">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="dbf7b-132">-MinChildEndpoints</span></span>
<span data-ttu-id="dbf7b-133">Especifique um nome de região do Azure.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-133">Specify an Azure region name.</span></span>
<span data-ttu-id="dbf7b-134">Para obter uma lista completa de regiões do Azure, consulte regiões do Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="dbf7b-134">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="dbf7b-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbf7b-135">-Name</span></span>
<span data-ttu-id="dbf7b-136">Especifica o nome do ponto de extremidade do Gerenciador de tráfego que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-136">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="dbf7b-137">-Priority</span><span class="sxs-lookup"><span data-stu-id="dbf7b-137">-Priority</span></span>
<span data-ttu-id="dbf7b-138">Especifica a prioridade que o Gerenciador de tráfego atribui ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-138">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="dbf7b-139">Esse parâmetro será usado somente se o perfil do Gerenciador de tráfego estiver configurado com o método para roteamento de tráfego prioritário.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-139">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="dbf7b-140">Os valores válidos são inteiros de 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-140">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="dbf7b-141">Valores inferiores representam prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-141">Lower values represent higher priority.</span></span>

<span data-ttu-id="dbf7b-142">Se você especificar uma prioridade, deverá especificar prioridades em todos os pontos de extremidade do perfil, e nenhum dois pontos de extremidade poderá compartilhar o mesmo valor de prioridade.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-142">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="dbf7b-143">Se você não especificar prioridades, o Gerenciador de tráfego atribuirá valores de prioridade padrão aos pontos de extremidade, começando com um (1), na ordem em que o perfil lista os pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-143">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="dbf7b-144">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="dbf7b-144">-ProfileName</span></span>
<span data-ttu-id="dbf7b-145">Especifica o nome de um perfil do Gerenciador de tráfego ao qual esse cmdlet adiciona um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-145">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="dbf7b-146">Para obter um perfil, use os cmdlets New-AzureRmTrafficManagerProfile ou Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-146">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="dbf7b-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf7b-147">-ResourceGroupName</span></span>
<span data-ttu-id="dbf7b-148">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-148">Specifies the name of a resource group.</span></span>
<span data-ttu-id="dbf7b-149">Esse cmdlet cria um ponto de extremidade do Gerenciador de tráfego no grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-149">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dbf7b-150">-Destino</span><span class="sxs-lookup"><span data-stu-id="dbf7b-150">-Target</span></span>
<span data-ttu-id="dbf7b-151">Especifica o nome DNS totalmente qualificado do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-151">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="dbf7b-152">O Gerenciador de tráfego retorna esse valor em respostas DNS quando direciona o tráfego para esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-152">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="dbf7b-153">Especifique esse parâmetro somente para o tipo de ponto de extremidade ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-153">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="dbf7b-154">Para outros tipos de ponto de extremidade, especifique o parâmetro *TargetResourceId* em vez disso.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-154">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="dbf7b-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="dbf7b-155">-TargetResourceId</span></span>
<span data-ttu-id="dbf7b-156">Especifica a ID do recurso do destino.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-156">Specifies resource ID of the target.</span></span>
<span data-ttu-id="dbf7b-157">Especifique esse parâmetro somente para os tipos de ponto de extremidade AzureEndpoints e NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-157">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="dbf7b-158">Para o tipo de ponto de extremidade ExternalEndpoints, especifique o parâmetro de *destino* em vez disso.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-158">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="dbf7b-159">-Digite</span><span class="sxs-lookup"><span data-stu-id="dbf7b-159">-Type</span></span>
<span data-ttu-id="dbf7b-160">Especifica o tipo de ponto de extremidade que este cmdlet adiciona ao perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-160">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="dbf7b-161">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dbf7b-161">Valid values are:</span></span> 

- <span data-ttu-id="dbf7b-162">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="dbf7b-162">AzureEndpoints</span></span>
- <span data-ttu-id="dbf7b-163">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="dbf7b-163">ExternalEndpoints</span></span>
- <span data-ttu-id="dbf7b-164">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="dbf7b-164">NestedEndpoints</span></span>

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

### <span data-ttu-id="dbf7b-165">-Weight</span><span class="sxs-lookup"><span data-stu-id="dbf7b-165">-Weight</span></span>
<span data-ttu-id="dbf7b-166">Especifica a espessura que o Gerenciador de tráfego atribui ao ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-166">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="dbf7b-167">Os valores válidos são inteiros de 1 a 1000.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-167">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="dbf7b-168">O valor padrão é um (1).</span><span class="sxs-lookup"><span data-stu-id="dbf7b-168">The default value is one (1).</span></span>
<span data-ttu-id="dbf7b-169">Esse parâmetro será usado somente se o perfil do Gerenciador de tráfego estiver configurado com o método de direcionamento de tráfego ponderado.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-169">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="dbf7b-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf7b-170">-DefaultProfile</span></span>
<span data-ttu-id="dbf7b-171">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbf7b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf7b-172">CommonParameters</span></span>
<span data-ttu-id="dbf7b-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf7b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf7b-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbf7b-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf7b-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dbf7b-175">INPUTS</span></span>

## <span data-ttu-id="dbf7b-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dbf7b-176">OUTPUTS</span></span>

### <span data-ttu-id="dbf7b-177">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dbf7b-177">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="dbf7b-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dbf7b-178">NOTES</span></span>

## <span data-ttu-id="dbf7b-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbf7b-179">RELATED LINKS</span></span>

[<span data-ttu-id="dbf7b-180">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dbf7b-180">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="dbf7b-181">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dbf7b-181">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="dbf7b-182">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dbf7b-182">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="dbf7b-183">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dbf7b-183">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="dbf7b-184">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dbf7b-184">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="dbf7b-185">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dbf7b-185">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="dbf7b-186">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dbf7b-186">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

