---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: f7dd02a214fa32223e052c1999329699f1c653e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434454"
---
# <span data-ttu-id="cee05-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="cee05-101">Update-AzBotService</span></span>

## <span data-ttu-id="cee05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cee05-102">SYNOPSIS</span></span>
<span data-ttu-id="cee05-103">Atualiza um serviço de bot</span><span class="sxs-lookup"><span data-stu-id="cee05-103">Updates a Bot Service</span></span>

## <span data-ttu-id="cee05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cee05-104">SYNTAX</span></span>

### <span data-ttu-id="cee05-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="cee05-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cee05-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cee05-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cee05-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cee05-107">DESCRIPTION</span></span>
<span data-ttu-id="cee05-108">Atualiza um serviço de bot</span><span class="sxs-lookup"><span data-stu-id="cee05-108">Updates a Bot Service</span></span>

## <span data-ttu-id="cee05-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cee05-109">EXAMPLES</span></span>

### <span data-ttu-id="cee05-110">Exemplo 1: Atualize o bot por nome e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cee05-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="cee05-111">Atualize o bot por nome e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cee05-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="cee05-112">Exemplo 2: Atualize o bot por InputObject</span><span class="sxs-lookup"><span data-stu-id="cee05-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="cee05-113">Atualize o bot por InputObject</span><span class="sxs-lookup"><span data-stu-id="cee05-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="cee05-114">OS</span><span class="sxs-lookup"><span data-stu-id="cee05-114">PARAMETERS</span></span>

### <span data-ttu-id="cee05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee05-115">-DefaultProfile</span></span>
<span data-ttu-id="cee05-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cee05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee05-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="cee05-117">-Description</span></span>
<span data-ttu-id="cee05-118">A descrição do bot</span><span class="sxs-lookup"><span data-stu-id="cee05-118">The description of the bot</span></span>

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

### <span data-ttu-id="cee05-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="cee05-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="cee05-120">A chave do Application insights</span><span class="sxs-lookup"><span data-stu-id="cee05-120">The Application Insights key</span></span>

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

### <span data-ttu-id="cee05-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="cee05-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="cee05-122">A chave de API do Application insights</span><span class="sxs-lookup"><span data-stu-id="cee05-122">The Application Insights Api Key</span></span>

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

### <span data-ttu-id="cee05-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="cee05-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="cee05-124">A ID do aplicativo insights do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cee05-124">The Application Insights App Id</span></span>

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

### <span data-ttu-id="cee05-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cee05-125">-DisplayName</span></span>
<span data-ttu-id="cee05-126">O nome do bot</span><span class="sxs-lookup"><span data-stu-id="cee05-126">The Name of the bot</span></span>

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

### <span data-ttu-id="cee05-127">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="cee05-127">-Endpoint</span></span>
<span data-ttu-id="cee05-128">O ponto de extremidade do bot</span><span class="sxs-lookup"><span data-stu-id="cee05-128">The bot's endpoint</span></span>

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

### <span data-ttu-id="cee05-129">-ETag</span><span class="sxs-lookup"><span data-stu-id="cee05-129">-Etag</span></span>
<span data-ttu-id="cee05-130">Marca de entidade</span><span class="sxs-lookup"><span data-stu-id="cee05-130">Entity Tag</span></span>

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

### <span data-ttu-id="cee05-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="cee05-131">-IconUrl</span></span>
<span data-ttu-id="cee05-132">A URL do ícone do bot</span><span class="sxs-lookup"><span data-stu-id="cee05-132">The Icon Url of the bot</span></span>

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

### <span data-ttu-id="cee05-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cee05-133">-InputObject</span></span>
<span data-ttu-id="cee05-134">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cee05-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cee05-135">-Kind</span><span class="sxs-lookup"><span data-stu-id="cee05-135">-Kind</span></span>
<span data-ttu-id="cee05-136">Necessário.</span><span class="sxs-lookup"><span data-stu-id="cee05-136">Required.</span></span>
<span data-ttu-id="cee05-137">Obtém ou define o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="cee05-137">Gets or sets the Kind of the resource.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.Kind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee05-138">-Local</span><span class="sxs-lookup"><span data-stu-id="cee05-138">-Location</span></span>
<span data-ttu-id="cee05-139">Especifica o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="cee05-139">Specifies the location of the resource.</span></span>

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

