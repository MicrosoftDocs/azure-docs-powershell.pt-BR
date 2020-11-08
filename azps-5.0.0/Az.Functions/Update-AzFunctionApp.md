---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 08485ab1686b87c6421f456b53caa5d1deaf0c7d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115407"
---
# <span data-ttu-id="cafb5-101">Update-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="cafb5-101">Update-AzFunctionApp</span></span>

## <span data-ttu-id="cafb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cafb5-102">SYNOPSIS</span></span>
<span data-ttu-id="cafb5-103">Atualiza um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-103">Updates a function app.</span></span>

## <span data-ttu-id="cafb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cafb5-104">SYNTAX</span></span>

### <span data-ttu-id="cafb5-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="cafb5-105">ByName (Default)</span></span>
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cafb5-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="cafb5-106">ByObjectInput</span></span>
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cafb5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cafb5-107">DESCRIPTION</span></span>
<span data-ttu-id="cafb5-108">Atualiza um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-108">Updates a function app.</span></span>

## <span data-ttu-id="cafb5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cafb5-109">EXAMPLES</span></span>

### <span data-ttu-id="cafb5-110">Exemplo 1: atualizar plano de hospedagem do aplicativo da função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-110">Example 1: Update function app hosting plan.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

<span data-ttu-id="cafb5-111">Este comando atualiza o plano de Hospedagem de aplicativos da função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-111">This command updates function app hosting plan.</span></span>

### <span data-ttu-id="cafb5-112">Exemplo 2: definir uma identidade gerenciada SystemAssigned para um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-112">Example 2: Set a SystemAssigned managed identity for a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

<span data-ttu-id="cafb5-113">Este comando define uma identidade gerenciada SystemAssigned para um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-113">This command sets a SystemAssigned managed identity for a function app.</span></span>

### <span data-ttu-id="cafb5-114">Exemplo 3: atualizar as ideias do aplicativo app app.</span><span class="sxs-lookup"><span data-stu-id="cafb5-114">Example 3: Update function app Application Insights.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

<span data-ttu-id="cafb5-115">Este comando atualiza o function app insights do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cafb5-115">This command updates function app Application Insights.</span></span>

### <span data-ttu-id="cafb5-116">Exemplo 3: remover a identidade gerenciada de um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-116">Example 3: Remove managed identity from a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

<span data-ttu-id="cafb5-117">Esse comando Remove uma identidade gerenciada de um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-117">This command removes a managed identity from a function app.</span></span>

## <span data-ttu-id="cafb5-118">OS</span><span class="sxs-lookup"><span data-stu-id="cafb5-118">PARAMETERS</span></span>

### <span data-ttu-id="cafb5-119">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="cafb5-119">-ApplicationInsightsKey</span></span>
<span data-ttu-id="cafb5-120">Chave de instrumentação de ideias do aplicativo a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="cafb5-120">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafb5-121">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="cafb5-121">-ApplicationInsightsName</span></span>
<span data-ttu-id="cafb5-122">Nome do projeto insights do App existente a ser adicionado ao aplicativo function.</span><span class="sxs-lookup"><span data-stu-id="cafb5-122">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafb5-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cafb5-123">-AsJob</span></span>
<span data-ttu-id="cafb5-124">Executa o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="cafb5-124">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="cafb5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cafb5-125">-DefaultProfile</span></span>


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

### <span data-ttu-id="cafb5-126">-Identityid</span><span class="sxs-lookup"><span data-stu-id="cafb5-126">-IdentityID</span></span>
<span data-ttu-id="cafb5-127">Especifica a lista de identidades de usuário associadas ao aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-127">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="cafb5-128">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="cafb5-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="cafb5-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="cafb5-129">-IdentityType</span></span>
<span data-ttu-id="cafb5-130">Especifica o tipo de identidade usado para o aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-130">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="cafb5-131">O tipo ' nenhum ' removerá todas as identidades do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-131">The type 'None' will remove any identities from the function app.</span></span>
<span data-ttu-id="cafb5-132">Os valores aceitáveis para esse parâmetro são:-SystemAssigned-userassigned-None</span><span class="sxs-lookup"><span data-stu-id="cafb5-132">The acceptable values for this parameter are: - SystemAssigned - UserAssigned - None</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafb5-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cafb5-133">-InputObject</span></span>
<span data-ttu-id="cafb5-134">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cafb5-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cafb5-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="cafb5-135">-Name</span></span>
<span data-ttu-id="cafb5-136">O nome do aplicativo da função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-136">The name of the function app.</span></span>

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

