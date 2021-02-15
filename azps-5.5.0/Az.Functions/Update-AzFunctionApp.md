---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 08485ab1686b87c6421f456b53caa5d1deaf0c7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113817"
---
# <span data-ttu-id="b4904-101">Update-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="b4904-101">Update-AzFunctionApp</span></span>

## <span data-ttu-id="b4904-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4904-102">SYNOPSIS</span></span>
<span data-ttu-id="b4904-103">Atualiza um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-103">Updates a function app.</span></span>

## <span data-ttu-id="b4904-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4904-104">SYNTAX</span></span>

### <span data-ttu-id="b4904-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="b4904-105">ByName (Default)</span></span>
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b4904-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="b4904-106">ByObjectInput</span></span>
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b4904-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4904-107">DESCRIPTION</span></span>
<span data-ttu-id="b4904-108">Atualiza um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-108">Updates a function app.</span></span>

## <span data-ttu-id="b4904-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4904-109">EXAMPLES</span></span>

### <span data-ttu-id="b4904-110">Exemplo 1: Atualizar o plano de hospedagem de aplicativos de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-110">Example 1: Update function app hosting plan.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

<span data-ttu-id="b4904-111">Este comando atualiza o plano de hospedagem de aplicativos de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-111">This command updates function app hosting plan.</span></span>

### <span data-ttu-id="b4904-112">Exemplo 2: Definir uma identidade gerenciada atribuída pelo SystemAssigned para um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-112">Example 2: Set a SystemAssigned managed identity for a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

<span data-ttu-id="b4904-113">Esse comando define uma identidade gerenciada atribuída pelo SystemAssigned para um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-113">This command sets a SystemAssigned managed identity for a function app.</span></span>

### <span data-ttu-id="b4904-114">Exemplo 3: Atualizar insights do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-114">Example 3: Update function app Application Insights.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

<span data-ttu-id="b4904-115">Este comando atualiza o aplicativo Application Insights.</span><span class="sxs-lookup"><span data-stu-id="b4904-115">This command updates function app Application Insights.</span></span>

### <span data-ttu-id="b4904-116">Exemplo 3: remover a identidade gerenciada de um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-116">Example 3: Remove managed identity from a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

<span data-ttu-id="b4904-117">Esse comando remove uma identidade gerenciada de um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-117">This command removes a managed identity from a function app.</span></span>

## <span data-ttu-id="b4904-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4904-118">PARAMETERS</span></span>

### <span data-ttu-id="b4904-119">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="b4904-119">-ApplicationInsightsKey</span></span>
<span data-ttu-id="b4904-120">Tecla de instrumentação do Insights do Aplicativo a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="b4904-120">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="b4904-121">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="b4904-121">-ApplicationInsightsName</span></span>
<span data-ttu-id="b4904-122">Nome do projeto Insights do Aplicativo existente a ser adicionado ao aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-122">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="b4904-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4904-123">-AsJob</span></span>
<span data-ttu-id="b4904-124">Executa o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b4904-124">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="b4904-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4904-125">-DefaultProfile</span></span>


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

### <span data-ttu-id="b4904-126">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="b4904-126">-IdentityID</span></span>
<span data-ttu-id="b4904-127">Especifica a lista de identidades de usuário associadas ao aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-127">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="b4904-128">As referências de identidade do usuário serão IDs de recurso ARM no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="b4904-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="b4904-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b4904-129">-IdentityType</span></span>
<span data-ttu-id="b4904-130">Especifica o tipo de identidade usado para o aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-130">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="b4904-131">O tipo "Nenhum" removerá as identidades do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-131">The type 'None' will remove any identities from the function app.</span></span>
<span data-ttu-id="b4904-132">Os valores aceitáveis para este parâmetro são: - SystemAssigned - UserAssigned - None</span><span class="sxs-lookup"><span data-stu-id="b4904-132">The acceptable values for this parameter are: - SystemAssigned - UserAssigned - None</span></span>

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

### <span data-ttu-id="b4904-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4904-133">-InputObject</span></span>
<span data-ttu-id="b4904-134">Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="b4904-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b4904-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4904-135">-Name</span></span>
<span data-ttu-id="b4904-136">O nome do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-136">The name of the function app.</span></span>

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

