---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 7a01cd2b6810d8405f2aba0a56e232891bd036f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115422"
---
# <span data-ttu-id="74e21-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="74e21-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="74e21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74e21-102">SYNOPSIS</span></span>
<span data-ttu-id="74e21-103">Cria um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="74e21-103">Creates a function app.</span></span>

## <span data-ttu-id="74e21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74e21-104">SYNTAX</span></span>

### <span data-ttu-id="74e21-105">Consumo (padrão)</span><span class="sxs-lookup"><span data-stu-id="74e21-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74e21-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="74e21-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74e21-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="74e21-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74e21-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74e21-108">DESCRIPTION</span></span>
<span data-ttu-id="74e21-109">Cria um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="74e21-109">Creates a function app.</span></span>

## <span data-ttu-id="74e21-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74e21-110">EXAMPLES</span></span>

### <span data-ttu-id="74e21-111">Exemplo 1: criar um aplicativo de função de consumo do PowerShell nos EUA.</span><span class="sxs-lookup"><span data-stu-id="74e21-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="74e21-112">Esse comando cria um aplicativo de função de consumo do PowerShell nos EUA.</span><span class="sxs-lookup"><span data-stu-id="74e21-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="74e21-113">Exemplo 2: criar um aplicativo de função do PowerShell que será hospedado em um plano de serviço.</span><span class="sxs-lookup"><span data-stu-id="74e21-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="74e21-114">Esse comando cria um aplicativo de função do PowerShell que será hospedado em um plano de serviço.</span><span class="sxs-lookup"><span data-stu-id="74e21-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="74e21-115">Exemplo 3: criar um aplicativo de função usando uma imagem de ACR particular.</span><span class="sxs-lookup"><span data-stu-id="74e21-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="74e21-116">Esse comando cria um aplicativo de função usando uma imagem de ACR particular.</span><span class="sxs-lookup"><span data-stu-id="74e21-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="74e21-117">OS</span><span class="sxs-lookup"><span data-stu-id="74e21-117">PARAMETERS</span></span>

### <span data-ttu-id="74e21-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="74e21-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="74e21-119">Chave de instrumentação de ideias do aplicativo a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="74e21-119">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="74e21-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="74e21-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="74e21-121">Nome do projeto insights do App existente a ser adicionado ao aplicativo function.</span><span class="sxs-lookup"><span data-stu-id="74e21-121">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="74e21-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="74e21-122">-AppSetting</span></span>
<span data-ttu-id="74e21-123">Função configurações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="74e21-123">Function app settings.</span></span>

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

### <span data-ttu-id="74e21-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74e21-124">-AsJob</span></span>
<span data-ttu-id="74e21-125">Executa o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="74e21-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="74e21-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e21-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="74e21-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="74e21-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="74e21-128">Desabilitar a criação do recurso de insights do aplicativo durante a criação da função do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="74e21-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="74e21-129">Nenhum registro estará disponível.</span><span class="sxs-lookup"><span data-stu-id="74e21-129">No logs will be available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: DisableAppInsights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="74e21-130">-DockerImageName</span></span>
<span data-ttu-id="74e21-131">Somente para Linux.</span><span class="sxs-lookup"><span data-stu-id="74e21-131">Linux only.</span></span>
<span data-ttu-id="74e21-132">Nome da imagem do contêiner do registro do Docker, por exemplo: Publisher/Image-Name: tag.</span><span class="sxs-lookup"><span data-stu-id="74e21-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="74e21-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="74e21-134">O nome de usuário e a senha do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="74e21-134">The container registry user name and password.</span></span>
<span data-ttu-id="74e21-135">Obrigatório para registros particulares.</span><span class="sxs-lookup"><span data-stu-id="74e21-135">Required for private registries.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CustomDockerImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="74e21-136">-FunctionsVersion</span></span>
<span data-ttu-id="74e21-137">A versão de funções.</span><span class="sxs-lookup"><span data-stu-id="74e21-137">The Functions version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-138">-Identityid</span><span class="sxs-lookup"><span data-stu-id="74e21-138">-IdentityID</span></span>
<span data-ttu-id="74e21-139">Especifica a lista de identidades de usuário associadas ao aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="74e21-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="74e21-140">As referências de identidade do usuário serão identificadores de recurso ARM no formato: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="74e21-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="74e21-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="74e21-141">-IdentityType</span></span>
<span data-ttu-id="74e21-142">Especifica o tipo de identidade usado para o aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="74e21-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="74e21-143">Os valores aceitáveis para esse parâmetro são:-SystemAssigned-userassigned</span><span class="sxs-lookup"><span data-stu-id="74e21-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

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

