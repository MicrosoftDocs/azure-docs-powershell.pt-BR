---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 682c12270608f9c75e86cea742fd411e0eb657a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427650"
---
# <span data-ttu-id="db4ee-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="db4ee-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="db4ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="db4ee-103">Cria um ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="db4ee-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db4ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db4ee-104">SYNTAX</span></span>

### <span data-ttu-id="db4ee-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="db4ee-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db4ee-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db4ee-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db4ee-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db4ee-107">DESCRIPTION</span></span>
<span data-ttu-id="db4ee-108">O cmdlet **New-AzureRmCdnEndpoint** cria um ponto de extremidade de CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="db4ee-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="db4ee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db4ee-109">EXAMPLES</span></span>

## <span data-ttu-id="db4ee-110">OS</span><span class="sxs-lookup"><span data-stu-id="db4ee-110">PARAMETERS</span></span>

### <span data-ttu-id="db4ee-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="db4ee-111">-CdnProfile</span></span>
<span data-ttu-id="db4ee-112">Especifica o objeto de perfil CDN ao qual o ponto de extremidade é adicionado.</span><span class="sxs-lookup"><span data-stu-id="db4ee-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="db4ee-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="db4ee-114">Especifica uma matriz de tipos de conteúdo a serem compactados do nó de borda ao cliente.</span><span class="sxs-lookup"><span data-stu-id="db4ee-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db4ee-115">-DefaultProfile</span></span>
<span data-ttu-id="db4ee-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="db4ee-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db4ee-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="db4ee-117">-EndpointName</span></span>
<span data-ttu-id="db4ee-118">Especifica o nome do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="db4ee-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="db4ee-119">-Filtros geográficos</span><span class="sxs-lookup"><span data-stu-id="db4ee-119">-GeoFilters</span></span>
<span data-ttu-id="db4ee-120">A lista de filtros geográficos que se aplicam a esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="db4ee-120">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="db4ee-121">-HttpPort</span></span>
<span data-ttu-id="db4ee-122">Especifica o número da porta HTTP no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="db4ee-122">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-123">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="db4ee-123">-HttpsPort</span></span>
<span data-ttu-id="db4ee-124">Especifica o número da porta HTTPS no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="db4ee-124">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-125">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="db4ee-125">-IsCompressionEnabled</span></span>
<span data-ttu-id="db4ee-126">Indica se a compactação está habilitada para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="db4ee-126">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-127">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="db4ee-127">-IsHttpAllowed</span></span>
<span data-ttu-id="db4ee-128">Indica se o ponto de extremidade permite tráfego HTTP.</span><span class="sxs-lookup"><span data-stu-id="db4ee-128">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-129">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="db4ee-129">-IsHttpsAllowed</span></span>
<span data-ttu-id="db4ee-130">Indica se o ponto de extremidade permite tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="db4ee-130">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-131">-Local</span><span class="sxs-lookup"><span data-stu-id="db4ee-131">-Location</span></span>
<span data-ttu-id="db4ee-132">Especifica o local do recurso do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="db4ee-132">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-133">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="db4ee-133">-OptimizationType</span></span>
<span data-ttu-id="db4ee-134">Especifica qualquer otimização que este ponto de extremidade tem.</span><span class="sxs-lookup"><span data-stu-id="db4ee-134">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="db4ee-135">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="db4ee-135">-OriginHostHeader</span></span>
<span data-ttu-id="db4ee-136">Especifica o cabeçalho do host de origem do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="db4ee-136">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="db4ee-137">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="db4ee-137">-OriginHostName</span></span>
<span data-ttu-id="db4ee-138">Especifica o nome do host do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="db4ee-138">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="db4ee-139">-Originname</span><span class="sxs-lookup"><span data-stu-id="db4ee-139">-OriginName</span></span>
<span data-ttu-id="db4ee-140">Especifica o nome do recurso do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="db4ee-140">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="db4ee-141">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="db4ee-141">-OriginPath</span></span>
<span data-ttu-id="db4ee-142">Especifica o caminho do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="db4ee-142">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="db4ee-143">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="db4ee-143">-ProfileName</span></span>
<span data-ttu-id="db4ee-144">Especifica o nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="db4ee-144">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-145">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="db4ee-145">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="db4ee-146">Especifica o comportamento do ponto de extremidade CDN quando uma cadeia de consulta está na URL de solicitação.</span><span class="sxs-lookup"><span data-stu-id="db4ee-146">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: PSQueryStringCachingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db4ee-147">-ResourceGroupName</span></span>
<span data-ttu-id="db4ee-148">Especifica o nome do grupo de recursos ao qual este ponto de extremidade pertence.</span><span class="sxs-lookup"><span data-stu-id="db4ee-148">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-149">-Marca</span><span class="sxs-lookup"><span data-stu-id="db4ee-149">-Tag</span></span>
<span data-ttu-id="db4ee-150">As marcas a serem associadas ao ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="db4ee-150">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db4ee-151">-Confirm</span></span>
<span data-ttu-id="db4ee-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db4ee-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db4ee-153">-WhatIf</span></span>
<span data-ttu-id="db4ee-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db4ee-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db4ee-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db4ee-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4ee-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4ee-156">CommonParameters</span></span>
<span data-ttu-id="db4ee-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db4ee-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4ee-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db4ee-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4ee-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db4ee-159">INPUTS</span></span>

### <span data-ttu-id="db4ee-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="db4ee-160">PSProfile</span></span>
<span data-ttu-id="db4ee-161">O parâmetro ' CdnProfile ' aceita o valor do tipo ' PSProfile ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="db4ee-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="db4ee-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db4ee-162">OUTPUTS</span></span>

### <span data-ttu-id="db4ee-163">Microsoft. Azure. Commands. cdn. Models. EndPoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="db4ee-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="db4ee-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db4ee-164">NOTES</span></span>

## <span data-ttu-id="db4ee-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db4ee-165">RELATED LINKS</span></span>

[<span data-ttu-id="db4ee-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="db4ee-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="db4ee-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="db4ee-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="db4ee-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="db4ee-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="db4ee-169">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="db4ee-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="db4ee-170">Parar-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="db4ee-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


