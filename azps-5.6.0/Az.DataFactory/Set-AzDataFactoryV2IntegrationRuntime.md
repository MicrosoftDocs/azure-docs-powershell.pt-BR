---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 09b0ac3083a0440b6c229da6f45bf6412817b7ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887003"
---
# <span data-ttu-id="3e2da-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3e2da-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="3e2da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e2da-102">SYNOPSIS</span></span>
<span data-ttu-id="3e2da-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e2da-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="3e2da-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3e2da-104">SYNTAX</span></span>

### <span data-ttu-id="3e2da-105">ByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3e2da-105">ByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="3e2da-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e2da-106">ByResourceId</span></span>
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

### <span data-ttu-id="3e2da-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="3e2da-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e2da-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="3e2da-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e2da-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3e2da-109">ByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="3e2da-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3e2da-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e2da-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3e2da-111">DESCRIPTION</span></span>
<span data-ttu-id="3e2da-112">O Set-AzDataFactoryV2IntegrationRuntime atualiza um tempo de execução de integração com parâmetros específicos.</span><span class="sxs-lookup"><span data-stu-id="3e2da-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="3e2da-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e2da-113">EXAMPLES</span></span>

### <span data-ttu-id="3e2da-114">Exemplo 1: Atualizar a descrição do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="3e2da-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="3e2da-115">O cmdlet atualiza a descrição do tempo de execução de integração chamado 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="3e2da-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="3e2da-116">Exemplo 2: Compartilhar tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="3e2da-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="3e2da-117">O cmdlet adiciona o ADF para usar o tempo de execução de integração compartilhada.</span><span class="sxs-lookup"><span data-stu-id="3e2da-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="3e2da-118">Ao usar `-SharedIntegrationRuntimeResourceId` o parâmetro, `-Type` o também deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="3e2da-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="3e2da-119">Observe que o fábrica de dados precisa ter permissão para usar o tempo de execução de integração antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e2da-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="3e2da-120">Exemplo 3: Configure Self-Hosted IR como um proxy para o IR do Azure-SSIS no ADF.</span><span class="sxs-lookup"><span data-stu-id="3e2da-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="3e2da-121">O cmdlet atualiza o tempo de execução de integração do Azure-SSIS para usar o tempo de execução de integração auto-hospedado como um proxy de dados.</span><span class="sxs-lookup"><span data-stu-id="3e2da-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="3e2da-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3e2da-122">PARAMETERS</span></span>

### <span data-ttu-id="3e2da-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="3e2da-123">-AuthKey</span></span>
<span data-ttu-id="3e2da-124">A chave de autenticação do tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="3e2da-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="3e2da-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="3e2da-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="3e2da-126">A credencial de administrador de banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e2da-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="3e2da-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="3e2da-127">-CatalogPricingTier</span></span>
<span data-ttu-id="3e2da-128">A camada de preços do banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e2da-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="3e2da-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3e2da-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="3e2da-130">O ponto de extremidade do servidor de banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e2da-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="3e2da-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3e2da-131">-DataFactoryName</span></span>
<span data-ttu-id="3e2da-132">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3e2da-132">The data factory name.</span></span>

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

### <span data-ttu-id="3e2da-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="3e2da-133">-DataFlowComputeType</span></span>
<span data-ttu-id="3e2da-134">Calcular o tipo do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="3e2da-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="3e2da-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="3e2da-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="3e2da-136">Contagem principal do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="3e2da-136">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="3e2da-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="3e2da-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="3e2da-138">Hora de vida (em minutos) da configuração do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="3e2da-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="3e2da-139">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="3e2da-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="3e2da-140">O Self-Hosted de tempo de execução de integração que é usado como proxy</span><span class="sxs-lookup"><span data-stu-id="3e2da-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="3e2da-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="3e2da-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="3e2da-142">O nome do Serviço Vinculado ao Armazenamento de Blob do Azure que faz referência ao armazenamento de dados de preparação a ser usado ao mover dados entre o Self-Hosted e o Tempo de Execução de Integração do Azure-SSIS</span><span class="sxs-lookup"><span data-stu-id="3e2da-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="3e2da-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="3e2da-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="3e2da-144">O caminho no armazenamento de dados de preparação a ser usado ao mover dados entre o Self-Hosted e o Azure-SSIS Integration Runtimes, um contêiner padrão será usado se não especificado</span><span class="sxs-lookup"><span data-stu-id="3e2da-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="3e2da-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e2da-145">-DefaultProfile</span></span>
<span data-ttu-id="3e2da-146">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3e2da-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e2da-147">-Description</span><span class="sxs-lookup"><span data-stu-id="3e2da-147">-Description</span></span>
<span data-ttu-id="3e2da-148">A descrição do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e2da-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="3e2da-149">-Edition</span><span class="sxs-lookup"><span data-stu-id="3e2da-149">-Edition</span></span>
<span data-ttu-id="3e2da-150">A edição para o tempo de execução de integração do SSIS que pode ser Standard ou Enterprise, padrão é Standard se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="3e2da-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="3e2da-151">-Force</span><span class="sxs-lookup"><span data-stu-id="3e2da-151">-Force</span></span>
<span data-ttu-id="3e2da-152">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="3e2da-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3e2da-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e2da-153">-InputObject</span></span>
<span data-ttu-id="3e2da-154">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e2da-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="3e2da-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3e2da-155">-LicenseType</span></span>
<span data-ttu-id="3e2da-156">O tipo de licença que você deseja selecionar para o IR do SSIS.</span><span class="sxs-lookup"><span data-stu-id="3e2da-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="3e2da-157">Há dois tipos: LicenseIncluded ou BasePrice.</span><span class="sxs-lookup"><span data-stu-id="3e2da-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="3e2da-158">Se você estiver qualificado para o preço do Azure Hybrid Use Benefit (AHUB), selecione BasePrice.</span><span class="sxs-lookup"><span data-stu-id="3e2da-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="3e2da-159">Caso não seja, selecione LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="3e2da-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="3e2da-160">-Location</span><span class="sxs-lookup"><span data-stu-id="3e2da-160">-Location</span></span>
<span data-ttu-id="3e2da-161">O local do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e2da-161">The integration runtime location.</span></span>

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

