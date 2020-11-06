---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 62a4859b5a64003956a4975411f809176f2917e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432056"
---
# <span data-ttu-id="41795-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="41795-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="41795-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41795-102">SYNOPSIS</span></span>
<span data-ttu-id="41795-103">Cria um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="41795-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41795-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41795-104">SYNTAX</span></span>

### <span data-ttu-id="41795-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="41795-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41795-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41795-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41795-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41795-107">DESCRIPTION</span></span>
<span data-ttu-id="41795-108">O cmdlet **New-AzureRmCdnEndpoint** cria um ponto de extremidade de CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="41795-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="41795-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41795-109">EXAMPLES</span></span>

## <span data-ttu-id="41795-110">OS</span><span class="sxs-lookup"><span data-stu-id="41795-110">PARAMETERS</span></span>

### <span data-ttu-id="41795-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="41795-111">-CdnProfile</span></span>
<span data-ttu-id="41795-112">Especifica o objeto de perfil CDN ao qual o ponto de extremidade é adicionado.</span><span class="sxs-lookup"><span data-stu-id="41795-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="41795-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="41795-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="41795-114">Especifica uma matriz de tipos de conteúdo a serem compactados do nó de borda ao cliente.</span><span class="sxs-lookup"><span data-stu-id="41795-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="41795-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41795-115">-DefaultProfile</span></span>
<span data-ttu-id="41795-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="41795-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41795-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="41795-117">-DeliveryPolicy</span></span>
<span data-ttu-id="41795-118">A política de entrega para este ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="41795-118">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="41795-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="41795-119">-EndpointName</span></span>
<span data-ttu-id="41795-120">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="41795-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="41795-121">-Filtros geográficos</span><span class="sxs-lookup"><span data-stu-id="41795-121">-GeoFilters</span></span>
<span data-ttu-id="41795-122">A lista de filtros geográficos que se aplicam a esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="41795-122">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="41795-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="41795-123">-HttpPort</span></span>
<span data-ttu-id="41795-124">Especifica o número da porta HTTP no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="41795-124">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="41795-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="41795-125">-HttpsPort</span></span>
<span data-ttu-id="41795-126">Especifica o número da porta HTTPS no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="41795-126">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="41795-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="41795-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="41795-128">Indica se a compactação está habilitada para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="41795-128">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="41795-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="41795-129">-IsHttpAllowed</span></span>
<span data-ttu-id="41795-130">Indica se o ponto de extremidade permite tráfego HTTP.</span><span class="sxs-lookup"><span data-stu-id="41795-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="41795-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="41795-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="41795-132">Indica se o ponto de extremidade permite tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="41795-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="41795-133">-Local</span><span class="sxs-lookup"><span data-stu-id="41795-133">-Location</span></span>
<span data-ttu-id="41795-134">Especifica o local do recurso do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="41795-134">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="41795-135">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="41795-135">-OptimizationType</span></span>
<span data-ttu-id="41795-136">Especifica qualquer otimização que este ponto de extremidade tem.</span><span class="sxs-lookup"><span data-stu-id="41795-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="41795-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="41795-137">-OriginHostHeader</span></span>
<span data-ttu-id="41795-138">Especifica o cabeçalho do host de origem do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="41795-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="41795-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="41795-139">-OriginHostName</span></span>
<span data-ttu-id="41795-140">Especifica o nome do host do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="41795-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="41795-141">-Originname</span><span class="sxs-lookup"><span data-stu-id="41795-141">-OriginName</span></span>
<span data-ttu-id="41795-142">Especifica o nome do recurso do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="41795-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="41795-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="41795-143">-OriginPath</span></span>
<span data-ttu-id="41795-144">Especifica o caminho do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="41795-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="41795-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="41795-145">-ProbePath</span></span>
<span data-ttu-id="41795-146">Especifica o caminho de sondagem para a aceleração dinâmica do site</span><span class="sxs-lookup"><span data-stu-id="41795-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="41795-147">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="41795-147">-ProfileName</span></span>
<span data-ttu-id="41795-148">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="41795-148">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="41795-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="41795-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="41795-150">Especifica o comportamento do ponto de extremidade CDN quando uma cadeia de consulta está na URL de solicitação.</span><span class="sxs-lookup"><span data-stu-id="41795-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="41795-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41795-151">-ResourceGroupName</span></span>
<span data-ttu-id="41795-152">Especifica o nome do grupo de recursos ao qual este ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="41795-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="41795-153">-Marca</span><span class="sxs-lookup"><span data-stu-id="41795-153">-Tag</span></span>
<span data-ttu-id="41795-154">As marcas a serem associadas ao ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="41795-154">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="41795-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41795-155">-Confirm</span></span>
<span data-ttu-id="41795-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41795-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41795-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41795-157">-WhatIf</span></span>
<span data-ttu-id="41795-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41795-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41795-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41795-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41795-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41795-160">CommonParameters</span></span>
<span data-ttu-id="41795-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41795-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41795-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41795-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41795-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41795-163">INPUTS</span></span>

### <span data-ttu-id="41795-164">Microsoft. Azure. Commands. cdn. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="41795-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="41795-165">Parâmetros: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="41795-165">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="41795-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41795-166">OUTPUTS</span></span>

### <span data-ttu-id="41795-167">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="41795-167">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="41795-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41795-168">NOTES</span></span>

## <span data-ttu-id="41795-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41795-169">RELATED LINKS</span></span>

[<span data-ttu-id="41795-170">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="41795-170">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="41795-171">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="41795-171">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="41795-172">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="41795-172">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="41795-173">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="41795-173">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="41795-174">Parar-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="41795-174">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


