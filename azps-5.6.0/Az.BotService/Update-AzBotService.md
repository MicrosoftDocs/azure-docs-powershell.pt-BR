---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: 330aca1a9d4cc9438bdf360d5aee4af914df6c7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892563"
---
# <span data-ttu-id="8a4f0-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="8a4f0-101">Update-AzBotService</span></span>

## <span data-ttu-id="8a4f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a4f0-102">SYNOPSIS</span></span>
<span data-ttu-id="8a4f0-103">Atualiza um Serviço de Bot</span><span class="sxs-lookup"><span data-stu-id="8a4f0-103">Updates a Bot Service</span></span>

## <span data-ttu-id="8a4f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8a4f0-104">SYNTAX</span></span>

### <span data-ttu-id="8a4f0-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8a4f0-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a4f0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8a4f0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8a4f0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8a4f0-107">DESCRIPTION</span></span>
<span data-ttu-id="8a4f0-108">Atualiza um Serviço de Bot</span><span class="sxs-lookup"><span data-stu-id="8a4f0-108">Updates a Bot Service</span></span>

## <span data-ttu-id="8a4f0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a4f0-109">EXAMPLES</span></span>

### <span data-ttu-id="8a4f0-110">Exemplo 1: Atualizar o Bot por Nome e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a4f0-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="8a4f0-111">Atualizar o Bot por Nome e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a4f0-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="8a4f0-112">Exemplo 2: Atualizar o Bot por InputObject</span><span class="sxs-lookup"><span data-stu-id="8a4f0-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="8a4f0-113">Atualizar o Bot por InputObject</span><span class="sxs-lookup"><span data-stu-id="8a4f0-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="8a4f0-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8a4f0-114">PARAMETERS</span></span>

### <span data-ttu-id="8a4f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a4f0-115">-DefaultProfile</span></span>
<span data-ttu-id="8a4f0-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a4f0-117">-Description</span><span class="sxs-lookup"><span data-stu-id="8a4f0-117">-Description</span></span>
<span data-ttu-id="8a4f0-118">A descrição do bot</span><span class="sxs-lookup"><span data-stu-id="8a4f0-118">The description of the bot</span></span>

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

### <span data-ttu-id="8a4f0-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="8a4f0-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="8a4f0-120">A chave Application Insights</span><span class="sxs-lookup"><span data-stu-id="8a4f0-120">The Application Insights key</span></span>

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

### <span data-ttu-id="8a4f0-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="8a4f0-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="8a4f0-122">A Chave da Api de Insights do Aplicativo</span><span class="sxs-lookup"><span data-stu-id="8a4f0-122">The Application Insights Api Key</span></span>

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

### <span data-ttu-id="8a4f0-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="8a4f0-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="8a4f0-124">A ID do Aplicativo Insights</span><span class="sxs-lookup"><span data-stu-id="8a4f0-124">The Application Insights App Id</span></span>

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

### <span data-ttu-id="8a4f0-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8a4f0-125">-DisplayName</span></span>
<span data-ttu-id="8a4f0-126">O nome do bot</span><span class="sxs-lookup"><span data-stu-id="8a4f0-126">The Name of the bot</span></span>

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

### <span data-ttu-id="8a4f0-127">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="8a4f0-127">-Endpoint</span></span>
<span data-ttu-id="8a4f0-128">Ponto de extremidade do bot</span><span class="sxs-lookup"><span data-stu-id="8a4f0-128">The bot's endpoint</span></span>

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

### <span data-ttu-id="8a4f0-129">-Etag</span><span class="sxs-lookup"><span data-stu-id="8a4f0-129">-Etag</span></span>
<span data-ttu-id="8a4f0-130">Entity Tag</span><span class="sxs-lookup"><span data-stu-id="8a4f0-130">Entity Tag</span></span>

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

### <span data-ttu-id="8a4f0-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="8a4f0-131">-IconUrl</span></span>
<span data-ttu-id="8a4f0-132">A Url do ícone do bot</span><span class="sxs-lookup"><span data-stu-id="8a4f0-132">The Icon Url of the bot</span></span>

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