### <span data-ttu-id="3e2da-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="3e2da-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="3e2da-163">Contagem máxima de execução paralela por nó para um tempo de execução de integração dedicado gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3e2da-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="3e2da-164">-Name</span><span class="sxs-lookup"><span data-stu-id="3e2da-164">-Name</span></span>
<span data-ttu-id="3e2da-165">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e2da-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="3e2da-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="3e2da-166">-NodeCount</span></span>
<span data-ttu-id="3e2da-167">Contagem de nós de destino do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e2da-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="3e2da-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="3e2da-168">-NodeSize</span></span>
<span data-ttu-id="3e2da-169">O tamanho do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e2da-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="3e2da-170">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="3e2da-170">-PublicIPs</span></span>
<span data-ttu-id="3e2da-171">Os endereços IP públicos estáticos que o tempo de execução de integração usará.</span><span class="sxs-lookup"><span data-stu-id="3e2da-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="3e2da-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e2da-172">-ResourceGroupName</span></span>
<span data-ttu-id="3e2da-173">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e2da-173">The resource group name.</span></span>

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

### <span data-ttu-id="3e2da-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e2da-174">-ResourceId</span></span>
<span data-ttu-id="3e2da-175">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e2da-175">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3e2da-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="3e2da-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="3e2da-177">O URI SAS do contêiner de blob do Azure que contém o script de configuração personalizado.</span><span class="sxs-lookup"><span data-stu-id="3e2da-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="3e2da-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="3e2da-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="3e2da-179">A id de recurso do tempo de execução de integração compartilhada auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="3e2da-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="3e2da-180">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="3e2da-180">-Subnet</span></span>
<span data-ttu-id="3e2da-181">O nome da sub-rede na VNet.</span><span class="sxs-lookup"><span data-stu-id="3e2da-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="3e2da-182">-Type</span><span class="sxs-lookup"><span data-stu-id="3e2da-182">-Type</span></span>
<span data-ttu-id="3e2da-183">O tipo de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3e2da-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="3e2da-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="3e2da-184">-VNetId</span></span>
<span data-ttu-id="3e2da-185">A ID da VNet que o tempo de execução de integração ins junta.</span><span class="sxs-lookup"><span data-stu-id="3e2da-185">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="3e2da-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e2da-186">-Confirm</span></span>
<span data-ttu-id="3e2da-187">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e2da-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e2da-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e2da-188">-WhatIf</span></span>
<span data-ttu-id="3e2da-189">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e2da-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3e2da-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e2da-190">CommonParameters</span></span>
<span data-ttu-id="3e2da-191">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e2da-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e2da-192">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e2da-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e2da-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e2da-193">INPUTS</span></span>

### <span data-ttu-id="3e2da-194">System.String</span><span class="sxs-lookup"><span data-stu-id="3e2da-194">System.String</span></span>

### <span data-ttu-id="3e2da-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3e2da-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3e2da-196">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3e2da-196">OUTPUTS</span></span>

### <span data-ttu-id="3e2da-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3e2da-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3e2da-198">NOTES</span><span class="sxs-lookup"><span data-stu-id="3e2da-198">NOTES</span></span>

## <span data-ttu-id="3e2da-199">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e2da-199">RELATED LINKS</span></span>

[<span data-ttu-id="3e2da-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3e2da-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
