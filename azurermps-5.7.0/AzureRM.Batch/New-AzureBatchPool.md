---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 54a5d6dc737bc0bd6a7f1d236ce855b2a08dca6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441346"
---
# <span data-ttu-id="03c96-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="03c96-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="03c96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03c96-102">SYNOPSIS</span></span>
<span data-ttu-id="03c96-103">Cria um pool no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="03c96-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03c96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03c96-104">SYNTAX</span></span>

### <span data-ttu-id="03c96-105">CloudServiceAndTargetDedicated (padrão)</span><span class="sxs-lookup"><span data-stu-id="03c96-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c96-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="03c96-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03c96-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="03c96-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c96-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="03c96-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03c96-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03c96-109">DESCRIPTION</span></span>
<span data-ttu-id="03c96-110">O cmdlet **New-AzureBatchPool** cria um pool no serviço de lote do Azure na conta especificada pelo parâmetro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="03c96-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="03c96-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03c96-111">EXAMPLES</span></span>

### <span data-ttu-id="03c96-112">Exemplo 1: criar um novo pool usando o conjunto de parâmetros TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="03c96-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="03c96-113">Esse comando cria um novo pool com ID mypool usando o parâmetro TargetDedicated definido.</span><span class="sxs-lookup"><span data-stu-id="03c96-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="03c96-114">A alocação de destino é de três nós de computação.</span><span class="sxs-lookup"><span data-stu-id="03c96-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="03c96-115">O pool está configurado para usar pequenas máquinas virtuais com a imagem da versão mais recente do sistema operacional da família quatro.</span><span class="sxs-lookup"><span data-stu-id="03c96-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="03c96-116">Exemplo 2: criar um novo pool usando o conjunto de parâmetros de autoescala</span><span class="sxs-lookup"><span data-stu-id="03c96-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="03c96-117">Esse comando cria um novo pool com ID AutoScalePool usando o conjunto de parâmetros de autoescala.</span><span class="sxs-lookup"><span data-stu-id="03c96-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="03c96-118">O pool está configurado para usar pequenas máquinas virtuais com a imagem da última versão do sistema operacional da família quatro, e o número de destino dos nós de computação é determinado pela fórmula de autoescala.</span><span class="sxs-lookup"><span data-stu-id="03c96-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="03c96-119">Exemplo 3: criar um pool com nós em uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="03c96-119">Example 3: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="03c96-120">Exemplo 4: criar um pool com contas de usuário personalizadas</span><span class="sxs-lookup"><span data-stu-id="03c96-120">Example 4: Create a pool with custom user accounts</span></span>
```
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="03c96-121">OS</span><span class="sxs-lookup"><span data-stu-id="03c96-121">PARAMETERS</span></span>

### <span data-ttu-id="03c96-122">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="03c96-122">-ApplicationLicenses</span></span>
<span data-ttu-id="03c96-123">A lista de licenças de aplicativos que o serviço em lotes disponibilizará em cada nó de computação do pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-123">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: ApplicationLicense

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-124">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="03c96-124">-ApplicationPackageReferences</span></span>
```yaml
Type: PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-125">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="03c96-125">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="03c96-126">Especifica a quantidade de tempo, em minutos, que decorre antes que o tamanho do pool seja ajustado automaticamente de acordo com a fórmula de autoescala.</span><span class="sxs-lookup"><span data-stu-id="03c96-126">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="03c96-127">O valor padrão é 15 minutos, e o valor mínimo é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="03c96-127">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-128">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="03c96-128">-AutoScaleFormula</span></span>
<span data-ttu-id="03c96-129">Especifica a fórmula para dimensionar automaticamente o pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-129">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-130">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="03c96-130">-BatchContext</span></span>
<span data-ttu-id="03c96-131">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="03c96-131">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="03c96-132">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="03c96-132">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="03c96-133">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="03c96-133">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="03c96-134">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="03c96-134">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="03c96-135">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="03c96-135">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-136">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="03c96-136">-CertificateReferences</span></span>
<span data-ttu-id="03c96-137">Especifica certificados associados ao pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-137">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="03c96-138">O serviço em lotes instala os certificados referenciados em cada nó de computação do pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-138">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-139">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="03c96-139">-CloudServiceConfiguration</span></span>
<span data-ttu-id="03c96-140">Especifica as definições de configuração para um pool baseado na plataforma de serviço de nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="03c96-140">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c96-141">-DefaultProfile</span></span>
<span data-ttu-id="03c96-142">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03c96-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03c96-143">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="03c96-143">-DisplayName</span></span>
<span data-ttu-id="03c96-144">Especifica o nome de exibição do pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-144">Specifies the display name of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-145">-ID</span><span class="sxs-lookup"><span data-stu-id="03c96-145">-Id</span></span>
<span data-ttu-id="03c96-146">Especifica a ID do pool a ser criado.</span><span class="sxs-lookup"><span data-stu-id="03c96-146">Specifies the ID of the pool to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-147">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="03c96-147">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="03c96-148">Indica que esse cmdlet configura o pool para comunicação direta entre nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="03c96-148">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-149">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="03c96-149">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="03c96-150">Especifica o número máximo de tarefas que podem ser executadas em um único nó de computação.</span><span class="sxs-lookup"><span data-stu-id="03c96-150">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-151">-Metadados</span><span class="sxs-lookup"><span data-stu-id="03c96-151">-Metadata</span></span>
<span data-ttu-id="03c96-152">Especifica os metadados, como pares de chave/valor, a serem adicionados ao novo pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-152">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="03c96-153">A chave é o nome dos metadados.</span><span class="sxs-lookup"><span data-stu-id="03c96-153">The key is the metadata name.</span></span>
<span data-ttu-id="03c96-154">O valor é o valor dos metadados.</span><span class="sxs-lookup"><span data-stu-id="03c96-154">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-155">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="03c96-155">-NetworkConfiguration</span></span>
<span data-ttu-id="03c96-156">A configuração de rede do pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-156">The network configuration for the pool.</span></span>

