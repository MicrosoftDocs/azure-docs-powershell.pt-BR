---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: f7dd02a214fa32223e052c1999329699f1c653e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116927"
---
# <span data-ttu-id="8f2dd-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="8f2dd-101">Update-AzBotService</span></span>

## <span data-ttu-id="8f2dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f2dd-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2dd-103">Atualiza um Serviço de Bot</span><span class="sxs-lookup"><span data-stu-id="8f2dd-103">Updates a Bot Service</span></span>

## <span data-ttu-id="8f2dd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f2dd-104">SYNTAX</span></span>

### <span data-ttu-id="8f2dd-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f2dd-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f2dd-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8f2dd-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f2dd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f2dd-107">DESCRIPTION</span></span>
<span data-ttu-id="8f2dd-108">Atualiza um Serviço de Bot</span><span class="sxs-lookup"><span data-stu-id="8f2dd-108">Updates a Bot Service</span></span>

## <span data-ttu-id="8f2dd-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f2dd-109">EXAMPLES</span></span>

### <span data-ttu-id="8f2dd-110">Exemplo 1: Atualizar o bot por Nome e NomedoGrupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8f2dd-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="8f2dd-111">Atualizar o bot por Nome e NomedoGrupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8f2dd-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="8f2dd-112">Exemplo 2: Atualizar o bot por InputObject</span><span class="sxs-lookup"><span data-stu-id="8f2dd-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="8f2dd-113">Atualizar o bot por InputObject</span><span class="sxs-lookup"><span data-stu-id="8f2dd-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="8f2dd-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f2dd-114">PARAMETERS</span></span>

### <span data-ttu-id="8f2dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2dd-115">-DefaultProfile</span></span>
<span data-ttu-id="8f2dd-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f2dd-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="8f2dd-117">-Description</span></span>
<span data-ttu-id="8f2dd-118">A descrição do bot</span><span class="sxs-lookup"><span data-stu-id="8f2dd-118">The description of the bot</span></span>

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

### <span data-ttu-id="8f2dd-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="8f2dd-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="8f2dd-120">A tecla Insights do Aplicativo</span><span class="sxs-lookup"><span data-stu-id="8f2dd-120">The Application Insights key</span></span>

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

### <span data-ttu-id="8f2dd-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="8f2dd-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="8f2dd-122">Chave da Api do Insights do Aplicativo</span><span class="sxs-lookup"><span data-stu-id="8f2dd-122">The Application Insights Api Key</span></span>

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

### <span data-ttu-id="8f2dd-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="8f2dd-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="8f2dd-124">A ID do aplicativo Insights do Aplicativo</span><span class="sxs-lookup"><span data-stu-id="8f2dd-124">The Application Insights App Id</span></span>

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

### <span data-ttu-id="8f2dd-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8f2dd-125">-DisplayName</span></span>
<span data-ttu-id="8f2dd-126">O Nome do bot</span><span class="sxs-lookup"><span data-stu-id="8f2dd-126">The Name of the bot</span></span>

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

### <span data-ttu-id="8f2dd-127">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="8f2dd-127">-Endpoint</span></span>
<span data-ttu-id="8f2dd-128">Ponto de extremidade do bot</span><span class="sxs-lookup"><span data-stu-id="8f2dd-128">The bot's endpoint</span></span>

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

### <span data-ttu-id="8f2dd-129">-Etag</span><span class="sxs-lookup"><span data-stu-id="8f2dd-129">-Etag</span></span>
<span data-ttu-id="8f2dd-130">Marca de Entidade</span><span class="sxs-lookup"><span data-stu-id="8f2dd-130">Entity Tag</span></span>

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

### <span data-ttu-id="8f2dd-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="8f2dd-131">-IconUrl</span></span>
<span data-ttu-id="8f2dd-132">A Url do Ícone do bot</span><span class="sxs-lookup"><span data-stu-id="8f2dd-132">The Icon Url of the bot</span></span>

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

### <span data-ttu-id="8f2dd-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f2dd-133">-InputObject</span></span>
<span data-ttu-id="8f2dd-134">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8f2dd-135">-Tipo</span><span class="sxs-lookup"><span data-stu-id="8f2dd-135">-Kind</span></span>
<span data-ttu-id="8f2dd-136">Necessário.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-136">Required.</span></span>
<span data-ttu-id="8f2dd-137">Obtém ou define o Tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-137">Gets or sets the Kind of the resource.</span></span>

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