### <span data-ttu-id="b4904-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b4904-137">-NoWait</span></span>
<span data-ttu-id="b4904-138">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="b4904-138">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="b4904-139">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="b4904-139">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="b4904-140">-PlanName</span><span class="sxs-lookup"><span data-stu-id="b4904-140">-PlanName</span></span>
<span data-ttu-id="b4904-141">O nome do plano de serviço.</span><span class="sxs-lookup"><span data-stu-id="b4904-141">The name of the service plan.</span></span>

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

### <span data-ttu-id="b4904-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4904-142">-ResourceGroupName</span></span>
<span data-ttu-id="b4904-143">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4904-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="b4904-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4904-144">-SubscriptionId</span></span>
<span data-ttu-id="b4904-145">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4904-145">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="b4904-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4904-146">-Tag</span></span>
<span data-ttu-id="b4904-147">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="b4904-147">Resource tags.</span></span>

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

### <span data-ttu-id="b4904-148">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b4904-148">-Confirm</span></span>
<span data-ttu-id="b4904-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4904-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4904-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4904-150">-WhatIf</span></span>
<span data-ttu-id="b4904-151">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b4904-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4904-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4904-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4904-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4904-153">CommonParameters</span></span>
<span data-ttu-id="b4904-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4904-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4904-155">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4904-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4904-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="b4904-156">INPUTS</span></span>

### <span data-ttu-id="b4904-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="b4904-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="b4904-158">Saídas</span><span class="sxs-lookup"><span data-stu-id="b4904-158">OUTPUTS</span></span>

### <span data-ttu-id="b4904-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="b4904-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="b4904-160">Notas</span><span class="sxs-lookup"><span data-stu-id="b4904-160">NOTES</span></span>

<span data-ttu-id="b4904-161">Aliases</span><span class="sxs-lookup"><span data-stu-id="b4904-161">ALIASES</span></span>

