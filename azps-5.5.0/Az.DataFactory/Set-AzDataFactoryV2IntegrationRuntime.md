---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0a687c1a2c21301ca61d92d7c4701d7b59d227f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117742"
---
# <span data-ttu-id="43c72-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="43c72-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="43c72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43c72-102">SYNOPSIS</span></span>
<span data-ttu-id="43c72-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="43c72-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="43c72-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43c72-104">SYNTAX</span></span>

### <span data-ttu-id="43c72-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="43c72-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-ExpressCustomSetup <ArrayList>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>]
 [-DataProxyStagingPath <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]
 [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43c72-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="43c72-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIPs <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43c72-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="43c72-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43c72-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="43c72-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43c72-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="43c72-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43c72-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="43c72-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43c72-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="43c72-111">DESCRIPTION</span></span>
<span data-ttu-id="43c72-112">O Set-AzDataFactoryV2IntegrationRuntime cmdlet atualiza um tempo de execução de integração com parâmetros específicos.</span><span class="sxs-lookup"><span data-stu-id="43c72-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="43c72-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="43c72-113">EXAMPLES</span></span>

### <span data-ttu-id="43c72-114">Exemplo 1: Descrição de tempo de execução de integração de atualização.</span><span class="sxs-lookup"><span data-stu-id="43c72-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="43c72-115">O cmdlet atualiza a descrição do tempo de execução de integração chamado "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="43c72-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="43c72-116">Exemplo 2: Compartilhar tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="43c72-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="43c72-117">O cmdlet adiciona o ADF para usar o tempo de execução de integração compartilhada.</span><span class="sxs-lookup"><span data-stu-id="43c72-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="43c72-118">Ao usar `-SharedIntegrationRuntimeResourceId` o parâmetro, `-Type` o parâmetro também deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="43c72-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="43c72-119">Observe que o data factory precisa ter permissão para usar o tempo de execução de integração antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43c72-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="43c72-120">Exemplo 3: Configurar Self-Hosted IR como um proxy para IR do Azure-SSIS no ADF.</span><span class="sxs-lookup"><span data-stu-id="43c72-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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
    PublicIPs                         : 
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

<span data-ttu-id="43c72-121">O cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span><span class="sxs-lookup"><span data-stu-id="43c72-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="43c72-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43c72-122">PARAMETERS</span></span>

### <span data-ttu-id="43c72-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="43c72-123">-AuthKey</span></span>
<span data-ttu-id="43c72-124">A chave de autenticação do tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="43c72-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="43c72-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="43c72-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="43c72-126">A credencial de administrador de banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="43c72-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="43c72-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="43c72-127">-CatalogPricingTier</span></span>
<span data-ttu-id="43c72-128">O nível de preço do banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="43c72-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="43c72-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="43c72-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="43c72-130">O ponto de extremidade do servidor de banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="43c72-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="43c72-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="43c72-131">-DataFactoryName</span></span>
<span data-ttu-id="43c72-132">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="43c72-132">The data factory name.</span></span>

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

### <span data-ttu-id="43c72-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="43c72-133">-DataFlowComputeType</span></span>
<span data-ttu-id="43c72-134">Tipo de cálculo do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="43c72-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="43c72-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="43c72-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="43c72-136">Contagem principal do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="43c72-136">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="43c72-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="43c72-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="43c72-138">Hora de vida (em minutos) da configuração do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="43c72-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="43c72-139">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="43c72-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="43c72-140">O Self-Hosted Integration Runtime, que é usado como proxy</span><span class="sxs-lookup"><span data-stu-id="43c72-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="43c72-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="43c72-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="43c72-142">O nome do Serviço Vinculado de Armazenamento de Blob do Azure que faz referência ao armazenamento de dados de preparação a ser usado ao mover dados entre o Self-Hosted e o Runtime de Integração do Azure-SSIS</span><span class="sxs-lookup"><span data-stu-id="43c72-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="43c72-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="43c72-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="43c72-144">O caminho no armazenamento de dados de preparação a ser usado ao mover dados entre o Self-Hosted e o Azure-SSIS Integration Runtimes, um contêiner padrão será usado se não especificado</span><span class="sxs-lookup"><span data-stu-id="43c72-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="43c72-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c72-145">-DefaultProfile</span></span>
<span data-ttu-id="43c72-146">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="43c72-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43c72-147">-Descrição</span><span class="sxs-lookup"><span data-stu-id="43c72-147">-Description</span></span>
<span data-ttu-id="43c72-148">A descrição de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="43c72-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="43c72-149">-Edição</span><span class="sxs-lookup"><span data-stu-id="43c72-149">-Edition</span></span>
<span data-ttu-id="43c72-150">A edição do tempo de execução de integração do SSIS que pode ser Padrão ou Enterprise, padrão é Padrão se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="43c72-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="43c72-151">-Forçar</span><span class="sxs-lookup"><span data-stu-id="43c72-151">-Force</span></span>
<span data-ttu-id="43c72-152">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="43c72-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="43c72-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43c72-153">-InputObject</span></span>
<span data-ttu-id="43c72-154">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="43c72-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="43c72-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="43c72-155">-LicenseType</span></span>
<span data-ttu-id="43c72-156">O tipo de licença que você deseja selecionar para o IR do SSIS.</span><span class="sxs-lookup"><span data-stu-id="43c72-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="43c72-157">Há dois tipos: LicenseInc ltda ou BasePrice.</span><span class="sxs-lookup"><span data-stu-id="43c72-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="43c72-158">Se você estiver qualificado para o preço do Azure Hybrid Use Benefit (AHUB), selecione Preço Base.</span><span class="sxs-lookup"><span data-stu-id="43c72-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="43c72-159">Caso não, selecione LicençaInc inclusa.</span><span class="sxs-lookup"><span data-stu-id="43c72-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="43c72-160">-Local</span><span class="sxs-lookup"><span data-stu-id="43c72-160">-Location</span></span>
<span data-ttu-id="43c72-161">O local de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="43c72-161">The integration runtime location.</span></span>

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

### <span data-ttu-id="43c72-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="43c72-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="43c72-163">Contagem máxima de execução paralela por nó para um tempo de execução de integração dedicado gerenciado.</span><span class="sxs-lookup"><span data-stu-id="43c72-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="43c72-164">-Nome</span><span class="sxs-lookup"><span data-stu-id="43c72-164">-Name</span></span>
<span data-ttu-id="43c72-165">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="43c72-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="43c72-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="43c72-166">-NodeCount</span></span>
<span data-ttu-id="43c72-167">Contagem de nós de destino do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="43c72-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="43c72-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="43c72-168">-NodeSize</span></span>
<span data-ttu-id="43c72-169">O tamanho do nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="43c72-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="43c72-170">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="43c72-170">-PublicIPs</span></span>
<span data-ttu-id="43c72-171">Os endereços IP públicos estáticos que o tempo de execução da integração usará.</span><span class="sxs-lookup"><span data-stu-id="43c72-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c72-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43c72-172">-ResourceGroupName</span></span>
<span data-ttu-id="43c72-173">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="43c72-173">The resource group name.</span></span>

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

### <span data-ttu-id="43c72-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43c72-174">-ResourceId</span></span>
<span data-ttu-id="43c72-175">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="43c72-175">The Azure resource ID.</span></span>

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

### <span data-ttu-id="43c72-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="43c72-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="43c72-177">O URI SAS do contêiner de blob do Azure que contém o script de configuração personalizada.</span><span class="sxs-lookup"><span data-stu-id="43c72-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="43c72-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="43c72-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="43c72-179">A ID do recurso do tempo de execução de integração auto-hospedado compartilhado.</span><span class="sxs-lookup"><span data-stu-id="43c72-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="43c72-180">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="43c72-180">-Subnet</span></span>
<span data-ttu-id="43c72-181">O nome da sub-rede na VNet.</span><span class="sxs-lookup"><span data-stu-id="43c72-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="43c72-182">-Tipo</span><span class="sxs-lookup"><span data-stu-id="43c72-182">-Type</span></span>
<span data-ttu-id="43c72-183">O tipo de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="43c72-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="43c72-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="43c72-184">-VNetId</span></span>
<span data-ttu-id="43c72-185">A ID da VNet em que o tempo de execução de integração se une.</span><span class="sxs-lookup"><span data-stu-id="43c72-185">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="43c72-186">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="43c72-186">-Confirm</span></span>
<span data-ttu-id="43c72-187">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43c72-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43c72-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43c72-188">-WhatIf</span></span>
<span data-ttu-id="43c72-189">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43c72-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="43c72-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c72-190">CommonParameters</span></span>
<span data-ttu-id="43c72-191">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c72-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c72-192">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43c72-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c72-193">Entradas</span><span class="sxs-lookup"><span data-stu-id="43c72-193">INPUTS</span></span>

### <span data-ttu-id="43c72-194">System.String</span><span class="sxs-lookup"><span data-stu-id="43c72-194">System.String</span></span>

### <span data-ttu-id="43c72-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="43c72-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="43c72-196">Saídas</span><span class="sxs-lookup"><span data-stu-id="43c72-196">OUTPUTS</span></span>

### <span data-ttu-id="43c72-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="43c72-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="43c72-198">Notas</span><span class="sxs-lookup"><span data-stu-id="43c72-198">NOTES</span></span>

## <span data-ttu-id="43c72-199">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43c72-199">RELATED LINKS</span></span>

[<span data-ttu-id="43c72-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="43c72-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
