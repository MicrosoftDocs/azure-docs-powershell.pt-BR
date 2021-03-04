---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
ms.openlocfilehash: 24a74380fe6930c730357476792cea81ebaf7b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890277"
---
# <span data-ttu-id="a19a8-101">Update-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="a19a8-101">Update-AzFunctionAppSetting</span></span>

## <span data-ttu-id="a19a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a19a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a19a8-103">Adiciona ou atualiza as configurações do aplicativo em um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="a19a8-103">Adds or updates app settings in a function app.</span></span>

## <span data-ttu-id="a19a8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a19a8-104">SYNTAX</span></span>

### <span data-ttu-id="a19a8-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a19a8-105">ByName (Default)</span></span>
```
Update-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSetting <Hashtable>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a19a8-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="a19a8-106">ByObjectInput</span></span>
```
Update-AzFunctionAppSetting -AppSetting <Hashtable> -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a19a8-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a19a8-107">DESCRIPTION</span></span>
<span data-ttu-id="a19a8-108">Adiciona ou atualiza as configurações do aplicativo em um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="a19a8-108">Adds or updates app settings in a function app.</span></span>

## <span data-ttu-id="a19a8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a19a8-109">EXAMPLES</span></span>

### <span data-ttu-id="a19a8-110">Exemplo 1: Adicionar uma nova configuração de aplicativo em um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="a19a8-110">Example 1: Add a new app setting in a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSetting @{"Name1" = "Value1"}
```

<span data-ttu-id="a19a8-111">Este comando adiciona uma nova configuração de aplicativo em um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="a19a8-111">This command adds a new app setting in a function app.</span></span>

## <span data-ttu-id="a19a8-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a19a8-112">PARAMETERS</span></span>

### <span data-ttu-id="a19a8-113">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="a19a8-113">-AppSetting</span></span>
<span data-ttu-id="a19a8-114">Hashtable com chaves e valores descrevem as configurações do aplicativo a serem adicionadas ou atualizadas no aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="a19a8-114">Hashtable with keys and values describe the app settings to be added or updated in the function app.</span></span>
<span data-ttu-id="a19a8-115">Por exemplo: @{"myappsetting"="123"}</span><span class="sxs-lookup"><span data-stu-id="a19a8-115">For example: @{"myappsetting"="123"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a19a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19a8-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="a19a8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a19a8-117">-Force</span></span>
<span data-ttu-id="a19a8-118">Força o cmdlet a atualizar a configuração do aplicativo de função sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="a19a8-118">Forces the cmdlet to update function app setting without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a19a8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a19a8-119">-InputObject</span></span>
<span data-ttu-id="a19a8-120">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a19a8-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a19a8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a19a8-121">-Name</span></span>
<span data-ttu-id="a19a8-122">Nome do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="a19a8-122">Name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a19a8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a19a8-123">-ResourceGroupName</span></span>
<span data-ttu-id="a19a8-124">Nome do grupo de recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="a19a8-124">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a19a8-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a19a8-125">-SubscriptionId</span></span>
<span data-ttu-id="a19a8-126">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a19a8-126">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a19a8-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a19a8-127">-Confirm</span></span>
<span data-ttu-id="a19a8-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a19a8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a19a8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a19a8-129">-WhatIf</span></span>
<span data-ttu-id="a19a8-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a19a8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a19a8-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a19a8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a19a8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19a8-132">CommonParameters</span></span>
<span data-ttu-id="a19a8-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a19a8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19a8-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a19a8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19a8-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a19a8-135">INPUTS</span></span>

### <span data-ttu-id="a19a8-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="a19a8-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="a19a8-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a19a8-137">OUTPUTS</span></span>

### <span data-ttu-id="a19a8-138">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="a19a8-138">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="a19a8-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="a19a8-139">NOTES</span></span>

<span data-ttu-id="a19a8-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a19a8-140">ALIASES</span></span>

<span data-ttu-id="a19a8-141">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="a19a8-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a19a8-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a19a8-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a19a8-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a19a8-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a19a8-144">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="a19a8-144">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="a19a8-145">`Location <String>`: Localização do Recurso.</span><span class="sxs-lookup"><span data-stu-id="a19a8-145">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="a19a8-146">`CloningInfoSourceWebAppId <String>`: ARM ID de recurso do aplicativo de origem.</span><span class="sxs-lookup"><span data-stu-id="a19a8-146">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="a19a8-147">A ID de recurso do aplicativo é do formulário /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} para slots de produção e /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} para outros slots.</span><span class="sxs-lookup"><span data-stu-id="a19a8-147">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="a19a8-148">`[Kind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="a19a8-148">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="a19a8-149">`[Tag <IResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="a19a8-149">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="a19a8-150">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="a19a8-150">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a19a8-151">`[ClientAffinityEnabled <Boolean?>]`: para habilitar a afinidade do cliente; para parar de enviar cookies de afinidade de sessão, que encaminham solicitações de cliente na mesma sessão <code>true</code> <code>false</code> para a mesma instância.</span><span class="sxs-lookup"><span data-stu-id="a19a8-151">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="a19a8-152">O padrão é <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-152">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="a19a8-153">`[ClientCertEnabled <Boolean?>]`: <code>true</code> para habilitar a autenticação de certificado do cliente (autenticação mútua TLS); caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-153">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="a19a8-154">O padrão é <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-154">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="a19a8-155">`[ClientCertExclusionPath <String>]`: caminhos de exclusão separados por vírgulas de autenticação de certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="a19a8-155">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="a19a8-156">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: A configuração do aplicativo substitui o aplicativo clonado.</span><span class="sxs-lookup"><span data-stu-id="a19a8-156">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="a19a8-157">Se especificado, essas configurações substituem as configurações clonadas do aplicativo de origem.</span><span class="sxs-lookup"><span data-stu-id="a19a8-157">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="a19a8-158">Caso contrário, as configurações do aplicativo de origem são mantidas.</span><span class="sxs-lookup"><span data-stu-id="a19a8-158">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="a19a8-159">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="a19a8-159">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a19a8-160">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> para clonar nomes de host personalizados do aplicativo de origem; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-160">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="a19a8-161">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> para clonar o controle de origem do aplicativo de origem; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-161">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="a19a8-162">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> para configurar o balanceamento de carga para o aplicativo de origem e destino.</span><span class="sxs-lookup"><span data-stu-id="a19a8-162">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="a19a8-163">`[CloningInfoCorrelationId <String>]`: ID de correlação da operação de clonagem.</span><span class="sxs-lookup"><span data-stu-id="a19a8-163">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="a19a8-164">Essa ID vincula várias operações de clonagem para usar o mesmo instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a19a8-164">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="a19a8-165">`[CloningInfoHostingEnvironment <String>]`: Ambiente de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a19a8-165">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="a19a8-166">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> para substituir o aplicativo de destino; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-166">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="a19a8-167">`[CloningInfoSourceWebAppLocation <String>]`: Local do aplicativo de origem ex: Oeste dos EUA ou norte da Europa</span><span class="sxs-lookup"><span data-stu-id="a19a8-167">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="a19a8-168">`[CloningInfoTrafficManagerProfileId <String>]`: ARM ID de recurso do perfil do Gerenciador de Tráfego a ser usado, se existir.</span><span class="sxs-lookup"><span data-stu-id="a19a8-168">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="a19a8-169">A ID de recurso do Gerenciador de Tráfego é do formulário /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="a19a8-169">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="a19a8-170">`[CloningInfoTrafficManagerProfileName <String>]`: Nome do perfil do Gerenciador de Tráfego a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a19a8-170">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="a19a8-171">Isso só será necessário se o perfil do Gerenciador de Tráfego ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="a19a8-171">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="a19a8-172">`[Config <ISiteConfig>]`: Configuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a19a8-172">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="a19a8-173">`IsPushEnabled <Boolean>`: Obtém ou define um sinalizador indicando se o ponto de extremidade push está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a19a8-173">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="a19a8-174">`[ActionMinProcessExecutionTime <String>]`: Tempo mínimo em que o processo deve ser executado antes de executar a ação</span><span class="sxs-lookup"><span data-stu-id="a19a8-174">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="a19a8-175">`[ActionType <AutoHealActionType?>]`: Ação predefinida a ser tomada.</span><span class="sxs-lookup"><span data-stu-id="a19a8-175">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="a19a8-176">`[AlwaysOn <Boolean?>]`: <code>true</code> se Always On estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-176">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a19a8-177">`[ApiDefinitionUrl <String>]`: A URL da definição da API.</span><span class="sxs-lookup"><span data-stu-id="a19a8-177">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="a19a8-178">`[ApiManagementConfigId <String>]`: APIM-Api Identificador.</span><span class="sxs-lookup"><span data-stu-id="a19a8-178">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="a19a8-179">`[AppCommandLine <String>]`: Linha de comando do aplicativo a ser lançada.</span><span class="sxs-lookup"><span data-stu-id="a19a8-179">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="a19a8-180">`[AppSetting <INameValuePair[]>]`: Configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a19a8-180">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="a19a8-181">`[Name <String>]`: Nome do par.</span><span class="sxs-lookup"><span data-stu-id="a19a8-181">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="a19a8-182">`[Value <String>]`: Valor do par.</span><span class="sxs-lookup"><span data-stu-id="a19a8-182">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="a19a8-183">`[AutoHealEnabled <Boolean?>]`: <code>true</code> se a Cura Automática estiver habilitada; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-183">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a19a8-184">`[AutoSwapSlotName <String>]`: Nome do slot de troca automática.</span><span class="sxs-lookup"><span data-stu-id="a19a8-184">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="a19a8-185">`[ConnectionString <IConnStringInfo[]>]`: Cadeias de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="a19a8-185">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="a19a8-186">`[ConnectionString <String>]`: Valor da cadeia de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="a19a8-186">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="a19a8-187">`[Name <String>]`: Nome da cadeia de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="a19a8-187">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="a19a8-188">`[Type <ConnectionStringType?>]`: Tipo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a19a8-188">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="a19a8-189">`[CorAllowedOrigin <String[]>]`: Obtém ou define a lista de origens que devem ser permitidas para fazer chamadas de origem cruzada (por exemplo: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="a19a8-189">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="a19a8-190">Use "\*" para permitir tudo.</span><span class="sxs-lookup"><span data-stu-id="a19a8-190">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="a19a8-191">`[CorSupportCredentials <Boolean?>]`: Obtém ou define se solicitações CORS com credenciais são permitidas.</span><span class="sxs-lookup"><span data-stu-id="a19a8-191">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="a19a8-192">Confira         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="a19a8-192">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="a19a8-193">`[CustomActionExe <String>]`: Executável a ser executado.</span><span class="sxs-lookup"><span data-stu-id="a19a8-193">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="a19a8-194">`[CustomActionParameter <String>]`: Parâmetros para o executável.</span><span class="sxs-lookup"><span data-stu-id="a19a8-194">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="a19a8-195">`[DefaultDocument <String[]>]`: Documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="a19a8-195">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="a19a8-196">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> se o log de erros detalhado estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-196">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a19a8-197">`[DocumentRoot <String>]`: Raiz do documento.</span><span class="sxs-lookup"><span data-stu-id="a19a8-197">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="a19a8-198">`[DynamicTagsJson <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas dinâmicas que serão avaliadas a partir de declarações do usuário no ponto de extremidade de registro por push.</span><span class="sxs-lookup"><span data-stu-id="a19a8-198">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="a19a8-199">`[ExperimentRampUpRule <IRampUpRule[]>]`: Lista de regras de rampa.</span><span class="sxs-lookup"><span data-stu-id="a19a8-199">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="a19a8-200">`[ActionHostName <String>]`: Nome do host de um slot para o qual o tráfego será redirecionado se decidir.</span><span class="sxs-lookup"><span data-stu-id="a19a8-200">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="a19a8-201">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="a19a8-201">E.g.</span></span> <span data-ttu-id="a19a8-202">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="a19a8-202">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="a19a8-203">`[ChangeDecisionCallbackUrl <String>]`: Algoritmo de decisão personalizado pode ser fornecido na extensão de site TiPCallback qual URL pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="a19a8-203">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="a19a8-204">Consulte Extensão de site TiPCallback para o scaffold e contratos.</span><span class="sxs-lookup"><span data-stu-id="a19a8-204">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="a19a8-205"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="a19a8-205">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="a19a8-206">`[ChangeIntervalInMinute <Int32?>]`: Especifica o intervalo em minutos para reavaliar ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="a19a8-206">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="a19a8-207">`[ChangeStep <Double?>]`: No cenário de rampa automática, esta é a etapa para adicionar/remover até atingir <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> ou         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-207">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="a19a8-208">As métricas de site são verificadas a cada N minutos especificado no algoritmo de decisão .\nCustom pode ser fornecido na extensão de <code>ChangeIntervalInMinutes</code> site TiPCallback, que URL pode ser especificada em <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-208">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="a19a8-209">`[MaxReroutePercentage <Double?>]`: Especifica o limite superior abaixo do qual ReroutePercentage ficará.</span><span class="sxs-lookup"><span data-stu-id="a19a8-209">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="a19a8-210">`[MinReroutePercentage <Double?>]`: Especifica o limite inferior acima do qual ReroutePercentage ficará.</span><span class="sxs-lookup"><span data-stu-id="a19a8-210">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="a19a8-211">`[Name <String>]`: Nome da regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="a19a8-211">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="a19a8-212">O nome recomendado seria apontar para o slot que receberá o tráfego no experimento.</span><span class="sxs-lookup"><span data-stu-id="a19a8-212">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="a19a8-213">`[ReroutePercentage <Double?>]`: Porcentagem do tráfego que será redirecionado para <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-213">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="a19a8-214">`[FtpsState <FtpsState?>]`: Estado do serviço FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="a19a8-214">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="a19a8-215">`[HandlerMapping <IHandlerMapping[]>]`: Mapeamentos de manipuladores.</span><span class="sxs-lookup"><span data-stu-id="a19a8-215">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="a19a8-216">`[Argument <String>]`: Argumentos de linha de comando a serem passados para o processador de script.</span><span class="sxs-lookup"><span data-stu-id="a19a8-216">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="a19a8-217">`[Extension <String>]`: As solicitações com essa extensão serão tratadas usando o aplicativo FastCGI especificado.</span><span class="sxs-lookup"><span data-stu-id="a19a8-217">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="a19a8-218">`[ScriptProcessor <String>]`: O caminho absoluto para o aplicativo FastCGI.</span><span class="sxs-lookup"><span data-stu-id="a19a8-218">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="a19a8-219">`[HealthCheckPath <String>]`: Caminho de verificação de saúde</span><span class="sxs-lookup"><span data-stu-id="a19a8-219">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="a19a8-220">`[Http20Enabled <Boolean?>]`: Http20Enabled: configura um site para permitir que os clientes se conectem por http2.0</span><span class="sxs-lookup"><span data-stu-id="a19a8-220">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="a19a8-221">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> se o log HTTP estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-221">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a19a8-222">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrições de segurança IP para principal.</span><span class="sxs-lookup"><span data-stu-id="a19a8-222">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="a19a8-223">`[Action <String>]`: Permitir ou negar acesso a esse intervalo DE IP.</span><span class="sxs-lookup"><span data-stu-id="a19a8-223">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="a19a8-224">`[Description <String>]`: Descrição da regra de restrição de IP.</span><span class="sxs-lookup"><span data-stu-id="a19a8-224">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="a19a8-225">`[IPAddress <String>]`: Endereço IP para o que a restrição de segurança é válida.</span><span class="sxs-lookup"><span data-stu-id="a19a8-225">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="a19a8-226">Ele pode estar em forma de endereço ipv4 puro (propriedade SubnetMask necessária) ou notação CIDR, como ipv4/mask (combinação de bits à frente).</span><span class="sxs-lookup"><span data-stu-id="a19a8-226">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="a19a8-227">Para CIDR, a propriedade SubnetMask não deve ser especificada.</span><span class="sxs-lookup"><span data-stu-id="a19a8-227">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="a19a8-228">`[Name <String>]`: Nome da regra de restrição de IP.</span><span class="sxs-lookup"><span data-stu-id="a19a8-228">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="a19a8-229">`[Priority <Int32?>]`: Prioridade da regra de restrição de IP.</span><span class="sxs-lookup"><span data-stu-id="a19a8-229">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="a19a8-230">`[SubnetMask <String>]`: Máscara de sub-rede para o intervalo de endereços IP para o que a restrição é válida.</span><span class="sxs-lookup"><span data-stu-id="a19a8-230">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="a19a8-231">`[SubnetTrafficTag <Int32?>]`: (interna) Marca de tráfego de sub-rede</span><span class="sxs-lookup"><span data-stu-id="a19a8-231">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="a19a8-232">`[Tag <IPFilterTag?>]`: Define para que esse filtro IP será usado.</span><span class="sxs-lookup"><span data-stu-id="a19a8-232">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="a19a8-233">Isso é para dar suporte à filtragem de IP em proxies.</span><span class="sxs-lookup"><span data-stu-id="a19a8-233">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="a19a8-234">`[VnetSubnetResourceId <String>]`: ID de recurso de rede virtual</span><span class="sxs-lookup"><span data-stu-id="a19a8-234">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="a19a8-235">`[VnetTrafficTag <Int32?>]`: marca de tráfego Vnet (interna)</span><span class="sxs-lookup"><span data-stu-id="a19a8-235">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="a19a8-236">`[JavaContainer <String>]`: Java contêiner.</span><span class="sxs-lookup"><span data-stu-id="a19a8-236">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="a19a8-237">`[JavaContainerVersion <String>]`: Java versão do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a19a8-237">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="a19a8-238">`[JavaVersion <String>]`: Java versão.</span><span class="sxs-lookup"><span data-stu-id="a19a8-238">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="a19a8-239">`[LimitMaxDiskSizeInMb <Int64?>]`: Uso máximo permitido do tamanho do disco em MB.</span><span class="sxs-lookup"><span data-stu-id="a19a8-239">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="a19a8-240">`[LimitMaxMemoryInMb <Int64?>]`: Uso máximo permitido de memória em MB.</span><span class="sxs-lookup"><span data-stu-id="a19a8-240">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="a19a8-241">`[LimitMaxPercentageCpu <Double?>]`: Percentual máximo permitido de uso da CPU.</span><span class="sxs-lookup"><span data-stu-id="a19a8-241">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="a19a8-242">`[LinuxFxVersion <String>]`: Estrutura e versão do aplicativo Linux</span><span class="sxs-lookup"><span data-stu-id="a19a8-242">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="a19a8-243">`[LoadBalancing <SiteLoadBalancing?>]`: Balanceamento de carga do site.</span><span class="sxs-lookup"><span data-stu-id="a19a8-243">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="a19a8-244">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> para habilitar MySQL local; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-244">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a19a8-245">`[LogsDirectorySizeLimit <Int32?>]`: Http registra o limite de tamanho do diretório.</span><span class="sxs-lookup"><span data-stu-id="a19a8-245">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="a19a8-246">`[MachineKeyDecryption <String>]`: Algoritmo usado para descriptografia.</span><span class="sxs-lookup"><span data-stu-id="a19a8-246">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="a19a8-247">`[MachineKeyDecryptionKey <String>]`: Chave de descriptografia.</span><span class="sxs-lookup"><span data-stu-id="a19a8-247">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="a19a8-248">`[MachineKeyValidation <String>]`: Validação MachineKey.</span><span class="sxs-lookup"><span data-stu-id="a19a8-248">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="a19a8-249">`[MachineKeyValidationKey <String>]`: Chave de validação.</span><span class="sxs-lookup"><span data-stu-id="a19a8-249">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="a19a8-250">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Modo de pipeline gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a19a8-250">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="a19a8-251">`[ManagedServiceIdentityId <Int32?>]`: ID de Identidade de Serviço Gerenciado</span><span class="sxs-lookup"><span data-stu-id="a19a8-251">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="a19a8-252">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configura a versão mínima do TLS necessária para solicitações SSL</span><span class="sxs-lookup"><span data-stu-id="a19a8-252">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="a19a8-253">`[NetFrameworkVersion <String>]`: .NET Framework versão.</span><span class="sxs-lookup"><span data-stu-id="a19a8-253">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="a19a8-254">`[NodeVersion <String>]`: Versão do Node.js.</span><span class="sxs-lookup"><span data-stu-id="a19a8-254">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="a19a8-255">`[NumberOfWorker <Int32?>]`: Número de funcionários.</span><span class="sxs-lookup"><span data-stu-id="a19a8-255">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="a19a8-256">`[PhpVersion <String>]`: Versão do PHP.</span><span class="sxs-lookup"><span data-stu-id="a19a8-256">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="a19a8-257">`[PowerShellVersion <String>]`: Versão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a19a8-257">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="a19a8-258">`[PreWarmedInstanceCount <Int32?>]`: Número de instâncias pré-armas.</span><span class="sxs-lookup"><span data-stu-id="a19a8-258">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="a19a8-259">Essa configuração só se aplica aos Planos de Consumo e Elástica</span><span class="sxs-lookup"><span data-stu-id="a19a8-259">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="a19a8-260">`[PublishingUsername <String>]`: Nome de usuário de publicação.</span><span class="sxs-lookup"><span data-stu-id="a19a8-260">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="a19a8-261">`[PushKind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="a19a8-261">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="a19a8-262">`[PythonVersion <String>]`: Versão do Python.</span><span class="sxs-lookup"><span data-stu-id="a19a8-262">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="a19a8-263">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> se a depuração remota estiver habilitada; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-263">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a19a8-264">`[RemoteDebuggingVersion <String>]`: Versão de depuração remota.</span><span class="sxs-lookup"><span data-stu-id="a19a8-264">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="a19a8-265">`[RequestCount <Int32?>]`: Contagem de solicitação.</span><span class="sxs-lookup"><span data-stu-id="a19a8-265">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="a19a8-266">`[RequestTimeInterval <String>]`: Intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="a19a8-266">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="a19a8-267">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> se o rastreamento de solicitação estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-267">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a19a8-268">`[RequestTracingExpirationTime <DateTime?>]`: Solicitar o tempo de expiração do rastreamento.</span><span class="sxs-lookup"><span data-stu-id="a19a8-268">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="a19a8-269">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrições de segurança IP para scm.</span><span class="sxs-lookup"><span data-stu-id="a19a8-269">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="a19a8-270">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Restrições de segurança IP para scm usar principal.</span><span class="sxs-lookup"><span data-stu-id="a19a8-270">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="a19a8-271">`[ScmType <ScmType?>]`: Tipo SCM.</span><span class="sxs-lookup"><span data-stu-id="a19a8-271">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="a19a8-272">`[SlowRequestCount <Int32?>]`: Contagem de solicitação.</span><span class="sxs-lookup"><span data-stu-id="a19a8-272">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="a19a8-273">`[SlowRequestTimeInterval <String>]`: Intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="a19a8-273">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="a19a8-274">`[SlowRequestTimeTaken <String>]`: Tempo de vida.</span><span class="sxs-lookup"><span data-stu-id="a19a8-274">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="a19a8-275">`[TagWhitelistJson <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas que estão listadas em branco para uso pelo ponto de extremidade de registro por push.</span><span class="sxs-lookup"><span data-stu-id="a19a8-275">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="a19a8-276">`[TagsRequiringAuth <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas que exigem que a autenticação do usuário seja usada no ponto de extremidade de registro por push.</span><span class="sxs-lookup"><span data-stu-id="a19a8-276">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="a19a8-277">As marcas podem consistir em caracteres alfanuméricos e os seguintes: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="a19a8-277">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="a19a8-278">A validação deve ser realizada no PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="a19a8-278">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="a19a8-279">`[TracingOption <String>]`: Opções de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="a19a8-279">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="a19a8-280">`[TriggerPrivateBytesInKb <Int32?>]`: Uma regra baseada em bytes privados.</span><span class="sxs-lookup"><span data-stu-id="a19a8-280">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="a19a8-281">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Uma regra baseada em códigos de status.</span><span class="sxs-lookup"><span data-stu-id="a19a8-281">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="a19a8-282">`[Count <Int32?>]`: Contagem de solicitação.</span><span class="sxs-lookup"><span data-stu-id="a19a8-282">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="a19a8-283">`[Status <Int32?>]`: Código de status HTTP.</span><span class="sxs-lookup"><span data-stu-id="a19a8-283">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="a19a8-284">`[SubStatus <Int32?>]`: Solicitar Sub Status.</span><span class="sxs-lookup"><span data-stu-id="a19a8-284">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="a19a8-285">`[TimeInterval <String>]`: Intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="a19a8-285">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="a19a8-286">`[Win32Status <Int32?>]`: Código de erro win32.</span><span class="sxs-lookup"><span data-stu-id="a19a8-286">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="a19a8-287">`[Use32BitWorkerProcess <Boolean?>]`: para usar o processo de trabalho de <code>true</code> 32 bits; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-287">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a19a8-288">`[VirtualApplication <IVirtualApplication[]>]`: Aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="a19a8-288">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="a19a8-289">`[PhysicalPath <String>]`: Caminho físico.</span><span class="sxs-lookup"><span data-stu-id="a19a8-289">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="a19a8-290">`[PreloadEnabled <Boolean?>]`: <code>true</code> se o pré-carregamento estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-290">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="a19a8-291">`[VirtualDirectory <IVirtualDirectory[]>]`: Diretórios virtuais para aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="a19a8-291">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="a19a8-292">`[PhysicalPath <String>]`: Caminho físico.</span><span class="sxs-lookup"><span data-stu-id="a19a8-292">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="a19a8-293">`[VirtualPath <String>]`: Caminho para aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="a19a8-293">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="a19a8-294">`[VirtualPath <String>]`: Caminho virtual.</span><span class="sxs-lookup"><span data-stu-id="a19a8-294">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="a19a8-295">`[VnetName <String>]`: Nome da Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="a19a8-295">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="a19a8-296">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> se WebSocket estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-296">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a19a8-297">`[WindowsFxVersion <String>]`: Estrutura e versão do aplicativo xenónio</span><span class="sxs-lookup"><span data-stu-id="a19a8-297">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="a19a8-298">`[XManagedServiceIdentityId <Int32?>]`: Id de Identidade de Serviço Gerenciado Explícito</span><span class="sxs-lookup"><span data-stu-id="a19a8-298">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="a19a8-299">`[ContainerSize <Int32?>]`: Tamanho do contêiner de função.</span><span class="sxs-lookup"><span data-stu-id="a19a8-299">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="a19a8-300">`[DailyMemoryTimeQuota <Int32?>]`: Cota máxima permitida diária de tempo de memória (aplicável somente a aplicativos dinâmicos).</span><span class="sxs-lookup"><span data-stu-id="a19a8-300">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="a19a8-301">`[Enabled <Boolean?>]`: <code>true</code> se o aplicativo estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-301">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="a19a8-302">Definir esse valor como false desabilita o aplicativo (faz com que o aplicativo seja offline).</span><span class="sxs-lookup"><span data-stu-id="a19a8-302">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="a19a8-303">`[HostNameSslState <IHostNameSslState[]>]`: Os estados SSL do nome do host são usados para gerenciar as vinculações SSL para nomes de host do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a19a8-303">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="a19a8-304">`[HostType <HostType?>]`: Indica se o nome do host é um nome de host padrão ou de repositório.</span><span class="sxs-lookup"><span data-stu-id="a19a8-304">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="a19a8-305">`[Name <String>]`: Nomedo host.</span><span class="sxs-lookup"><span data-stu-id="a19a8-305">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="a19a8-306">`[SslState <SslState?>]`: Tipo SSL.</span><span class="sxs-lookup"><span data-stu-id="a19a8-306">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="a19a8-307">`[Thumbprint <String>]`: Impressão digital do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="a19a8-307">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="a19a8-308">`[ToUpdate <Boolean?>]`: De definida <code>true</code> como para atualizar o nome de host existente.</span><span class="sxs-lookup"><span data-stu-id="a19a8-308">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="a19a8-309">`[VirtualIP <String>]`: Endereço IP virtual atribuído ao nome do host se O SSL baseado em IP estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="a19a8-309">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="a19a8-310">`[HostNamesDisabled <Boolean?>]`: <code>true</code> para desabilitar os nomes de host públicos do aplicativo; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-310">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="a19a8-311">Se <code>true</code> , o aplicativo só está acessível por meio do processo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a19a8-311">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="a19a8-312">`[HostingEnvironmentProfileId <String>]`: ID de recurso do ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a19a8-312">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="a19a8-313">`[HttpsOnly <Boolean?>]`: HttpsOnly: configura um site para aceitar apenas solicitações https.</span><span class="sxs-lookup"><span data-stu-id="a19a8-313">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="a19a8-314">Problemas de redirecionamento para solicitações http</span><span class="sxs-lookup"><span data-stu-id="a19a8-314">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="a19a8-315">`[HyperV <Boolean?>]`: Área de ressufla do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="a19a8-315">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="a19a8-316">`[IdentityType <ManagedServiceIdentityType?>]`: Tipo de identidade de serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a19a8-316">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="a19a8-317">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: A lista de identidades atribuídas pelo usuário associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="a19a8-317">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="a19a8-318">As referências de chave do dicionário de identidade do usuário serão ARM ids de recurso no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="a19a8-318">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="a19a8-319">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="a19a8-319">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a19a8-320">`[IsXenon <Boolean?>]`: Obsoleto: área de ressufla do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="a19a8-320">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="a19a8-321">`[RedundancyMode <RedundancyMode?>]`: Modo de redundância de site</span><span class="sxs-lookup"><span data-stu-id="a19a8-321">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="a19a8-322">`[Reserved <Boolean?>]`: <code>true</code> se reservado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-322">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="a19a8-323">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> para interromper o site do SCM (KUDU) quando o aplicativo for interrompido; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-323">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="a19a8-324">O padrão é <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a19a8-324">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="a19a8-325">`[ServerFarmId <String>]`: ID de recurso do plano de Serviço de Aplicativo associado, formatado como: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="a19a8-325">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="a19a8-326">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a19a8-326">RELATED LINKS</span></span>