<span data-ttu-id="b4904-162">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="b4904-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b4904-163">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b4904-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b4904-164">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b4904-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b4904-165">INPUTOBJECT: <ISite></span><span class="sxs-lookup"><span data-stu-id="b4904-165">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="b4904-166">`Location <String>`: Localização do Recurso.</span><span class="sxs-lookup"><span data-stu-id="b4904-166">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="b4904-167">`CloningInfoSourceWebAppId <String>`: ID do recurso ARM do aplicativo de origem.</span><span class="sxs-lookup"><span data-stu-id="b4904-167">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="b4904-168">A ID do recurso de aplicativo é do formulário /assinaturas/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} para slots de produção e /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} para outros slots.</span><span class="sxs-lookup"><span data-stu-id="b4904-168">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="b4904-169">`[Kind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="b4904-169">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="b4904-170">`[Tag <IResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="b4904-170">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="b4904-171">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="b4904-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b4904-172">`[ClientAffinityEnabled <Boolean?>]`: para habilitar a afiliação do cliente; para parar de enviar cookies de afiliação de sessão, que roteam solicitações de cliente na mesma sessão <code>true</code> <code>false</code> para a mesma instância.</span><span class="sxs-lookup"><span data-stu-id="b4904-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="b4904-173">O padrão é <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-173">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="b4904-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> para habilitar a autenticação de certificado do cliente (autenticação mútuo TLS); caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="b4904-175">O padrão é <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-175">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="b4904-176">`[ClientCertExclusionPath <String>]`: caminhos de exclusão separados por vírgulas separados por autenticação de certificado do cliente</span><span class="sxs-lookup"><span data-stu-id="b4904-176">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="b4904-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: A configuração do aplicativo substitui o aplicativo clonado.</span><span class="sxs-lookup"><span data-stu-id="b4904-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="b4904-178">Se especificado, essas configurações substituem as configurações clonadas do aplicativo de origem.</span><span class="sxs-lookup"><span data-stu-id="b4904-178">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="b4904-179">Caso contrário, as configurações do aplicativo de origem são mantidas.</span><span class="sxs-lookup"><span data-stu-id="b4904-179">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="b4904-180">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="b4904-180">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b4904-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> para clonar nomes de host personalizados do aplicativo de origem; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="b4904-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> para clonar o controle de origem do aplicativo de origem; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="b4904-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> para configurar o balanceamento de carga para o aplicativo de origem e destino.</span><span class="sxs-lookup"><span data-stu-id="b4904-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="b4904-184">`[CloningInfoCorrelationId <String>]`: ID de correlação da operação de clonagem.</span><span class="sxs-lookup"><span data-stu-id="b4904-184">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="b4904-185">Esta ID vincula várias operações de clonagem para usar o mesmo instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b4904-185">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="b4904-186">`[CloningInfoHostingEnvironment <String>]`: Ambiente de Serviço de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b4904-186">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="b4904-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> para substituir o aplicativo de destino; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="b4904-188">`[CloningInfoSourceWebAppLocation <String>]`: localização do aplicativo de origem, por ex: Oeste dos EUA ou Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="b4904-188">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="b4904-189">`[CloningInfoTrafficManagerProfileId <String>]`: ID do recurso ARM do perfil do Gerenciador de Tráfego a ser usado, se ele existir.</span><span class="sxs-lookup"><span data-stu-id="b4904-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="b4904-190">A ID de recurso do Gerenciador de Tráfego é do formulário /assinaturas/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="b4904-190">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="b4904-191">`[CloningInfoTrafficManagerProfileName <String>]`: Nome do perfil do Gerenciador de Tráfego para criar.</span><span class="sxs-lookup"><span data-stu-id="b4904-191">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="b4904-192">Isso só será necessário se o perfil do Gerenciador de Tráfego ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="b4904-192">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="b4904-193">`[Config <ISiteConfig>]`: Configuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b4904-193">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="b4904-194">`IsPushEnabled <Boolean>`: Obtém ou define um sinalizador indicando se o ponto de extremidade push está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b4904-194">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="b4904-195">`[ActionMinProcessExecutionTime <String>]`: Tempo mínimo que o processo deve executar antes de executar a ação</span><span class="sxs-lookup"><span data-stu-id="b4904-195">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="b4904-196">`[ActionType <AutoHealActionType?>]`: Ação predefinida a ser tomada.</span><span class="sxs-lookup"><span data-stu-id="b4904-196">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="b4904-197">`[AlwaysOn <Boolean?>]`: <code>true</code> se Always On estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-197">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b4904-198">`[ApiDefinitionUrl <String>]`: A URL da definição da API.</span><span class="sxs-lookup"><span data-stu-id="b4904-198">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="b4904-199">`[ApiManagementConfigId <String>]`: APIM-Api Identificador.</span><span class="sxs-lookup"><span data-stu-id="b4904-199">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="b4904-200">`[AppCommandLine <String>]`: Linha de comando do aplicativo para iniciar.</span><span class="sxs-lookup"><span data-stu-id="b4904-200">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="b4904-201">`[AppSetting <INameValuePair[]>]`: Configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b4904-201">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="b4904-202">`[Name <String>]`: Nome do par.</span><span class="sxs-lookup"><span data-stu-id="b4904-202">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="b4904-203">`[Value <String>]`: Valor do par.</span><span class="sxs-lookup"><span data-stu-id="b4904-203">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="b4904-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> se AutoCarros estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b4904-205">`[AutoSwapSlotName <String>]`: nome do slot de troca automática.</span><span class="sxs-lookup"><span data-stu-id="b4904-205">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="b4904-206">`[ConnectionString <IConnStringInfo[]>]`: cadeias de conexão.</span><span class="sxs-lookup"><span data-stu-id="b4904-206">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="b4904-207">`[ConnectionString <String>]`: valor da cadeia de conexão.</span><span class="sxs-lookup"><span data-stu-id="b4904-207">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="b4904-208">`[Name <String>]`: Nome da cadeia de conexão.</span><span class="sxs-lookup"><span data-stu-id="b4904-208">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="b4904-209">`[Type <ConnectionStringType?>]`: Tipo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b4904-209">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="b4904-210">`[CorAllowedOrigin <String[]>]`: obtém ou define a lista de origens que devem ser permitidas para fazer chamadas de origem cruzada (por exemplo: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="b4904-210">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="b4904-211">Use "\*" para permitir tudo.</span><span class="sxs-lookup"><span data-stu-id="b4904-211">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="b4904-212">`[CorSupportCredentials <Boolean?>]`: Obtém ou define se as solicitações do CORS com credenciais são permitidas.</span><span class="sxs-lookup"><span data-stu-id="b4904-212">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="b4904-213">Veja         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="b4904-213">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="b4904-214">`[CustomActionExe <String>]`: Executável para ser executado.</span><span class="sxs-lookup"><span data-stu-id="b4904-214">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="b4904-215">`[CustomActionParameter <String>]`: Parâmetros para o executável.</span><span class="sxs-lookup"><span data-stu-id="b4904-215">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="b4904-216">`[DefaultDocument <String[]>]`: Documentos padrão.</span><span class="sxs-lookup"><span data-stu-id="b4904-216">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="b4904-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> se o log de erros detalhado estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b4904-218">`[DocumentRoot <String>]`: raiz do documento.</span><span class="sxs-lookup"><span data-stu-id="b4904-218">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="b4904-219">`[DynamicTagsJson <String>]`: Obtém ou define uma cadeia de caracteres JSON contendo uma lista de marcas dinâmicas que serão avaliadas a partir de reclamações de usuários no ponto de extremidade de registro por push.</span><span class="sxs-lookup"><span data-stu-id="b4904-219">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="b4904-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: Lista de regras de aumento.</span><span class="sxs-lookup"><span data-stu-id="b4904-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="b4904-221">`[ActionHostName <String>]`: Nome do host de um slot para o qual o tráfego será redirecionado se decidir.</span><span class="sxs-lookup"><span data-stu-id="b4904-221">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="b4904-222">E.g.</span><span class="sxs-lookup"><span data-stu-id="b4904-222">E.g.</span></span> <span data-ttu-id="b4904-223">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="b4904-223">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="b4904-224">`[ChangeDecisionCallbackUrl <String>]`: Algoritmo de decisão personalizado pode ser fornecido na extensão de site TiPCallback qual URL pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="b4904-224">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="b4904-225">Consulte a extensão do site TiPCallback para o cadapasta e contratos.</span><span class="sxs-lookup"><span data-stu-id="b4904-225">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="b4904-226"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="b4904-226">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="b4904-227">`[ChangeIntervalInMinute <Int32?>]`: Especifica o intervalo em minutos para reavaliar ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="b4904-227">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="b4904-228">`[ChangeStep <Double?>]`: No cenário de aumento automático, esta é a etapa a ser seguida para adicionar/remover até <code>ReroutePercentage</code> atingir \n <code>MinReroutePercentage</code> ou         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-228">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="b4904-229">As métricas do site são verificadas a cada N minutos especificado no algoritmo de decisão .\nCustom pode ser fornecido na extensão do site TiPCallback em que a URL pode ser <code>ChangeIntervalInMinutes</code> <code>ChangeDecisionCallbackUrl</code> especificada.</span><span class="sxs-lookup"><span data-stu-id="b4904-229">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="b4904-230">`[MaxReroutePercentage <Double?>]`: especifica o limite superior abaixo do qual o RedirecionamentoPercentage ficará.</span><span class="sxs-lookup"><span data-stu-id="b4904-230">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="b4904-231">`[MinReroutePercentage <Double?>]`: especifica o limite inferior acima do qual o RedirecionamentoPercentagem ficará.</span><span class="sxs-lookup"><span data-stu-id="b4904-231">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="b4904-232">`[Name <String>]`: Nome da regra de roteamento.</span><span class="sxs-lookup"><span data-stu-id="b4904-232">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="b4904-233">O nome recomendado seria apontar para o slot que receberá o tráfego no experimento.</span><span class="sxs-lookup"><span data-stu-id="b4904-233">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="b4904-234">`[ReroutePercentage <Double?>]`: porcentagem do tráfego para o qual será <code>ActionHostName</code> redirecionado.</span><span class="sxs-lookup"><span data-stu-id="b4904-234">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="b4904-235">`[FtpsState <FtpsState?>]`: Estado do serviço FTP/FTPS</span><span class="sxs-lookup"><span data-stu-id="b4904-235">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="b4904-236">`[HandlerMapping <IHandlerMapping[]>]`: Mapeamentos de manipuladores.</span><span class="sxs-lookup"><span data-stu-id="b4904-236">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="b4904-237">`[Argument <String>]`: argumentos de linha de comando a serem passados para o processador de script.</span><span class="sxs-lookup"><span data-stu-id="b4904-237">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="b4904-238">`[Extension <String>]`: As solicitações com essa extensão serão tratadas usando o aplicativo FastCGI especificado.</span><span class="sxs-lookup"><span data-stu-id="b4904-238">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="b4904-239">`[ScriptProcessor <String>]`: o caminho absoluto para o aplicativo FastCGI.</span><span class="sxs-lookup"><span data-stu-id="b4904-239">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="b4904-240">`[HealthCheckPath <String>]`: Caminho de verificação de saúde</span><span class="sxs-lookup"><span data-stu-id="b4904-240">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="b4904-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: configura um site para permitir que os clientes se conectem por http2.0</span><span class="sxs-lookup"><span data-stu-id="b4904-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="b4904-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> se o log HTTP estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b4904-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: restrições de segurança IP para principal.</span><span class="sxs-lookup"><span data-stu-id="b4904-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="b4904-244">`[Action <String>]`: Permitir ou Negar acesso a este intervalo IP.</span><span class="sxs-lookup"><span data-stu-id="b4904-244">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="b4904-245">`[Description <String>]`: descrição da regra de restrição de IP.</span><span class="sxs-lookup"><span data-stu-id="b4904-245">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="b4904-246">`[IPAddress <String>]`: endereço IP para o que a restrição de segurança é válida.</span><span class="sxs-lookup"><span data-stu-id="b4904-246">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="b4904-247">Pode ser em forma de endereço ipv4 puro (propriedade Desprot. de SubnetMask necessária) ou notação CIDR, como ipv4/mask (bit match à frente).</span><span class="sxs-lookup"><span data-stu-id="b4904-247">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="b4904-248">Para CIDR, a propriedade SubnetMask não deve ser especificada.</span><span class="sxs-lookup"><span data-stu-id="b4904-248">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="b4904-249">`[Name <String>]`: nome da regra de restrição de IP.</span><span class="sxs-lookup"><span data-stu-id="b4904-249">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="b4904-250">`[Priority <Int32?>]`: Prioridade da regra de restrição de IP.</span><span class="sxs-lookup"><span data-stu-id="b4904-250">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="b4904-251">`[SubnetMask <String>]`: A máscara de sub-rede para o intervalo de endereços IP para a restrição é válida.</span><span class="sxs-lookup"><span data-stu-id="b4904-251">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="b4904-252">`[SubnetTrafficTag <Int32?>]`: marca de tráfego da sub-rede (interna)</span><span class="sxs-lookup"><span data-stu-id="b4904-252">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="b4904-253">`[Tag <IPFilterTag?>]`: define para que esse filtro IP será usado.</span><span class="sxs-lookup"><span data-stu-id="b4904-253">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="b4904-254">Isso é para dar suporte à filtragem de IP em proxies.</span><span class="sxs-lookup"><span data-stu-id="b4904-254">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="b4904-255">`[VnetSubnetResourceId <String>]`: ID do recurso de rede virtual</span><span class="sxs-lookup"><span data-stu-id="b4904-255">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="b4904-256">`[VnetTrafficTag <Int32?>]`: (interno) marca de tráfego da Vnet</span><span class="sxs-lookup"><span data-stu-id="b4904-256">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="b4904-257">`[JavaContainer <String>]`: contêiner Java.</span><span class="sxs-lookup"><span data-stu-id="b4904-257">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="b4904-258">`[JavaContainerVersion <String>]`: Versão do contêiner Java.</span><span class="sxs-lookup"><span data-stu-id="b4904-258">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="b4904-259">`[JavaVersion <String>]`: versão Java.</span><span class="sxs-lookup"><span data-stu-id="b4904-259">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="b4904-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Uso máximo de tamanho de disco permitido em MB.</span><span class="sxs-lookup"><span data-stu-id="b4904-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="b4904-261">`[LimitMaxMemoryInMb <Int64?>]`: Uso máximo permitido de memória em MB.</span><span class="sxs-lookup"><span data-stu-id="b4904-261">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="b4904-262">`[LimitMaxPercentageCpu <Double?>]`: porcentagem máxima de uso da CPU permitida.</span><span class="sxs-lookup"><span data-stu-id="b4904-262">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="b4904-263">`[LinuxFxVersion <String>]`: Linux App Framework e versão</span><span class="sxs-lookup"><span data-stu-id="b4904-263">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="b4904-264">`[LoadBalancing <SiteLoadBalancing?>]`: Balanceamento de carga do site.</span><span class="sxs-lookup"><span data-stu-id="b4904-264">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="b4904-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> para habilitar o MySQL local; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b4904-266">`[LogsDirectorySizeLimit <Int32?>]`: limite de tamanho de diretório de logs HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4904-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="b4904-267">`[MachineKeyDecryption <String>]`: Algoritmo usado para descriptografia.</span><span class="sxs-lookup"><span data-stu-id="b4904-267">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="b4904-268">`[MachineKeyDecryptionKey <String>]`: Chave de descriptografia.</span><span class="sxs-lookup"><span data-stu-id="b4904-268">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="b4904-269">`[MachineKeyValidation <String>]`: Validação do MachineKey.</span><span class="sxs-lookup"><span data-stu-id="b4904-269">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="b4904-270">`[MachineKeyValidationKey <String>]`: Chave de validação.</span><span class="sxs-lookup"><span data-stu-id="b4904-270">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="b4904-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Modo de pipeline gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b4904-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="b4904-272">`[ManagedServiceIdentityId <Int32?>]`: ID de Identidade de Serviço Gerenciado</span><span class="sxs-lookup"><span data-stu-id="b4904-272">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="b4904-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configura a versão mínima de TLS necessária para solicitações SSL</span><span class="sxs-lookup"><span data-stu-id="b4904-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="b4904-274">`[NetFrameworkVersion <String>]`: .NET Framework versão.</span><span class="sxs-lookup"><span data-stu-id="b4904-274">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="b4904-275">`[NodeVersion <String>]`: Versão do Node.js.</span><span class="sxs-lookup"><span data-stu-id="b4904-275">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="b4904-276">`[NumberOfWorker <Int32?>]`: Número de trabalhadores.</span><span class="sxs-lookup"><span data-stu-id="b4904-276">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="b4904-277">`[PhpVersion <String>]`: Versão do PHP.</span><span class="sxs-lookup"><span data-stu-id="b4904-277">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="b4904-278">`[PowerShellVersion <String>]`: Versão do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4904-278">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="b4904-279">`[PreWarmedInstanceCount <Int32?>]`: Número de instâncias pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="b4904-279">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="b4904-280">Essa configuração se aplica somente aos Planos de Consumo e Elástica</span><span class="sxs-lookup"><span data-stu-id="b4904-280">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="b4904-281">`[PublishingUsername <String>]`: Nome de usuário de publicação.</span><span class="sxs-lookup"><span data-stu-id="b4904-281">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="b4904-282">`[PushKind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="b4904-282">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="b4904-283">`[PythonVersion <String>]`: Versão do Python.</span><span class="sxs-lookup"><span data-stu-id="b4904-283">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="b4904-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> se a depuração remota estiver habilitada; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b4904-285">`[RemoteDebuggingVersion <String>]`: Versão de depuração remota.</span><span class="sxs-lookup"><span data-stu-id="b4904-285">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="b4904-286">`[RequestCount <Int32?>]`: Solicitar Contagem.</span><span class="sxs-lookup"><span data-stu-id="b4904-286">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="b4904-287">`[RequestTimeInterval <String>]`: Intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="b4904-287">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="b4904-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> se o rastreamento de solicitação estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b4904-289">`[RequestTracingExpirationTime <DateTime?>]`: Solicitar o rastreamento do tempo de expiração.</span><span class="sxs-lookup"><span data-stu-id="b4904-289">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="b4904-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: restrições de segurança IP para scm.</span><span class="sxs-lookup"><span data-stu-id="b4904-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="b4904-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: restrições de segurança IP para scm usar principal.</span><span class="sxs-lookup"><span data-stu-id="b4904-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="b4904-292">`[ScmType <ScmType?>]`: tipo de SCM.</span><span class="sxs-lookup"><span data-stu-id="b4904-292">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="b4904-293">`[SlowRequestCount <Int32?>]`: Solicitar Contagem.</span><span class="sxs-lookup"><span data-stu-id="b4904-293">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="b4904-294">`[SlowRequestTimeInterval <String>]`: Intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="b4904-294">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="b4904-295">`[SlowRequestTimeTaken <String>]`: Tempo de tomada.</span><span class="sxs-lookup"><span data-stu-id="b4904-295">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="b4904-296">`[TagWhitelistJson <String>]`: Obtém ou define uma cadeia de caracteres JSON contendo uma lista de marcas listadas em branco para uso pelo ponto de extremidade de registro por push.</span><span class="sxs-lookup"><span data-stu-id="b4904-296">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="b4904-297">`[TagsRequiringAuth <String>]`: Obtém ou define uma cadeia de caracteres JSON contendo uma lista de marcas que exigem que a autenticação do usuário seja usada no ponto de extremidade de registro por push.</span><span class="sxs-lookup"><span data-stu-id="b4904-297">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="b4904-298">As marcas podem consistir em caracteres alfanuméricos e os seguintes: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="b4904-298">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="b4904-299">A validação deve ser realizada no PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="b4904-299">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="b4904-300">`[TracingOption <String>]`: Opções de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="b4904-300">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="b4904-301">`[TriggerPrivateBytesInKb <Int32?>]`: uma regra baseada em bytes particulares.</span><span class="sxs-lookup"><span data-stu-id="b4904-301">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="b4904-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: uma regra baseada em códigos de status.</span><span class="sxs-lookup"><span data-stu-id="b4904-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="b4904-303">`[Count <Int32?>]`: Solicitar Contagem.</span><span class="sxs-lookup"><span data-stu-id="b4904-303">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="b4904-304">`[Status <Int32?>]`: código de status HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4904-304">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="b4904-305">`[SubStatus <Int32?>]`: Solicitar Sub Status.</span><span class="sxs-lookup"><span data-stu-id="b4904-305">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="b4904-306">`[TimeInterval <String>]`: Intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="b4904-306">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="b4904-307">`[Win32Status <Int32?>]`: código de erro Win32.</span><span class="sxs-lookup"><span data-stu-id="b4904-307">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="b4904-308">`[Use32BitWorkerProcess <Boolean?>]`: para usar o processo de trabalhador de <code>true</code> 32 bits; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b4904-309">`[VirtualApplication <IVirtualApplication[]>]`: Aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="b4904-309">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="b4904-310">`[PhysicalPath <String>]`: Caminho físico.</span><span class="sxs-lookup"><span data-stu-id="b4904-310">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="b4904-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> se o pré-carregamento estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="b4904-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Diretórios virtuais para aplicativos virtuais.</span><span class="sxs-lookup"><span data-stu-id="b4904-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="b4904-313">`[PhysicalPath <String>]`: Caminho físico.</span><span class="sxs-lookup"><span data-stu-id="b4904-313">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="b4904-314">`[VirtualPath <String>]`: Caminho para o aplicativo virtual.</span><span class="sxs-lookup"><span data-stu-id="b4904-314">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="b4904-315">`[VirtualPath <String>]`: Caminho virtual.</span><span class="sxs-lookup"><span data-stu-id="b4904-315">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="b4904-316">`[VnetName <String>]`: Nome da Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="b4904-316">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="b4904-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> se WebSocket estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b4904-318">`[WindowsFxVersion <String>]`: Framework e versão do aplicativo Dedados</span><span class="sxs-lookup"><span data-stu-id="b4904-318">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="b4904-319">`[XManagedServiceIdentityId <Int32?>]`: ID de identidade de serviço gerenciado explícita</span><span class="sxs-lookup"><span data-stu-id="b4904-319">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="b4904-320">`[ContainerSize <Int32?>]`: Tamanho do contêiner de função.</span><span class="sxs-lookup"><span data-stu-id="b4904-320">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="b4904-321">`[DailyMemoryTimeQuota <Int32?>]`: cota máxima permitida diária de tempo de memória (aplicável somente a aplicativos dinâmicos).</span><span class="sxs-lookup"><span data-stu-id="b4904-321">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="b4904-322">`[Enabled <Boolean?>]`: <code>true</code> se o aplicativo estiver habilitado; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-322">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="b4904-323">Definir esse valor como falso desabilita o aplicativo (o aplicativo fica offline).</span><span class="sxs-lookup"><span data-stu-id="b4904-323">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="b4904-324">`[HostNameSslState <IHostNameSslState[]>]`: Os estados SSL do nome do host são usados para gerenciar as ligações SSL para os nomes de host do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b4904-324">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="b4904-325">`[HostType <HostType?>]`: indica se o nome do host é um nome de host padrão ou de repositório.</span><span class="sxs-lookup"><span data-stu-id="b4904-325">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="b4904-326">`[Name <String>]`: Nome do host.</span><span class="sxs-lookup"><span data-stu-id="b4904-326">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="b4904-327">`[SslState <SslState?>]`: Tipo de SSL.</span><span class="sxs-lookup"><span data-stu-id="b4904-327">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="b4904-328">`[Thumbprint <String>]`: impressão de miniatura do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="b4904-328">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="b4904-329">`[ToUpdate <Boolean?>]`: Definido para <code>true</code> atualizar o nome de host existente.</span><span class="sxs-lookup"><span data-stu-id="b4904-329">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="b4904-330">`[VirtualIP <String>]`: Endereço IP virtual atribuído ao nome do host se SSL baseado em IP estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="b4904-330">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="b4904-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> para desabilitar os nomes de host públicos do aplicativo; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="b4904-332">Em <code>true</code> caso afirmativo, o aplicativo só pode ser acessado por meio de um processo de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="b4904-332">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="b4904-333">`[HostingEnvironmentProfileId <String>]`: ID do recurso do Ambiente de Serviço de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b4904-333">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="b4904-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: configura um site para aceitar apenas solicitações https.</span><span class="sxs-lookup"><span data-stu-id="b4904-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="b4904-335">Problemas redirecionados para solicitações http</span><span class="sxs-lookup"><span data-stu-id="b4904-335">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="b4904-336">`[HyperV <Boolean?>]`: áreas de areia hiperv.</span><span class="sxs-lookup"><span data-stu-id="b4904-336">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="b4904-337">`[IdentityType <ManagedServiceIdentityType?>]`: Tipo de identidade de serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b4904-337">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="b4904-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: a lista de identidades atribuídas pelo usuário associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="b4904-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="b4904-339">As referências de chave do dicionário de identidade do usuário serão IDs de recurso ARM no formulário: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="b4904-339">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="b4904-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="b4904-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b4904-341">`[IsXenon <Boolean?>]`: Obsoletas: área de areia hiperv.</span><span class="sxs-lookup"><span data-stu-id="b4904-341">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="b4904-342">`[RedundancyMode <RedundancyMode?>]`: Modo de redundância do site</span><span class="sxs-lookup"><span data-stu-id="b4904-342">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="b4904-343">`[Reserved <Boolean?>]`: <code>true</code> se reservada; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-343">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="b4904-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> para interromper o site do SCM (KUDU) quando o aplicativo for interrompido; caso contrário, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="b4904-345">O padrão é <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="b4904-345">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="b4904-346">`[ServerFarmId <String>]`: ID de recurso do plano de Serviço de Aplicativo associado, formatado como: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="b4904-346">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="b4904-347">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4904-347">RELATED LINKS</span></span>

