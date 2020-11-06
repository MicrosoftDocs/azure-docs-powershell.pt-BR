---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 2dfa72867655b95ea752c23c8605f19e7544e8e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426244"
---
# <span data-ttu-id="c8e91-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c8e91-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="c8e91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8e91-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e91-103">Cria um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e91-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8e91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8e91-104">SYNTAX</span></span>

### <span data-ttu-id="c8e91-105">SimpleParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c8e91-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8e91-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="c8e91-106">PrivateRegistry</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] -ContainerImageName <String> -ContainerRegistryUrl <String>
 -ContainerRegistryUser <String> -ContainerRegistryPassword <SecureString>
 [-EnableContainerContinuousDeployment] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8e91-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8e91-107">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>]
 [-EnableContainerContinuousDeployment] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-IncludeSourceWebAppSlots] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8e91-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8e91-108">DESCRIPTION</span></span>
<span data-ttu-id="c8e91-109">O cmdlet **New-AzureRmWebApp** cria um aplicativo Web do Azure em um determinado grupo de recursos que usa o plano do serviço de aplicativo especificado e o Data Center.</span><span class="sxs-lookup"><span data-stu-id="c8e91-109">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="c8e91-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8e91-110">EXAMPLES</span></span>

### <span data-ttu-id="c8e91-111">Exemplo 1: criar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="c8e91-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="c8e91-112">Esse comando cria um aplicativo Web do Azure chamado ContosoSite no grupo de recursos existente chamado Default-Web-Oesteus no centro de dados West US.</span><span class="sxs-lookup"><span data-stu-id="c8e91-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="c8e91-113">O comando usa um plano do serviço de aplicativo existente chamado ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="c8e91-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="c8e91-114">OS</span><span class="sxs-lookup"><span data-stu-id="c8e91-114">PARAMETERS</span></span>

### <span data-ttu-id="c8e91-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c8e91-115">-AppServicePlan</span></span>
<span data-ttu-id="c8e91-116">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c8e91-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="c8e91-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="c8e91-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="c8e91-118">Configurações do aplicativo substitui HashTable</span><span class="sxs-lookup"><span data-stu-id="c8e91-118">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="c8e91-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="c8e91-119">-AseName</span></span>
<span data-ttu-id="c8e91-120">Nome do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c8e91-120">App Service Environment Name</span></span>

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

### <span data-ttu-id="c8e91-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e91-121">-AseResourceGroupName</span></span>
<span data-ttu-id="c8e91-122">Nome do grupo de recursos do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c8e91-122">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="c8e91-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8e91-123">-AsJob</span></span>
<span data-ttu-id="c8e91-124">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c8e91-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8e91-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="c8e91-125">-ContainerImageName</span></span>
<span data-ttu-id="c8e91-126">Nome da imagem do contêiner e marca opcional, por exemplo (imagem: marca)</span><span class="sxs-lookup"><span data-stu-id="c8e91-126">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="c8e91-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="c8e91-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="c8e91-128">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="c8e91-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="c8e91-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="c8e91-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="c8e91-130">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="c8e91-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="c8e91-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="c8e91-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="c8e91-132">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="c8e91-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="c8e91-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e91-133">-DefaultProfile</span></span>
<span data-ttu-id="c8e91-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e91-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e91-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="c8e91-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="c8e91-136">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="c8e91-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="c8e91-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="c8e91-137">-GitRepositoryPath</span></span>
<span data-ttu-id="c8e91-138">Caminho para o repositório GitHub containign o aplicativo Web a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="c8e91-138">Path to the GitHub repository containign the web application to deploy.</span></span>

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

### <span data-ttu-id="c8e91-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="c8e91-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="c8e91-140">Opção ignorar nomes de host personalizados</span><span class="sxs-lookup"><span data-stu-id="c8e91-140">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="c8e91-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="c8e91-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="c8e91-142">Opção ignorar controle de origem</span><span class="sxs-lookup"><span data-stu-id="c8e91-142">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="c8e91-143">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="c8e91-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="c8e91-144">Opção incluir slots do WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="c8e91-144">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="c8e91-145">-Local</span><span class="sxs-lookup"><span data-stu-id="c8e91-145">-Location</span></span>
<span data-ttu-id="c8e91-146">Ponto</span><span class="sxs-lookup"><span data-stu-id="c8e91-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e91-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8e91-147">-Name</span></span>
<span data-ttu-id="c8e91-148">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="c8e91-148">WebApp Name</span></span>

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

### <span data-ttu-id="c8e91-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e91-149">-ResourceGroupName</span></span>
<span data-ttu-id="c8e91-150">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c8e91-150">Resource Group Name</span></span>

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

### <span data-ttu-id="c8e91-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="c8e91-151">-SourceWebApp</span></span>
<span data-ttu-id="c8e91-152">Objeto WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="c8e91-152">Source WebApp Object</span></span>

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

### <span data-ttu-id="c8e91-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c8e91-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="c8e91-154">ID do recurso do perfil do Gerenciador de tráfego existente</span><span class="sxs-lookup"><span data-stu-id="c8e91-154">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="c8e91-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c8e91-155">-Confirm</span></span>
<span data-ttu-id="c8e91-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8e91-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8e91-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8e91-157">-WhatIf</span></span>
<span data-ttu-id="c8e91-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8e91-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8e91-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8e91-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8e91-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e91-160">CommonParameters</span></span>
<span data-ttu-id="c8e91-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8e91-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e91-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8e91-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e91-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8e91-163">INPUTS</span></span>

### <span data-ttu-id="c8e91-164">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="c8e91-164">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c8e91-165">Parâmetros: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8e91-165">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="c8e91-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8e91-166">OUTPUTS</span></span>

### <span data-ttu-id="c8e91-167">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="c8e91-167">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="c8e91-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8e91-168">NOTES</span></span>

## <span data-ttu-id="c8e91-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8e91-169">RELATED LINKS</span></span>

[<span data-ttu-id="c8e91-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c8e91-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="c8e91-171">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c8e91-171">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="c8e91-172">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c8e91-172">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="c8e91-173">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c8e91-173">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="c8e91-174">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c8e91-174">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


