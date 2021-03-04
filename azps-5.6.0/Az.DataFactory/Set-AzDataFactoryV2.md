---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 10759ac90bf1d92243a8d706be3bbb345af4669c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891453"
---
# <span data-ttu-id="f314a-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f314a-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="f314a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f314a-102">SYNOPSIS</span></span>
<span data-ttu-id="f314a-103">Cria uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f314a-103">Creates a data factory.</span></span>

## <span data-ttu-id="f314a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f314a-104">SYNTAX</span></span>

### <span data-ttu-id="f314a-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f314a-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f314a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f314a-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f314a-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="f314a-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f314a-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="f314a-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f314a-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="f314a-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f314a-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="f314a-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f314a-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f314a-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f314a-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="f314a-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f314a-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="f314a-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f314a-114">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f314a-114">DESCRIPTION</span></span>
<span data-ttu-id="f314a-115">O cmdlet **Set-AzDataFactoryV2** cria um fábrica de dados com o nome e o local do grupo de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="f314a-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="f314a-116">Execute essas operações na seguinte ordem: -- Criar um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f314a-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="f314a-117">-- Crie serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="f314a-117">-- Create linked services.</span></span>
<span data-ttu-id="f314a-118">-- Criar conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="f314a-118">-- Create datasets.</span></span>
<span data-ttu-id="f314a-119">-- Crie um pipeline.</span><span class="sxs-lookup"><span data-stu-id="f314a-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="f314a-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f314a-120">EXAMPLES</span></span>

### <span data-ttu-id="f314a-121">Exemplo 1: Criar um fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="f314a-121">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration :
```

### <span data-ttu-id="f314a-122">Exemplo 2: Criar um fábrica de dados com detalhes de configuração de repo usando um objeto de fábrica existente.</span><span class="sxs-lookup"><span data-stu-id="f314a-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" | Set-AzDataFactoryV2 -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder / -ProjectName "Azure Data Factory"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryVSTSConfiguration
```

<span data-ttu-id="f314a-123">Este comando cria um fábrica de dados chamado WikiADF no grupo de recursos chamado ADF no local do EastUS com a configuração de controle de origem do Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f314a-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="f314a-124">Exemplo 3: Criar um fábrica de dados com detalhes de configuração de repositório do GitHub usando um novo objeto de fábrica.</span><span class="sxs-lookup"><span data-stu-id="f314a-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
```
PS C:\> New-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location 'EastUS' -HostName 'https://github.com' -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder /

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryGitHubConfiguration
```

<span data-ttu-id="f314a-125">Este comando cria um fábrica de dados chamado WikiADF no grupo de recursos chamado ADF no local do EastUS com a configuração de controle de origem do GitHub..</span><span class="sxs-lookup"><span data-stu-id="f314a-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="f314a-126">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f314a-126">PARAMETERS</span></span>

### <span data-ttu-id="f314a-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f314a-127">-AccountName</span></span>
<span data-ttu-id="f314a-128">O nome da conta para a configuração de repo.</span><span class="sxs-lookup"><span data-stu-id="f314a-128">The account name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="f314a-129">-CollaborationBranch</span></span>
<span data-ttu-id="f314a-130">O branch de colaboração para configuração de repo.</span><span class="sxs-lookup"><span data-stu-id="f314a-130">The collaboration branch for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f314a-131">-DefaultProfile</span></span>
<span data-ttu-id="f314a-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f314a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f314a-133">-Force</span><span class="sxs-lookup"><span data-stu-id="f314a-133">-Force</span></span>
<span data-ttu-id="f314a-134">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="f314a-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f314a-135">-GlobalParameterDefinition</span><span class="sxs-lookup"><span data-stu-id="f314a-135">-GlobalParameterDefinition</span></span>
<span data-ttu-id="f314a-136">O dicionário que contém os parâmetros globais do fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f314a-136">The dictionary containing the global parameters of the data factory.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="f314a-137">-HostName</span></span>
<span data-ttu-id="f314a-138">O nome do host para a configuração de repositório do GitHub.</span><span class="sxs-lookup"><span data-stu-id="f314a-138">The host name for GitHub repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f314a-139">-InputObject</span></span>
<span data-ttu-id="f314a-140">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f314a-140">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-141">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="f314a-141">-LastCommitId</span></span>
<span data-ttu-id="f314a-142">A última id de confirmação para configuração de repo.</span><span class="sxs-lookup"><span data-stu-id="f314a-142">The last commit id for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-143">-Location</span><span class="sxs-lookup"><span data-stu-id="f314a-143">-Location</span></span>
<span data-ttu-id="f314a-144">A fábrica de dados é criada nessa região.</span><span class="sxs-lookup"><span data-stu-id="f314a-144">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-145">-Name</span><span class="sxs-lookup"><span data-stu-id="f314a-145">-Name</span></span>
<span data-ttu-id="f314a-146">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f314a-146">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-147">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="f314a-147">-ProjectName</span></span>
<span data-ttu-id="f314a-148">O nome do projeto Azure DevOps para configuração de repo.</span><span class="sxs-lookup"><span data-stu-id="f314a-148">The project name Azure DevOps for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-149">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="f314a-149">-RepositoryName</span></span>
<span data-ttu-id="f314a-150">O nome do repositório para configuração de repositório.</span><span class="sxs-lookup"><span data-stu-id="f314a-150">The repository name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f314a-151">-ResourceGroupName</span></span>
<span data-ttu-id="f314a-152">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f314a-152">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f314a-153">-ResourceId</span></span>
<span data-ttu-id="f314a-154">A ID de recurso do Azure do fábrica de dados V2.</span><span class="sxs-lookup"><span data-stu-id="f314a-154">The Azure resource ID of V2 data factory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig
Aliases: Id, DataFactoryId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-155">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="f314a-155">-RootFolder</span></span>
<span data-ttu-id="f314a-156">A pasta raiz para configuração de repo.</span><span class="sxs-lookup"><span data-stu-id="f314a-156">The root folder for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="f314a-157">-Tag</span></span>
<span data-ttu-id="f314a-158">As marcas do fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f314a-158">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-159">-TenantId</span><span class="sxs-lookup"><span data-stu-id="f314a-159">-TenantId</span></span>
<span data-ttu-id="f314a-160">A id do locatário para a configuração de repo do Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="f314a-160">The tenant id for Azure DevOps repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f314a-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f314a-161">-Confirm</span></span>
<span data-ttu-id="f314a-162">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f314a-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f314a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f314a-163">-WhatIf</span></span>
<span data-ttu-id="f314a-164">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f314a-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f314a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f314a-165">CommonParameters</span></span>
<span data-ttu-id="f314a-166">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f314a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f314a-167">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f314a-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f314a-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f314a-168">INPUTS</span></span>

### <span data-ttu-id="f314a-169">System.String</span><span class="sxs-lookup"><span data-stu-id="f314a-169">System.String</span></span>

### <span data-ttu-id="f314a-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f314a-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="f314a-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f314a-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f314a-172">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f314a-172">OUTPUTS</span></span>

### <span data-ttu-id="f314a-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f314a-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f314a-174">NOTES</span><span class="sxs-lookup"><span data-stu-id="f314a-174">NOTES</span></span>
<span data-ttu-id="f314a-175">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="f314a-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f314a-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f314a-176">RELATED LINKS</span></span>

[<span data-ttu-id="f314a-177">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f314a-177">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="f314a-178">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f314a-178">Remove-AzDataFactoryV2</span></span>]()
