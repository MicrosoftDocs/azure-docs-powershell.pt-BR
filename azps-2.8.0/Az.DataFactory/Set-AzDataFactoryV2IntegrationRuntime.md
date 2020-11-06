---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 274c6cda9154348bfeffe600fd19512d1a85502d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596966"
---
# <span data-ttu-id="f5419-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f5419-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="f5419-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5419-102">SYNOPSIS</span></span>
<span data-ttu-id="f5419-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5419-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="f5419-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5419-104">SYNTAX</span></span>

### <span data-ttu-id="f5419-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f5419-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5419-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5419-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5419-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="f5419-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5419-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f5419-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5419-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f5419-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]  [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5419-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f5419-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5419-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5419-111">DESCRIPTION</span></span>
<span data-ttu-id="f5419-112">O cmdlet Set-AzDataFactoryV2IntegrationRuntime atualiza um tempo de execução de integração com parâmetros específicos.</span><span class="sxs-lookup"><span data-stu-id="f5419-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="f5419-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5419-113">EXAMPLES</span></span>

### <span data-ttu-id="f5419-114">Exemplo 1: Descrição da atualização do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5419-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="f5419-115">O cmdlet atualiza a descrição do tempo de execução de integração chamado ' test-selfhost-IV '.</span><span class="sxs-lookup"><span data-stu-id="f5419-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="f5419-116">Exemplo 2: compartilhar o tempo de execução de integração de hospedagem automática.</span><span class="sxs-lookup"><span data-stu-id="f5419-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="f5419-117">O cmdlet adiciona o ADF para usar o tempo de execução de integração compartilhada.</span><span class="sxs-lookup"><span data-stu-id="f5419-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="f5419-118">Ao usar `-SharedIntegrationRuntimeResourceId` o parâmetro, o `-Type` também deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="f5419-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="f5419-119">Observe que a fábrica de dados precisa receber permissão para usar o tempo de execução de integração antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5419-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="f5419-120">Exemplo 3: configurar o Self-Hosted IR como um proxy para o Azure-SSIS IV no ADF.</span><span class="sxs-lookup"><span data-stu-id="f5419-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName testgroup `
                                           -DataFactoryName testdf `
                                           -Name SSISIRWithDataProxy `
                                           -DataProxyIntegrationRuntimeName proxySelfhostedIR `
                                           -DataProxyStagingLinkedServiceName AzureBlobStorage `
                                           -DataProxyStagingPath teststaging

    Location                          : EastUS
    NodeSize                          : Standard_D8_v3
    NodeCount                         : 1
    MaxParallelExecutionsPerNode      : 8
    CatalogServerEndpoint             : 
    CatalogAdminUserName              : 
    CatalogAdminPassword              : 
    CatalogPricingTier                : 
    VNetId                            : 
    Subnet                            : 
    State                             : Initial
    LicenseType                       : LicenseIncluded
    SetupScriptContainerSasUri        : 
    DataProxyIntegrationRuntimeName   : proxySelfhostedIR
    DataProxyStagingLinkedServiceName : AzureBlobStorage
    DataProxyStagingPath              : 
    Edition                           : Standard
    Name                              : SSISIRWithDataProxy
    Type                              : Managed
    ResourceGroupName                 : testgroup
    DataFactoryName                   : testdf
    Description                       : 
    Id                                : /subscriptions/cb715d05-3337-4640-8c43-4f943c50d06e/resourceGroups/testgroup/providers/Microsoft.DataFactory/factories/testdf/integrationruntimes/SSISIRWithDataProxy
