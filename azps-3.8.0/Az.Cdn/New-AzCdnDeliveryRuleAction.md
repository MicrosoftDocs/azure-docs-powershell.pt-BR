---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942847"
---
# <span data-ttu-id="190f9-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="190f9-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="190f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="190f9-102">SYNOPSIS</span></span>
<span data-ttu-id="190f9-103">Cria uma ação de entrega.</span><span class="sxs-lookup"><span data-stu-id="190f9-103">Creates a delivery action.</span></span>

## <span data-ttu-id="190f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="190f9-104">SYNTAX</span></span>

### <span data-ttu-id="190f9-105">CacheExpirationActionParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="190f9-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="190f9-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="190f9-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="190f9-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="190f9-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="190f9-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="190f9-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="190f9-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="190f9-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="190f9-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="190f9-110">DESCRIPTION</span></span>
<span data-ttu-id="190f9-111">O cmdlet **New-AzCdnDeliveryRule** cria uma regra de entrega para criação de ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="190f9-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="190f9-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="190f9-112">EXAMPLES</span></span>

### <span data-ttu-id="190f9-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="190f9-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="190f9-114">Criar uma regra de entrega simples.</span><span class="sxs-lookup"><span data-stu-id="190f9-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="190f9-115">OS</span><span class="sxs-lookup"><span data-stu-id="190f9-115">PARAMETERS</span></span>

### <span data-ttu-id="190f9-116">-Ação</span><span class="sxs-lookup"><span data-stu-id="190f9-116">-Action</span></span>
<span data-ttu-id="190f9-117">Ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="190f9-117">Action to perform.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="190f9-118">-CacheBehavior</span></span>
<span data-ttu-id="190f9-119">Comportamento de cache da ação</span><span class="sxs-lookup"><span data-stu-id="190f9-119">Caching behavior for the action</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="190f9-120">-CacheDuration</span></span>
<span data-ttu-id="190f9-121">A duração para a qual o conteúdo precisa ser armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="190f9-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="190f9-122">O formato permitido é \[ d. \] hh: mm: SS</span><span class="sxs-lookup"><span data-stu-id="190f9-122">Allowed format is \[d.\]hh:mm:ss</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="190f9-123">-CustomFragment</span></span>
<span data-ttu-id="190f9-124">Fragmento para adicionar à URL de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="190f9-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="190f9-125">Fragmento é a parte da URL que vem após #.</span><span class="sxs-lookup"><span data-stu-id="190f9-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="190f9-126">Não inclua o #.</span><span class="sxs-lookup"><span data-stu-id="190f9-126">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="190f9-127">-CustomHostname</span></span>
<span data-ttu-id="190f9-128">Host para redirecionar.</span><span class="sxs-lookup"><span data-stu-id="190f9-128">Host to redirect.</span></span>
<span data-ttu-id="190f9-129">Deixe em branco para usar o host de entrada como o host de destino.</span><span class="sxs-lookup"><span data-stu-id="190f9-129">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="190f9-130">-CustomPath</span></span>
<span data-ttu-id="190f9-131">O caminho completo para redirecionar.</span><span class="sxs-lookup"><span data-stu-id="190f9-131">The full path to redirect.</span></span>
<span data-ttu-id="190f9-132">O caminho não pode estar vazio e deve começar com/.</span><span class="sxs-lookup"><span data-stu-id="190f9-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="190f9-133">Deixe em branco para usar o caminho de entrada como caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="190f9-133">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="190f9-134">-CustomQueryString</span></span>
<span data-ttu-id="190f9-135">O conjunto de cadeias de caracteres de consulta a serem colocadas na URL de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="190f9-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="190f9-136">Definir esse valor substituiria qualquer cadeia de caracteres de consulta existente; Deixe em branco para preservar a cadeia de caracteres de consulta recebida.</span><span class="sxs-lookup"><span data-stu-id="190f9-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="190f9-137">A cadeia de caracteres de consulta deve estar no \< \> = \< formato de valor chave \> .</span><span class="sxs-lookup"><span data-stu-id="190f9-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="190f9-138">?</span><span class="sxs-lookup"><span data-stu-id="190f9-138">?</span></span> <span data-ttu-id="190f9-139">e & serão adicionados automaticamente para não incluí-los.</span><span class="sxs-lookup"><span data-stu-id="190f9-139">and & will be added automatically so do not include them.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="190f9-140">-DefaultProfile</span></span>
<span data-ttu-id="190f9-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="190f9-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="190f9-142">-Destino</span><span class="sxs-lookup"><span data-stu-id="190f9-142">-Destination</span></span>
<span data-ttu-id="190f9-143">Defina a URL relativa para a qual as solicitações acima serão reescritas.</span><span class="sxs-lookup"><span data-stu-id="190f9-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="190f9-144">-DestinationProtocol</span></span>
<span data-ttu-id="190f9-145">Protocolo a ser usado para o redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="190f9-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="190f9-146">O valor padrão é MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="190f9-146">The default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="190f9-147">-HeaderActionType</span></span>
<span data-ttu-id="190f9-148">Se o cabeçalho de solicitação ou o cabeçalho de resposta devem ser modificados</span><span class="sxs-lookup"><span data-stu-id="190f9-148">Whether to modify request header or response header</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="190f9-149">-HeaderName</span></span>
<span data-ttu-id="190f9-150">Nome do cabeçalho a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="190f9-150">Name of the header to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="190f9-151">-PreservePath</span></span>
<span data-ttu-id="190f9-152">Se você deseja preservar o caminho não coincidente.</span><span class="sxs-lookup"><span data-stu-id="190f9-152">Whether to preserve unmatched path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="190f9-153">-QueryParameter</span></span>
<span data-ttu-id="190f9-154">Parâmetros de consulta para incluir ou excluir (separado por vírgulas).</span><span class="sxs-lookup"><span data-stu-id="190f9-154">Query parameters to include or exclude (comma separated).</span></span>

