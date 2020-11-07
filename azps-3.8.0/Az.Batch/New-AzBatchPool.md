---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: def1c315a99592ca584baa10194e7b9238984506
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93947214"
---
# <span data-ttu-id="4a3a5-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="4a3a5-101">New-AzBatchPool</span></span>

## <span data-ttu-id="4a3a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a3a5-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3a5-103">Cria um pool no serviço de lote.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="4a3a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a3a5-104">SYNTAX</span></span>

### <span data-ttu-id="4a3a5-105">CloudServiceAndTargetDedicated (padrão)</span><span class="sxs-lookup"><span data-stu-id="4a3a5-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a3a5-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="4a3a5-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a3a5-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="4a3a5-107">CloudServiceAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a3a5-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="4a3a5-108">VirtualMachineAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a3a5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a3a5-109">DESCRIPTION</span></span>
<span data-ttu-id="4a3a5-110">O cmdlet **New-AzBatchPool** cria um pool no serviço de lote do Azure na conta especificada pelo parâmetro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="4a3a5-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="4a3a5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a3a5-111">EXAMPLES</span></span>

### <span data-ttu-id="4a3a5-112">Exemplo 1: criar um novo pool usando o parâmetro TargetDedicated definido usando CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a3a5-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="4a3a5-113">O pool está configurado para usar STANDARD_D1_V2 máquinas virtuais com a versão do sistema operacional da família quatro.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-113">The pool is configured to use STANDARD_D1_V2 virtual machines with operating system version of family four.</span></span>

### <span data-ttu-id="4a3a5-114">Exemplo 2: criar um novo pool usando o parâmetro TargetDedicated definido usando VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a3a5-114">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="4a3a5-115">Esse comando cria um novo pool com ID mypool usando o parâmetro TargetDedicated definido.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-115">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="4a3a5-116">A alocação de destino é de três nós de computação.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-116">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="4a3a5-117">O pool está configurado para usar STANDARD_D1_V2 máquinas virtuais com a imagem do sistema operacional Windows-2016-datacenter.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-117">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image.</span></span>

### <span data-ttu-id="4a3a5-118">Exemplo 3: criar um novo pool usando o conjunto de parâmetros de autoescala</span><span class="sxs-lookup"><span data-stu-id="4a3a5-118">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="4a3a5-119">Esse comando cria um novo pool com ID AutoScalePool usando o conjunto de parâmetros de autoescala.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-119">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="4a3a5-120">O pool está configurado para usar STANDARD_D1_V2 máquinas virtuais com a imagem do sistema operacional Windows-2016-datacenter, e o número de destino dos nós de computação é determinado pela fórmula de autoescala.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-120">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="4a3a5-121">Exemplo 4: criar um pool com nós em uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="4a3a5-121">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="4a3a5-122">Exemplo 5: criar um pool com contas de usuário personalizadas</span><span class="sxs-lookup"><span data-stu-id="4a3a5-122">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="4a3a5-123">OS</span><span class="sxs-lookup"><span data-stu-id="4a3a5-123">PARAMETERS</span></span>

### <span data-ttu-id="4a3a5-124">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="4a3a5-124">-ApplicationLicenses</span></span>
<span data-ttu-id="4a3a5-125">A lista de licenças de aplicativos que o serviço em lotes disponibilizará em cada nó de computação do pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-125">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="4a3a5-126">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="4a3a5-126">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3a5-127">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="4a3a5-127">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="4a3a5-128">Especifica a quantidade de tempo, em minutos, que decorre antes que o tamanho do pool seja ajustado automaticamente de acordo com a fórmula de autoescala.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-128">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="4a3a5-129">O valor padrão é 15 minutos, e o valor mínimo é de 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-129">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="4a3a5-130">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="4a3a5-130">-AutoScaleFormula</span></span>
<span data-ttu-id="4a3a5-131">Especifica a fórmula para dimensionar automaticamente o pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-131">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="4a3a5-132">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4a3a5-132">-BatchContext</span></span>
<span data-ttu-id="4a3a5-133">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-133">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4a3a5-134">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-134">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4a3a5-135">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-135">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4a3a5-136">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-136">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4a3a5-137">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-137">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4a3a5-138">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="4a3a5-138">-CertificateReferences</span></span>
<span data-ttu-id="4a3a5-139">Especifica certificados associados ao pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-139">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="4a3a5-140">O serviço em lotes instala os certificados referenciados em cada nó de computação do pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-140">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3a5-141">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a3a5-141">-CloudServiceConfiguration</span></span>
<span data-ttu-id="4a3a5-142">Especifica as definições de configuração para um pool baseado na plataforma de serviço de nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-142">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="4a3a5-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3a5-143">-DefaultProfile</span></span>
<span data-ttu-id="4a3a5-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a3a5-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4a3a5-145">-DisplayName</span></span>
<span data-ttu-id="4a3a5-146">Especifica o nome de exibição do pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-146">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="4a3a5-147">-ID</span><span class="sxs-lookup"><span data-stu-id="4a3a5-147">-Id</span></span>
<span data-ttu-id="4a3a5-148">Especifica a ID do pool a ser criado.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-148">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="4a3a5-149">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="4a3a5-149">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="4a3a5-150">Indica que esse cmdlet configura o pool para comunicação direta entre nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-150">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="4a3a5-151">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="4a3a5-151">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="4a3a5-152">Especifica o número máximo de tarefas que podem ser executadas em um único nó de computação.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-152">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="4a3a5-153">-Metadados</span><span class="sxs-lookup"><span data-stu-id="4a3a5-153">-Metadata</span></span>
<span data-ttu-id="4a3a5-154">Especifica os metadados, como pares de chave/valor, a serem adicionados ao novo pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-154">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="4a3a5-155">A chave é o nome dos metadados.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-155">The key is the metadata name.</span></span>
<span data-ttu-id="4a3a5-156">O valor é o valor dos metadados.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-156">The value is the metadata value.</span></span>

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