### <span data-ttu-id="74e21-144">-Local</span><span class="sxs-lookup"><span data-stu-id="74e21-144">-Location</span></span>
<span data-ttu-id="74e21-145">O local para o plano de consumo.</span><span class="sxs-lookup"><span data-stu-id="74e21-145">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="74e21-146">-Name</span></span>
<span data-ttu-id="74e21-147">O nome do aplicativo da função.</span><span class="sxs-lookup"><span data-stu-id="74e21-147">The name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-148">-Nowait</span><span class="sxs-lookup"><span data-stu-id="74e21-148">-NoWait</span></span>
<span data-ttu-id="74e21-149">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="74e21-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="74e21-150">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="74e21-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="74e21-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="74e21-151">-OSType</span></span>
<span data-ttu-id="74e21-152">O sistema operacional para hospedar o aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="74e21-152">The OS to host the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74e21-153">-PassThru</span></span>
<span data-ttu-id="74e21-154">Retorna true quando o comando é bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="74e21-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="74e21-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="74e21-155">-PlanName</span></span>
<span data-ttu-id="74e21-156">O nome do plano de serviço.</span><span class="sxs-lookup"><span data-stu-id="74e21-156">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74e21-157">-ResourceGroupName</span></span>
<span data-ttu-id="74e21-158">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74e21-158">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-159">-Runtime</span><span class="sxs-lookup"><span data-stu-id="74e21-159">-Runtime</span></span>
<span data-ttu-id="74e21-160">O tempo de execução da função.</span><span class="sxs-lookup"><span data-stu-id="74e21-160">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="74e21-161">-RuntimeVersion</span></span>
<span data-ttu-id="74e21-162">O tempo de execução da função.</span><span class="sxs-lookup"><span data-stu-id="74e21-162">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="74e21-163">-StorageAccountName</span></span>
<span data-ttu-id="74e21-164">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="74e21-164">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74e21-165">-SubscriptionId</span></span>
<span data-ttu-id="74e21-166">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="74e21-166">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e21-167">-Marca</span><span class="sxs-lookup"><span data-stu-id="74e21-167">-Tag</span></span>
<span data-ttu-id="74e21-168">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="74e21-168">Resource tags.</span></span>

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

### <span data-ttu-id="74e21-169">-Confirme</span><span class="sxs-lookup"><span data-stu-id="74e21-169">-Confirm</span></span>
<span data-ttu-id="74e21-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74e21-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74e21-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74e21-171">-WhatIf</span></span>
<span data-ttu-id="74e21-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74e21-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74e21-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74e21-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74e21-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e21-174">CommonParameters</span></span>
<span data-ttu-id="74e21-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74e21-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e21-176">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74e21-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e21-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74e21-177">INPUTS</span></span>

## <span data-ttu-id="74e21-178">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74e21-178">OUTPUTS</span></span>

### <span data-ttu-id="74e21-179">Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="74e21-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="74e21-180">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74e21-180">NOTES</span></span>

<span data-ttu-id="74e21-181">ALIASES</span><span class="sxs-lookup"><span data-stu-id="74e21-181">ALIASES</span></span>

## <span data-ttu-id="74e21-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74e21-182">RELATED LINKS</span></span>