### <span data-ttu-id="8f2dd-138">-Local</span><span class="sxs-lookup"><span data-stu-id="8f2dd-138">-Location</span></span>
<span data-ttu-id="8f2dd-139">Especifica o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-139">Specifies the location of the resource.</span></span>

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

### <span data-ttu-id="8f2dd-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="8f2dd-140">-LuisAppId</span></span>
<span data-ttu-id="8f2dd-141">Conjunto de Ids de aplicativos LUIS</span><span class="sxs-lookup"><span data-stu-id="8f2dd-141">Collection of LUIS App Ids</span></span>

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

### <span data-ttu-id="8f2dd-142">-LuisKey</span><span class="sxs-lookup"><span data-stu-id="8f2dd-142">-LuisKey</span></span>
<span data-ttu-id="8f2dd-143">A chave LUIS</span><span class="sxs-lookup"><span data-stu-id="8f2dd-143">The LUIS Key</span></span>

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

### <span data-ttu-id="8f2dd-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="8f2dd-144">-MsaAppId</span></span>
<span data-ttu-id="8f2dd-145">ID do aplicativo Microsoft para o bot</span><span class="sxs-lookup"><span data-stu-id="8f2dd-145">Microsoft App Id for the bot</span></span>

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

### <span data-ttu-id="8f2dd-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f2dd-146">-Name</span></span>
<span data-ttu-id="8f2dd-147">O nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-147">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="8f2dd-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2dd-148">-ResourceGroupName</span></span>
<span data-ttu-id="8f2dd-149">O nome do grupo de recursos do Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-149">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="8f2dd-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8f2dd-150">-SkuName</span></span>
<span data-ttu-id="8f2dd-151">O nome da sKU</span><span class="sxs-lookup"><span data-stu-id="8f2dd-151">The sku name</span></span>

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

### <span data-ttu-id="8f2dd-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f2dd-152">-SubscriptionId</span></span>
<span data-ttu-id="8f2dd-153">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-153">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8f2dd-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="8f2dd-154">-Tag</span></span>
<span data-ttu-id="8f2dd-155">Contém marcas de recurso definidas como pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-155">Contains resource tags defined as key/value pairs.</span></span>

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

### <span data-ttu-id="8f2dd-156">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8f2dd-156">-Confirm</span></span>
<span data-ttu-id="8f2dd-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f2dd-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f2dd-158">-WhatIf</span></span>
<span data-ttu-id="8f2dd-159">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f2dd-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f2dd-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2dd-161">CommonParameters</span></span>
<span data-ttu-id="8f2dd-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2dd-163">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f2dd-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2dd-164">Entradas</span><span class="sxs-lookup"><span data-stu-id="8f2dd-164">INPUTS</span></span>

### <span data-ttu-id="8f2dd-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="8f2dd-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="8f2dd-166">Saídas</span><span class="sxs-lookup"><span data-stu-id="8f2dd-166">OUTPUTS</span></span>

### <span data-ttu-id="8f2dd-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="8f2dd-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="8f2dd-168">Notas</span><span class="sxs-lookup"><span data-stu-id="8f2dd-168">NOTES</span></span>

<span data-ttu-id="8f2dd-169">Aliases</span><span class="sxs-lookup"><span data-stu-id="8f2dd-169">ALIASES</span></span>

<span data-ttu-id="8f2dd-170">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="8f2dd-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8f2dd-171">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f2dd-172">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8f2dd-173">INPUTOBJECT: <IBotServiceIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="8f2dd-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f2dd-174">`[ChannelName <ChannelName?>]`: o nome do recurso Canal.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="8f2dd-175">`[ConnectionName <String>]`: o nome do recurso Configuração de Conexão de Serviço de Bot</span><span class="sxs-lookup"><span data-stu-id="8f2dd-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="8f2dd-176">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="8f2dd-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f2dd-177">`[ResourceGroupName <String>]`: o nome do grupo de recursos do Bot na assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="8f2dd-178">`[ResourceName <String>]`: o nome do recurso bot.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="8f2dd-179">`[SubscriptionId <String>]`: ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2dd-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="8f2dd-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f2dd-180">RELATED LINKS</span></span>

