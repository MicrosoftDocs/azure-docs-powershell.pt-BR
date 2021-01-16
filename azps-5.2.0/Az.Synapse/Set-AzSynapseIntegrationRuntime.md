---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258277"
---
# <span data-ttu-id="c5bd2-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c5bd2-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="c5bd2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bd2-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="c5bd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5bd2-104">SYNTAX</span></span>

### <span data-ttu-id="c5bd2-105">SetByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c5bd2-105">SetByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="c5bd2-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c5bd2-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5bd2-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="c5bd2-107">SetByParentObject</span></span>
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

### <span data-ttu-id="c5bd2-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="c5bd2-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5bd2-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c5bd2-109">SetByResourceId</span></span>
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

### <span data-ttu-id="c5bd2-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="c5bd2-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5bd2-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c5bd2-111">SetByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="c5bd2-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c5bd2-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5bd2-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5bd2-113">DESCRIPTION</span></span>
<span data-ttu-id="c5bd2-114">O cmdlet **set-AzSynapseIntegrationRuntime** atualiza um tempo de execução de integração com parâmetros específicos.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="c5bd2-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5bd2-115">EXAMPLES</span></span>

### <span data-ttu-id="c5bd2-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5bd2-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="c5bd2-117">O cmdlet atualiza a descrição do tempo de execução de integração chamado ' test-selfhost-IV '.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="c5bd2-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c5bd2-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="c5bd2-119">O cmdlet adiciona o espaço de trabalho para usar o tempo de execução de integração compartilhada.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="c5bd2-120">Ao usar `-SharedIntegrationRuntimeResourceId` o parâmetro, o `-Type` também deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="c5bd2-121">Observe que o espaço de trabalho precisa ser concedido permissão para usar o tempo de execução de integração antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="c5bd2-122">OS</span><span class="sxs-lookup"><span data-stu-id="c5bd2-122">PARAMETERS</span></span>

### <span data-ttu-id="c5bd2-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="c5bd2-123">-AuthKey</span></span>
<span data-ttu-id="c5bd2-124">A chave de autenticação do tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="c5bd2-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="c5bd2-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="c5bd2-126">A credencial de administrador do banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="c5bd2-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="c5bd2-127">-CatalogPricingTier</span></span>
<span data-ttu-id="c5bd2-128">O nível de preço do banco de dados do catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="c5bd2-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5bd2-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="c5bd2-130">O ponto de extremidade do servidor de banco de dados catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="c5bd2-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="c5bd2-131">-DataFlowComputeType</span></span>
<span data-ttu-id="c5bd2-132">Tipo de computação do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="c5bd2-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="c5bd2-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="c5bd2-134">Contagem central do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-134">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="c5bd2-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="c5bd2-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="c5bd2-136">Vida útil (em minutos) da configuração do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="c5bd2-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c5bd2-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="c5bd2-138">O nome do tempo de execução de integração do Self-Hosted que é usado como um proxy.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

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

### <span data-ttu-id="c5bd2-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="c5bd2-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="c5bd2-140">O nome do serviço vinculado do armazenamento do blob do Azure que faz referência ao repositório de dados de preparação a ser usado ao mover dados entre Self-Hosted e o tempo de execução de integração do Azure-SSIS.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

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

### <span data-ttu-id="c5bd2-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="c5bd2-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="c5bd2-142">O caminho no repositório de dados de preparo a ser usado ao mover dados entre Self-Hosted e os tempos de execução de integração do Azure-SSIS, um contêiner padrão será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

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

### <span data-ttu-id="c5bd2-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5bd2-143">-DefaultProfile</span></span>
<span data-ttu-id="c5bd2-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5bd2-145">-Descrição</span><span class="sxs-lookup"><span data-stu-id="c5bd2-145">-Description</span></span>
<span data-ttu-id="c5bd2-146">A descrição do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="c5bd2-147">-Edição</span><span class="sxs-lookup"><span data-stu-id="c5bd2-147">-Edition</span></span>
<span data-ttu-id="c5bd2-148">A edição para o tempo de execução de integração do SSIS que pode ser Standard ou Enterprise, o padrão é padrão se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="c5bd2-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="c5bd2-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="c5bd2-150">A configuração personalizada expressa para o tempo de execução de integração do SSIS que pode ser usada para configurar configurações e componentes de terceiros sem o script de instalação personalizada.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

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

