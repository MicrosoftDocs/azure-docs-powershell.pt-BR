---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: a76731c52de32f8b92ed244f82c6afd69bab32d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892588"
---
# <span data-ttu-id="f5627-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f5627-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="f5627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5627-102">SYNOPSIS</span></span>
<span data-ttu-id="f5627-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5627-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="f5627-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f5627-104">SYNTAX</span></span>

### <span data-ttu-id="f5627-105">SetByIntegrationRuntimeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f5627-105">SetByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="f5627-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f5627-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5627-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="f5627-107">SetByParentObject</span></span>
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

### <span data-ttu-id="f5627-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="f5627-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5627-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5627-109">SetByResourceId</span></span>
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

### <span data-ttu-id="f5627-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="f5627-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5627-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f5627-111">SetByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="f5627-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f5627-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5627-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f5627-113">DESCRIPTION</span></span>
<span data-ttu-id="f5627-114">O cmdlet **Set-AzSynapseIntegrationRuntime** atualiza um tempo de execução de integração com parâmetros específicos.</span><span class="sxs-lookup"><span data-stu-id="f5627-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="f5627-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5627-115">EXAMPLES</span></span>

### <span data-ttu-id="f5627-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f5627-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="f5627-117">O cmdlet atualiza a descrição do tempo de execução de integração chamado 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="f5627-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="f5627-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f5627-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="f5627-119">O cmdlet adiciona o espaço de trabalho para usar o tempo de execução de integração compartilhada.</span><span class="sxs-lookup"><span data-stu-id="f5627-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="f5627-120">Ao usar `-SharedIntegrationRuntimeResourceId` o parâmetro, `-Type` o também deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="f5627-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="f5627-121">Observe que o espaço de trabalho precisa ter permissão para usar o tempo de execução de integração antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5627-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="f5627-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f5627-122">PARAMETERS</span></span>

### <span data-ttu-id="f5627-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="f5627-123">-AuthKey</span></span>
<span data-ttu-id="f5627-124">A chave de autenticação do tempo de execução de integração auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="f5627-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="f5627-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="f5627-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="f5627-126">A credencial de administrador de banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5627-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="f5627-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="f5627-127">-CatalogPricingTier</span></span>
<span data-ttu-id="f5627-128">A camada de preços do banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5627-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="f5627-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5627-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="f5627-130">O ponto de extremidade do servidor de banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5627-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="f5627-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="f5627-131">-DataFlowComputeType</span></span>
<span data-ttu-id="f5627-132">Calcular o tipo do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="f5627-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="f5627-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="f5627-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="f5627-134">Contagem principal do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="f5627-134">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="f5627-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="f5627-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="f5627-136">Hora de vida (em minutos) da configuração do cluster de fluxo de dados que executará o trabalho de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="f5627-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="f5627-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f5627-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="f5627-138">O Self-Hosted de Tempo de Execução de Integração que é usado como proxy.</span><span class="sxs-lookup"><span data-stu-id="f5627-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

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

### <span data-ttu-id="f5627-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="f5627-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="f5627-140">O nome do Serviço Vinculado ao Armazenamento de Blob do Azure que faz referência ao armazenamento de dados de preparação a ser usado ao mover dados entre o Self-Hosted e o Tempo de Execução de Integração do Azure-SSIS.</span><span class="sxs-lookup"><span data-stu-id="f5627-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

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

### <span data-ttu-id="f5627-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="f5627-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="f5627-142">O caminho no armazenamento de dados de preparação a ser usado ao mover dados entre o Self-Hosted e o Azure-SSIS Integration Runtimes, um contêiner padrão será usado se não especificado.</span><span class="sxs-lookup"><span data-stu-id="f5627-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

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

### <span data-ttu-id="f5627-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5627-143">-DefaultProfile</span></span>
<span data-ttu-id="f5627-144">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5627-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5627-145">-Description</span><span class="sxs-lookup"><span data-stu-id="f5627-145">-Description</span></span>
<span data-ttu-id="f5627-146">A descrição do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5627-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="f5627-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="f5627-147">-Edition</span></span>
<span data-ttu-id="f5627-148">A edição para o tempo de execução de integração do SSIS que pode ser Standard ou Enterprise, padrão é Standard se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="f5627-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="f5627-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="f5627-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="f5627-150">A configuração personalizada expressa para o tempo de execução de integração do SSIS que poderia ser usada para configurações de configurações e componentes de terceiros sem script de configuração personalizado.</span><span class="sxs-lookup"><span data-stu-id="f5627-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

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

