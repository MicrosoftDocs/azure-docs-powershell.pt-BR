---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116923"
---
# <span data-ttu-id="ff29c-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff29c-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="ff29c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff29c-102">SYNOPSIS</span></span>
<span data-ttu-id="ff29c-103">Cria um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="ff29c-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="ff29c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff29c-104">SYNTAX</span></span>

### <span data-ttu-id="ff29c-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ff29c-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff29c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff29c-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff29c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff29c-107">DESCRIPTION</span></span>
<span data-ttu-id="ff29c-108">O cmdlet **New-AzCdnEndpoint** cria um ponto de extremidade de Rede de Distribuição de Conteúdo (CDN) do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff29c-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="ff29c-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ff29c-109">EXAMPLES</span></span>

## <span data-ttu-id="ff29c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff29c-110">PARAMETERS</span></span>

### <span data-ttu-id="ff29c-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="ff29c-111">-CdnProfile</span></span>
<span data-ttu-id="ff29c-112">Especifica o objeto de perfil cdn ao qual o ponto de extremidade é adicionado.</span><span class="sxs-lookup"><span data-stu-id="ff29c-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="ff29c-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="ff29c-114">Especifica uma matriz de tipos de conteúdo para compactar do nó de borda para o cliente.</span><span class="sxs-lookup"><span data-stu-id="ff29c-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="ff29c-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="ff29c-116">O grupo de origem padrão.</span><span class="sxs-lookup"><span data-stu-id="ff29c-116">The default origin group.</span></span>

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