### <span data-ttu-id="c5bd2-151">-Force</span><span class="sxs-lookup"><span data-stu-id="c5bd2-151">-Force</span></span>
<span data-ttu-id="c5bd2-152">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c5bd2-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5bd2-153">-InputObject</span></span>
<span data-ttu-id="c5bd2-154">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="c5bd2-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c5bd2-155">-LicenseType</span></span>
<span data-ttu-id="c5bd2-156">O tipo de licença que você deseja selecionar para o SSIS IV.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="c5bd2-157">Há dois tipos: LicenseIncluded ou BasePrice.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="c5bd2-158">Se você estiver qualificado para o preço do Azure Hybrid use beneficie-se (AHUB), selecione BasePrice.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="c5bd2-159">Caso contrário, selecione LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="c5bd2-160">-Local</span><span class="sxs-lookup"><span data-stu-id="c5bd2-160">-Location</span></span>
<span data-ttu-id="c5bd2-161">A descrição do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-161">The integration runtime description.</span></span>

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

### <span data-ttu-id="c5bd2-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="c5bd2-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="c5bd2-163">Contagem máxima de execuções paralelas por nó para um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="c5bd2-164">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5bd2-164">-Name</span></span>
<span data-ttu-id="c5bd2-165">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="c5bd2-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="c5bd2-166">-NodeCount</span></span>
<span data-ttu-id="c5bd2-167">Contagem de nós de destino do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="c5bd2-168">-Nós</span><span class="sxs-lookup"><span data-stu-id="c5bd2-168">-NodeSize</span></span>
<span data-ttu-id="c5bd2-169">O tamanho do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="c5bd2-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="c5bd2-170">-PublicIP</span></span>
<span data-ttu-id="c5bd2-171">Os endereços IP públicos estáticos que serão usados pelo tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="c5bd2-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5bd2-172">-ResourceGroupName</span></span>
<span data-ttu-id="c5bd2-173">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-173">Resource group name.</span></span>

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

### <span data-ttu-id="c5bd2-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5bd2-174">-ResourceId</span></span>
<span data-ttu-id="c5bd2-175">Identificador de recurso do tempo de execução de integração do Synapse.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-175">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="c5bd2-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="c5bd2-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="c5bd2-177">O URI da SAS do contêiner de blob do Azure que contém o script de instalação personalizada.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="c5bd2-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="c5bd2-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="c5bd2-179">A ID do recurso do tempo de execução de integração de hospedagem automática compartilhada.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="c5bd2-180">-Subnet</span><span class="sxs-lookup"><span data-stu-id="c5bd2-180">-Subnet</span></span>
<span data-ttu-id="c5bd2-181">O nome da sub-rede na VNet.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="c5bd2-182">-Digite</span><span class="sxs-lookup"><span data-stu-id="c5bd2-182">-Type</span></span>
<span data-ttu-id="c5bd2-183">O tipo de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="c5bd2-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="c5bd2-184">-VNetId</span></span>
<span data-ttu-id="c5bd2-185">A ID da VNet na qual o tempo de execução de integração entrará.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-185">The ID of the VNet which the integration runtime will join.</span></span>

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

### <span data-ttu-id="c5bd2-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5bd2-186">-WorkspaceName</span></span>
<span data-ttu-id="c5bd2-187">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-187">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c5bd2-188">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="c5bd2-188">-WorkspaceObject</span></span>
<span data-ttu-id="c5bd2-189">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-189">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c5bd2-190">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c5bd2-190">-Confirm</span></span>
<span data-ttu-id="c5bd2-191">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5bd2-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5bd2-192">-WhatIf</span></span>
<span data-ttu-id="c5bd2-193">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5bd2-194">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5bd2-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bd2-195">CommonParameters</span></span>
<span data-ttu-id="c5bd2-196">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bd2-197">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5bd2-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bd2-198">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5bd2-198">INPUTS</span></span>

### <span data-ttu-id="c5bd2-199">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c5bd2-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c5bd2-200">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c5bd2-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c5bd2-201">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5bd2-201">OUTPUTS</span></span>

### <span data-ttu-id="c5bd2-202">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c5bd2-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c5bd2-203">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5bd2-203">NOTES</span></span>

## <span data-ttu-id="c5bd2-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5bd2-204">RELATED LINKS</span></span>
