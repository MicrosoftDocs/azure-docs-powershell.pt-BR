---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 5020ddeccc755ef52bf7410d61eb57b637d261bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257200"
---
# <span data-ttu-id="e7fdb-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e7fdb-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="e7fdb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fdb-103">Cria uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-103">Creates a data factory.</span></span>

## <span data-ttu-id="e7fdb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7fdb-104">SYNTAX</span></span>

### <span data-ttu-id="e7fdb-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e7fdb-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7fdb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7fdb-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7fdb-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="e7fdb-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7fdb-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="e7fdb-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7fdb-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="e7fdb-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7fdb-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="e7fdb-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7fdb-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e7fdb-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7fdb-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="e7fdb-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7fdb-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="e7fdb-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7fdb-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7fdb-114">DESCRIPTION</span></span>
<span data-ttu-id="e7fdb-115">O cmdlet **set-AzDataFactoryV2** cria uma fábrica de dados com o nome e o local do grupo de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="e7fdb-116">Execute estas operações na seguinte ordem:--Crie uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="e7fdb-117">--Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-117">-- Create linked services.</span></span>
<span data-ttu-id="e7fdb-118">--Criar conjuntos de valores.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-118">-- Create datasets.</span></span>
<span data-ttu-id="e7fdb-119">--Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="e7fdb-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7fdb-120">EXAMPLES</span></span>

### <span data-ttu-id="e7fdb-121">Exemplo 1: criar uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="e7fdb-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="e7fdb-122">Exemplo 2: criar uma fábrica de dados com detalhes de configuração do repositório usando um objeto de fábrica existente.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
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

<span data-ttu-id="e7fdb-123">Esse comando cria uma fábrica de dados chamada WikiADF no grupo de recursos chamado ADF no local da Eastus com a configuração de controle de origem do DevOps do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="e7fdb-124">Exemplo 3: criar uma fábrica de dados com detalhes de configuração do repositório do GitHub usando um novo objeto de fábrica.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
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

<span data-ttu-id="e7fdb-125">Esse comando cria um data Factory chamado WikiADF no grupo de recursos chamado ADF no local da Eastus com configuração de controle de origem do GitHub..</span><span class="sxs-lookup"><span data-stu-id="e7fdb-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="e7fdb-126">OS</span><span class="sxs-lookup"><span data-stu-id="e7fdb-126">PARAMETERS</span></span>

### <span data-ttu-id="e7fdb-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e7fdb-127">-AccountName</span></span>
<span data-ttu-id="e7fdb-128">O nome da conta para a configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-128">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="e7fdb-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="e7fdb-129">-CollaborationBranch</span></span>
<span data-ttu-id="e7fdb-130">A ramificação de colaboração para a configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-130">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="e7fdb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7fdb-131">-DefaultProfile</span></span>
<span data-ttu-id="e7fdb-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7fdb-133">-Force</span><span class="sxs-lookup"><span data-stu-id="e7fdb-133">-Force</span></span>
<span data-ttu-id="e7fdb-134">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e7fdb-135">-GlobalParameterDefinition</span><span class="sxs-lookup"><span data-stu-id="e7fdb-135">-GlobalParameterDefinition</span></span>
<span data-ttu-id="e7fdb-136">O dicionário que contém os parâmetros globais da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-136">The dictionary containing the global parameters of the data factory.</span></span>

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

### <span data-ttu-id="e7fdb-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="e7fdb-137">-HostName</span></span>
<span data-ttu-id="e7fdb-138">O nome do host para configuração do repositório do GitHub.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-138">The host name for GitHub repo configuration.</span></span>

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

### <span data-ttu-id="e7fdb-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7fdb-139">-InputObject</span></span>
<span data-ttu-id="e7fdb-140">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-140">The data factory object.</span></span>

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

### <span data-ttu-id="e7fdb-141">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="e7fdb-141">-LastCommitId</span></span>
<span data-ttu-id="e7fdb-142">A última ID de confirmação da configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-142">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="e7fdb-143">-Local</span><span class="sxs-lookup"><span data-stu-id="e7fdb-143">-Location</span></span>
<span data-ttu-id="e7fdb-144">A fábrica de dados é criada nessa região.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-144">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="e7fdb-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7fdb-145">-Name</span></span>
<span data-ttu-id="e7fdb-146">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-146">The data factory name.</span></span>

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

### <span data-ttu-id="e7fdb-147">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="e7fdb-147">-ProjectName</span></span>
<span data-ttu-id="e7fdb-148">O nome do projeto DevOps para a configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-148">The project name Azure DevOps for repo configuration.</span></span>

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

### <span data-ttu-id="e7fdb-149">-Repositoryname</span><span class="sxs-lookup"><span data-stu-id="e7fdb-149">-RepositoryName</span></span>
<span data-ttu-id="e7fdb-150">O nome do repositório para a configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-150">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="e7fdb-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7fdb-151">-ResourceGroupName</span></span>
<span data-ttu-id="e7fdb-152">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-152">The resource group name.</span></span>

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

### <span data-ttu-id="e7fdb-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7fdb-153">-ResourceId</span></span>
<span data-ttu-id="e7fdb-154">A ID de recurso do Azure da fábrica de dados v2.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-154">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="e7fdb-155">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="e7fdb-155">-RootFolder</span></span>
<span data-ttu-id="e7fdb-156">A pasta raiz da configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-156">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="e7fdb-157">-Marca</span><span class="sxs-lookup"><span data-stu-id="e7fdb-157">-Tag</span></span>
<span data-ttu-id="e7fdb-158">As marcas do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-158">The tags of the data factory.</span></span>

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

### <span data-ttu-id="e7fdb-159">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="e7fdb-159">-TenantId</span></span>
<span data-ttu-id="e7fdb-160">A ID de locatário da configuração do repositório do Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-160">The tenant id for Azure DevOps repo configuration.</span></span>

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

### <span data-ttu-id="e7fdb-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7fdb-161">-Confirm</span></span>
<span data-ttu-id="e7fdb-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7fdb-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7fdb-163">-WhatIf</span></span>
<span data-ttu-id="e7fdb-164">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e7fdb-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fdb-165">CommonParameters</span></span>
<span data-ttu-id="e7fdb-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7fdb-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7fdb-167">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7fdb-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fdb-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7fdb-168">INPUTS</span></span>

### <span data-ttu-id="e7fdb-169">System. String</span><span class="sxs-lookup"><span data-stu-id="e7fdb-169">System.String</span></span>

### <span data-ttu-id="e7fdb-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e7fdb-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="e7fdb-171">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e7fdb-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e7fdb-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7fdb-172">OUTPUTS</span></span>

### <span data-ttu-id="e7fdb-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e7fdb-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e7fdb-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7fdb-174">NOTES</span></span>
<span data-ttu-id="e7fdb-175">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="e7fdb-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e7fdb-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7fdb-176">RELATED LINKS</span></span>

[<span data-ttu-id="e7fdb-177">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e7fdb-177">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="e7fdb-178">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e7fdb-178">Remove-AzDataFactoryV2</span></span>]()
