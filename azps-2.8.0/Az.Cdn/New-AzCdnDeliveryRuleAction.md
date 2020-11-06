---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: a1ebadb47bbde091ca6b430fab86111b35bf34bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597587"
---
# <span data-ttu-id="a5329-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="a5329-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="a5329-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5329-102">SYNOPSIS</span></span>
<span data-ttu-id="a5329-103">Cria uma ação de entrega.</span><span class="sxs-lookup"><span data-stu-id="a5329-103">Creates a delivery action.</span></span>

## <span data-ttu-id="a5329-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5329-104">SYNTAX</span></span>

### <span data-ttu-id="a5329-105">CacheExpirationActionParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a5329-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5329-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5329-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5329-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5329-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5329-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5329-108">DESCRIPTION</span></span>
<span data-ttu-id="a5329-109">O cmdlet **New-AzCdnDeliveryRule** cria uma regra de entrega para criação de ponto de extremidade CDN.</span><span class="sxs-lookup"><span data-stu-id="a5329-109">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="a5329-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5329-110">EXAMPLES</span></span>

### <span data-ttu-id="a5329-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5329-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="a5329-112">Criar uma regra de entrega simples.</span><span class="sxs-lookup"><span data-stu-id="a5329-112">Create a simple delivery rule.</span></span>

## <span data-ttu-id="a5329-113">OS</span><span class="sxs-lookup"><span data-stu-id="a5329-113">PARAMETERS</span></span>

### <span data-ttu-id="a5329-114">-Ação</span><span class="sxs-lookup"><span data-stu-id="a5329-114">-Action</span></span>
<span data-ttu-id="a5329-115">Ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="a5329-115">Action to perform.</span></span>

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

### <span data-ttu-id="a5329-116">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="a5329-116">-CacheBehavior</span></span>
<span data-ttu-id="a5329-117">Comportamento de cache da ação</span><span class="sxs-lookup"><span data-stu-id="a5329-117">Caching behavior for the action</span></span>

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

### <span data-ttu-id="a5329-118">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="a5329-118">-CacheDuration</span></span>
<span data-ttu-id="a5329-119">A duração para a qual o conteúdo precisa ser armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="a5329-119">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="a5329-120">O formato permitido é \[ d. \] hh: mm: SS</span><span class="sxs-lookup"><span data-stu-id="a5329-120">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="a5329-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="a5329-121">-CustomFragment</span></span>
<span data-ttu-id="a5329-122">Fragmento para adicionar à URL de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="a5329-122">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="a5329-123">Fragmento é a parte da URL que vem após #.</span><span class="sxs-lookup"><span data-stu-id="a5329-123">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="a5329-124">Não inclua o #.</span><span class="sxs-lookup"><span data-stu-id="a5329-124">Do not include the #.</span></span>

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

### <span data-ttu-id="a5329-125">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="a5329-125">-CustomHostname</span></span>
<span data-ttu-id="a5329-126">Host para redirecionar.</span><span class="sxs-lookup"><span data-stu-id="a5329-126">Host to redirect.</span></span>
<span data-ttu-id="a5329-127">Deixe em branco para usar o host de entrada como o host de destino.</span><span class="sxs-lookup"><span data-stu-id="a5329-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="a5329-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="a5329-128">-CustomPath</span></span>
<span data-ttu-id="a5329-129">O caminho completo para redirecionar.</span><span class="sxs-lookup"><span data-stu-id="a5329-129">The full path to redirect.</span></span>
<span data-ttu-id="a5329-130">O caminho não pode estar vazio e deve começar com/.</span><span class="sxs-lookup"><span data-stu-id="a5329-130">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="a5329-131">Deixe em branco para usar o caminho de entrada como caminho de destino.</span><span class="sxs-lookup"><span data-stu-id="a5329-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="a5329-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="a5329-132">-CustomQueryString</span></span>
<span data-ttu-id="a5329-133">O conjunto de cadeias de caracteres de consulta a serem colocadas na URL de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="a5329-133">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="a5329-134">Definir esse valor substituiria qualquer cadeia de caracteres de consulta existente; Deixe em branco para preservar a cadeia de caracteres de consulta recebida.</span><span class="sxs-lookup"><span data-stu-id="a5329-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="a5329-135">A cadeia de caracteres de consulta deve estar no \< \> = \< formato de valor chave \> .</span><span class="sxs-lookup"><span data-stu-id="a5329-135">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="a5329-136">?</span><span class="sxs-lookup"><span data-stu-id="a5329-136">?</span></span> <span data-ttu-id="a5329-137">e & serão adicionados automaticamente para não incluí-los.</span><span class="sxs-lookup"><span data-stu-id="a5329-137">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="a5329-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5329-138">-DefaultProfile</span></span>
<span data-ttu-id="a5329-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5329-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5329-140">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="a5329-140">-DestinationProtocol</span></span>
<span data-ttu-id="a5329-141">Protocolo a ser usado para o redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="a5329-141">Protocol to use for the redirect.</span></span>
<span data-ttu-id="a5329-142">O valor padrão é MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="a5329-142">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="a5329-143">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="a5329-143">-HeaderActionType</span></span>
<span data-ttu-id="a5329-144">Se o cabeçalho de solicitação ou o cabeçalho de resposta devem ser modificados</span><span class="sxs-lookup"><span data-stu-id="a5329-144">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="a5329-145">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="a5329-145">-HeaderName</span></span>
<span data-ttu-id="a5329-146">Nome do cabeçalho a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="a5329-146">Name of the header to modify.</span></span>

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

### <span data-ttu-id="a5329-147">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="a5329-147">-RedirectType</span></span>
<span data-ttu-id="a5329-148">O tipo de redirecionamento que a regra usará ao redirecionar o tráfego</span><span class="sxs-lookup"><span data-stu-id="a5329-148">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="a5329-149">-Valor</span><span class="sxs-lookup"><span data-stu-id="a5329-149">-Value</span></span>
<span data-ttu-id="a5329-150">Valor da ação especificada.</span><span class="sxs-lookup"><span data-stu-id="a5329-150">Value for the specified action.</span></span>

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

### <span data-ttu-id="a5329-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5329-151">CommonParameters</span></span>
<span data-ttu-id="a5329-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5329-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5329-153">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5329-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5329-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5329-154">INPUTS</span></span>

### <span data-ttu-id="a5329-155">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a5329-155">None</span></span>

## <span data-ttu-id="a5329-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5329-156">OUTPUTS</span></span>

### <span data-ttu-id="a5329-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="a5329-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="a5329-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5329-158">NOTES</span></span>

## <span data-ttu-id="a5329-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5329-159">RELATED LINKS</span></span>