```yaml
Type: PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-157">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="03c96-157">-ResizeTimeout</span></span>
<span data-ttu-id="03c96-158">Especifica o tempo limite para alocar nós de computação ao pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-158">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-159">-StartTask</span><span class="sxs-lookup"><span data-stu-id="03c96-159">-StartTask</span></span>
<span data-ttu-id="03c96-160">Especifica a especificação de tarefa inicial para o pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-160">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="03c96-161">A tarefa inicial é executada quando um nó de computação entra no pool ou quando o nó de computação é reinicializado ou renovada.</span><span class="sxs-lookup"><span data-stu-id="03c96-161">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-162">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="03c96-162">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="03c96-163">Especifica o número de destino dos nós de computação dedicados a serem alocados para o pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-163">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-164">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="03c96-164">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="03c96-165">Especifica o número de destino de nós de computação de baixa prioridade a serem alocados para o pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-165">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-166">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="03c96-166">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="03c96-167">Especifica a política de agendamento de tarefas, como ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="03c96-167">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-168">-USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="03c96-168">-UserAccount</span></span>
<span data-ttu-id="03c96-169">A lista de contas de usuário a serem criadas em cada nó do pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-169">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: PSUserAccount[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-170">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="03c96-170">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="03c96-171">Especifica as definições de configuração para um pool na infraestrutura de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="03c96-171">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-172">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="03c96-172">-VirtualMachineSize</span></span>
<span data-ttu-id="03c96-173">Especifica o tamanho das máquinas virtuais no pool.</span><span class="sxs-lookup"><span data-stu-id="03c96-173">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="03c96-174">Para obter mais informações sobre tamanhos de máquinas virtuais, consulte tamanhos para máquinas virtuais https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) no site do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="03c96-174">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="03c96-175">-Confirme</span><span class="sxs-lookup"><span data-stu-id="03c96-175">-Confirm</span></span>
<span data-ttu-id="03c96-176">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03c96-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c96-177">-WhatIf</span></span>
<span data-ttu-id="03c96-178">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03c96-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c96-179">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03c96-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c96-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c96-180">CommonParameters</span></span>
<span data-ttu-id="03c96-181">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c96-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c96-182">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03c96-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c96-183">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03c96-183">INPUTS</span></span>

### <span data-ttu-id="03c96-184">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="03c96-184">BatchAccountContext</span></span>
<span data-ttu-id="03c96-185">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="03c96-185">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="03c96-186">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03c96-186">OUTPUTS</span></span>

## <span data-ttu-id="03c96-187">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03c96-187">NOTES</span></span>

## <span data-ttu-id="03c96-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03c96-188">RELATED LINKS</span></span>

[<span data-ttu-id="03c96-189">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="03c96-189">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="03c96-190">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="03c96-190">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="03c96-191">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="03c96-191">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="03c96-192">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="03c96-192">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