### <span data-ttu-id="f5627-151">-Force</span><span class="sxs-lookup"><span data-stu-id="f5627-151">-Force</span></span>
<span data-ttu-id="f5627-152">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f5627-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f5627-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5627-153">-InputObject</span></span>
<span data-ttu-id="f5627-154">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5627-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="f5627-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f5627-155">-LicenseType</span></span>
<span data-ttu-id="f5627-156">O tipo de licença que você deseja selecionar para o IR do SSIS.</span><span class="sxs-lookup"><span data-stu-id="f5627-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="f5627-157">Há dois tipos: LicenseIncluded ou BasePrice.</span><span class="sxs-lookup"><span data-stu-id="f5627-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="f5627-158">Se você estiver qualificado para o preço do Azure Hybrid Use Benefit (AHUB), selecione BasePrice.</span><span class="sxs-lookup"><span data-stu-id="f5627-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="f5627-159">Caso não seja, selecione LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="f5627-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="f5627-160">-Location</span><span class="sxs-lookup"><span data-stu-id="f5627-160">-Location</span></span>
<span data-ttu-id="f5627-161">A descrição do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5627-161">The integration runtime description.</span></span>

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

### <span data-ttu-id="f5627-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="f5627-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="f5627-163">Contagem máxima de execução paralela por nó para um tempo de execução de integração dedicado gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f5627-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="f5627-164">-Name</span><span class="sxs-lookup"><span data-stu-id="f5627-164">-Name</span></span>
<span data-ttu-id="f5627-165">O nome do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5627-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="f5627-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="f5627-166">-NodeCount</span></span>
<span data-ttu-id="f5627-167">Contagem de nós de destino do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5627-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="f5627-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="f5627-168">-NodeSize</span></span>
<span data-ttu-id="f5627-169">O tamanho do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5627-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="f5627-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="f5627-170">-PublicIP</span></span>
<span data-ttu-id="f5627-171">Os endereços IP públicos estáticos que o tempo de execução de integração usará.</span><span class="sxs-lookup"><span data-stu-id="f5627-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="f5627-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5627-172">-ResourceGroupName</span></span>
<span data-ttu-id="f5627-173">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5627-173">Resource group name.</span></span>

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

### <span data-ttu-id="f5627-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5627-174">-ResourceId</span></span>
<span data-ttu-id="f5627-175">Identificador de recursos do tempo de execução de integração synapse.</span><span class="sxs-lookup"><span data-stu-id="f5627-175">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="f5627-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="f5627-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="f5627-177">O URI SAS do contêiner de blob do Azure que contém o script de configuração personalizado.</span><span class="sxs-lookup"><span data-stu-id="f5627-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="f5627-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="f5627-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="f5627-179">A id de recurso do tempo de execução de integração compartilhada auto-hospedado.</span><span class="sxs-lookup"><span data-stu-id="f5627-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="f5627-180">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="f5627-180">-Subnet</span></span>
<span data-ttu-id="f5627-181">O nome da sub-rede na VNet.</span><span class="sxs-lookup"><span data-stu-id="f5627-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="f5627-182">-Type</span><span class="sxs-lookup"><span data-stu-id="f5627-182">-Type</span></span>
<span data-ttu-id="f5627-183">O tipo de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="f5627-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="f5627-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="f5627-184">-VNetId</span></span>
<span data-ttu-id="f5627-185">A ID da VNet à qual o tempo de execução de integração ingressará.</span><span class="sxs-lookup"><span data-stu-id="f5627-185">The ID of the VNet which the integration runtime will join.</span></span>

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

### <span data-ttu-id="f5627-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5627-186">-WorkspaceName</span></span>
<span data-ttu-id="f5627-187">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="f5627-187">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f5627-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f5627-188">-WorkspaceObject</span></span>
<span data-ttu-id="f5627-189">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5627-189">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f5627-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5627-190">-Confirm</span></span>
<span data-ttu-id="f5627-191">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5627-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5627-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5627-192">-WhatIf</span></span>
<span data-ttu-id="f5627-193">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5627-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5627-194">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5627-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5627-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5627-195">CommonParameters</span></span>
<span data-ttu-id="f5627-196">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5627-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5627-197">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5627-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5627-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5627-198">INPUTS</span></span>

### <span data-ttu-id="f5627-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f5627-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f5627-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f5627-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f5627-201">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f5627-201">OUTPUTS</span></span>

### <span data-ttu-id="f5627-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f5627-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f5627-203">NOTES</span><span class="sxs-lookup"><span data-stu-id="f5627-203">NOTES</span></span>

## <span data-ttu-id="f5627-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5627-204">RELATED LINKS</span></span>
