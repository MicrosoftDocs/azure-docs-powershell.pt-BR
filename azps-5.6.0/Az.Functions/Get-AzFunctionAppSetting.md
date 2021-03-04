---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
ms.openlocfilehash: 5aff9382cbeac47c8d4423769d6256d34d5d109a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887520"
---
# <span data-ttu-id="a32af-101">Get-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="a32af-101">Get-AzFunctionAppSetting</span></span>

## <span data-ttu-id="a32af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a32af-102">SYNOPSIS</span></span>
<span data-ttu-id="a32af-103">Obtém configurações de aplicativo para um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="a32af-103">Gets app settings for a function app.</span></span>

## <span data-ttu-id="a32af-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a32af-104">SYNTAX</span></span>

### <span data-ttu-id="a32af-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a32af-105">ByName (Default)</span></span>
```
Get-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a32af-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="a32af-106">ByObjectInput</span></span>
```
Get-AzFunctionAppSetting -InputObject <ISite> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a32af-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a32af-107">DESCRIPTION</span></span>
<span data-ttu-id="a32af-108">Obtém configurações de aplicativo para um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="a32af-108">Gets app settings for a function app.</span></span>

## <span data-ttu-id="a32af-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a32af-109">EXAMPLES</span></span>

### <span data-ttu-id="a32af-110">Exemplo 1: Obter as configurações do aplicativo de um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="a32af-110">Example 1: Get the app settings of a function app.</span></span>
```powershell
PS C:\> Get-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a32af-111">Este comando obtém as configurações do aplicativo de um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="a32af-111">This command gets the app settings of a function app.</span></span>

## <span data-ttu-id="a32af-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a32af-112">PARAMETERS</span></span>

### <span data-ttu-id="a32af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32af-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="a32af-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a32af-114">-InputObject</span></span>
<span data-ttu-id="a32af-115">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a32af-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a32af-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a32af-116">-Name</span></span>
<span data-ttu-id="a32af-117">Nome do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="a32af-117">Name of the function app.</span></span>

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

### <span data-ttu-id="a32af-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a32af-118">-ResourceGroupName</span></span>
<span data-ttu-id="a32af-119">Nome do grupo de recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="a32af-119">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="a32af-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a32af-120">-SubscriptionId</span></span>
<span data-ttu-id="a32af-121">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a32af-121">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a32af-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a32af-122">-Confirm</span></span>
<span data-ttu-id="a32af-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a32af-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a32af-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a32af-124">-WhatIf</span></span>
<span data-ttu-id="a32af-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a32af-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a32af-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a32af-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a32af-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32af-127">CommonParameters</span></span>
<span data-ttu-id="a32af-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a32af-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32af-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a32af-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32af-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a32af-130">INPUTS</span></span>

### <span data-ttu-id="a32af-131">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="a32af-131">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="a32af-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a32af-132">OUTPUTS</span></span>

### <span data-ttu-id="a32af-133">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="a32af-133">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="a32af-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="a32af-134">NOTES</span></span>

<span data-ttu-id="a32af-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a32af-135">ALIASES</span></span>

<span data-ttu-id="a32af-136">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="a32af-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a32af-137">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a32af-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a32af-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a32af-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a32af-139">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="a32af-139">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="a32af-140">`Location <String>`: Localização do Recurso.</span><span class="sxs-lookup"><span data-stu-id="a32af-140">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="a32af-141">`CloningInfoSourceWebAppId <String>`: ARM ID de recurso do aplicativo de origem.</span><span class="sxs-lookup"><span data-stu-id="a32af-141">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="a32af-142">A ID de recurso do aplicativo é do formulário /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} para slots de produção e /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} para outros slots.</span><span class="sxs-lookup"><span data-stu-id="a32af-142">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="a32af-143">`[Kind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="a32af-143">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="a32af-144">`[Tag <IResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="a32af-144">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="a32af-145">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="a32af-145">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a32af-146">`[ClientAffinityEnabled <Boolean?>]`: para habilitar a afinidade do cliente; para parar de enviar cookies de afinidade de sessão, que encaminham solicitações de cliente na mesma sessão <code>true</code> <code>false</code> para a mesma instância.</span><span class="sxs-lookup"><span data-stu-id="a32af-146">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="a32af-147">O padrão é <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-147">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="a32af-148">`[ClientCertEnabled <Boolean?>]`: <code>true</code> para habilitar a autenticação de certificado do cliente (autenticação mútua TLS); caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-148">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="a32af-149">O padrão é <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-149">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="a32af-150">`[ClientCertExclusionPath <String>]`: caminhos de exclusão separados por vírgulas de autenticação de certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="a32af-150">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="a32af-151">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: A configuração do aplicativo substitui o aplicativo clonado.</span><span class="sxs-lookup"><span data-stu-id="a32af-151">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="a32af-152">Se especificado, essas configurações substituem as configurações clonadas do aplicativo de origem.</span><span class="sxs-lookup"><span data-stu-id="a32af-152">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="a32af-153">Caso contrário, as configurações do aplicativo de origem são mantidas.</span><span class="sxs-lookup"><span data-stu-id="a32af-153">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="a32af-154">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="a32af-154">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a32af-155">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> para clonar nomes de host personalizados do aplicativo de origem; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-155">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="a32af-156">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> para clonar o controle de origem do aplicativo de origem; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-156">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="a32af-157">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> para configurar o balanceamento de carga para o aplicativo de origem e destino.</span><span class="sxs-lookup"><span data-stu-id="a32af-157">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="a32af-158">`[CloningInfoCorrelationId <String>]`: ID de correlação da operação de clonagem.</span><span class="sxs-lookup"><span data-stu-id="a32af-158">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="a32af-159">Essa ID vincula várias operações de clonagem para usar o mesmo instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a32af-159">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="a32af-160">`[CloningInfoHostingEnvironment <String>]`: Ambiente de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a32af-160">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="a32af-161">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> para substituir o aplicativo de destino; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-161">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="a32af-162">`[CloningInfoSourceWebAppLocation <String>]`: Local do aplicativo de origem ex: Oeste dos EUA ou norte da Europa</span><span class="sxs-lookup"><span data-stu-id="a32af-162">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="a32af-163">`[CloningInfoTrafficManagerProfileId <String>]`: ARM ID de recurso do perfil do Gerenciador de Tráfego a ser usado, se existir.</span><span class="sxs-lookup"><span data-stu-id="a32af-163">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="a32af-164">A ID de recurso do Gerenciador de Tráfego é do formulário /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="a32af-164">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="a32af-165">`[CloningInfoTrafficManagerProfileName <String>]`: Nome do perfil do Gerenciador de Tráfego a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a32af-165">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="a32af-166">Isso só será necessário se o perfil do Gerenciador de Tráfego ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="a32af-166">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="a32af-167">`[Config <ISiteConfig>]`: Configuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a32af-167">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="a32af-168">`IsPushEnabled <Boolean>`: Obtém ou define um sinalizador indicando se o ponto de extremidade push está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a32af-168">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="a32af-169">`[ActionMinProcessExecutionTime <String>]`: Tempo mínimo em que o processo deve ser executado antes de executar a ação</span><span class="sxs-lookup"><span data-stu-id="a32af-169">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="a32af-170">`[ActionType <AutoHealActionType?>]`: Ação predefinida a ser tomada.</span><span class="sxs-lookup"><span data-stu-id="a32af-170">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="a32af-171">`[AlwaysOn <Boolean?>]`: <code>true</code> se Always On estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-171">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a32af-172">`[ApiDefinitionUrl <String>]`: A URL da definição da API.</span><span class="sxs-lookup"><span data-stu-id="a32af-172">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="a32af-173">`[ApiManagementConfigId <String>]`: APIM-Api Identificador.</span><span class="sxs-lookup"><span data-stu-id="a32af-173">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="a32af-174">`[AppCommandLine <String>]`: Linha de comando do aplicativo a ser lançada.</span><span class="sxs-lookup"><span data-stu-id="a32af-174">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="a32af-175">`[AppSetting <INameValuePair[]>]`: Configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a32af-175">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="a32af-176">`[Name <String>]`: Nome do par.</span><span class="sxs-lookup"><span data-stu-id="a32af-176">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="a32af-177">`[Value <String>]`: Valor do par.</span><span class="sxs-lookup"><span data-stu-id="a32af-177">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="a32af-178">`[AutoHealEnabled <Boolean?>]`: <code>true</code> se a Cura Automática estiver habilitada; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-178">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a32af-179">`[AutoSwapSlotName <String>]`: Nome do slot de troca automática.</span><span class="sxs-lookup"><span data-stu-id="a32af-179">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="a32af-180">`[ConnectionString <IConnStringInfo[]>]`: Cadeias de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="a32af-180">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="a32af-181">`[ConnectionString <String>]`: Valor da cadeia de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="a32af-181">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="a32af-182">`[Name <String>]`: Nome da cadeia de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="a32af-182">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="a32af-183">`[Type <ConnectionStringType?>]`: Tipo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a32af-183">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="a32af-184">`[CorAllowedOrigin <String[]>]`: Obtém ou define a lista de origens que devem ser permitidas para fazer chamadas de origem cruzada (por exemplo: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="a32af-184">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="a32af-185">Use "\*" para permitir tudo.</span><span class="sxs-lookup"><span data-stu-id="a32af-185">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="a32af-186">`[CorSupportCredentials <Boolean?>]`: Obtém ou define se solicitações CORS com credenciais são permitidas.</span><span class="sxs-lookup"><span data-stu-id="a32af-186">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="a32af-187">Confira         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="a32af-187">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="a32af-188">`[CustomActionExe <String>]`: Executável a ser executado.</span><span class="sxs-lookup"><span data-stu-id="a32af-188">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="a32af-189">`[CustomActionParameter <String>]`: Parâmetros para o executável.</span><span class="sxs-lookup"><span data-stu-id="a32af-189">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="a32af-190">`[DefaultDocument <String[]>]`: Documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="a32af-190">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="a32af-191">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> se o log de erros detalhado estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-191">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a32af-192">`[DocumentRoot <String>]`: Raiz do documento.</span><span class="sxs-lookup"><span data-stu-id="a32af-192">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="a32af-193">`[DynamicTagsJson <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas dinâmicas que serão avaliadas a partir de declarações do usuário no ponto de extremidade de registro por push.</span><span class="sxs-lookup"><span data-stu-id="a32af-193">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="a32af-194">`[ExperimentRampUpRule <IRampUpRule[]>]`: Lista de regras de rampa.</span><span class="sxs-lookup"><span data-stu-id="a32af-194">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="a32af-195">`[ActionHostName <String>]`: Nome do host de um slot para o qual o tráfego será redirecionado se decidir.</span><span class="sxs-lookup"><span data-stu-id="a32af-195">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="a32af-196">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="a32af-196">E.g.</span></span> <span data-ttu-id="a32af-197">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="a32af-197">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="a32af-198">`[ChangeDecisionCallbackUrl <String>]`: Algoritmo de decisão personalizado pode ser fornecido na extensão de site TiPCallback qual URL pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="a32af-198">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="a32af-199">Consulte Extensão de site TiPCallback para o scaffold e contratos.</span><span class="sxs-lookup"><span data-stu-id="a32af-199">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="a32af-200"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="a32af-200">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="a32af-201">`[ChangeIntervalInMinute <Int32?>]`: Especifica o intervalo em minutos para reavaliar ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="a32af-201">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="a32af-202">`[ChangeStep <Double?>]`: No cenário de rampa automática, esta é a etapa para adicionar/remover até atingir <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> ou         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-202">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="a32af-203">As métricas de site são verificadas a cada N minutos especificado no algoritmo de decisão .\nCustom pode ser fornecido na extensão de <code>ChangeIntervalInMinutes</code> site TiPCallback, que URL pode ser especificada em <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-203">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="a32af-204">`[MaxReroutePercentage <Double?>]`: Especifica o limite superior abaixo do qual ReroutePercentage ficará.</span><span class="sxs-lookup"><span data-stu-id="a32af-204">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="a32af-205">`[MinReroutePercentage <Double?>]`: Especifica o limite inferior acima do qual ReroutePercentage ficará.</span><span class="sxs-lookup"><span data-stu-id="a32af-205">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="a32af-206">`[Name <String>]`: Nome da regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="a32af-206">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="a32af-207">O nome recomendado seria apontar para o slot que receberá o tráfego no experimento.</span><span class="sxs-lookup"><span data-stu-id="a32af-207">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="a32af-208">`[ReroutePercentage <Double?>]`: Porcentagem do tráfego que será redirecionado para <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-208">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="a32af-209">`[FtpsState <FtpsState?>]`: Estado do serviço FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="a32af-209">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="a32af-210">`[HandlerMapping <IHandlerMapping[]>]`: Mapeamentos de manipuladores.</span><span class="sxs-lookup"><span data-stu-id="a32af-210">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="a32af-211">`[Argument <String>]`: Argumentos de linha de comando a serem passados para o processador de script.</span><span class="sxs-lookup"><span data-stu-id="a32af-211">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="a32af-212">`[Extension <String>]`: As solicitações com essa extensão serão tratadas usando o aplicativo FastCGI especificado.</span><span class="sxs-lookup"><span data-stu-id="a32af-212">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="a32af-213">`[ScriptProcessor <String>]`: O caminho absoluto para o aplicativo FastCGI.</span><span class="sxs-lookup"><span data-stu-id="a32af-213">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="a32af-214">`[HealthCheckPath <String>]`: Caminho de verificação de saúde</span><span class="sxs-lookup"><span data-stu-id="a32af-214">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="a32af-215">`[Http20Enabled <Boolean?>]`: Http20Enabled: configura um site para permitir que os clientes se conectem por http2.0</span><span class="sxs-lookup"><span data-stu-id="a32af-215">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="a32af-216">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> se o log HTTP estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-216">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a32af-217">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrições de segurança IP para principal.</span><span class="sxs-lookup"><span data-stu-id="a32af-217">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="a32af-218">`[Action <String>]`: Permitir ou negar acesso a esse intervalo DE IP.</span><span class="sxs-lookup"><span data-stu-id="a32af-218">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="a32af-219">`[Description <String>]`: Descrição da regra de restrição de IP.</span><span class="sxs-lookup"><span data-stu-id="a32af-219">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="a32af-220">`[IPAddress <String>]`: Endereço IP para o que a restrição de segurança é válida.</span><span class="sxs-lookup"><span data-stu-id="a32af-220">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="a32af-221">Ele pode estar em forma de endereço ipv4 puro (propriedade SubnetMask necessária) ou notação CIDR, como ipv4/mask (combinação de bits à frente).</span><span class="sxs-lookup"><span data-stu-id="a32af-221">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="a32af-222">Para CIDR, a propriedade SubnetMask não deve ser especificada.</span><span class="sxs-lookup"><span data-stu-id="a32af-222">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="a32af-223">`[Name <String>]`: Nome da regra de restrição de IP.</span><span class="sxs-lookup"><span data-stu-id="a32af-223">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="a32af-224">`[Priority <Int32?>]`: Prioridade da regra de restrição de IP.</span><span class="sxs-lookup"><span data-stu-id="a32af-224">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="a32af-225">`[SubnetMask <String>]`: Máscara de sub-rede para o intervalo de endereços IP para o que a restrição é válida.</span><span class="sxs-lookup"><span data-stu-id="a32af-225">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="a32af-226">`[SubnetTrafficTag <Int32?>]`: (interna) Marca de tráfego de sub-rede</span><span class="sxs-lookup"><span data-stu-id="a32af-226">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="a32af-227">`[Tag <IPFilterTag?>]`: Define para que esse filtro IP será usado.</span><span class="sxs-lookup"><span data-stu-id="a32af-227">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="a32af-228">Isso é para dar suporte à filtragem de IP em proxies.</span><span class="sxs-lookup"><span data-stu-id="a32af-228">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="a32af-229">`[VnetSubnetResourceId <String>]`: ID de recurso de rede virtual</span><span class="sxs-lookup"><span data-stu-id="a32af-229">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="a32af-230">`[VnetTrafficTag <Int32?>]`: marca de tráfego Vnet (interna)</span><span class="sxs-lookup"><span data-stu-id="a32af-230">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="a32af-231">`[JavaContainer <String>]`: Java contêiner.</span><span class="sxs-lookup"><span data-stu-id="a32af-231">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="a32af-232">`[JavaContainerVersion <String>]`: Java versão do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a32af-232">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="a32af-233">`[JavaVersion <String>]`: Java versão.</span><span class="sxs-lookup"><span data-stu-id="a32af-233">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="a32af-234">`[LimitMaxDiskSizeInMb <Int64?>]`: Uso máximo permitido do tamanho do disco em MB.</span><span class="sxs-lookup"><span data-stu-id="a32af-234">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="a32af-235">`[LimitMaxMemoryInMb <Int64?>]`: Uso máximo permitido de memória em MB.</span><span class="sxs-lookup"><span data-stu-id="a32af-235">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="a32af-236">`[LimitMaxPercentageCpu <Double?>]`: Percentual máximo permitido de uso da CPU.</span><span class="sxs-lookup"><span data-stu-id="a32af-236">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="a32af-237">`[LinuxFxVersion <String>]`: Estrutura e versão do aplicativo Linux</span><span class="sxs-lookup"><span data-stu-id="a32af-237">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="a32af-238">`[LoadBalancing <SiteLoadBalancing?>]`: Balanceamento de carga do site.</span><span class="sxs-lookup"><span data-stu-id="a32af-238">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="a32af-239">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> para habilitar MySQL local; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-239">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a32af-240">`[LogsDirectorySizeLimit <Int32?>]`: Http registra o limite de tamanho do diretório.</span><span class="sxs-lookup"><span data-stu-id="a32af-240">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="a32af-241">`[MachineKeyDecryption <String>]`: Algoritmo usado para descriptografia.</span><span class="sxs-lookup"><span data-stu-id="a32af-241">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="a32af-242">`[MachineKeyDecryptionKey <String>]`: Chave de descriptografia.</span><span class="sxs-lookup"><span data-stu-id="a32af-242">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="a32af-243">`[MachineKeyValidation <String>]`: Validação MachineKey.</span><span class="sxs-lookup"><span data-stu-id="a32af-243">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="a32af-244">`[MachineKeyValidationKey <String>]`: Chave de validação.</span><span class="sxs-lookup"><span data-stu-id="a32af-244">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="a32af-245">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Modo de pipeline gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a32af-245">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="a32af-246">`[ManagedServiceIdentityId <Int32?>]`: ID de Identidade de Serviço Gerenciado</span><span class="sxs-lookup"><span data-stu-id="a32af-246">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="a32af-247">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configura a versão mínima do TLS necessária para solicitações SSL</span><span class="sxs-lookup"><span data-stu-id="a32af-247">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="a32af-248">`[NetFrameworkVersion <String>]`: .NET Framework versão.</span><span class="sxs-lookup"><span data-stu-id="a32af-248">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="a32af-249">`[NodeVersion <String>]`: Versão do Node.js.</span><span class="sxs-lookup"><span data-stu-id="a32af-249">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="a32af-250">`[NumberOfWorker <Int32?>]`: Número de funcionários.</span><span class="sxs-lookup"><span data-stu-id="a32af-250">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="a32af-251">`[PhpVersion <String>]`: Versão do PHP.</span><span class="sxs-lookup"><span data-stu-id="a32af-251">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="a32af-252">`[PowerShellVersion <String>]`: Versão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a32af-252">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="a32af-253">`[PreWarmedInstanceCount <Int32?>]`: Número de instâncias pré-armas.</span><span class="sxs-lookup"><span data-stu-id="a32af-253">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="a32af-254">Essa configuração só se aplica aos Planos de Consumo e Elástica</span><span class="sxs-lookup"><span data-stu-id="a32af-254">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="a32af-255">`[PublishingUsername <String>]`: Nome de usuário de publicação.</span><span class="sxs-lookup"><span data-stu-id="a32af-255">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="a32af-256">`[PushKind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="a32af-256">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="a32af-257">`[PythonVersion <String>]`: Versão do Python.</span><span class="sxs-lookup"><span data-stu-id="a32af-257">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="a32af-258">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> se a depuração remota estiver habilitada; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-258">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a32af-259">`[RemoteDebuggingVersion <String>]`: Versão de depuração remota.</span><span class="sxs-lookup"><span data-stu-id="a32af-259">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="a32af-260">`[RequestCount <Int32?>]`: Contagem de solicitação.</span><span class="sxs-lookup"><span data-stu-id="a32af-260">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="a32af-261">`[RequestTimeInterval <String>]`: Intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="a32af-261">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="a32af-262">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> se o rastreamento de solicitação estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-262">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a32af-263">`[RequestTracingExpirationTime <DateTime?>]`: Solicitar o tempo de expiração do rastreamento.</span><span class="sxs-lookup"><span data-stu-id="a32af-263">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="a32af-264">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrições de segurança IP para scm.</span><span class="sxs-lookup"><span data-stu-id="a32af-264">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="a32af-265">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Restrições de segurança IP para scm usar principal.</span><span class="sxs-lookup"><span data-stu-id="a32af-265">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="a32af-266">`[ScmType <ScmType?>]`: Tipo SCM.</span><span class="sxs-lookup"><span data-stu-id="a32af-266">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="a32af-267">`[SlowRequestCount <Int32?>]`: Contagem de solicitação.</span><span class="sxs-lookup"><span data-stu-id="a32af-267">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="a32af-268">`[SlowRequestTimeInterval <String>]`: Intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="a32af-268">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="a32af-269">`[SlowRequestTimeTaken <String>]`: Tempo de vida.</span><span class="sxs-lookup"><span data-stu-id="a32af-269">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="a32af-270">`[TagWhitelistJson <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas que estão listadas em branco para uso pelo ponto de extremidade de registro por push.</span><span class="sxs-lookup"><span data-stu-id="a32af-270">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="a32af-271">`[TagsRequiringAuth <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas que exigem que a autenticação do usuário seja usada no ponto de extremidade de registro por push.</span><span class="sxs-lookup"><span data-stu-id="a32af-271">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="a32af-272">As marcas podem consistir em caracteres alfanuméricos e os seguintes: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="a32af-272">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="a32af-273">A validação deve ser realizada no PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="a32af-273">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="a32af-274">`[TracingOption <String>]`: Opções de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="a32af-274">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="a32af-275">`[TriggerPrivateBytesInKb <Int32?>]`: Uma regra baseada em bytes privados.</span><span class="sxs-lookup"><span data-stu-id="a32af-275">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="a32af-276">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Uma regra baseada em códigos de status.</span><span class="sxs-lookup"><span data-stu-id="a32af-276">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="a32af-277">`[Count <Int32?>]`: Contagem de solicitação.</span><span class="sxs-lookup"><span data-stu-id="a32af-277">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="a32af-278">`[Status <Int32?>]`: Código de status HTTP.</span><span class="sxs-lookup"><span data-stu-id="a32af-278">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="a32af-279">`[SubStatus <Int32?>]`: Solicitar Sub Status.</span><span class="sxs-lookup"><span data-stu-id="a32af-279">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="a32af-280">`[TimeInterval <String>]`: Intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="a32af-280">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="a32af-281">`[Win32Status <Int32?>]`: Código de erro win32.</span><span class="sxs-lookup"><span data-stu-id="a32af-281">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="a32af-282">`[Use32BitWorkerProcess <Boolean?>]`: para usar o processo de trabalho de <code>true</code> 32 bits; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-282">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a32af-283">`[VirtualApplication <IVirtualApplication[]>]`: Aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="a32af-283">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="a32af-284">`[PhysicalPath <String>]`: Caminho físico.</span><span class="sxs-lookup"><span data-stu-id="a32af-284">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="a32af-285">`[PreloadEnabled <Boolean?>]`: <code>true</code> se o pré-carregamento estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-285">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="a32af-286">`[VirtualDirectory <IVirtualDirectory[]>]`: Diretórios virtuais para aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="a32af-286">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="a32af-287">`[PhysicalPath <String>]`: Caminho físico.</span><span class="sxs-lookup"><span data-stu-id="a32af-287">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="a32af-288">`[VirtualPath <String>]`: Caminho para aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="a32af-288">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="a32af-289">`[VirtualPath <String>]`: Caminho virtual.</span><span class="sxs-lookup"><span data-stu-id="a32af-289">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="a32af-290">`[VnetName <String>]`: Nome da Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="a32af-290">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="a32af-291">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> se WebSocket estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-291">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="a32af-292">`[WindowsFxVersion <String>]`: Estrutura e versão do aplicativo xenónio</span><span class="sxs-lookup"><span data-stu-id="a32af-292">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="a32af-293">`[XManagedServiceIdentityId <Int32?>]`: Id de Identidade de Serviço Gerenciado Explícito</span><span class="sxs-lookup"><span data-stu-id="a32af-293">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="a32af-294">`[ContainerSize <Int32?>]`: Tamanho do contêiner de função.</span><span class="sxs-lookup"><span data-stu-id="a32af-294">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="a32af-295">`[DailyMemoryTimeQuota <Int32?>]`: Cota máxima permitida diária de tempo de memória (aplicável somente a aplicativos dinâmicos).</span><span class="sxs-lookup"><span data-stu-id="a32af-295">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="a32af-296">`[Enabled <Boolean?>]`: <code>true</code> se o aplicativo estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-296">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="a32af-297">Definir esse valor como false desabilita o aplicativo (faz com que o aplicativo seja offline).</span><span class="sxs-lookup"><span data-stu-id="a32af-297">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="a32af-298">`[HostNameSslState <IHostNameSslState[]>]`: Os estados SSL do nome do host são usados para gerenciar as vinculações SSL para nomes de host do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a32af-298">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="a32af-299">`[HostType <HostType?>]`: Indica se o nome do host é um nome de host padrão ou de repositório.</span><span class="sxs-lookup"><span data-stu-id="a32af-299">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="a32af-300">`[Name <String>]`: Nomedo host.</span><span class="sxs-lookup"><span data-stu-id="a32af-300">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="a32af-301">`[SslState <SslState?>]`: Tipo SSL.</span><span class="sxs-lookup"><span data-stu-id="a32af-301">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="a32af-302">`[Thumbprint <String>]`: Impressão digital do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="a32af-302">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="a32af-303">`[ToUpdate <Boolean?>]`: De definida <code>true</code> como para atualizar o nome de host existente.</span><span class="sxs-lookup"><span data-stu-id="a32af-303">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="a32af-304">`[VirtualIP <String>]`: Endereço IP virtual atribuído ao nome do host se O SSL baseado em IP estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="a32af-304">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="a32af-305">`[HostNamesDisabled <Boolean?>]`: <code>true</code> para desabilitar os nomes de host públicos do aplicativo; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-305">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="a32af-306">Se <code>true</code> , o aplicativo só está acessível por meio do processo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="a32af-306">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="a32af-307">`[HostingEnvironmentProfileId <String>]`: ID de recurso do ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a32af-307">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="a32af-308">`[HttpsOnly <Boolean?>]`: HttpsOnly: configura um site para aceitar apenas solicitações https.</span><span class="sxs-lookup"><span data-stu-id="a32af-308">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="a32af-309">Problemas de redirecionamento para solicitações http</span><span class="sxs-lookup"><span data-stu-id="a32af-309">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="a32af-310">`[HyperV <Boolean?>]`: Área de ressufla do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="a32af-310">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="a32af-311">`[IdentityType <ManagedServiceIdentityType?>]`: Tipo de identidade de serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a32af-311">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="a32af-312">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: A lista de identidades atribuídas pelo usuário associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="a32af-312">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="a32af-313">As referências de chave do dicionário de identidade do usuário serão ARM ids de recurso no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="a32af-313">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="a32af-314">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="a32af-314">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a32af-315">`[IsXenon <Boolean?>]`: Obsoleto: área de ressufla do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="a32af-315">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="a32af-316">`[RedundancyMode <RedundancyMode?>]`: Modo de redundância de site</span><span class="sxs-lookup"><span data-stu-id="a32af-316">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="a32af-317">`[Reserved <Boolean?>]`: <code>true</code> se reservado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-317">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="a32af-318">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> para interromper o site do SCM (KUDU) quando o aplicativo for interrompido; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-318">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="a32af-319">O padrão é <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="a32af-319">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="a32af-320">`[ServerFarmId <String>]`: ID de recurso do plano de Serviço de Aplicativo associado, formatado como: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="a32af-320">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="a32af-321">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a32af-321">RELATED LINKS</span></span>