### <span data-ttu-id="cafb5-137">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cafb5-137">-NoWait</span></span>
<span data-ttu-id="cafb5-138">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="cafb5-138">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="cafb5-139">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="cafb5-139">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cafb5-140">-PlanName</span><span class="sxs-lookup"><span data-stu-id="cafb5-140">-PlanName</span></span>
<span data-ttu-id="cafb5-141">O nome do plano de serviço.</span><span class="sxs-lookup"><span data-stu-id="cafb5-141">The name of the service plan.</span></span>

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

### <span data-ttu-id="cafb5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cafb5-142">-ResourceGroupName</span></span>
<span data-ttu-id="cafb5-143">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cafb5-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="cafb5-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cafb5-144">-SubscriptionId</span></span>
<span data-ttu-id="cafb5-145">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="cafb5-145">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="cafb5-146">-Marca</span><span class="sxs-lookup"><span data-stu-id="cafb5-146">-Tag</span></span>
<span data-ttu-id="cafb5-147">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="cafb5-147">Resource tags.</span></span>

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

### <span data-ttu-id="cafb5-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cafb5-148">-Confirm</span></span>
<span data-ttu-id="cafb5-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cafb5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cafb5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cafb5-150">-WhatIf</span></span>
<span data-ttu-id="cafb5-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cafb5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cafb5-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cafb5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cafb5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cafb5-153">CommonParameters</span></span>
<span data-ttu-id="cafb5-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cafb5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cafb5-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cafb5-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cafb5-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cafb5-156">INPUTS</span></span>

### <span data-ttu-id="cafb5-157">Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="cafb5-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="cafb5-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cafb5-158">OUTPUTS</span></span>

### <span data-ttu-id="cafb5-159">Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="cafb5-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="cafb5-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cafb5-160">NOTES</span></span>

<span data-ttu-id="cafb5-161">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cafb5-161">ALIASES</span></span>

