---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111185"
---
# <span data-ttu-id="592a0-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="592a0-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="592a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="592a0-102">SYNOPSIS</span></span>
<span data-ttu-id="592a0-103">Cria uma ação de entrega.</span><span class="sxs-lookup"><span data-stu-id="592a0-103">Creates a delivery action.</span></span>

## <span data-ttu-id="592a0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="592a0-104">SYNTAX</span></span>

### <span data-ttu-id="592a0-105">CacheExpirationActionParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="592a0-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="592a0-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="592a0-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="592a0-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="592a0-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="592a0-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="592a0-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="592a0-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="592a0-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="592a0-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="592a0-110">DESCRIPTION</span></span>
<span data-ttu-id="592a0-111">O cmdlet **New-AzCdnDeliveryRule** cria uma regra de entrega para a criação do ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="592a0-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="592a0-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="592a0-112">EXAMPLES</span></span>

### <span data-ttu-id="592a0-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="592a0-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="592a0-114">Crie uma regra de entrega simples.</span><span class="sxs-lookup"><span data-stu-id="592a0-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="592a0-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="592a0-115">PARAMETERS</span></span>

### <span data-ttu-id="592a0-116">-Ação</span><span class="sxs-lookup"><span data-stu-id="592a0-116">-Action</span></span>
<span data-ttu-id="592a0-117">Ação a ser tomada.</span><span class="sxs-lookup"><span data-stu-id="592a0-117">Action to perform.</span></span>

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

### <span data-ttu-id="592a0-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="592a0-118">-CacheBehavior</span></span>
<span data-ttu-id="592a0-119">Comportamento de cache para a ação</span><span class="sxs-lookup"><span data-stu-id="592a0-119">Caching behavior for the action</span></span>

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

### <span data-ttu-id="592a0-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="592a0-120">-CacheDuration</span></span>
<span data-ttu-id="592a0-121">A duração para a qual o conteúdo precisa ser armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="592a0-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="592a0-122">O formato permitido é \[ d. \] hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="592a0-122">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="592a0-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="592a0-123">-CustomFragment</span></span>
<span data-ttu-id="592a0-124">Fragmente para adicionar à URL de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="592a0-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="592a0-125">Fragmentar é a parte da URL que vem depois de #.</span><span class="sxs-lookup"><span data-stu-id="592a0-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="592a0-126">Não inclua o #.</span><span class="sxs-lookup"><span data-stu-id="592a0-126">Do not include the #.</span></span>

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

### <span data-ttu-id="592a0-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="592a0-127">-CustomHostname</span></span>
<span data-ttu-id="592a0-128">Hospede para redirecionar.</span><span class="sxs-lookup"><span data-stu-id="592a0-128">Host to redirect.</span></span>
<span data-ttu-id="592a0-129">Deixe vazia para usar o host de entrada como host de destino.</span><span class="sxs-lookup"><span data-stu-id="592a0-129">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="592a0-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="592a0-130">-CustomPath</span></span>
<span data-ttu-id="592a0-131">O caminho completo para redirecionar.</span><span class="sxs-lookup"><span data-stu-id="592a0-131">The full path to redirect.</span></span>
<span data-ttu-id="592a0-132">O caminho não pode estar vazio e deve começar com /.</span><span class="sxs-lookup"><span data-stu-id="592a0-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="592a0-133">Deixe vazia para usar o caminho de entrada como caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="592a0-133">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="592a0-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="592a0-134">-CustomQueryString</span></span>
<span data-ttu-id="592a0-135">O conjunto de cadeias de caracteres de consulta a ser colocado na URL de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="592a0-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="592a0-136">Definir esse valor substituiria qualquer cadeia de caracteres de consulta existente; deixe vazia para preservar a cadeia de caracteres de consulta de entrada.</span><span class="sxs-lookup"><span data-stu-id="592a0-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="592a0-137">A cadeia de caracteres de consulta deve estar no \<key\> = \<value\> formato.</span><span class="sxs-lookup"><span data-stu-id="592a0-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="592a0-138">?</span><span class="sxs-lookup"><span data-stu-id="592a0-138">?</span></span> <span data-ttu-id="592a0-139">e & serão adicionados automaticamente, portanto, não os inclua.</span><span class="sxs-lookup"><span data-stu-id="592a0-139">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="592a0-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592a0-140">-DefaultProfile</span></span>
<span data-ttu-id="592a0-141">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="592a0-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="592a0-142">-Destino</span><span class="sxs-lookup"><span data-stu-id="592a0-142">-Destination</span></span>
<span data-ttu-id="592a0-143">Defina a URL relativa à qual as solicitações acima serão reescritas.</span><span class="sxs-lookup"><span data-stu-id="592a0-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

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

