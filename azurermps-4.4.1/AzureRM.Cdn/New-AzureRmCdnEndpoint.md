---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 5d2bfdf2bf5f87ccb0213c006de8612b5eaf0730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432657"
---
# <span data-ttu-id="eaaa4-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaaa4-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="eaaa4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eaaa4-102">SYNOPSIS</span></span>
<span data-ttu-id="eaaa4-103">Cria um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaaa4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eaaa4-104">SYNTAX</span></span>

### <span data-ttu-id="eaaa4-105">Conjunto de parâmetros para parâmetros de campos (padrão)</span><span class="sxs-lookup"><span data-stu-id="eaaa4-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaaa4-106">Conjunto de parâmetros para parâmetros de objeto</span><span class="sxs-lookup"><span data-stu-id="eaaa4-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaaa4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eaaa4-107">DESCRIPTION</span></span>
<span data-ttu-id="eaaa4-108">O cmdlet **New-AzureRmCdnEndpoint** cria um ponto de extremidade de CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="eaaa4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eaaa4-109">EXAMPLES</span></span>

## <span data-ttu-id="eaaa4-110">OS</span><span class="sxs-lookup"><span data-stu-id="eaaa4-110">PARAMETERS</span></span>

### <span data-ttu-id="eaaa4-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="eaaa4-111">-CdnProfile</span></span>
<span data-ttu-id="eaaa4-112">Especifica o objeto de perfil CDN ao qual o ponto de extremidade é adicionado.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eaaa4-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="eaaa4-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="eaaa4-114">Especifica uma matriz de tipos de conteúdo a serem compactados do nó de borda ao cliente.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="eaaa4-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="eaaa4-115">-EndpointName</span></span>
<span data-ttu-id="eaaa4-116">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="eaaa4-117">-Filtros geográficos</span><span class="sxs-lookup"><span data-stu-id="eaaa4-117">-GeoFilters</span></span>
<span data-ttu-id="eaaa4-118">A lista de filtros geográficos que se aplicam a esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-118">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="eaaa4-119">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="eaaa4-119">-HttpPort</span></span>
<span data-ttu-id="eaaa4-120">Especifica o número da porta HTTP no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-120">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="eaaa4-121">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="eaaa4-121">-HttpsPort</span></span>
<span data-ttu-id="eaaa4-122">Especifica o número da porta HTTPS no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-122">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="eaaa4-123">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="eaaa4-123">-IsCompressionEnabled</span></span>
<span data-ttu-id="eaaa4-124">Indica se a compactação está habilitada para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-124">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="eaaa4-125">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="eaaa4-125">-IsHttpAllowed</span></span>
<span data-ttu-id="eaaa4-126">Indica se o ponto de extremidade permite tráfego HTTP.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-126">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="eaaa4-127">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="eaaa4-127">-IsHttpsAllowed</span></span>
<span data-ttu-id="eaaa4-128">Indica se o ponto de extremidade permite tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-128">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="eaaa4-129">-Local</span><span class="sxs-lookup"><span data-stu-id="eaaa4-129">-Location</span></span>
<span data-ttu-id="eaaa4-130">Especifica o local do recurso do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-130">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaaa4-131">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="eaaa4-131">-OptimizationType</span></span>
<span data-ttu-id="eaaa4-132">Especifica qualquer otimização que este ponto de extremidade tem.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-132">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="eaaa4-133">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="eaaa4-133">-OriginHostHeader</span></span>
<span data-ttu-id="eaaa4-134">Especifica o cabeçalho do host de origem do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-134">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="eaaa4-135">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="eaaa4-135">-OriginHostName</span></span>
<span data-ttu-id="eaaa4-136">Especifica o nome do host do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-136">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="eaaa4-137">-Originname</span><span class="sxs-lookup"><span data-stu-id="eaaa4-137">-OriginName</span></span>
<span data-ttu-id="eaaa4-138">Especifica o nome do recurso do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-138">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="eaaa4-139">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="eaaa4-139">-OriginPath</span></span>
<span data-ttu-id="eaaa4-140">Especifica o caminho do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-140">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="eaaa4-141">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="eaaa4-141">-ProfileName</span></span>
<span data-ttu-id="eaaa4-142">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-142">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaaa4-143">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="eaaa4-143">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="eaaa4-144">Especifica o comportamento do ponto de extremidade CDN quando uma cadeia de consulta está na URL de solicitação.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-144">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="eaaa4-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaaa4-145">-ResourceGroupName</span></span>
<span data-ttu-id="eaaa4-146">Especifica o nome do grupo de recursos ao qual este ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-146">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaaa4-147">-Marcas</span><span class="sxs-lookup"><span data-stu-id="eaaa4-147">-Tags</span></span>
<span data-ttu-id="eaaa4-148">Especifica uma tabela de hash das marcas que estão associadas a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-148">Specifies a hash table of the tags that associated with this resource.</span></span>

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

### <span data-ttu-id="eaaa4-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eaaa4-149">-Confirm</span></span>
<span data-ttu-id="eaaa4-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaaa4-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaaa4-151">-WhatIf</span></span>
<span data-ttu-id="eaaa4-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaaa4-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaaa4-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaaa4-154">-DefaultProfile</span></span>
<span data-ttu-id="eaaa4-155">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaaa4-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaaa4-156">CommonParameters</span></span>
<span data-ttu-id="eaaa4-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaaa4-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaaa4-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaaa4-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaaa4-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eaaa4-159">INPUTS</span></span>

### <span data-ttu-id="eaaa4-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="eaaa4-160">PSProfile</span></span>
<span data-ttu-id="eaaa4-161">O parâmetro ' CdnProfile ' aceita o valor do tipo ' PSProfile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="eaaa4-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="eaaa4-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eaaa4-162">OUTPUTS</span></span>

### <span data-ttu-id="eaaa4-163">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaaa4-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="eaaa4-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eaaa4-164">NOTES</span></span>

## <span data-ttu-id="eaaa4-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eaaa4-165">RELATED LINKS</span></span>

[<span data-ttu-id="eaaa4-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaaa4-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="eaaa4-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaaa4-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="eaaa4-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaaa4-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="eaaa4-169">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaaa4-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="eaaa4-170">Parar-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eaaa4-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