### <span data-ttu-id="4a3a5-157">-MountConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a3a5-157">-MountConfiguration</span></span>
<span data-ttu-id="4a3a5-158">Uma lista de sistemas de arquivos para montar em cada nó do pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-158">A list of file systems to mount on each node in the pool.</span></span> <span data-ttu-id="4a3a5-159">Isso dá suporte a arquivos do Azure, NFS, CIFS/SMB e Blobfuse.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-159">This supports Azure Files, NFS, CIFS/SMB, and Blobfuse.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMountConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3a5-160">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a3a5-160">-NetworkConfiguration</span></span>
<span data-ttu-id="4a3a5-161">A configuração de rede do pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-161">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="4a3a5-162">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="4a3a5-162">-ResizeTimeout</span></span>
<span data-ttu-id="4a3a5-163">Especifica o tempo limite para alocar nós de computação ao pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-163">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="4a3a5-164">-StartTask</span><span class="sxs-lookup"><span data-stu-id="4a3a5-164">-StartTask</span></span>
<span data-ttu-id="4a3a5-165">Especifica a especificação de tarefa inicial para o pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-165">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="4a3a5-166">A tarefa inicial é executada quando um nó de computação entra no pool ou quando o nó de computação é reinicializado ou renovada.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-166">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="4a3a5-167">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="4a3a5-167">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="4a3a5-168">Especifica o número de destino dos nós de computação dedicados a serem alocados para o pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-168">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3a5-169">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="4a3a5-169">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="4a3a5-170">Especifica o número de destino de nós de computação de baixa prioridade a serem alocados para o pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-170">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="4a3a5-171">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="4a3a5-171">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="4a3a5-172">Especifica a política de agendamento de tarefas, como ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-172">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="4a3a5-173">-USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="4a3a5-173">-UserAccount</span></span>
<span data-ttu-id="4a3a5-174">A lista de contas de usuário a serem criadas em cada nó do pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-174">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a3a5-175">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a3a5-175">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="4a3a5-176">Especifica as definições de configuração para um pool na infraestrutura de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-176">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="4a3a5-177">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="4a3a5-177">-VirtualMachineSize</span></span>
<span data-ttu-id="4a3a5-178">Especifica o tamanho das máquinas virtuais no pool.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-178">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="4a3a5-179">Para obter mais informações sobre tamanhos de máquinas virtuais, consulte tamanhos para máquinas virtuais https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) no site do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-179">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="4a3a5-180">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4a3a5-180">-Confirm</span></span>
<span data-ttu-id="4a3a5-181">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a3a5-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a3a5-182">-WhatIf</span></span>
<span data-ttu-id="4a3a5-183">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a3a5-184">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a3a5-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3a5-185">CommonParameters</span></span>
<span data-ttu-id="4a3a5-186">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a3a5-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3a5-187">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a3a5-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3a5-188">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a3a5-188">INPUTS</span></span>

### <span data-ttu-id="4a3a5-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4a3a5-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4a3a5-190">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a3a5-190">OUTPUTS</span></span>

### <span data-ttu-id="4a3a5-191">System. void</span><span class="sxs-lookup"><span data-stu-id="4a3a5-191">System.Void</span></span>

## <span data-ttu-id="4a3a5-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a3a5-192">NOTES</span></span>

## <span data-ttu-id="4a3a5-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a3a5-193">RELATED LINKS</span></span>

[<span data-ttu-id="4a3a5-194">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4a3a5-194">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4a3a5-195">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="4a3a5-195">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="4a3a5-196">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="4a3a5-196">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="4a3a5-197">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="4a3a5-197">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


