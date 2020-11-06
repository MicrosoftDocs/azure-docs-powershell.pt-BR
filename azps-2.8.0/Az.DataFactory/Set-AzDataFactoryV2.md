---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 374263c26a3572e8d85e18d1795c27a761866a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596972"
---
# <span data-ttu-id="d2855-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d2855-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="d2855-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2855-102">SYNOPSIS</span></span>
<span data-ttu-id="d2855-103">Cria uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d2855-103">Creates a data factory.</span></span>

## <span data-ttu-id="d2855-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2855-104">SYNTAX</span></span>

### <span data-ttu-id="d2855-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d2855-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2855-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2855-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2855-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="d2855-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2855-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="d2855-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2855-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="d2855-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2855-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="d2855-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2855-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d2855-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2855-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="d2855-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2855-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="d2855-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2855-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2855-114">DESCRIPTION</span></span>
<span data-ttu-id="d2855-115">O cmdlet **set-AzDataFactoryV2** cria uma fábrica de dados com o nome e o local do grupo de recursos especificados.</span><span class="sxs-lookup"><span data-stu-id="d2855-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="d2855-116">Execute estas operações na seguinte ordem:--Crie uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d2855-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="d2855-117">--Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="d2855-117">-- Create linked services.</span></span>
<span data-ttu-id="d2855-118">--Criar conjuntos de valores.</span><span class="sxs-lookup"><span data-stu-id="d2855-118">-- Create datasets.</span></span>
<span data-ttu-id="d2855-119">--Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="d2855-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="d2855-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2855-120">EXAMPLES</span></span>

### <span data-ttu-id="d2855-121">Exemplo 1: criar uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="d2855-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="d2855-122">Exemplo 2: criar uma fábrica de dados com detalhes do repoconfiguration usando um objeto de fábrica existente.</span><span class="sxs-lookup"><span data-stu-id="d2855-122">Example 2: Create a data factory with repoconfiguration details using an existing factory object.</span></span>
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

<span data-ttu-id="d2855-123">Esse comando cria um data Factory chamado WikiADF no grupo de recursos chamado ADF no local da Westus.</span><span class="sxs-lookup"><span data-stu-id="d2855-123">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="d2855-124">OS</span><span class="sxs-lookup"><span data-stu-id="d2855-124">PARAMETERS</span></span>

### <span data-ttu-id="d2855-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2855-125">-AccountName</span></span>
<span data-ttu-id="d2855-126">O nome da conta para a configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="d2855-126">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="d2855-127">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="d2855-127">-CollaborationBranch</span></span>
<span data-ttu-id="d2855-128">A ramificação de colaboração para a configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="d2855-128">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="d2855-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2855-129">-DefaultProfile</span></span>
<span data-ttu-id="d2855-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2855-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2855-131">-Force</span><span class="sxs-lookup"><span data-stu-id="d2855-131">-Force</span></span>
<span data-ttu-id="d2855-132">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="d2855-132">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d2855-133">-HostName</span><span class="sxs-lookup"><span data-stu-id="d2855-133">-HostName</span></span>
<span data-ttu-id="d2855-134">O nome do host para a configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="d2855-134">The host name for repo configuration.</span></span>

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

### <span data-ttu-id="d2855-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2855-135">-InputObject</span></span>
<span data-ttu-id="d2855-136">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d2855-136">The data factory object.</span></span>

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

### <span data-ttu-id="d2855-137">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="d2855-137">-LastCommitId</span></span>
<span data-ttu-id="d2855-138">A última ID de confirmação da configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="d2855-138">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="d2855-139">-Local</span><span class="sxs-lookup"><span data-stu-id="d2855-139">-Location</span></span>
<span data-ttu-id="d2855-140">A fábrica de dados é criada nessa região.</span><span class="sxs-lookup"><span data-stu-id="d2855-140">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="d2855-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2855-141">-Name</span></span>
<span data-ttu-id="d2855-142">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="d2855-142">The data factory name.</span></span>

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

### <span data-ttu-id="d2855-143">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="d2855-143">-ProjectName</span></span>
<span data-ttu-id="d2855-144">O nome do projeto para a configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="d2855-144">The project name for repo configuration.</span></span>

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

### <span data-ttu-id="d2855-145">-Repositoryname</span><span class="sxs-lookup"><span data-stu-id="d2855-145">-RepositoryName</span></span>
<span data-ttu-id="d2855-146">O nome do repositório para a configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="d2855-146">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="d2855-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2855-147">-ResourceGroupName</span></span>
<span data-ttu-id="d2855-148">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2855-148">The resource group name.</span></span>

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

### <span data-ttu-id="d2855-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2855-149">-ResourceId</span></span>
<span data-ttu-id="d2855-150">A ID de recurso do Azure da fábrica de dados v2.</span><span class="sxs-lookup"><span data-stu-id="d2855-150">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="d2855-151">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="d2855-151">-RootFolder</span></span>
<span data-ttu-id="d2855-152">A pasta raiz da configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="d2855-152">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="d2855-153">-Marca</span><span class="sxs-lookup"><span data-stu-id="d2855-153">-Tag</span></span>
<span data-ttu-id="d2855-154">As marcas do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="d2855-154">The tags of the data factory.</span></span>

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

### <span data-ttu-id="d2855-155">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="d2855-155">-TenantId</span></span>
<span data-ttu-id="d2855-156">A ID do locatário para a configuração do repositório.</span><span class="sxs-lookup"><span data-stu-id="d2855-156">The tenant id for repo configuration.</span></span>

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

### <span data-ttu-id="d2855-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2855-157">-Confirm</span></span>
<span data-ttu-id="d2855-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2855-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2855-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2855-159">-WhatIf</span></span>
<span data-ttu-id="d2855-160">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2855-160">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d2855-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2855-161">CommonParameters</span></span>
<span data-ttu-id="d2855-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2855-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2855-163">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2855-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2855-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2855-164">INPUTS</span></span>

### <span data-ttu-id="d2855-165">System. String</span><span class="sxs-lookup"><span data-stu-id="d2855-165">System.String</span></span>

### <span data-ttu-id="d2855-166">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d2855-166">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d2855-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2855-167">OUTPUTS</span></span>

### <span data-ttu-id="d2855-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d2855-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d2855-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2855-169">NOTES</span></span>
<span data-ttu-id="d2855-170">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="d2855-170">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d2855-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2855-171">RELATED LINKS</span></span>

[<span data-ttu-id="d2855-172">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d2855-172">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="d2855-173">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d2855-173">Remove-AzDataFactoryV2</span></span>]()
