---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113916"
---
# <span data-ttu-id="515ef-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="515ef-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="515ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="515ef-102">SYNOPSIS</span></span>
<span data-ttu-id="515ef-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="515ef-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="515ef-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="515ef-104">SYNTAX</span></span>

### <span data-ttu-id="515ef-105">SetByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="515ef-105">SetByIntegrationRuntimeName (Default)</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515ef-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="515ef-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515ef-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="515ef-107">SetByParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515ef-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="515ef-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515ef-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="515ef-109">SetByResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515ef-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="515ef-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515ef-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="515ef-111">SetByIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515ef-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="515ef-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="515ef-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="515ef-113">DESCRIPTION</span></span>
<span data-ttu-id="515ef-114">O cmdlet **Set-AzSynapseIntegrationRuntime** atualiza um tempo de execução de integração com parâmetros específicos.</span><span class="sxs-lookup"><span data-stu-id="515ef-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="515ef-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="515ef-115">EXAMPLES</span></span>

### <span data-ttu-id="515ef-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="515ef-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="515ef-117">O cmdlet atualiza a descrição do tempo de execução de integração chamado "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="515ef-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="515ef-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="515ef-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="515ef-119">O cmdlet adiciona o espaço de trabalho para usar o tempo de execução de integração compartilhada.</span><span class="sxs-lookup"><span data-stu-id="515ef-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="515ef-120">Ao usar `-SharedIntegrationRuntimeResourceId` o parâmetro, `-Type` o parâmetro também deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="515ef-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="515ef-121">Observe que o espaço de trabalho precisa ter permissão para usar o tempo de execução de integração antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="515ef-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="515ef-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="515ef-122">PARAMETERS</span></span>

### <span data-ttu-id="515ef-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="515ef-123">-AuthKey</span></span>
<span data-ttu-id="515ef-124">A chave de autenticação do tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="515ef-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="515ef-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="515ef-126">A credencial de administrador de banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="515ef-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="515ef-127">-CatalogPricingTier</span></span>
<span data-ttu-id="515ef-128">O nível de preço do banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="515ef-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="515ef-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="515ef-130">O ponto de extremidade do servidor de banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="515ef-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="515ef-131">-DataFlowComputeType</span></span>
<span data-ttu-id="515ef-132">Tipo de cálculo do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="515ef-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="515ef-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="515ef-134">Contagem principal do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="515ef-134">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="515ef-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="515ef-136">Hora de vida (em minutos) da configuração do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="515ef-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="515ef-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="515ef-138">O Self-Hosted Integration Runtime, que é usado como proxy.</span><span class="sxs-lookup"><span data-stu-id="515ef-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="515ef-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="515ef-140">O nome do Serviço Vinculado de Armazenamento de Blob do Azure que faz referência ao armazenamento de dados de preparação a ser usado ao mover dados entre o Self-Hosted e o Runtime de Integração do Azure-SSIS.</span><span class="sxs-lookup"><span data-stu-id="515ef-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="515ef-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="515ef-142">O caminho no armazenamento de dados de preparação a ser usado ao mover dados entre o Self-Hosted e o Azure-SSIS Integration Runtimes, um contêiner padrão será usado se não especificado.</span><span class="sxs-lookup"><span data-stu-id="515ef-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515ef-143">-DefaultProfile</span></span>
<span data-ttu-id="515ef-144">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="515ef-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="515ef-145">-Descrição</span><span class="sxs-lookup"><span data-stu-id="515ef-145">-Description</span></span>
<span data-ttu-id="515ef-146">A descrição de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="515ef-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="515ef-147">-Edição</span><span class="sxs-lookup"><span data-stu-id="515ef-147">-Edition</span></span>
<span data-ttu-id="515ef-148">A edição do tempo de execução de integração do SSIS que pode ser Padrão ou Enterprise, padrão é Padrão se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="515ef-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="515ef-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="515ef-150">A configuração personalizada expressa para o tempo de execução de integração do SSIS que poderia ser usado para configurações de configuração e componentes de terceiros sem script de configuração personalizada.</span><span class="sxs-lookup"><span data-stu-id="515ef-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