### <span data-ttu-id="cee05-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="cee05-140">-LuisAppId</span></span>
<span data-ttu-id="cee05-141">Coleção de IDs do aplicativo LUIS</span><span class="sxs-lookup"><span data-stu-id="cee05-141">Collection of LUIS App Ids</span></span>

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

### <span data-ttu-id="cee05-142">-LuisKey</span><span class="sxs-lookup"><span data-stu-id="cee05-142">-LuisKey</span></span>
<span data-ttu-id="cee05-143">A chave LUIS</span><span class="sxs-lookup"><span data-stu-id="cee05-143">The LUIS Key</span></span>

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

### <span data-ttu-id="cee05-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="cee05-144">-MsaAppId</span></span>
<span data-ttu-id="cee05-145">ID do aplicativo da Microsoft para o bot</span><span class="sxs-lookup"><span data-stu-id="cee05-145">Microsoft App Id for the bot</span></span>

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

### <span data-ttu-id="cee05-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="cee05-146">-Name</span></span>
<span data-ttu-id="cee05-147">O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="cee05-147">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee05-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cee05-148">-ResourceGroupName</span></span>
<span data-ttu-id="cee05-149">O nome do grupo de recursos de bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="cee05-149">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee05-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cee05-150">-SkuName</span></span>
<span data-ttu-id="cee05-151">O nome do SKU</span><span class="sxs-lookup"><span data-stu-id="cee05-151">The sku name</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee05-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cee05-152">-SubscriptionId</span></span>
<span data-ttu-id="cee05-153">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="cee05-153">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee05-154">-Marca</span><span class="sxs-lookup"><span data-stu-id="cee05-154">-Tag</span></span>
<span data-ttu-id="cee05-155">Contém marcas de recurso definidas como pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="cee05-155">Contains resource tags defined as key/value pairs.</span></span>

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

### <span data-ttu-id="cee05-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cee05-156">-Confirm</span></span>
<span data-ttu-id="cee05-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cee05-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee05-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cee05-158">-WhatIf</span></span>
<span data-ttu-id="cee05-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cee05-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cee05-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cee05-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cee05-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee05-161">CommonParameters</span></span>
<span data-ttu-id="cee05-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cee05-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee05-163">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cee05-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee05-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cee05-164">INPUTS</span></span>

### <span data-ttu-id="cee05-165">Microsoft. Azure. PowerShell. cmdlets. BotService. Models. IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="cee05-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="cee05-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cee05-166">OUTPUTS</span></span>

### <span data-ttu-id="cee05-167">Microsoft. Azure. PowerShell. cmdlets. BotService. Models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="cee05-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="cee05-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cee05-168">NOTES</span></span>

<span data-ttu-id="cee05-169">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cee05-169">ALIASES</span></span>

<span data-ttu-id="cee05-170">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="cee05-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cee05-171">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="cee05-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cee05-172">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cee05-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cee05-173">INPUTobject <IBotServiceIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="cee05-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cee05-174">`[ChannelName <ChannelName?>]`: O nome do recurso de canal.</span><span class="sxs-lookup"><span data-stu-id="cee05-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="cee05-175">`[ConnectionName <String>]`: O nome do recurso de configuração de conexão do serviço bot</span><span class="sxs-lookup"><span data-stu-id="cee05-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="cee05-176">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="cee05-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cee05-177">`[ResourceGroupName <String>]`: O nome do grupo de recursos de bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="cee05-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="cee05-178">`[ResourceName <String>]`: O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="cee05-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="cee05-179">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="cee05-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="cee05-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cee05-180">RELATED LINKS</span></span>