### <span data-ttu-id="ff29c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff29c-117">-DefaultProfile</span></span>
<span data-ttu-id="ff29c-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ff29c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff29c-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="ff29c-119">-DeliveryPolicy</span></span>
<span data-ttu-id="ff29c-120">A política de entrega deste ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ff29c-120">The delivery policy for this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-121">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="ff29c-121">-EndpointName</span></span>
<span data-ttu-id="ff29c-122">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ff29c-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="ff29c-123">-Filtros GeoFiltros</span><span class="sxs-lookup"><span data-stu-id="ff29c-123">-GeoFilters</span></span>
<span data-ttu-id="ff29c-124">A lista de filtros geográficas que se aplica a esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ff29c-124">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-125">-httpPort</span><span class="sxs-lookup"><span data-stu-id="ff29c-125">-HttpPort</span></span>
<span data-ttu-id="ff29c-126">Especifica o número da porta HTTP no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="ff29c-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="ff29c-127">-httpsPort</span><span class="sxs-lookup"><span data-stu-id="ff29c-127">-HttpsPort</span></span>
<span data-ttu-id="ff29c-128">Especifica o número da porta HTTPS no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="ff29c-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="ff29c-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="ff29c-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="ff29c-130">Indica se a compactação está habilitada para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ff29c-130">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="ff29c-131">-IsHttpAllowed</span></span>
<span data-ttu-id="ff29c-132">Indica se o ponto de extremidade habilita o tráfego HTTP.</span><span class="sxs-lookup"><span data-stu-id="ff29c-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="ff29c-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="ff29c-134">Indica se o ponto de extremidade habilita o tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ff29c-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-135">-Local</span><span class="sxs-lookup"><span data-stu-id="ff29c-135">-Location</span></span>
<span data-ttu-id="ff29c-136">Especifica o local do recurso do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ff29c-136">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="ff29c-137">-OptimizationType</span></span>
<span data-ttu-id="ff29c-138">Especifica qualquer otimização que este ponto de extremidade tenha.</span><span class="sxs-lookup"><span data-stu-id="ff29c-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="ff29c-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="ff29c-139">-OriginGroupName</span></span>
<span data-ttu-id="ff29c-140">O nome do grupo de origem.</span><span class="sxs-lookup"><span data-stu-id="ff29c-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="ff29c-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ff29c-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="ff29c-142">O número de segundos entre problemas de saúde.</span><span class="sxs-lookup"><span data-stu-id="ff29c-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="ff29c-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="ff29c-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="ff29c-144">O caminho em relação à origem usado para determinar a saúde da origem.</span><span class="sxs-lookup"><span data-stu-id="ff29c-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="ff29c-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="ff29c-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="ff29c-146">Protocolo a ser usado para a saúde.</span><span class="sxs-lookup"><span data-stu-id="ff29c-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="ff29c-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="ff29c-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="ff29c-148">O tipo de solicitação de saúde que é feita.</span><span class="sxs-lookup"><span data-stu-id="ff29c-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="ff29c-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="ff29c-149">-OriginHostHeader</span></span>
<span data-ttu-id="ff29c-150">Especifica o chefe de host de origem do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ff29c-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="ff29c-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="ff29c-151">-OriginHostName</span></span>
<span data-ttu-id="ff29c-152">Especifica o nome de host do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="ff29c-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="ff29c-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="ff29c-153">-OriginId</span></span>
<span data-ttu-id="ff29c-154">IDs do grupo de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff29c-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="ff29c-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="ff29c-155">-OriginName</span></span>
<span data-ttu-id="ff29c-156">Especifica o nome do recurso do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="ff29c-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="ff29c-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="ff29c-157">-OriginPath</span></span>
<span data-ttu-id="ff29c-158">Especifica o caminho do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="ff29c-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="ff29c-159">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="ff29c-159">-Priority</span></span>
<span data-ttu-id="ff29c-160">Prioridade de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff29c-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="ff29c-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="ff29c-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="ff29c-162">Uma mensagem personalizada a ser incluída na solicitação de aprovação para se conectar ao Link Particular.</span><span class="sxs-lookup"><span data-stu-id="ff29c-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="ff29c-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="ff29c-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="ff29c-164">Local do link particular de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff29c-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="ff29c-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="ff29c-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="ff29c-166">ID do recurso de link privado de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff29c-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="ff29c-167">-Path</span><span class="sxs-lookup"><span data-stu-id="ff29c-167">-ProbePath</span></span>
<span data-ttu-id="ff29c-168">Especifica o caminho de busca para Aceleração Dinâmica do Site</span><span class="sxs-lookup"><span data-stu-id="ff29c-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="ff29c-169">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ff29c-169">-ProfileName</span></span>
<span data-ttu-id="ff29c-170">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="ff29c-170">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="ff29c-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="ff29c-172">Especifica o comportamento do ponto de extremidade CDN quando uma cadeia de caracteres de consulta está na URL da solicitação.</span><span class="sxs-lookup"><span data-stu-id="ff29c-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSQueryStringCachingBehavior]
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff29c-173">-ResourceGroupName</span></span>
<span data-ttu-id="ff29c-174">Especifica o nome do grupo de recursos ao qual este ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="ff29c-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff29c-175">-Tag</span></span>
<span data-ttu-id="ff29c-176">As marcas a associar ao ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff29c-176">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-177">-Peso</span><span class="sxs-lookup"><span data-stu-id="ff29c-177">-Weight</span></span>
<span data-ttu-id="ff29c-178">Azure CDN origin weight.</span><span class="sxs-lookup"><span data-stu-id="ff29c-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="ff29c-179">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ff29c-179">-Confirm</span></span>
<span data-ttu-id="ff29c-180">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff29c-180">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff29c-181">-WhatIf</span></span>
<span data-ttu-id="ff29c-182">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ff29c-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff29c-183">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff29c-183">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff29c-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff29c-184">CommonParameters</span></span>
<span data-ttu-id="ff29c-185">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff29c-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff29c-186">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff29c-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff29c-187">Entradas</span><span class="sxs-lookup"><span data-stu-id="ff29c-187">INPUTS</span></span>

### <span data-ttu-id="ff29c-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="ff29c-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="ff29c-189">Saídas</span><span class="sxs-lookup"><span data-stu-id="ff29c-189">OUTPUTS</span></span>

### <span data-ttu-id="ff29c-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff29c-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="ff29c-191">Notas</span><span class="sxs-lookup"><span data-stu-id="ff29c-191">NOTES</span></span>

## <span data-ttu-id="ff29c-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff29c-192">RELATED LINKS</span></span>

[<span data-ttu-id="ff29c-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff29c-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="ff29c-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff29c-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="ff29c-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff29c-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="ff29c-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff29c-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="ff29c-197">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff29c-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