<span data-ttu-id="cafb5-162">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="cafb5-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cafb5-163">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="cafb5-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cafb5-164">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cafb5-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cafb5-165">INPUTobject <ISite> :</span><span class="sxs-lookup"><span data-stu-id="cafb5-165">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="cafb5-166">`Location <String>`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="cafb5-166">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="cafb5-167">`CloningInfoSourceWebAppId <String>`: ID do recurso ARM do aplicativo de origem.</span><span class="sxs-lookup"><span data-stu-id="cafb5-167">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="cafb5-168">A ID do recurso do aplicativo é do formulário/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} para slots de produção e/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} para outros slots.</span><span class="sxs-lookup"><span data-stu-id="cafb5-168">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="cafb5-169">`[Kind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="cafb5-169">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="cafb5-170">`[Tag <IResourceTags>]`: Marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="cafb5-170">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="cafb5-171">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="cafb5-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cafb5-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> para habilitar a afinidade do cliente; <code>false</code> para parar de enviar cookies de afinidade de sessão, que roteiam solicitações de cliente na mesma sessão para a mesma instância.</span><span class="sxs-lookup"><span data-stu-id="cafb5-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="cafb5-173">O padrão é <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-173">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="cafb5-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> para habilitar a autenticação de certificado de cliente (autenticação mútua do TLS); caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="cafb5-175">O padrão é <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-175">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="cafb5-176">`[ClientCertExclusionPath <String>]`: caminhos de exclusão separados por vírgula de autenticação de certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="cafb5-176">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="cafb5-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Substituições de configuração de aplicativo para o aplicativo clonado.</span><span class="sxs-lookup"><span data-stu-id="cafb5-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="cafb5-178">Se especificado, essas configurações substituirão as configurações clonadas do aplicativo de origem.</span><span class="sxs-lookup"><span data-stu-id="cafb5-178">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="cafb5-179">Caso contrário, as configurações do aplicativo do aplicativo de origem serão mantidas.</span><span class="sxs-lookup"><span data-stu-id="cafb5-179">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="cafb5-180">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="cafb5-180">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cafb5-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> para clonar nomes de host personalizados do aplicativo de origem; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="cafb5-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> para clonar o controle de origem do aplicativo de origem; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="cafb5-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> para configurar o balanceamento de carga para o aplicativo de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="cafb5-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="cafb5-184">`[CloningInfoCorrelationId <String>]`: ID de correlação da operação de clonagem.</span><span class="sxs-lookup"><span data-stu-id="cafb5-184">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="cafb5-185">Esse ID une várias operações de clonagem em conjunto para usar o mesmo instantâneo.</span><span class="sxs-lookup"><span data-stu-id="cafb5-185">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="cafb5-186">`[CloningInfoHostingEnvironment <String>]`: Ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cafb5-186">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="cafb5-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> para substituir o aplicativo de destino; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="cafb5-188">`[CloningInfoSourceWebAppLocation <String>]`: Local do aplicativo de origem por exemplo: Oeste EUA ou Europa norte</span><span class="sxs-lookup"><span data-stu-id="cafb5-188">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="cafb5-189">`[CloningInfoTrafficManagerProfileId <String>]`: ID do recurso ARM do perfil do Gerenciador de tráfego a ser usado, se existir.</span><span class="sxs-lookup"><span data-stu-id="cafb5-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="cafb5-190">O ID do recurso do Gerenciador de tráfego tem o formato/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="cafb5-190">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="cafb5-191">`[CloningInfoTrafficManagerProfileName <String>]`: Nome do perfil do Gerenciador de tráfego a ser criado.</span><span class="sxs-lookup"><span data-stu-id="cafb5-191">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="cafb5-192">Isso só é necessário se o perfil do Gerenciador de tráfego ainda não existe.</span><span class="sxs-lookup"><span data-stu-id="cafb5-192">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="cafb5-193">`[Config <ISiteConfig>]`: Configuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cafb5-193">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="cafb5-194">`IsPushEnabled <Boolean>`: Obtém ou define um sinalizador que indica se o ponto de extremidade de envio está habilitado.</span><span class="sxs-lookup"><span data-stu-id="cafb5-194">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="cafb5-195">`[ActionMinProcessExecutionTime <String>]`: Tempo mínimo que o processo deve executar antes de realizar a ação</span><span class="sxs-lookup"><span data-stu-id="cafb5-195">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="cafb5-196">`[ActionType <AutoHealActionType?>]`: Ação predefinida a ser executada.</span><span class="sxs-lookup"><span data-stu-id="cafb5-196">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="cafb5-197">`[AlwaysOn <Boolean?>]`: <code>true</code> se a AlwaysOn estiver habilitada; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-197">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cafb5-198">`[ApiDefinitionUrl <String>]`: A URL da definição de API.</span><span class="sxs-lookup"><span data-stu-id="cafb5-198">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="cafb5-199">`[ApiManagementConfigId <String>]`: Identificador de APIM-Api.</span><span class="sxs-lookup"><span data-stu-id="cafb5-199">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="cafb5-200">`[AppCommandLine <String>]`: Linha de comando do aplicativo a ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="cafb5-200">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="cafb5-201">`[AppSetting <INameValuePair[]>]`: Configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cafb5-201">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="cafb5-202">`[Name <String>]`: Nome do par.</span><span class="sxs-lookup"><span data-stu-id="cafb5-202">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="cafb5-203">`[Value <String>]`: Emparelhar o valor.</span><span class="sxs-lookup"><span data-stu-id="cafb5-203">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="cafb5-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> se a Rereparo automática estiver habilitada; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cafb5-205">`[AutoSwapSlotName <String>]`: Nome do slot de troca automática.</span><span class="sxs-lookup"><span data-stu-id="cafb5-205">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="cafb5-206">`[ConnectionString <IConnStringInfo[]>]`: Cadeias de conexão.</span><span class="sxs-lookup"><span data-stu-id="cafb5-206">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="cafb5-207">`[ConnectionString <String>]`: Valor da cadeia de conexão.</span><span class="sxs-lookup"><span data-stu-id="cafb5-207">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="cafb5-208">`[Name <String>]`: Nome da cadeia de conexão.</span><span class="sxs-lookup"><span data-stu-id="cafb5-208">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="cafb5-209">`[Type <ConnectionStringType?>]`: Tipo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cafb5-209">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="cafb5-210">`[CorAllowedOrigin <String[]>]`: Obtém ou define a lista de origens que devem ser permitidas para fazer chamadas entre origens (por exemplo: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="cafb5-210">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="cafb5-211">Use "\*" para permitir tudo.</span><span class="sxs-lookup"><span data-stu-id="cafb5-211">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="cafb5-212">`[CorSupportCredentials <Boolean?>]`: Obtém ou define se as solicitações CORS com credenciais são permitidas.</span><span class="sxs-lookup"><span data-stu-id="cafb5-212">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="cafb5-213">Veja         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="cafb5-213">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="cafb5-214">`[CustomActionExe <String>]`: Executável a ser executado.</span><span class="sxs-lookup"><span data-stu-id="cafb5-214">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="cafb5-215">`[CustomActionParameter <String>]`: Parâmetros para o executável.</span><span class="sxs-lookup"><span data-stu-id="cafb5-215">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="cafb5-216">`[DefaultDocument <String[]>]`: Documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="cafb5-216">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="cafb5-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> se o log de erros detalhado estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cafb5-218">`[DocumentRoot <String>]`: Raiz do documento.</span><span class="sxs-lookup"><span data-stu-id="cafb5-218">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="cafb5-219">`[DynamicTagsJson <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas dinâmicas que serão avaliadas de declarações de usuário no ponto de extremidade de registro Push.</span><span class="sxs-lookup"><span data-stu-id="cafb5-219">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="cafb5-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: Lista de regras de rampa.</span><span class="sxs-lookup"><span data-stu-id="cafb5-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="cafb5-221">`[ActionHostName <String>]`: Nome do host de um slot ao qual o tráfego será redirecionado se for decidido.</span><span class="sxs-lookup"><span data-stu-id="cafb5-221">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="cafb5-222">:.</span><span class="sxs-lookup"><span data-stu-id="cafb5-222">E.g.</span></span> <span data-ttu-id="cafb5-223">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="cafb5-223">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="cafb5-224">`[ChangeDecisionCallbackUrl <String>]`: O algoritmo de decisão personalizado pode ser fornecido na extensão de site do TiPCallback, a URL que pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="cafb5-224">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="cafb5-225">Consulte extensão de site TiPCallback para o criam uma e contratos.</span><span class="sxs-lookup"><span data-stu-id="cafb5-225">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="cafb5-226"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="cafb5-226">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="cafb5-227">`[ChangeIntervalInMinute <Int32?>]`: Especifica o intervalo em minutos para reavaliar o ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="cafb5-227">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="cafb5-228">`[ChangeStep <Double?>]`: Em cenário de aumento automático, esta é a etapa a ser adicionada/removida <code>ReroutePercentage</code> até atingir \n <code>MinReroutePercentage</code> ou         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-228">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="cafb5-229">As métricas do site são verificadas a cada N minutos especificado no <code>ChangeIntervalInMinutes</code> algoritmo de decisão .\nCustom pode ser fornecido na extensão de site do TiPCallback na qual a URL pode ser especificada <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-229">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="cafb5-230">`[MaxReroutePercentage <Double?>]`: Especifica o limite superior abaixo do qual o ReroutePercentage permanecerá.</span><span class="sxs-lookup"><span data-stu-id="cafb5-230">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="cafb5-231">`[MinReroutePercentage <Double?>]`: Especifica o limite inferior acima do qual o ReroutePercentage permanecerá.</span><span class="sxs-lookup"><span data-stu-id="cafb5-231">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="cafb5-232">`[Name <String>]`: Nome da regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="cafb5-232">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="cafb5-233">O nome recomendado seria apontar para o slot, o que receberá o tráfego no experimento.</span><span class="sxs-lookup"><span data-stu-id="cafb5-233">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="cafb5-234">`[ReroutePercentage <Double?>]`: Porcentagem do tráfego que será redirecionado para <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-234">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="cafb5-235">`[FtpsState <FtpsState?>]`: Estado do serviço de FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="cafb5-235">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="cafb5-236">`[HandlerMapping <IHandlerMapping[]>]`: Mapeamentos de manipuladores.</span><span class="sxs-lookup"><span data-stu-id="cafb5-236">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="cafb5-237">`[Argument <String>]`: Argumentos de linha de comando a serem passados para o processador de script.</span><span class="sxs-lookup"><span data-stu-id="cafb5-237">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="cafb5-238">`[Extension <String>]`: As solicitações com essa extensão serão manipuladas usando o aplicativo FastCGI especificado.</span><span class="sxs-lookup"><span data-stu-id="cafb5-238">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="cafb5-239">`[ScriptProcessor <String>]`: O caminho absoluto para o aplicativo FastCGI.</span><span class="sxs-lookup"><span data-stu-id="cafb5-239">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="cafb5-240">`[HealthCheckPath <String>]`: Caminho da verificação de integridade</span><span class="sxs-lookup"><span data-stu-id="cafb5-240">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="cafb5-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: configura um site da Web para permitir que os clientes se conectem via http 2.0</span><span class="sxs-lookup"><span data-stu-id="cafb5-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="cafb5-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> se o log http estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cafb5-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrições de segurança IP para Main.</span><span class="sxs-lookup"><span data-stu-id="cafb5-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="cafb5-244">`[Action <String>]`: Permitir ou negar acesso para este intervalo de IP.</span><span class="sxs-lookup"><span data-stu-id="cafb5-244">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="cafb5-245">`[Description <String>]`: Descrição da regra de restrição de IP.</span><span class="sxs-lookup"><span data-stu-id="cafb5-245">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="cafb5-246">`[IPAddress <String>]`: Endereço IP para o qual a restrição de segurança é válida.</span><span class="sxs-lookup"><span data-stu-id="cafb5-246">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="cafb5-247">Ela pode ser em forma de endereço IPv4 puro (Propriedade obrigatório submáscara de submáscara) ou de notação CIDR, como IPv4/máscara (correspondência de bit à esquerda).</span><span class="sxs-lookup"><span data-stu-id="cafb5-247">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="cafb5-248">Para CIDR, a propriedade Máscara_de_Sub-máscara não deve ser especificada.</span><span class="sxs-lookup"><span data-stu-id="cafb5-248">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="cafb5-249">`[Name <String>]`: Nome da regra de restrição de IP.</span><span class="sxs-lookup"><span data-stu-id="cafb5-249">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="cafb5-250">`[Priority <Int32?>]`: Prioridade da regra de restrição de IP.</span><span class="sxs-lookup"><span data-stu-id="cafb5-250">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="cafb5-251">`[SubnetMask <String>]`: Máscara de sub-rede para o intervalo de endereços IP para o qual a restrição é válida.</span><span class="sxs-lookup"><span data-stu-id="cafb5-251">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="cafb5-252">`[SubnetTrafficTag <Int32?>]`: marca de tráfego de sub-rede (interna)</span><span class="sxs-lookup"><span data-stu-id="cafb5-252">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="cafb5-253">`[Tag <IPFilterTag?>]`: Define para que esse filtro de IP será usado.</span><span class="sxs-lookup"><span data-stu-id="cafb5-253">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="cafb5-254">Isso é para dar suporte à filtragem de IP em proxies.</span><span class="sxs-lookup"><span data-stu-id="cafb5-254">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="cafb5-255">`[VnetSubnetResourceId <String>]`: ID do recurso de rede virtual</span><span class="sxs-lookup"><span data-stu-id="cafb5-255">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="cafb5-256">`[VnetTrafficTag <Int32?>]`: marca de tráfego de rede virtual (interna)</span><span class="sxs-lookup"><span data-stu-id="cafb5-256">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="cafb5-257">`[JavaContainer <String>]`: Contêiner Java.</span><span class="sxs-lookup"><span data-stu-id="cafb5-257">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="cafb5-258">`[JavaContainerVersion <String>]`: Versão do contêiner Java.</span><span class="sxs-lookup"><span data-stu-id="cafb5-258">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="cafb5-259">`[JavaVersion <String>]`: Versão Java.</span><span class="sxs-lookup"><span data-stu-id="cafb5-259">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="cafb5-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Uso máximo de tamanho de disco permitido em MB.</span><span class="sxs-lookup"><span data-stu-id="cafb5-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="cafb5-261">`[LimitMaxMemoryInMb <Int64?>]`: Máximo de uso de memória permitido em MB.</span><span class="sxs-lookup"><span data-stu-id="cafb5-261">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="cafb5-262">`[LimitMaxPercentageCpu <Double?>]`: Porcentagem máxima de uso de CPU permitida.</span><span class="sxs-lookup"><span data-stu-id="cafb5-262">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="cafb5-263">`[LinuxFxVersion <String>]`: Estrutura e versão do aplicativo Linux</span><span class="sxs-lookup"><span data-stu-id="cafb5-263">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="cafb5-264">`[LoadBalancing <SiteLoadBalancing?>]`: Balanceamento de carga do site.</span><span class="sxs-lookup"><span data-stu-id="cafb5-264">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="cafb5-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> para habilitar o MySQL local; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cafb5-266">`[LogsDirectorySizeLimit <Int32?>]`: O limite de tamanho do diretório de logs HTTP.</span><span class="sxs-lookup"><span data-stu-id="cafb5-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="cafb5-267">`[MachineKeyDecryption <String>]`: Algoritmo usado para decodificação.</span><span class="sxs-lookup"><span data-stu-id="cafb5-267">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="cafb5-268">`[MachineKeyDecryptionKey <String>]`: Chave de descriptografia.</span><span class="sxs-lookup"><span data-stu-id="cafb5-268">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="cafb5-269">`[MachineKeyValidation <String>]`: Validação de MachineKey.</span><span class="sxs-lookup"><span data-stu-id="cafb5-269">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="cafb5-270">`[MachineKeyValidationKey <String>]`: Chave de validação.</span><span class="sxs-lookup"><span data-stu-id="cafb5-270">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="cafb5-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Modo de pipeline gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cafb5-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="cafb5-272">`[ManagedServiceIdentityId <Int32?>]`: ID de identidade do serviço gerenciado</span><span class="sxs-lookup"><span data-stu-id="cafb5-272">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="cafb5-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configura a versão mínima do TLS necessária para solicitações SSL</span><span class="sxs-lookup"><span data-stu-id="cafb5-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="cafb5-274">`[NetFrameworkVersion <String>]`: Versão do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="cafb5-274">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="cafb5-275">`[NodeVersion <String>]`: Versão do Node.js.</span><span class="sxs-lookup"><span data-stu-id="cafb5-275">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="cafb5-276">`[NumberOfWorker <Int32?>]`: Número de trabalhadores.</span><span class="sxs-lookup"><span data-stu-id="cafb5-276">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="cafb5-277">`[PhpVersion <String>]`: Versão do PHP.</span><span class="sxs-lookup"><span data-stu-id="cafb5-277">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="cafb5-278">`[PowerShellVersion <String>]`: Versão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cafb5-278">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="cafb5-279">`[PreWarmedInstanceCount <Int32?>]`: Número de instâncias prequentes.</span><span class="sxs-lookup"><span data-stu-id="cafb5-279">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="cafb5-280">Essa configuração aplica-se somente aos planos de consumo e elástico</span><span class="sxs-lookup"><span data-stu-id="cafb5-280">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="cafb5-281">`[PublishingUsername <String>]`: Publicando o nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="cafb5-281">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="cafb5-282">`[PushKind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="cafb5-282">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="cafb5-283">`[PythonVersion <String>]`: Versão do Python.</span><span class="sxs-lookup"><span data-stu-id="cafb5-283">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="cafb5-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> se a depuração remota estiver habilitada; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cafb5-285">`[RemoteDebuggingVersion <String>]`: Versão de depuração remota.</span><span class="sxs-lookup"><span data-stu-id="cafb5-285">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="cafb5-286">`[RequestCount <Int32?>]`: Contagem de solicitações.</span><span class="sxs-lookup"><span data-stu-id="cafb5-286">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="cafb5-287">`[RequestTimeInterval <String>]`: Intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="cafb5-287">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="cafb5-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> se o rastreamento de solicitação estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cafb5-289">`[RequestTracingExpirationTime <DateTime?>]`: Solicitação de tempo de expiração do rastreamento.</span><span class="sxs-lookup"><span data-stu-id="cafb5-289">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="cafb5-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Restrições de segurança IP para SCM.</span><span class="sxs-lookup"><span data-stu-id="cafb5-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="cafb5-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Restrições de segurança IP para que o SCM use Main.</span><span class="sxs-lookup"><span data-stu-id="cafb5-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="cafb5-292">`[ScmType <ScmType?>]`: Tipo de SCM.</span><span class="sxs-lookup"><span data-stu-id="cafb5-292">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="cafb5-293">`[SlowRequestCount <Int32?>]`: Contagem de solicitações.</span><span class="sxs-lookup"><span data-stu-id="cafb5-293">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="cafb5-294">`[SlowRequestTimeInterval <String>]`: Intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="cafb5-294">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="cafb5-295">`[SlowRequestTimeTaken <String>]`: Tempo deutilizado.</span><span class="sxs-lookup"><span data-stu-id="cafb5-295">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="cafb5-296">`[TagWhitelistJson <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas que são brancas para uso pelo ponto de extremidade de registro Push.</span><span class="sxs-lookup"><span data-stu-id="cafb5-296">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="cafb5-297">`[TagsRequiringAuth <String>]`: Obtém ou define uma cadeia de caracteres JSON que contém uma lista de marcas que exigem que a autenticação do usuário seja usada no ponto de extremidade de registro Push.</span><span class="sxs-lookup"><span data-stu-id="cafb5-297">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="cafb5-298">As marcas podem consistir em caracteres alfanuméricos e o seguinte: ' _ ', ' @ ', ' # ', '. ', ': ', '-'.</span><span class="sxs-lookup"><span data-stu-id="cafb5-298">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="cafb5-299">A validação deve ser realizada no PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="cafb5-299">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="cafb5-300">`[TracingOption <String>]`: Opções de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="cafb5-300">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="cafb5-301">`[TriggerPrivateBytesInKb <Int32?>]`: Uma regra com base em bytes particulares.</span><span class="sxs-lookup"><span data-stu-id="cafb5-301">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="cafb5-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Uma regra com base em códigos de status.</span><span class="sxs-lookup"><span data-stu-id="cafb5-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="cafb5-303">`[Count <Int32?>]`: Contagem de solicitações.</span><span class="sxs-lookup"><span data-stu-id="cafb5-303">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="cafb5-304">`[Status <Int32?>]`: Código de status HTTP.</span><span class="sxs-lookup"><span data-stu-id="cafb5-304">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="cafb5-305">`[SubStatus <Int32?>]`: Solicitação de status de subscrição.</span><span class="sxs-lookup"><span data-stu-id="cafb5-305">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="cafb5-306">`[TimeInterval <String>]`: Intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="cafb5-306">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="cafb5-307">`[Win32Status <Int32?>]`: Código de erro Win32.</span><span class="sxs-lookup"><span data-stu-id="cafb5-307">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="cafb5-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> para usar o processo de trabalho de 32 bits; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cafb5-309">`[VirtualApplication <IVirtualApplication[]>]`: Aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="cafb5-309">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="cafb5-310">`[PhysicalPath <String>]`: Caminho físico.</span><span class="sxs-lookup"><span data-stu-id="cafb5-310">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="cafb5-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> se o pré-carregamento estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="cafb5-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Diretórios virtuais para o aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="cafb5-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="cafb5-313">`[PhysicalPath <String>]`: Caminho físico.</span><span class="sxs-lookup"><span data-stu-id="cafb5-313">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="cafb5-314">`[VirtualPath <String>]`: Caminho para o aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="cafb5-314">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="cafb5-315">`[VirtualPath <String>]`: Caminho virtual.</span><span class="sxs-lookup"><span data-stu-id="cafb5-315">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="cafb5-316">`[VnetName <String>]`: Nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="cafb5-316">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="cafb5-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> se WebSocket estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cafb5-318">`[WindowsFxVersion <String>]`: A estrutura e a versão do aplicativo Xenon</span><span class="sxs-lookup"><span data-stu-id="cafb5-318">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="cafb5-319">`[XManagedServiceIdentityId <Int32?>]`: ID de identidade do serviço explicitamente gerenciado</span><span class="sxs-lookup"><span data-stu-id="cafb5-319">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="cafb5-320">`[ContainerSize <Int32?>]`: Tamanho do contêiner da função.</span><span class="sxs-lookup"><span data-stu-id="cafb5-320">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="cafb5-321">`[DailyMemoryTimeQuota <Int32?>]`: Cota máxima permitida diária de tempo de memória (aplicável somente em aplicativos dinâmicos).</span><span class="sxs-lookup"><span data-stu-id="cafb5-321">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="cafb5-322">`[Enabled <Boolean?>]`: <code>true</code> se o aplicativo estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-322">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="cafb5-323">Definir esse valor como false desabilita o aplicativo (usa o aplicativo offline).</span><span class="sxs-lookup"><span data-stu-id="cafb5-323">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="cafb5-324">`[HostNameSslState <IHostNameSslState[]>]`: Os Estados SSL do nome do host são usados para gerenciar as associações SSL dos nomes de hosts do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cafb5-324">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="cafb5-325">`[HostType <HostType?>]`: Indica se o nome do host é um nome de host padrão ou de repositório.</span><span class="sxs-lookup"><span data-stu-id="cafb5-325">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="cafb5-326">`[Name <String>]`Hostname.</span><span class="sxs-lookup"><span data-stu-id="cafb5-326">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="cafb5-327">`[SslState <SslState?>]`: Tipo de SSL.</span><span class="sxs-lookup"><span data-stu-id="cafb5-327">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="cafb5-328">`[Thumbprint <String>]`: Impressão digital do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="cafb5-328">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="cafb5-329">`[ToUpdate <Boolean?>]`: Definido como <code>true</code> para atualizar o nome do host existente.</span><span class="sxs-lookup"><span data-stu-id="cafb5-329">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="cafb5-330">`[VirtualIP <String>]`: Endereço IP virtual atribuído ao nome do host se a SSL baseado em IP estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="cafb5-330">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="cafb5-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> para desabilitar os nomes de host públicos do aplicativo; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="cafb5-332">Se <code>true</code> , o aplicativo estará acessível somente por meio do processo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="cafb5-332">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="cafb5-333">`[HostingEnvironmentProfileId <String>]`: ID do recurso do ambiente do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cafb5-333">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="cafb5-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: configura um site da Web para aceitar apenas solicitações HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cafb5-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="cafb5-335">Problemas de redirecionamento para solicitações http</span><span class="sxs-lookup"><span data-stu-id="cafb5-335">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="cafb5-336">`[HyperV <Boolean?>]`: Área restrita do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="cafb5-336">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="cafb5-337">`[IdentityType <ManagedServiceIdentityType?>]`: Tipo de identidade de serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cafb5-337">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="cafb5-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: A lista de identidades atribuídas pelo usuário associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="cafb5-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="cafb5-339">As referências de chave de dicionário de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="cafb5-339">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="cafb5-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="cafb5-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cafb5-341">`[IsXenon <Boolean?>]`: Obsoleto: área restrita do Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="cafb5-341">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="cafb5-342">`[RedundancyMode <RedundancyMode?>]`: Modo de redundância do site</span><span class="sxs-lookup"><span data-stu-id="cafb5-342">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="cafb5-343">`[Reserved <Boolean?>]`: <code>true</code> se reservada; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-343">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="cafb5-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> para interromper o site do SCM (KUDU) quando o aplicativo for interrompido; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="cafb5-345">O padrão é <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cafb5-345">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="cafb5-346">`[ServerFarmId <String>]`: ID do recurso do plano do serviço de aplicativo associado, formatada como: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="cafb5-346">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="cafb5-347">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cafb5-347">RELATED LINKS</span></span>

