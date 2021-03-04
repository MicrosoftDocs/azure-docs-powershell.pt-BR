---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: e09c2660f37a7b737d137c0907ff74ef9e39a5ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887931"
---
# <span data-ttu-id="69283-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69283-101">New-AzWebApp</span></span>

## <span data-ttu-id="69283-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69283-102">SYNOPSIS</span></span>
<span data-ttu-id="69283-103">Cria um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="69283-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="69283-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="69283-104">SYNTAX</span></span>

### <span data-ttu-id="69283-105">SimpleParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="69283-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69283-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="69283-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69283-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="69283-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69283-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="69283-108">DESCRIPTION</span></span>
<span data-ttu-id="69283-109">O cmdlet **New-AzWebApp** cria um Aplicativo Web do Azure em um determinado grupo de recursos que usa o plano de Serviço de Aplicativo especificado e o data center.</span><span class="sxs-lookup"><span data-stu-id="69283-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="69283-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69283-110">EXAMPLES</span></span>

### <span data-ttu-id="69283-111">Exemplo 1: Criar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="69283-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="69283-112">Este comando cria um Aplicativo Web do Azure chamado ContosoSite no grupo de recursos existente chamado Default-Web-WestUS no data center West US.</span><span class="sxs-lookup"><span data-stu-id="69283-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="69283-113">O comando usa um plano de Serviço de Aplicativo existente chamado ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="69283-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="69283-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="69283-114">PARAMETERS</span></span>

### <span data-ttu-id="69283-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69283-115">-AppServicePlan</span></span>
<span data-ttu-id="69283-116">Nome do Plano de Serviço de Aplicativo ou ID do Plano de Serviço de Aplicativo. Se um Plano de Serviço de Aplicativo e WebApp estiver em grupos de recursos diferentes, use a ID em vez do nome.</span><span class="sxs-lookup"><span data-stu-id="69283-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="69283-117">A ID do Plano de Serviço de Aplicativo pode ser recuperada usando: $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id retorna a ID do Plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69283-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="69283-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="69283-119">Configurações do aplicativo substitui HashTable</span><span class="sxs-lookup"><span data-stu-id="69283-119">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="69283-120">-AseName</span></span>
<span data-ttu-id="69283-121">Nome do ambiente de serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="69283-121">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69283-122">-AseResourceGroupName</span></span>
<span data-ttu-id="69283-123">Nome do grupo de recursos do ambiente de serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="69283-123">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69283-124">-AsJob</span></span>
<span data-ttu-id="69283-125">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="69283-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69283-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="69283-126">-ContainerImageName</span></span>
<span data-ttu-id="69283-127">Nome da imagem do contêiner e marca opcional, por exemplo (image:tag)</span><span class="sxs-lookup"><span data-stu-id="69283-127">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="69283-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="69283-129">Senha do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="69283-129">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="69283-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="69283-131">Url do Servidor de Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="69283-131">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="69283-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="69283-133">Nome de usuário do Registro de Contêiner Particular</span><span class="sxs-lookup"><span data-stu-id="69283-133">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69283-134">-DefaultProfile</span></span>
<span data-ttu-id="69283-135">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="69283-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69283-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="69283-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="69283-137">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="69283-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="69283-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="69283-138">-GitRepositoryPath</span></span>
<span data-ttu-id="69283-139">Caminho para o repositório do GitHub que contém o aplicativo Web a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="69283-139">Path to the GitHub repository containing the web application to deploy.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="69283-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="69283-141">Ignorar a opção Nomes de Host Personalizados</span><span class="sxs-lookup"><span data-stu-id="69283-141">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="69283-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="69283-143">Ignorar a opção de controle de origem</span><span class="sxs-lookup"><span data-stu-id="69283-143">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="69283-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="69283-145">Incluir a opção Slots webApp de origem</span><span class="sxs-lookup"><span data-stu-id="69283-145">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-146">-Location</span><span class="sxs-lookup"><span data-stu-id="69283-146">-Location</span></span>
<span data-ttu-id="69283-147">Local</span><span class="sxs-lookup"><span data-stu-id="69283-147">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-148">-Name</span><span class="sxs-lookup"><span data-stu-id="69283-148">-Name</span></span>
<span data-ttu-id="69283-149">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="69283-149">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69283-150">-ResourceGroupName</span></span>
<span data-ttu-id="69283-151">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="69283-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry, WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="69283-152">-SourceWebApp</span></span>
<span data-ttu-id="69283-153">Objeto WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="69283-153">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69283-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="69283-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="69283-155">ID de recurso do perfil de gerente de tráfego existente</span><span class="sxs-lookup"><span data-stu-id="69283-155">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69283-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69283-156">-Confirm</span></span>
<span data-ttu-id="69283-157">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69283-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69283-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69283-158">-WhatIf</span></span>
<span data-ttu-id="69283-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69283-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69283-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69283-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69283-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69283-161">CommonParameters</span></span>
<span data-ttu-id="69283-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69283-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69283-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69283-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69283-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69283-164">INPUTS</span></span>

### <span data-ttu-id="69283-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="69283-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="69283-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="69283-166">OUTPUTS</span></span>

### <span data-ttu-id="69283-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="69283-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="69283-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="69283-168">NOTES</span></span>

## <span data-ttu-id="69283-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69283-169">RELATED LINKS</span></span>

[<span data-ttu-id="69283-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69283-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="69283-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69283-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="69283-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69283-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="69283-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69283-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="69283-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="69283-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


