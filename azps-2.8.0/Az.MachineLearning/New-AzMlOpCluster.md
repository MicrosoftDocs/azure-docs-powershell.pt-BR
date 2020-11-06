---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
ms.openlocfilehash: 51c8beb396bb0795fa77431a256ddc38e4e8df38
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595969"
---
# <span data-ttu-id="f1da7-101">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f1da7-101">New-AzMlOpCluster</span></span>

## <span data-ttu-id="f1da7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1da7-102">SYNOPSIS</span></span>
<span data-ttu-id="f1da7-103">Cria um novo cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="f1da7-103">Creates a new operationalization cluster.</span></span>

## <span data-ttu-id="f1da7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1da7-104">SYNTAX</span></span>

### <span data-ttu-id="f1da7-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="f1da7-105">CreateWithInputObject</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1da7-106">Createwithparameters</span><span class="sxs-lookup"><span data-stu-id="f1da7-106">CreateWithParameters</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1da7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1da7-107">DESCRIPTION</span></span>
<span data-ttu-id="f1da7-108">Cria um novo cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="f1da7-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="f1da7-109">Isso criará um objeto de cluster, um serviço de contêiner se necessário, o Application insights e um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1da7-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="f1da7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1da7-110">EXAMPLES</span></span>

### <span data-ttu-id="f1da7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f1da7-111">Example 1</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="f1da7-112">Cria um novo cluster de operação de funcionamento com o serviço de contêiner do Azure e o kubernetes como o Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="f1da7-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="f1da7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f1da7-113">Example 2</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="f1da7-114">Cria um novo cluster de operação operacional localmente.</span><span class="sxs-lookup"><span data-stu-id="f1da7-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="f1da7-115">Isso cria um registro de contêiner do Azure, o Application insights e uma conta de armazenamento, mas não cria um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f1da7-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="f1da7-116">OS</span><span class="sxs-lookup"><span data-stu-id="f1da7-116">PARAMETERS</span></span>

### <span data-ttu-id="f1da7-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="f1da7-117">-AgentCount</span></span>
<span data-ttu-id="f1da7-118">O número de nós de agente no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="f1da7-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="f1da7-119">-AgentVmSize</span></span>
<span data-ttu-id="f1da7-120">O número de nós de agente no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="f1da7-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f1da7-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="f1da7-122">O URI do registro do contêiner do Azure a ser usado em vez de criar um.</span><span class="sxs-lookup"><span data-stu-id="f1da7-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="f1da7-123">-ClientId</span></span>
<span data-ttu-id="f1da7-124">A ID da entidade de serviço do Orchestrator do cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="f1da7-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-125">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="f1da7-125">-ClusterType</span></span>
<span data-ttu-id="f1da7-126">O tipo de cluster operacional de operação.</span><span class="sxs-lookup"><span data-stu-id="f1da7-126">The operationalization cluster type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1da7-127">-DefaultProfile</span></span>
<span data-ttu-id="f1da7-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1da7-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1da7-129">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f1da7-129">-Description</span></span>
<span data-ttu-id="f1da7-130">O número de nós mestres no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="f1da7-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="f1da7-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="f1da7-132">Propriedades adicionais para a configuração de serviço global.</span><span class="sxs-lookup"><span data-stu-id="f1da7-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="f1da7-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="f1da7-134">A configuração ETag para atualizações.</span><span class="sxs-lookup"><span data-stu-id="f1da7-134">The configuration ETag for updates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1da7-135">-InputObject</span></span>
<span data-ttu-id="f1da7-136">As propriedades do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="f1da7-136">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-137">-Local</span><span class="sxs-lookup"><span data-stu-id="f1da7-137">-Location</span></span>
<span data-ttu-id="f1da7-138">O local do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="f1da7-138">The operationalization cluster's location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="f1da7-139">-MasterCount</span></span>
<span data-ttu-id="f1da7-140">O número de nós mestres no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="f1da7-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1da7-141">-Name</span></span>
<span data-ttu-id="f1da7-142">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="f1da7-142">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="f1da7-143">-OrchestratorType</span></span>
<span data-ttu-id="f1da7-144">O tipo Orchestrator do cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="f1da7-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1da7-145">-ResourceGroupName</span></span>
<span data-ttu-id="f1da7-146">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="f1da7-146">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-147">-Segredo</span><span class="sxs-lookup"><span data-stu-id="f1da7-147">-Secret</span></span>
<span data-ttu-id="f1da7-148">O segredo de entidade de serviço do Orchestrator do cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="f1da7-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="f1da7-149">-SslCertificate</span></span>
<span data-ttu-id="f1da7-150">Os dados do certificado SSL no formato PEM codificados como cadeia de caracteres base64.</span><span class="sxs-lookup"><span data-stu-id="f1da7-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="f1da7-151">-SslCName</span></span>
<span data-ttu-id="f1da7-152">O CName do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="f1da7-152">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="f1da7-153">-SslKey</span></span>
<span data-ttu-id="f1da7-154">Os dados da chave SSL em formato PEM codificados como cadeia de caracteres base64.</span><span class="sxs-lookup"><span data-stu-id="f1da7-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="f1da7-155">-SslStatus</span></span>
<span data-ttu-id="f1da7-156">Status da SSL.</span><span class="sxs-lookup"><span data-stu-id="f1da7-156">SSL status.</span></span>
<span data-ttu-id="f1da7-157">Os valores possíveis são ' Enabled ' e ' disabled '.</span><span class="sxs-lookup"><span data-stu-id="f1da7-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1da7-158">-StorageAccount</span></span>
<span data-ttu-id="f1da7-159">O URI da conta de armazenamento a ser usada em vez da criação de uma.</span><span class="sxs-lookup"><span data-stu-id="f1da7-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1da7-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1da7-160">-Confirm</span></span>
<span data-ttu-id="f1da7-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1da7-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1da7-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1da7-162">-WhatIf</span></span>
<span data-ttu-id="f1da7-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1da7-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1da7-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1da7-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1da7-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1da7-165">CommonParameters</span></span>
<span data-ttu-id="f1da7-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1da7-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1da7-167">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1da7-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1da7-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1da7-168">INPUTS</span></span>

### <span data-ttu-id="f1da7-169">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f1da7-169">None</span></span>

## <span data-ttu-id="f1da7-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1da7-170">OUTPUTS</span></span>

### <span data-ttu-id="f1da7-171">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="f1da7-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="f1da7-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1da7-172">NOTES</span></span>

## <span data-ttu-id="f1da7-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1da7-173">RELATED LINKS</span></span>
