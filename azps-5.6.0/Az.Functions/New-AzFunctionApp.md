---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 97a1fa7aa5488034fa1f0147ae5a06ff639ecc06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887518"
---
# <span data-ttu-id="05cc6-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="05cc6-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="05cc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="05cc6-103">Cria um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="05cc6-103">Creates a function app.</span></span>

## <span data-ttu-id="05cc6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="05cc6-104">SYNTAX</span></span>

### <span data-ttu-id="05cc6-105">Consumo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="05cc6-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05cc6-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="05cc6-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05cc6-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="05cc6-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="05cc6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="05cc6-108">DESCRIPTION</span></span>
<span data-ttu-id="05cc6-109">Cria um aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="05cc6-109">Creates a function app.</span></span>

## <span data-ttu-id="05cc6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05cc6-110">EXAMPLES</span></span>

### <span data-ttu-id="05cc6-111">Exemplo 1: Criar um aplicativo de função do PowerShell de consumo na Central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="05cc6-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="05cc6-112">Este comando cria um aplicativo de função de consumo do PowerShell no Central US.</span><span class="sxs-lookup"><span data-stu-id="05cc6-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="05cc6-113">Exemplo 2: Crie um aplicativo de função do PowerShell que será hospedado em um plano de serviço.</span><span class="sxs-lookup"><span data-stu-id="05cc6-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="05cc6-114">Este comando cria um aplicativo de função do PowerShell que será hospedado em um plano de serviço.</span><span class="sxs-lookup"><span data-stu-id="05cc6-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="05cc6-115">Exemplo 3: Criar um aplicativo de função usando uma imagem ACR privada.</span><span class="sxs-lookup"><span data-stu-id="05cc6-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="05cc6-116">Este comando cria um aplicativo de função usando uma imagem ACR privada.</span><span class="sxs-lookup"><span data-stu-id="05cc6-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="05cc6-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="05cc6-117">PARAMETERS</span></span>

### <span data-ttu-id="05cc6-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="05cc6-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="05cc6-119">Chave de instrumentação do App Insights a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="05cc6-119">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="05cc6-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="05cc6-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="05cc6-121">Nome do projeto do App Insights existente a ser adicionado ao aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="05cc6-121">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="05cc6-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="05cc6-122">-AppSetting</span></span>
<span data-ttu-id="05cc6-123">Configurações do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="05cc6-123">Function app settings.</span></span>

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

### <span data-ttu-id="05cc6-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05cc6-124">-AsJob</span></span>
<span data-ttu-id="05cc6-125">Executa o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="05cc6-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="05cc6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05cc6-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="05cc6-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="05cc6-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="05cc6-128">Desabilite a criação de recursos de insights de aplicativo durante a criação do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="05cc6-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="05cc6-129">Nenhum logs estará disponível.</span><span class="sxs-lookup"><span data-stu-id="05cc6-129">No logs will be available.</span></span>

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

### <span data-ttu-id="05cc6-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="05cc6-130">-DockerImageName</span></span>
<span data-ttu-id="05cc6-131">Somente Linux.</span><span class="sxs-lookup"><span data-stu-id="05cc6-131">Linux only.</span></span>
<span data-ttu-id="05cc6-132">Nome da imagem do contêiner do Registro do Docker, por exemplo, publisher/image-name:tag.</span><span class="sxs-lookup"><span data-stu-id="05cc6-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

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

### <span data-ttu-id="05cc6-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="05cc6-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="05cc6-134">O nome de usuário e a senha do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="05cc6-134">The container registry user name and password.</span></span>
<span data-ttu-id="05cc6-135">Obrigatório para registros privados.</span><span class="sxs-lookup"><span data-stu-id="05cc6-135">Required for private registries.</span></span>

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

### <span data-ttu-id="05cc6-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="05cc6-136">-FunctionsVersion</span></span>
<span data-ttu-id="05cc6-137">A versão Functions.</span><span class="sxs-lookup"><span data-stu-id="05cc6-137">The Functions version.</span></span>

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

