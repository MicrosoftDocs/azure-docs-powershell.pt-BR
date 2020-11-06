---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/new-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 8e93847c3a6d993c689d0ac8c40327ddfcbe76af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439858"
---
# <span data-ttu-id="59678-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="59678-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="59678-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59678-102">SYNOPSIS</span></span>
<span data-ttu-id="59678-103">Cria um novo cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="59678-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59678-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59678-104">SYNTAX</span></span>

### <span data-ttu-id="59678-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="59678-105">CreateWithInputObject</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59678-106">Createwithparameters</span><span class="sxs-lookup"><span data-stu-id="59678-106">CreateWithParameters</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59678-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59678-107">DESCRIPTION</span></span>
<span data-ttu-id="59678-108">Cria um novo cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="59678-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="59678-109">Isso criará um objeto de cluster, um serviço de contêiner se necessário, o Application insights e um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="59678-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="59678-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59678-110">EXAMPLES</span></span>

### <span data-ttu-id="59678-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="59678-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="59678-112">Cria um novo cluster de operação de funcionamento com o serviço de contêiner do Azure e o kubernetes como o Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="59678-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="59678-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="59678-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="59678-114">Cria um novo cluster de operação operacional localmente.</span><span class="sxs-lookup"><span data-stu-id="59678-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="59678-115">Isso cria um registro de contêiner do Azure, o Application insights e uma conta de armazenamento, mas não cria um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="59678-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="59678-116">OS</span><span class="sxs-lookup"><span data-stu-id="59678-116">PARAMETERS</span></span>

### <span data-ttu-id="59678-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="59678-117">-AgentCount</span></span>
<span data-ttu-id="59678-118">O número de nós de agente no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="59678-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="59678-119">-AgentVmSize</span></span>
<span data-ttu-id="59678-120">O número de nós de agente no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="59678-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="59678-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="59678-122">O URI do registro do contêiner do Azure a ser usado em vez de criar um.</span><span class="sxs-lookup"><span data-stu-id="59678-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="59678-123">-ClientId</span></span>
<span data-ttu-id="59678-124">A ID da entidade de serviço do Orchestrator do cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="59678-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-125">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="59678-125">-ClusterType</span></span>
<span data-ttu-id="59678-126">O tipo de cluster operacional de operação.</span><span class="sxs-lookup"><span data-stu-id="59678-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59678-127">-DefaultProfile</span></span>
<span data-ttu-id="59678-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59678-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-129">-Descrição</span><span class="sxs-lookup"><span data-stu-id="59678-129">-Description</span></span>
<span data-ttu-id="59678-130">O número de nós mestres no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="59678-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="59678-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="59678-132">Propriedades adicionais para a configuração de serviço global.</span><span class="sxs-lookup"><span data-stu-id="59678-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="59678-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="59678-134">A configuração ETag para atualizações.</span><span class="sxs-lookup"><span data-stu-id="59678-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59678-135">-InputObject</span></span>
<span data-ttu-id="59678-136">As propriedades do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="59678-136">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-137">-Local</span><span class="sxs-lookup"><span data-stu-id="59678-137">-Location</span></span>
<span data-ttu-id="59678-138">O local do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="59678-138">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="59678-139">-MasterCount</span></span>
<span data-ttu-id="59678-140">O número de nós mestres no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="59678-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="59678-141">-Name</span></span>
<span data-ttu-id="59678-142">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="59678-142">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="59678-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="59678-143">-OrchestratorType</span></span>
<span data-ttu-id="59678-144">O tipo Orchestrator do cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="59678-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59678-145">-ResourceGroupName</span></span>
<span data-ttu-id="59678-146">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="59678-146">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="59678-147">-Segredo</span><span class="sxs-lookup"><span data-stu-id="59678-147">-Secret</span></span>
<span data-ttu-id="59678-148">O segredo de entidade de serviço do Orchestrator do cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="59678-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="59678-149">-SslCertificate</span></span>
<span data-ttu-id="59678-150">Os dados do certificado SSL no formato PEM codificados como cadeia de caracteres base64.</span><span class="sxs-lookup"><span data-stu-id="59678-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="59678-151">-SslCName</span></span>
<span data-ttu-id="59678-152">O CName do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="59678-152">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="59678-153">-SslKey</span></span>
<span data-ttu-id="59678-154">Os dados da chave SSL em formato PEM codificados como cadeia de caracteres base64.</span><span class="sxs-lookup"><span data-stu-id="59678-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="59678-155">-SslStatus</span></span>
<span data-ttu-id="59678-156">Status da SSL.</span><span class="sxs-lookup"><span data-stu-id="59678-156">SSL status.</span></span>
<span data-ttu-id="59678-157">Os valores possíveis são ' Enabled ' e ' disabled '.</span><span class="sxs-lookup"><span data-stu-id="59678-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="59678-158">-StorageAccount</span></span>
<span data-ttu-id="59678-159">O URI da conta de armazenamento a ser usada em vez da criação de uma.</span><span class="sxs-lookup"><span data-stu-id="59678-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59678-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="59678-160">-Confirm</span></span>
<span data-ttu-id="59678-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59678-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59678-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59678-162">-WhatIf</span></span>
<span data-ttu-id="59678-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="59678-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59678-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="59678-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59678-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59678-165">CommonParameters</span></span>
<span data-ttu-id="59678-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59678-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59678-167">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59678-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59678-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59678-168">INPUTS</span></span>

### <span data-ttu-id="59678-169">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="59678-169">None</span></span>

## <span data-ttu-id="59678-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59678-170">OUTPUTS</span></span>

### <span data-ttu-id="59678-171">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="59678-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="59678-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59678-172">NOTES</span></span>

## <span data-ttu-id="59678-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59678-173">RELATED LINKS</span></span>