```yaml
Type: System.String[]
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="190f9-155">-QueryStringBehavior</span></span>
<span data-ttu-id="190f9-156">Comportamento de QueryString para as solicitações</span><span class="sxs-lookup"><span data-stu-id="190f9-156">QueryString behavior for the requests</span></span>

```yaml
Type: System.String
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-157">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="190f9-157">-RedirectType</span></span>
<span data-ttu-id="190f9-158">O tipo de redirecionamento que a regra usará ao redirecionar o tráfego</span><span class="sxs-lookup"><span data-stu-id="190f9-158">The redirect type the rule will use when redirecting traffic</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="190f9-159">-SourcePattern</span></span>
<span data-ttu-id="190f9-160">Defina um padrão de URI de solicitação que identifique o tipo de solicitação que pode ser regravada.</span><span class="sxs-lookup"><span data-stu-id="190f9-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="190f9-161">Se value estiver em branco, todas as cadeias de caracteres serão combinadas.</span><span class="sxs-lookup"><span data-stu-id="190f9-161">If value is blank, all strings are matched.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-162">-Valor</span><span class="sxs-lookup"><span data-stu-id="190f9-162">-Value</span></span>
<span data-ttu-id="190f9-163">Valor da ação especificada.</span><span class="sxs-lookup"><span data-stu-id="190f9-163">Value for the specified action.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f9-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="190f9-164">CommonParameters</span></span>
<span data-ttu-id="190f9-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="190f9-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="190f9-166">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="190f9-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="190f9-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="190f9-167">INPUTS</span></span>

### <span data-ttu-id="190f9-168">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="190f9-168">None</span></span>

## <span data-ttu-id="190f9-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="190f9-169">OUTPUTS</span></span>

### <span data-ttu-id="190f9-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="190f9-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="190f9-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="190f9-171">NOTES</span></span>

## <span data-ttu-id="190f9-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="190f9-172">RELATED LINKS</span></span>