### <span data-ttu-id="05cc6-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="05cc6-138">-IdentityID</span></span>
<span data-ttu-id="05cc6-139">Especifica a lista de identidades de usuário associadas ao aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="05cc6-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="05cc6-140">As referências de identidade do usuário serão ARM ids de recurso no formato: '/subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identity/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="05cc6-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="05cc6-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="05cc6-141">-IdentityType</span></span>
<span data-ttu-id="05cc6-142">Especifica o tipo de identidade usada para o aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="05cc6-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="05cc6-143">Os valores aceitáveis para este parâmetro são: - SystemAssigned - UserAssigned</span><span class="sxs-lookup"><span data-stu-id="05cc6-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

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

### <span data-ttu-id="05cc6-144">-Location</span><span class="sxs-lookup"><span data-stu-id="05cc6-144">-Location</span></span>
<span data-ttu-id="05cc6-145">O local do plano de consumo.</span><span class="sxs-lookup"><span data-stu-id="05cc6-145">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="05cc6-146">-Name</span><span class="sxs-lookup"><span data-stu-id="05cc6-146">-Name</span></span>
<span data-ttu-id="05cc6-147">O nome do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="05cc6-147">The name of the function app.</span></span>

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

### <span data-ttu-id="05cc6-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="05cc6-148">-NoWait</span></span>
<span data-ttu-id="05cc6-149">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="05cc6-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="05cc6-150">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="05cc6-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="05cc6-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="05cc6-151">-OSType</span></span>
<span data-ttu-id="05cc6-152">O sistema operacional para hospedar o aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="05cc6-152">The OS to host the function app.</span></span>

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

### <span data-ttu-id="05cc6-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05cc6-153">-PassThru</span></span>
<span data-ttu-id="05cc6-154">Retorna true quando o comando é bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="05cc6-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="05cc6-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="05cc6-155">-PlanName</span></span>
<span data-ttu-id="05cc6-156">O nome do plano de serviço.</span><span class="sxs-lookup"><span data-stu-id="05cc6-156">The name of the service plan.</span></span>

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

### <span data-ttu-id="05cc6-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05cc6-157">-ResourceGroupName</span></span>
<span data-ttu-id="05cc6-158">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="05cc6-158">The name of the resource group.</span></span>

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

### <span data-ttu-id="05cc6-159">-Runtime</span><span class="sxs-lookup"><span data-stu-id="05cc6-159">-Runtime</span></span>
<span data-ttu-id="05cc6-160">O tempo de execução da função.</span><span class="sxs-lookup"><span data-stu-id="05cc6-160">The function runtime.</span></span>

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

### <span data-ttu-id="05cc6-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="05cc6-161">-RuntimeVersion</span></span>
<span data-ttu-id="05cc6-162">O tempo de execução da função.</span><span class="sxs-lookup"><span data-stu-id="05cc6-162">The function runtime.</span></span>

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

### <span data-ttu-id="05cc6-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="05cc6-163">-StorageAccountName</span></span>
<span data-ttu-id="05cc6-164">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="05cc6-164">The name of the storage account.</span></span>

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

### <span data-ttu-id="05cc6-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05cc6-165">-SubscriptionId</span></span>
<span data-ttu-id="05cc6-166">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="05cc6-166">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="05cc6-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="05cc6-167">-Tag</span></span>
<span data-ttu-id="05cc6-168">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="05cc6-168">Resource tags.</span></span>

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

### <span data-ttu-id="05cc6-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05cc6-169">-Confirm</span></span>
<span data-ttu-id="05cc6-170">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05cc6-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05cc6-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05cc6-171">-WhatIf</span></span>
<span data-ttu-id="05cc6-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05cc6-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05cc6-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05cc6-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05cc6-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05cc6-174">CommonParameters</span></span>
<span data-ttu-id="05cc6-175">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05cc6-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05cc6-176">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05cc6-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05cc6-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05cc6-177">INPUTS</span></span>

## <span data-ttu-id="05cc6-178">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="05cc6-178">OUTPUTS</span></span>

### <span data-ttu-id="05cc6-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="05cc6-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="05cc6-180">NOTES</span><span class="sxs-lookup"><span data-stu-id="05cc6-180">NOTES</span></span>

<span data-ttu-id="05cc6-181">ALIASES</span><span class="sxs-lookup"><span data-stu-id="05cc6-181">ALIASES</span></span>

## <span data-ttu-id="05cc6-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05cc6-182">RELATED LINKS</span></span>