### <span data-ttu-id="8a4f0-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a4f0-133">-InputObject</span></span>
<span data-ttu-id="8a4f0-134">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8a4f0-135">-Kind</span><span class="sxs-lookup"><span data-stu-id="8a4f0-135">-Kind</span></span>
<span data-ttu-id="8a4f0-136">Necessário.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-136">Required.</span></span>
<span data-ttu-id="8a4f0-137">Obtém ou define o Tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-137">Gets or sets the Kind of the resource.</span></span>

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

### <span data-ttu-id="8a4f0-138">-Location</span><span class="sxs-lookup"><span data-stu-id="8a4f0-138">-Location</span></span>
<span data-ttu-id="8a4f0-139">Especifica o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-139">Specifies the location of the resource.</span></span>

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

### <span data-ttu-id="8a4f0-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="8a4f0-140">-LuisAppId</span></span>
<span data-ttu-id="8a4f0-141">Coleção de Ids de aplicativos DOLS</span><span class="sxs-lookup"><span data-stu-id="8a4f0-141">Collection of LUIS App Ids</span></span>

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

### <span data-ttu-id="8a4f0-142">-LuisKey</span><span class="sxs-lookup"><span data-stu-id="8a4f0-142">-LuisKey</span></span>
<span data-ttu-id="8a4f0-143">A chave LUIS</span><span class="sxs-lookup"><span data-stu-id="8a4f0-143">The LUIS Key</span></span>

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

### <span data-ttu-id="8a4f0-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="8a4f0-144">-MsaAppId</span></span>
<span data-ttu-id="8a4f0-145">ID de aplicativo da Microsoft para o bot</span><span class="sxs-lookup"><span data-stu-id="8a4f0-145">Microsoft App Id for the bot</span></span>

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

### <span data-ttu-id="8a4f0-146">-Name</span><span class="sxs-lookup"><span data-stu-id="8a4f0-146">-Name</span></span>
<span data-ttu-id="8a4f0-147">O nome do recurso Bot.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-147">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="8a4f0-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a4f0-148">-ResourceGroupName</span></span>
<span data-ttu-id="8a4f0-149">O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-149">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="8a4f0-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8a4f0-150">-SkuName</span></span>
<span data-ttu-id="8a4f0-151">O nome sku</span><span class="sxs-lookup"><span data-stu-id="8a4f0-151">The sku name</span></span>

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

### <span data-ttu-id="8a4f0-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a4f0-152">-SubscriptionId</span></span>
<span data-ttu-id="8a4f0-153">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-153">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8a4f0-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="8a4f0-154">-Tag</span></span>
<span data-ttu-id="8a4f0-155">Contém marcas de recurso definidas como pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-155">Contains resource tags defined as key/value pairs.</span></span>

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

### <span data-ttu-id="8a4f0-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a4f0-156">-Confirm</span></span>
<span data-ttu-id="8a4f0-157">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a4f0-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a4f0-158">-WhatIf</span></span>
<span data-ttu-id="8a4f0-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a4f0-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a4f0-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4f0-161">CommonParameters</span></span>
<span data-ttu-id="8a4f0-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a4f0-163">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a4f0-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4f0-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a4f0-164">INPUTS</span></span>

### <span data-ttu-id="8a4f0-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="8a4f0-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="8a4f0-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8a4f0-166">OUTPUTS</span></span>

### <span data-ttu-id="8a4f0-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="8a4f0-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="8a4f0-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="8a4f0-168">NOTES</span></span>

<span data-ttu-id="8a4f0-169">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8a4f0-169">ALIASES</span></span>

<span data-ttu-id="8a4f0-170">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="8a4f0-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a4f0-171">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a4f0-172">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a4f0-173">INPUTOBJECT <IBotServiceIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="8a4f0-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a4f0-174">`[ChannelName <ChannelName?>]`: O nome do recurso Channel.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="8a4f0-175">`[ConnectionName <String>]`: O nome do recurso Configuração de Conexão de Serviço bot</span><span class="sxs-lookup"><span data-stu-id="8a4f0-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="8a4f0-176">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8a4f0-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a4f0-177">`[ResourceGroupName <String>]`: O nome do grupo de recursos Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="8a4f0-178">`[ResourceName <String>]`: O nome do recurso Bot.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="8a4f0-179">`[SubscriptionId <String>]`: ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4f0-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="8a4f0-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a4f0-180">RELATED LINKS</span></span>