```yaml
Type: System.Collections.ArrayList
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-151">-Forçar</span><span class="sxs-lookup"><span data-stu-id="515ef-151">-Force</span></span>
<span data-ttu-id="515ef-152">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="515ef-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="515ef-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="515ef-153">-InputObject</span></span>
<span data-ttu-id="515ef-154">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="515ef-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: SetByIntegrationRuntimeObject, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="515ef-155">-LicenseType</span></span>
<span data-ttu-id="515ef-156">O tipo de licença que você deseja selecionar para o IR do SSIS.</span><span class="sxs-lookup"><span data-stu-id="515ef-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="515ef-157">Há dois tipos: LicenseInc ltda ou BasePrice.</span><span class="sxs-lookup"><span data-stu-id="515ef-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="515ef-158">Se você estiver qualificado para o preço do Azure Hybrid Use Benefit (AHUB), selecione Preço Base.</span><span class="sxs-lookup"><span data-stu-id="515ef-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="515ef-159">Caso não, selecione LicençaInc inclusa.</span><span class="sxs-lookup"><span data-stu-id="515ef-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-160">-Local</span><span class="sxs-lookup"><span data-stu-id="515ef-160">-Location</span></span>
<span data-ttu-id="515ef-161">A descrição de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="515ef-161">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="515ef-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="515ef-163">Contagem máxima de execução paralela por nó para um tempo de execução de integração dedicado gerenciado.</span><span class="sxs-lookup"><span data-stu-id="515ef-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-164">-Nome</span><span class="sxs-lookup"><span data-stu-id="515ef-164">-Name</span></span>
<span data-ttu-id="515ef-165">O nome de tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="515ef-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName, SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="515ef-166">-NodeCount</span></span>
<span data-ttu-id="515ef-167">Contagem de nós de destino do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="515ef-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="515ef-168">-NodeSize</span></span>
<span data-ttu-id="515ef-169">O tamanho do nó de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="515ef-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="515ef-170">-PublicIP</span></span>
<span data-ttu-id="515ef-171">Os endereços IP públicos estáticos que o tempo de execução da integração usará.</span><span class="sxs-lookup"><span data-stu-id="515ef-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: PublicIPs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="515ef-172">-ResourceGroupName</span></span>
<span data-ttu-id="515ef-173">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="515ef-173">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="515ef-174">-ResourceId</span></span>
<span data-ttu-id="515ef-175">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="515ef-175">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByLinkedIntegrationRuntimeResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="515ef-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="515ef-177">O URI SAS do contêiner de blob do Azure que contém o script de configuração personalizada.</span><span class="sxs-lookup"><span data-stu-id="515ef-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="515ef-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="515ef-179">A ID do recurso do tempo de execução de integração auto-hospedado compartilhado.</span><span class="sxs-lookup"><span data-stu-id="515ef-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLinkedIntegrationRuntimeName, SetByLinkedIntegrationRuntimeParentObject, SetByLinkedIntegrationRuntimeResourceId, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-180">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="515ef-180">-Subnet</span></span>
<span data-ttu-id="515ef-181">O nome da sub-rede na VNet.</span><span class="sxs-lookup"><span data-stu-id="515ef-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-182">-Tipo</span><span class="sxs-lookup"><span data-stu-id="515ef-182">-Type</span></span>
<span data-ttu-id="515ef-183">O tipo de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="515ef-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="515ef-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="515ef-184">-VNetId</span></span>
<span data-ttu-id="515ef-185">A ID da VNet na qual o tempo de execução de integração será integrado.</span><span class="sxs-lookup"><span data-stu-id="515ef-185">The ID of the VNet which the integration runtime will join.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-186">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="515ef-186">-WorkspaceName</span></span>
<span data-ttu-id="515ef-187">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="515ef-187">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="515ef-188">-WorkspaceObject</span></span>
<span data-ttu-id="515ef-189">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="515ef-189">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="515ef-190">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="515ef-190">-Confirm</span></span>
<span data-ttu-id="515ef-191">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="515ef-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="515ef-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="515ef-192">-WhatIf</span></span>
<span data-ttu-id="515ef-193">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="515ef-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="515ef-194">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="515ef-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="515ef-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515ef-195">CommonParameters</span></span>
<span data-ttu-id="515ef-196">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="515ef-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515ef-197">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="515ef-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515ef-198">Entradas</span><span class="sxs-lookup"><span data-stu-id="515ef-198">INPUTS</span></span>

### <span data-ttu-id="515ef-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="515ef-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="515ef-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="515ef-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="515ef-201">Saídas</span><span class="sxs-lookup"><span data-stu-id="515ef-201">OUTPUTS</span></span>

### <span data-ttu-id="515ef-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="515ef-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="515ef-203">Notas</span><span class="sxs-lookup"><span data-stu-id="515ef-203">NOTES</span></span>

## <span data-ttu-id="515ef-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="515ef-204">RELATED LINKS</span></span>
