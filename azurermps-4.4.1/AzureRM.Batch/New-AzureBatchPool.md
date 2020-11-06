---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 3a9534ea2fd0f1bcfc17f9eb5df63b25f7760f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431148"
---
# <span data-ttu-id="63dc3-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="63dc3-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="63dc3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="63dc3-103">Cria um pool no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="63dc3-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63dc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63dc3-104">SYNTAX</span></span>

### <span data-ttu-id="63dc3-105">CloudServiceAndTargetDedicated (padrão)</span><span class="sxs-lookup"><span data-stu-id="63dc3-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63dc3-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="63dc3-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63dc3-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="63dc3-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63dc3-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="63dc3-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63dc3-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63dc3-109">DESCRIPTION</span></span>
<span data-ttu-id="63dc3-110">O cmdlet **New-AzureBatchPool** cria um pool no serviço de lote do Azure na conta especificada pelo parâmetro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="63dc3-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="63dc3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63dc3-111">EXAMPLES</span></span>

### <span data-ttu-id="63dc3-112">Exemplo 1: criar um novo pool usando o conjunto de parâmetros TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="63dc3-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicated 3 -BatchContext $Context
```

<span data-ttu-id="63dc3-113">Esse comando cria um novo pool com ID mypool usando o parâmetro TargetDedicated definido.</span><span class="sxs-lookup"><span data-stu-id="63dc3-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="63dc3-114">A alocação de destino é de três nós de computação.</span><span class="sxs-lookup"><span data-stu-id="63dc3-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="63dc3-115">O pool está configurado para usar pequenas máquinas virtuais com a imagem da versão mais recente do sistema operacional da família quatro.</span><span class="sxs-lookup"><span data-stu-id="63dc3-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="63dc3-116">Exemplo 2: criar um novo pool usando o conjunto de parâmetros de autoescala</span><span class="sxs-lookup"><span data-stu-id="63dc3-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="63dc3-117">Esse comando cria um novo pool com ID AutoScalePool usando o conjunto de parâmetros de autoescala.</span><span class="sxs-lookup"><span data-stu-id="63dc3-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="63dc3-118">O pool está configurado para usar pequenas máquinas virtuais com a imagem da última versão do sistema operacional da família quatro, e o número de destino dos nós de computação é determinado pela fórmula de autoescala.</span><span class="sxs-lookup"><span data-stu-id="63dc3-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

## <span data-ttu-id="63dc3-119">OS</span><span class="sxs-lookup"><span data-stu-id="63dc3-119">PARAMETERS</span></span>

### <span data-ttu-id="63dc3-120">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="63dc3-120">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-121">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="63dc3-121">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="63dc3-122">Especifica a quantidade de tempo, em minutos, que decorre antes que o tamanho do pool seja ajustado automaticamente de acordo com a fórmula de autoescala.</span><span class="sxs-lookup"><span data-stu-id="63dc3-122">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="63dc3-123">O valor padrão é 15 minutos, e o valor mínimo é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="63dc3-123">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-124">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="63dc3-124">-AutoScaleFormula</span></span>
<span data-ttu-id="63dc3-125">Especifica a fórmula para dimensionar automaticamente o pool.</span><span class="sxs-lookup"><span data-stu-id="63dc3-125">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-126">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="63dc3-126">-BatchContext</span></span>
<span data-ttu-id="63dc3-127">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="63dc3-127">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="63dc3-128">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="63dc3-128">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-129">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="63dc3-129">-CertificateReferences</span></span>
<span data-ttu-id="63dc3-130">Especifica certificados associados ao pool.</span><span class="sxs-lookup"><span data-stu-id="63dc3-130">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="63dc3-131">O serviço em lotes instala os certificados referenciados em cada nó de computação do pool.</span><span class="sxs-lookup"><span data-stu-id="63dc3-131">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-132">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="63dc3-132">-CloudServiceConfiguration</span></span>
<span data-ttu-id="63dc3-133">Especifica as definições de configuração para um pool baseado na plataforma de serviço de nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="63dc3-133">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-134">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="63dc3-134">-DisplayName</span></span>
<span data-ttu-id="63dc3-135">Especifica o nome de exibição do pool.</span><span class="sxs-lookup"><span data-stu-id="63dc3-135">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="63dc3-136">-ID</span><span class="sxs-lookup"><span data-stu-id="63dc3-136">-Id</span></span>
<span data-ttu-id="63dc3-137">Especifica a ID do pool a ser criado.</span><span class="sxs-lookup"><span data-stu-id="63dc3-137">Specifies the ID of the pool to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-138">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="63dc3-138">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="63dc3-139">Indica que esse cmdlet configura o pool para comunicação direta entre nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="63dc3-139">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="63dc3-140">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="63dc3-140">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="63dc3-141">Especifica o número máximo de tarefas que podem ser executadas em um único nó de computação.</span><span class="sxs-lookup"><span data-stu-id="63dc3-141">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-142">-Metadados</span><span class="sxs-lookup"><span data-stu-id="63dc3-142">-Metadata</span></span>
<span data-ttu-id="63dc3-143">Especifica os metadados, como pares de chave/valor, a serem adicionados ao novo pool.</span><span class="sxs-lookup"><span data-stu-id="63dc3-143">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="63dc3-144">A chave é o nome dos metadados.</span><span class="sxs-lookup"><span data-stu-id="63dc3-144">The key is the metadata name.</span></span>
<span data-ttu-id="63dc3-145">O valor é o valor dos metadados.</span><span class="sxs-lookup"><span data-stu-id="63dc3-145">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-146">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="63dc3-146">-NetworkConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-147">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="63dc3-147">-ResizeTimeout</span></span>
<span data-ttu-id="63dc3-148">Especifica o tempo limite para alocar nós de computação ao pool.</span><span class="sxs-lookup"><span data-stu-id="63dc3-148">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-149">-StartTask</span><span class="sxs-lookup"><span data-stu-id="63dc3-149">-StartTask</span></span>
<span data-ttu-id="63dc3-150">Especifica a especificação de tarefa inicial para o pool.</span><span class="sxs-lookup"><span data-stu-id="63dc3-150">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="63dc3-151">A tarefa inicial é executada quando um nó de computação entra no pool ou quando o nó de computação é reinicializado ou renovada.</span><span class="sxs-lookup"><span data-stu-id="63dc3-151">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-152">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="63dc3-152">-TargetDedicated</span></span>
<span data-ttu-id="63dc3-153">Especifica o número de destino dos nós de computação a serem alocados para o pool.</span><span class="sxs-lookup"><span data-stu-id="63dc3-153">Specifies the target number of compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-154">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="63dc3-154">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="63dc3-155">Especifica a política de agendamento de tarefas, como ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="63dc3-155">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-156">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="63dc3-156">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="63dc3-157">Especifica as definições de configuração para um pool na infraestrutura de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="63dc3-157">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-158">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="63dc3-158">-VirtualMachineSize</span></span>
<span data-ttu-id="63dc3-159">Especifica o tamanho das máquinas virtuais no pool.</span><span class="sxs-lookup"><span data-stu-id="63dc3-159">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="63dc3-160">Para obter mais informações sobre tamanhos de máquinas virtuais, consulte tamanhos para máquinas virtuais https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) no site do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="63dc3-160">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="63dc3-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="63dc3-161">-Confirm</span></span>
<span data-ttu-id="63dc3-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63dc3-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63dc3-163">-WhatIf</span></span>
<span data-ttu-id="63dc3-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="63dc3-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63dc3-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63dc3-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63dc3-166">-DefaultProfile</span></span>
<span data-ttu-id="63dc3-167">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63dc3-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc3-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63dc3-168">CommonParameters</span></span>
<span data-ttu-id="63dc3-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63dc3-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63dc3-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63dc3-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63dc3-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63dc3-171">INPUTS</span></span>

### <span data-ttu-id="63dc3-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="63dc3-172">BatchAccountContext</span></span>
<span data-ttu-id="63dc3-173">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="63dc3-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="63dc3-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63dc3-174">OUTPUTS</span></span>

## <span data-ttu-id="63dc3-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63dc3-175">NOTES</span></span>

## <span data-ttu-id="63dc3-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63dc3-176">RELATED LINKS</span></span>

[<span data-ttu-id="63dc3-177">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="63dc3-177">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="63dc3-178">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="63dc3-178">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="63dc3-179">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="63dc3-179">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="63dc3-180">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="63dc3-180">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