### <span data-ttu-id="592a0-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="592a0-144">-DestinationProtocol</span></span>
<span data-ttu-id="592a0-145">Protocolo a ser usado para o redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="592a0-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="592a0-146">O valor padrão é MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="592a0-146">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="592a0-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="592a0-147">-HeaderActionType</span></span>
<span data-ttu-id="592a0-148">Se você quer modificar o header de solicitação ou o header de resposta</span><span class="sxs-lookup"><span data-stu-id="592a0-148">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="592a0-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="592a0-149">-HeaderName</span></span>
<span data-ttu-id="592a0-150">Nome do header a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="592a0-150">Name of the header to modify.</span></span>

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

### <span data-ttu-id="592a0-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="592a0-151">-PreservePath</span></span>
<span data-ttu-id="592a0-152">Se você deve preservar o caminho não imparável.</span><span class="sxs-lookup"><span data-stu-id="592a0-152">Whether to preserve unmatched path.</span></span>

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

### <span data-ttu-id="592a0-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="592a0-153">-QueryParameter</span></span>
<span data-ttu-id="592a0-154">Parâmetros de consulta a incluir ou excluir (separados por vírgula).</span><span class="sxs-lookup"><span data-stu-id="592a0-154">Query parameters to include or exclude (comma separated).</span></span>

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

### <span data-ttu-id="592a0-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="592a0-155">-QueryStringBehavior</span></span>
<span data-ttu-id="592a0-156">Comportamento de QueryString para as solicitações</span><span class="sxs-lookup"><span data-stu-id="592a0-156">QueryString behavior for the requests</span></span>

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

### <span data-ttu-id="592a0-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="592a0-157">-RedirectType</span></span>
<span data-ttu-id="592a0-158">O tipo de redirecionamento que a regra usará ao redirecionar o tráfego</span><span class="sxs-lookup"><span data-stu-id="592a0-158">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="592a0-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="592a0-159">-SourcePattern</span></span>
<span data-ttu-id="592a0-160">Defina um padrão de URI de solicitação que identifique o tipo de solicitações que podem ser reescritas.</span><span class="sxs-lookup"><span data-stu-id="592a0-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="592a0-161">Se o valor estiver em branco, todas as cadeias de caracteres serão corresponderes.</span><span class="sxs-lookup"><span data-stu-id="592a0-161">If value is blank, all strings are matched.</span></span>

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

### <span data-ttu-id="592a0-162">-Valor</span><span class="sxs-lookup"><span data-stu-id="592a0-162">-Value</span></span>
<span data-ttu-id="592a0-163">Valor da ação especificada.</span><span class="sxs-lookup"><span data-stu-id="592a0-163">Value for the specified action.</span></span>

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

### <span data-ttu-id="592a0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592a0-164">CommonParameters</span></span>
<span data-ttu-id="592a0-165">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="592a0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592a0-166">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="592a0-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592a0-167">Entradas</span><span class="sxs-lookup"><span data-stu-id="592a0-167">INPUTS</span></span>

### <span data-ttu-id="592a0-168">Nenhum</span><span class="sxs-lookup"><span data-stu-id="592a0-168">None</span></span>

## <span data-ttu-id="592a0-169">Saídas</span><span class="sxs-lookup"><span data-stu-id="592a0-169">OUTPUTS</span></span>

### <span data-ttu-id="592a0-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="592a0-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="592a0-171">Notas</span><span class="sxs-lookup"><span data-stu-id="592a0-171">NOTES</span></span>

## <span data-ttu-id="592a0-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="592a0-172">RELATED LINKS</span></span>
