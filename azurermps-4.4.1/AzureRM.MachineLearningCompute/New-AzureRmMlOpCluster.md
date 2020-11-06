---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 222813dc78b4dd7c0118b8146a75ca4d225ce83c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432614"
---
# <span data-ttu-id="a729c-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a729c-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="a729c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a729c-102">SYNOPSIS</span></span>
<span data-ttu-id="a729c-103">Cria um novo cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="a729c-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a729c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a729c-104">SYNTAX</span></span>

### <span data-ttu-id="a729c-105">Crie um novo cluster de operação de funcionamento a partir de uma definição de instância OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="a729c-105">Create a new operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a729c-106">Crie um novo cluster de operação de funcionamento a partir de parâmetros de entrada de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a729c-106">Create a new operationalization cluster from cmdlet input parameters.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <String>]
 [-Description <String>] [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-GlobalServiceConfigurationAdditionalProperties <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a729c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a729c-107">DESCRIPTION</span></span>
<span data-ttu-id="a729c-108">Cria um novo cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="a729c-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="a729c-109">Isso criará um objeto de cluster, um serviço de contêiner se necessário, o Application insights e um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="a729c-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="a729c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a729c-110">EXAMPLES</span></span>

### <span data-ttu-id="a729c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a729c-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="a729c-112">Cria um novo cluster de operação de funcionamento com o serviço de contêiner do Azure e o kubernetes como o Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="a729c-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="a729c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a729c-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="a729c-114">Cria um novo cluster de operação operacional localmente.</span><span class="sxs-lookup"><span data-stu-id="a729c-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="a729c-115">Isso cria um registro de contêiner do Azure, o Application insights e uma conta de armazenamento, mas não cria um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="a729c-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="a729c-116">OS</span><span class="sxs-lookup"><span data-stu-id="a729c-116">PARAMETERS</span></span>

### <span data-ttu-id="a729c-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="a729c-117">-AgentCount</span></span>
<span data-ttu-id="a729c-118">O número de nós de agente no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="a729c-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="a729c-119">-AgentVmSize</span></span>
<span data-ttu-id="a729c-120">O número de nós de agente no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="a729c-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a729c-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="a729c-122">O URI do registro do contêiner do Azure a ser usado em vez de criar um.</span><span class="sxs-lookup"><span data-stu-id="a729c-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a729c-123">-InputObject</span></span>
<span data-ttu-id="a729c-124">As propriedades do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="a729c-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Create a new operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-125">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="a729c-125">-ClusterType</span></span>
<span data-ttu-id="a729c-126">O tipo de cluster operacional de operação.</span><span class="sxs-lookup"><span data-stu-id="a729c-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a729c-127">-Confirm</span></span>
<span data-ttu-id="a729c-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a729c-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-129">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a729c-129">-Description</span></span>
<span data-ttu-id="a729c-130">O número de nós mestres no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="a729c-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="a729c-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="a729c-132">Propriedades adicionais para a configuração de serviço global.</span><span class="sxs-lookup"><span data-stu-id="a729c-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="a729c-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="a729c-134">A configuração ETag para atualizações.</span><span class="sxs-lookup"><span data-stu-id="a729c-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-135">-Local</span><span class="sxs-lookup"><span data-stu-id="a729c-135">-Location</span></span>
<span data-ttu-id="a729c-136">O local do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="a729c-136">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-137">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="a729c-137">-MasterCount</span></span>
<span data-ttu-id="a729c-138">O número de nós mestres no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="a729c-138">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="a729c-139">-Name</span></span>
<span data-ttu-id="a729c-140">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="a729c-140">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-141">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="a729c-141">-OrchestratorType</span></span>
<span data-ttu-id="a729c-142">O tipo Orchestrator do cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="a729c-142">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a729c-143">-ResourceGroupName</span></span>
<span data-ttu-id="a729c-144">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="a729c-144">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-145">-ClientId</span><span class="sxs-lookup"><span data-stu-id="a729c-145">-ClientId</span></span>
<span data-ttu-id="a729c-146">A ID da entidade de serviço do Orchestrator do cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="a729c-146">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-147">-Segredo</span><span class="sxs-lookup"><span data-stu-id="a729c-147">-Secret</span></span>
<span data-ttu-id="a729c-148">O segredo de entidade de serviço do Orchestrator do cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="a729c-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-149">-SslCName</span><span class="sxs-lookup"><span data-stu-id="a729c-149">-SslCName</span></span>
<span data-ttu-id="a729c-150">O CName do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="a729c-150">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-151">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a729c-151">-SslCertificate</span></span>
<span data-ttu-id="a729c-152">Os dados do certificado SSL no formato PEM codificados como cadeia de caracteres base64.</span><span class="sxs-lookup"><span data-stu-id="a729c-152">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="a729c-153">-SslKey</span></span>
<span data-ttu-id="a729c-154">Os dados da chave SSL em formato PEM codificados como cadeia de caracteres base64.</span><span class="sxs-lookup"><span data-stu-id="a729c-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="a729c-155">-SslStatus</span></span>
<span data-ttu-id="a729c-156">Status da SSL.</span><span class="sxs-lookup"><span data-stu-id="a729c-156">SSL status.</span></span>
<span data-ttu-id="a729c-157">Os valores possíveis são ' Enabled ' e ' disabled '.</span><span class="sxs-lookup"><span data-stu-id="a729c-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a729c-158">-StorageAccount</span></span>
<span data-ttu-id="a729c-159">O URI da conta de armazenamento a ser usada em vez da criação de uma.</span><span class="sxs-lookup"><span data-stu-id="a729c-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a729c-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a729c-160">-WhatIf</span></span>
<span data-ttu-id="a729c-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a729c-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a729c-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a729c-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a729c-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a729c-163">INPUTS</span></span>

### <span data-ttu-id="a729c-164">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a729c-164">None</span></span>


## <span data-ttu-id="a729c-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a729c-165">OUTPUTS</span></span>

### <span data-ttu-id="a729c-166">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="a729c-166">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="a729c-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a729c-167">NOTES</span></span>

## <span data-ttu-id="a729c-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a729c-168">RELATED LINKS</span></span>

