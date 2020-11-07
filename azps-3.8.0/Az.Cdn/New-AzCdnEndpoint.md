---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: ba06dcabe874161c9f801841a5be8b0337614799
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942845"
---
# <span data-ttu-id="5777a-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5777a-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="5777a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5777a-102">SYNOPSIS</span></span>
<span data-ttu-id="5777a-103">Cria um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="5777a-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="5777a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5777a-104">SYNTAX</span></span>

### <span data-ttu-id="5777a-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5777a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5777a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5777a-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5777a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5777a-107">DESCRIPTION</span></span>
<span data-ttu-id="5777a-108">O cmdlet **New-AzCdnEndpoint** cria um ponto de extremidade de CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="5777a-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="5777a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5777a-109">EXAMPLES</span></span>

## <span data-ttu-id="5777a-110">OS</span><span class="sxs-lookup"><span data-stu-id="5777a-110">PARAMETERS</span></span>

### <span data-ttu-id="5777a-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5777a-111">-CdnProfile</span></span>
<span data-ttu-id="5777a-112">Especifica o objeto de perfil CDN ao qual o ponto de extremidade é adicionado.</span><span class="sxs-lookup"><span data-stu-id="5777a-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="5777a-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="5777a-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="5777a-114">Especifica uma matriz de tipos de conteúdo a serem compactados do nó de borda ao cliente.</span><span class="sxs-lookup"><span data-stu-id="5777a-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="5777a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5777a-115">-DefaultProfile</span></span>
<span data-ttu-id="5777a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5777a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5777a-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="5777a-117">-DeliveryPolicy</span></span>
<span data-ttu-id="5777a-118">A política de entrega para este ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5777a-118">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="5777a-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5777a-119">-EndpointName</span></span>
<span data-ttu-id="5777a-120">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5777a-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="5777a-121">-Filtros geográficos</span><span class="sxs-lookup"><span data-stu-id="5777a-121">-GeoFilters</span></span>
<span data-ttu-id="5777a-122">A lista de filtros geográficos que se aplicam a esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5777a-122">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="5777a-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="5777a-123">-HttpPort</span></span>
<span data-ttu-id="5777a-124">Especifica o número da porta HTTP no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="5777a-124">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="5777a-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="5777a-125">-HttpsPort</span></span>
<span data-ttu-id="5777a-126">Especifica o número da porta HTTPS no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="5777a-126">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="5777a-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="5777a-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="5777a-128">Indica se a compactação está habilitada para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5777a-128">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="5777a-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="5777a-129">-IsHttpAllowed</span></span>
<span data-ttu-id="5777a-130">Indica se o ponto de extremidade permite tráfego HTTP.</span><span class="sxs-lookup"><span data-stu-id="5777a-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="5777a-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="5777a-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="5777a-132">Indica se o ponto de extremidade permite tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5777a-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="5777a-133">-Local</span><span class="sxs-lookup"><span data-stu-id="5777a-133">-Location</span></span>
<span data-ttu-id="5777a-134">Especifica o local do recurso do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5777a-134">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="5777a-135">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="5777a-135">-OptimizationType</span></span>
<span data-ttu-id="5777a-136">Especifica qualquer otimização que este ponto de extremidade tem.</span><span class="sxs-lookup"><span data-stu-id="5777a-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="5777a-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="5777a-137">-OriginHostHeader</span></span>
<span data-ttu-id="5777a-138">Especifica o cabeçalho do host de origem do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5777a-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="5777a-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="5777a-139">-OriginHostName</span></span>
<span data-ttu-id="5777a-140">Especifica o nome do host do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="5777a-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="5777a-141">-Originname</span><span class="sxs-lookup"><span data-stu-id="5777a-141">-OriginName</span></span>
<span data-ttu-id="5777a-142">Especifica o nome do recurso do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="5777a-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="5777a-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="5777a-143">-OriginPath</span></span>
<span data-ttu-id="5777a-144">Especifica o caminho do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="5777a-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="5777a-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="5777a-145">-ProbePath</span></span>
<span data-ttu-id="5777a-146">Especifica o caminho de sondagem para a aceleração dinâmica do site</span><span class="sxs-lookup"><span data-stu-id="5777a-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="5777a-147">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5777a-147">-ProfileName</span></span>
<span data-ttu-id="5777a-148">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="5777a-148">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="5777a-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="5777a-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="5777a-150">Especifica o comportamento do ponto de extremidade CDN quando uma cadeia de consulta está na URL de solicitação.</span><span class="sxs-lookup"><span data-stu-id="5777a-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="5777a-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5777a-151">-ResourceGroupName</span></span>
<span data-ttu-id="5777a-152">Especifica o nome do grupo de recursos ao qual este ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="5777a-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="5777a-153">-Marca</span><span class="sxs-lookup"><span data-stu-id="5777a-153">-Tag</span></span>
<span data-ttu-id="5777a-154">As marcas a serem associadas ao ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="5777a-154">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="5777a-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5777a-155">-Confirm</span></span>
<span data-ttu-id="5777a-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5777a-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5777a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5777a-157">-WhatIf</span></span>
<span data-ttu-id="5777a-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5777a-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5777a-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5777a-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5777a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5777a-160">CommonParameters</span></span>
<span data-ttu-id="5777a-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5777a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5777a-162">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5777a-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5777a-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5777a-163">INPUTS</span></span>

### <span data-ttu-id="5777a-164">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="5777a-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="5777a-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5777a-165">OUTPUTS</span></span>

### <span data-ttu-id="5777a-166">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5777a-166">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="5777a-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5777a-167">NOTES</span></span>

## <span data-ttu-id="5777a-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5777a-168">RELATED LINKS</span></span>

[<span data-ttu-id="5777a-169">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5777a-169">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="5777a-170">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5777a-170">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="5777a-171">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5777a-171">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="5777a-172">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5777a-172">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="5777a-173">Parar-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5777a-173">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