```

<span data-ttu-id="f5419-121">O cmdlet Update o tempo de execução de integração do Azure-SSIS para usar o tempo de execução de integração de hospedagem interna como um proxy de dados.</span><span class="sxs-lookup"><span data-stu-id="f5419-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="f5419-122">OS</span><span class="sxs-lookup"><span data-stu-id="f5419-122">PARAMETERS</span></span>

### <span data-ttu-id="f5419-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="f5419-123">-AuthKey</span></span>
<span data-ttu-id="f5419-124">A chave de autenticação do tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="f5419-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="f5419-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="f5419-126">A credencial de administrador do banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5419-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="f5419-127">-CatalogPricingTier</span></span>
<span data-ttu-id="f5419-128">O nível de preço do banco de dados do catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5419-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5419-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="f5419-130">O ponto de extremidade do servidor de banco de dados catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5419-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-131">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f5419-131">-DataFactoryName</span></span>
<span data-ttu-id="f5419-132">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="f5419-132">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-133">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f5419-133">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="f5419-134">O nome do tempo de execução de integração do Self-Hosted que é usado como um proxy</span><span class="sxs-lookup"><span data-stu-id="f5419-134">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-135">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="f5419-135">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="f5419-136">O nome do serviço vinculado do armazenamento do blob do Azure que faz referência ao repositório de dados de preparação a ser usado ao mover dados entre Self-Hosted e o tempo de execução de integração do Azure-SSIS</span><span class="sxs-lookup"><span data-stu-id="f5419-136">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-137">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="f5419-137">-DataProxyStagingPath</span></span>
<span data-ttu-id="f5419-138">O caminho no repositório de dados de preparo a ser usado ao mover dados entre Self-Hosted e os tempos de execução de integração do Azure-SSIS, um contêiner padrão será usado se não for especificado</span><span class="sxs-lookup"><span data-stu-id="f5419-138">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5419-139">-DefaultProfile</span></span>
<span data-ttu-id="f5419-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5419-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5419-141">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f5419-141">-Description</span></span>
<span data-ttu-id="f5419-142">A descrição do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5419-142">The integration runtime description.</span></span>

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

### <span data-ttu-id="f5419-143">-Edição</span><span class="sxs-lookup"><span data-stu-id="f5419-143">-Edition</span></span>
<span data-ttu-id="f5419-144">A edição para o tempo de execução de integração do SSIS que pode ser Standard ou Enterprise, o padrão é padrão se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="f5419-144">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-145">-Force</span><span class="sxs-lookup"><span data-stu-id="f5419-145">-Force</span></span>
<span data-ttu-id="f5419-146">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="f5419-146">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f5419-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5419-147">-InputObject</span></span>
<span data-ttu-id="f5419-148">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5419-148">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f5419-149">-LicenseType</span></span>
<span data-ttu-id="f5419-150">O tipo de licença que você deseja selecionar para o SSIS IV.</span><span class="sxs-lookup"><span data-stu-id="f5419-150">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="f5419-151">Há dois tipos: LicenseIncluded ou BasePrice.</span><span class="sxs-lookup"><span data-stu-id="f5419-151">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="f5419-152">Se você estiver qualificado para o preço do Azure Hybrid use beneficie-se (AHUB), selecione BasePrice.</span><span class="sxs-lookup"><span data-stu-id="f5419-152">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="f5419-153">Caso contrário, selecione LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="f5419-153">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-154">-Local</span><span class="sxs-lookup"><span data-stu-id="f5419-154">-Location</span></span>
<span data-ttu-id="f5419-155">O local do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5419-155">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-156">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="f5419-156">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="f5419-157">Contagem máxima de execuções paralelas por nó para um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f5419-157">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-158">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5419-158">-Name</span></span>
<span data-ttu-id="f5419-159">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="f5419-159">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-160">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="f5419-160">-NodeCount</span></span>
<span data-ttu-id="f5419-161">Contagem de nós de destino do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5419-161">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-162">-Nós</span><span class="sxs-lookup"><span data-stu-id="f5419-162">-NodeSize</span></span>
<span data-ttu-id="f5419-163">O tamanho do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5419-163">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5419-164">-ResourceGroupName</span></span>
<span data-ttu-id="f5419-165">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5419-165">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-166">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5419-166">-ResourceId</span></span>
<span data-ttu-id="f5419-167">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="f5419-167">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByLinkedIntegrationRuntimeResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-168">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="f5419-168">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="f5419-169">O URI da SAS do contêiner de blob do Azure que contém o script de instalação personalizada.</span><span class="sxs-lookup"><span data-stu-id="f5419-169">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-170">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="f5419-170">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="f5419-171">A ID do recurso do tempo de execução de integração de hospedagem automática compartilhada.</span><span class="sxs-lookup"><span data-stu-id="f5419-171">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLinkedIntegrationRuntimeResourceId, ByLinkedIntegrationRuntimeName, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-172">-Subnet</span><span class="sxs-lookup"><span data-stu-id="f5419-172">-Subnet</span></span>
<span data-ttu-id="f5419-173">O nome da sub-rede na VNet.</span><span class="sxs-lookup"><span data-stu-id="f5419-173">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-174">-Digite</span><span class="sxs-lookup"><span data-stu-id="f5419-174">-Type</span></span>
<span data-ttu-id="f5419-175">O tipo de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5419-175">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-176">-VNetId</span><span class="sxs-lookup"><span data-stu-id="f5419-176">-VNetId</span></span>
<span data-ttu-id="f5419-177">A ID da VNet que o tempo de execução de integração une.</span><span class="sxs-lookup"><span data-stu-id="f5419-177">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5419-178">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5419-178">-Confirm</span></span>
<span data-ttu-id="f5419-179">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5419-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5419-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5419-180">-WhatIf</span></span>
<span data-ttu-id="f5419-181">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5419-181">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f5419-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5419-182">CommonParameters</span></span>
<span data-ttu-id="f5419-183">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5419-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5419-184">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5419-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5419-185">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5419-185">INPUTS</span></span>

### <span data-ttu-id="f5419-186">System. String</span><span class="sxs-lookup"><span data-stu-id="f5419-186">System.String</span></span>

### <span data-ttu-id="f5419-187">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f5419-187">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f5419-188">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5419-188">OUTPUTS</span></span>

### <span data-ttu-id="f5419-189">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f5419-189">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f5419-190">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5419-190">NOTES</span></span>

## <span data-ttu-id="f5419-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5419-191">RELATED LINKS</span></span>

[<span data-ttu-id="f5419-192">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f5419-192">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
