---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 760aacba880276059c4a468454cccec29d397183
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941680"
---
# <span data-ttu-id="17f37-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17f37-101">New-AzWebApp</span></span>

## <span data-ttu-id="17f37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17f37-102">SYNOPSIS</span></span>
<span data-ttu-id="17f37-103">Cria um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="17f37-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="17f37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17f37-104">SYNTAX</span></span>

### <span data-ttu-id="17f37-105">SimpleParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="17f37-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17f37-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="17f37-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17f37-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="17f37-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17f37-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17f37-108">DESCRIPTION</span></span>
<span data-ttu-id="17f37-109">O cmdlet **New-AzWebApp** cria um aplicativo Web do Azure em um determinado grupo de recursos que usa o plano do serviço de aplicativo especificado e o Data Center.</span><span class="sxs-lookup"><span data-stu-id="17f37-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="17f37-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17f37-110">EXAMPLES</span></span>

### <span data-ttu-id="17f37-111">Exemplo 1: criar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="17f37-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="17f37-112">Esse comando cria um aplicativo Web do Azure chamado ContosoSite no grupo de recursos existente chamado Default-Web-Oesteus no centro de dados West US.</span><span class="sxs-lookup"><span data-stu-id="17f37-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="17f37-113">O comando usa um plano do serviço de aplicativo existente chamado ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="17f37-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="17f37-114">OS</span><span class="sxs-lookup"><span data-stu-id="17f37-114">PARAMETERS</span></span>

### <span data-ttu-id="17f37-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="17f37-115">-AppServicePlan</span></span>
<span data-ttu-id="17f37-116">Nome do plano do serviço de aplicativo ou ID do plano do serviço de aplicativo. Se um plano do WebApp e do serviço de App estiver em grupos de recursos diferentes, use a ID em vez do nome.</span><span class="sxs-lookup"><span data-stu-id="17f37-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="17f37-117">A ID do plano do serviço de aplicativo pode ser recuperada usando: $asp = Get-AzAppServicePlan-myRG-nome do plano de-Name myWebApp $asp. ID retorna a ID do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="17f37-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


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

### <span data-ttu-id="17f37-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="17f37-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="17f37-119">Configurações do aplicativo substitui HashTable</span><span class="sxs-lookup"><span data-stu-id="17f37-119">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="17f37-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="17f37-120">-AseName</span></span>
<span data-ttu-id="17f37-121">Nome do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="17f37-121">App Service Environment Name</span></span>

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

### <span data-ttu-id="17f37-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17f37-122">-AseResourceGroupName</span></span>
<span data-ttu-id="17f37-123">Nome do grupo de recursos do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="17f37-123">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="17f37-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17f37-124">-AsJob</span></span>
<span data-ttu-id="17f37-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="17f37-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17f37-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="17f37-126">-ContainerImageName</span></span>
<span data-ttu-id="17f37-127">Nome da imagem do contêiner e marca opcional, por exemplo (imagem: marca)</span><span class="sxs-lookup"><span data-stu-id="17f37-127">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="17f37-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="17f37-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="17f37-129">Senha do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="17f37-129">Private Container Registry Password</span></span>

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

### <span data-ttu-id="17f37-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="17f37-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="17f37-131">URL do servidor do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="17f37-131">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="17f37-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="17f37-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="17f37-133">Nome de usuário do registro do contêiner privado</span><span class="sxs-lookup"><span data-stu-id="17f37-133">Private Container Registry Username</span></span>

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

### <span data-ttu-id="17f37-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f37-134">-DefaultProfile</span></span>
<span data-ttu-id="17f37-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17f37-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17f37-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="17f37-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="17f37-137">Habilita/desabilita o webhook de implantação contínua do contêiner</span><span class="sxs-lookup"><span data-stu-id="17f37-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="17f37-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="17f37-138">-GitRepositoryPath</span></span>
<span data-ttu-id="17f37-139">Caminho para o repositório GitHub que contém o aplicativo Web a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="17f37-139">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="17f37-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="17f37-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="17f37-141">Opção ignorar nomes de host personalizados</span><span class="sxs-lookup"><span data-stu-id="17f37-141">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="17f37-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="17f37-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="17f37-143">Opção ignorar controle de origem</span><span class="sxs-lookup"><span data-stu-id="17f37-143">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="17f37-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="17f37-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="17f37-145">Opção incluir slots do WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="17f37-145">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="17f37-146">-Local</span><span class="sxs-lookup"><span data-stu-id="17f37-146">-Location</span></span>
<span data-ttu-id="17f37-147">Ponto</span><span class="sxs-lookup"><span data-stu-id="17f37-147">Location</span></span>

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

### <span data-ttu-id="17f37-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="17f37-148">-Name</span></span>
<span data-ttu-id="17f37-149">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="17f37-149">WebApp Name</span></span>

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

### <span data-ttu-id="17f37-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17f37-150">-ResourceGroupName</span></span>
<span data-ttu-id="17f37-151">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="17f37-151">Resource Group Name</span></span>

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

### <span data-ttu-id="17f37-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="17f37-152">-SourceWebApp</span></span>
<span data-ttu-id="17f37-153">Objeto WebApp de origem</span><span class="sxs-lookup"><span data-stu-id="17f37-153">Source WebApp Object</span></span>

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

### <span data-ttu-id="17f37-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="17f37-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="17f37-155">ID do recurso do perfil do Gerenciador de tráfego existente</span><span class="sxs-lookup"><span data-stu-id="17f37-155">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="17f37-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="17f37-156">-Confirm</span></span>
<span data-ttu-id="17f37-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17f37-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17f37-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17f37-158">-WhatIf</span></span>
<span data-ttu-id="17f37-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17f37-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17f37-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17f37-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17f37-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f37-161">CommonParameters</span></span>
<span data-ttu-id="17f37-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17f37-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f37-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17f37-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f37-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17f37-164">INPUTS</span></span>

### <span data-ttu-id="17f37-165">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="17f37-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="17f37-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17f37-166">OUTPUTS</span></span>

### <span data-ttu-id="17f37-167">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="17f37-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="17f37-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17f37-168">NOTES</span></span>

## <span data-ttu-id="17f37-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17f37-169">RELATED LINKS</span></span>

[<span data-ttu-id="17f37-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17f37-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="17f37-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17f37-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="17f37-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17f37-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="17f37-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17f37-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="17f37-174">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17f37-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


