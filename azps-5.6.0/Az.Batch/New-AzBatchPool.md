---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 7fef035eda89d68d757658a512ca00369b69694a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890660"
---
# <span data-ttu-id="e5fb9-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e5fb9-101">New-AzBatchPool</span></span>

## <span data-ttu-id="e5fb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fb9-103">Cria um pool no serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="e5fb9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e5fb9-104">SYNTAX</span></span>

### <span data-ttu-id="e5fb9-105">CloudServiceAndTargetDedicated (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e5fb9-105">CloudServiceAndTargetDedicated (Default)</span></span>
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

### <span data-ttu-id="e5fb9-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="e5fb9-106">VirtualMachineAndTargetDedicated</span></span>
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

### <span data-ttu-id="e5fb9-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="e5fb9-107">CloudServiceAndAutoScale</span></span>
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

### <span data-ttu-id="e5fb9-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="e5fb9-108">VirtualMachineAndAutoScale</span></span>
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

## <span data-ttu-id="e5fb9-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e5fb9-109">DESCRIPTION</span></span>
<span data-ttu-id="e5fb9-110">O cmdlet **New-AzBatchPool** cria um pool no serviço Lote do Azure na conta especificada pelo parâmetro *BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="e5fb9-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="e5fb9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5fb9-111">EXAMPLES</span></span>

### <span data-ttu-id="e5fb9-112">Exemplo 1: Criar um novo pool usando o conjunto de parâmetros TargetDedicated usando CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5fb9-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="e5fb9-113">O pool é configurado para usar STANDARD_D1_V2 virtuais com a versão do sistema operacional da família quatro.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-113">The pool is configured to use STANDARD_D1_V2 virtual machines with operating system version of family four.</span></span>

### <span data-ttu-id="e5fb9-114">Exemplo 2: Criar um novo pool usando o conjunto de parâmetros TargetDedicated usando VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5fb9-114">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="e5fb9-115">Este comando cria um novo pool com a ID MyPool usando o conjunto de parâmetros TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-115">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="e5fb9-116">A alocação de destino são três nós de computação.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-116">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="e5fb9-117">O pool está configurado para usar STANDARD_D1_V2 virtuais com a imagem do sistema operacional Windows-2016-Datacenter.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-117">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image.</span></span>

### <span data-ttu-id="e5fb9-118">Exemplo 3: Criar um novo pool usando o conjunto de parâmetros AutoScale</span><span class="sxs-lookup"><span data-stu-id="e5fb9-118">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="e5fb9-119">Este comando cria um novo pool com ID AutoScalePool usando o conjunto de parâmetros AutoScale.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-119">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="e5fb9-120">O pool é configurado para usar STANDARD_D1_V2 virtuais com a imagem do sistema operacional Windows-2016-Datacenter, e o número de destino dos nós de computação é determinado pela fórmula de escala automática.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-120">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="e5fb9-121">Exemplo 4: Criar um pool com nós em uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="e5fb9-121">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="e5fb9-122">Exemplo 5: Criar um pool com contas de usuário personalizadas</span><span class="sxs-lookup"><span data-stu-id="e5fb9-122">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="e5fb9-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e5fb9-123">PARAMETERS</span></span>

### <span data-ttu-id="e5fb9-124">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="e5fb9-124">-ApplicationLicenses</span></span>
<span data-ttu-id="e5fb9-125">A lista de licenças de aplicativos que o serviço Batch disponibiliza em cada nó de computação no pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-125">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="e5fb9-126">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="e5fb9-126">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="e5fb9-127">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="e5fb9-127">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="e5fb9-128">Especifica a quantidade de tempo, em minutos, que se elava antes que o tamanho do pool seja ajustado automaticamente de acordo com a fórmula AutoScale.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-128">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="e5fb9-129">O valor padrão é 15 minutos e o valor mínimo é 5 minutos.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-129">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="e5fb9-130">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="e5fb9-130">-AutoScaleFormula</span></span>
<span data-ttu-id="e5fb9-131">Especifica a fórmula para dimensionar automaticamente o pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-131">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="e5fb9-132">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e5fb9-132">-BatchContext</span></span>
<span data-ttu-id="e5fb9-133">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-133">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e5fb9-134">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-134">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e5fb9-135">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-135">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e5fb9-136">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-136">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e5fb9-137">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-137">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e5fb9-138">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="e5fb9-138">-CertificateReferences</span></span>
<span data-ttu-id="e5fb9-139">Especifica certificados associados ao pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-139">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="e5fb9-140">O serviço Batch instala os certificados referenciados em cada nó de computação do pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-140">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

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

### <span data-ttu-id="e5fb9-141">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5fb9-141">-CloudServiceConfiguration</span></span>
<span data-ttu-id="e5fb9-142">Especifica as configurações de um pool com base na plataforma de serviço de nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-142">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="e5fb9-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fb9-143">-DefaultProfile</span></span>
<span data-ttu-id="e5fb9-144">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5fb9-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e5fb9-145">-DisplayName</span></span>
<span data-ttu-id="e5fb9-146">Especifica o nome de exibição do pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-146">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="e5fb9-147">-Id</span><span class="sxs-lookup"><span data-stu-id="e5fb9-147">-Id</span></span>
<span data-ttu-id="e5fb9-148">Especifica a ID do pool a ser criado.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-148">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="e5fb9-149">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="e5fb9-149">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="e5fb9-150">Indica que esse cmdlet configura o pool para comunicação direta entre nós de computação dedicados.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-150">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="e5fb9-151">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="e5fb9-151">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="e5fb9-152">Especifica o número máximo de tarefas que podem ser executadas em um único nó de computação.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-152">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="e5fb9-153">-Metadados</span><span class="sxs-lookup"><span data-stu-id="e5fb9-153">-Metadata</span></span>
<span data-ttu-id="e5fb9-154">Especifica os metadados, como pares de chave/valor, para adicionar ao novo pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-154">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="e5fb9-155">A chave é o nome dos metadados.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-155">The key is the metadata name.</span></span>
<span data-ttu-id="e5fb9-156">O valor é o valor de metadados.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-156">The value is the metadata value.</span></span>

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

### <span data-ttu-id="e5fb9-157">-MountConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5fb9-157">-MountConfiguration</span></span>
<span data-ttu-id="e5fb9-158">Uma lista de sistemas de arquivos para montar em cada nó no pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-158">A list of file systems to mount on each node in the pool.</span></span> <span data-ttu-id="e5fb9-159">Isso dá suporte a Arquivos do Azure, NFS, CIFS/SMB e Blobfuse.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-159">This supports Azure Files, NFS, CIFS/SMB, and Blobfuse.</span></span>

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

### <span data-ttu-id="e5fb9-160">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5fb9-160">-NetworkConfiguration</span></span>
<span data-ttu-id="e5fb9-161">A configuração de rede do pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-161">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="e5fb9-162">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="e5fb9-162">-ResizeTimeout</span></span>
<span data-ttu-id="e5fb9-163">Especifica o tempo de tempo para alocar nós de computação ao pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-163">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="e5fb9-164">-StartTask</span><span class="sxs-lookup"><span data-stu-id="e5fb9-164">-StartTask</span></span>
<span data-ttu-id="e5fb9-165">Especifica a especificação da tarefa inicial do pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-165">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="e5fb9-166">A tarefa inicial é executado quando um nó de computação ins junta ao pool ou quando o nó de computação é reiniciado ou reimaginado.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-166">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="e5fb9-167">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="e5fb9-167">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="e5fb9-168">Especifica o número de destino de nós de computação dedicados para alocar ao pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-168">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="e5fb9-169">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="e5fb9-169">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="e5fb9-170">Especifica o número de destino de nós de computação de baixa prioridade para alocar ao pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-170">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="e5fb9-171">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="e5fb9-171">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="e5fb9-172">Especifica a política de agendamento de tarefas, como ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-172">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="e5fb9-173">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="e5fb9-173">-UserAccount</span></span>
<span data-ttu-id="e5fb9-174">A lista de contas de usuário a serem criadas em cada nó no pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-174">The list of user accounts to be created on each node in the pool.</span></span>

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

### <span data-ttu-id="e5fb9-175">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5fb9-175">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="e5fb9-176">Especifica as configurações de um pool na infraestrutura de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-176">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="e5fb9-177">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="e5fb9-177">-VirtualMachineSize</span></span>
<span data-ttu-id="e5fb9-178">Especifica o tamanho das máquinas virtuais no pool.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-178">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="e5fb9-179">Para obter mais informações sobre tamanhos de máquinas virtuais, consulte Tamanhos para máquinas virtuais https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( no site do Microsoft https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) Azure.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-179">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="e5fb9-180">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5fb9-180">-Confirm</span></span>
<span data-ttu-id="e5fb9-181">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5fb9-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5fb9-182">-WhatIf</span></span>
<span data-ttu-id="e5fb9-183">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5fb9-184">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5fb9-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fb9-185">CommonParameters</span></span>
<span data-ttu-id="e5fb9-186">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5fb9-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fb9-187">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5fb9-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fb9-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5fb9-188">INPUTS</span></span>

### <span data-ttu-id="e5fb9-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e5fb9-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e5fb9-190">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e5fb9-190">OUTPUTS</span></span>

### <span data-ttu-id="e5fb9-191">System.Void</span><span class="sxs-lookup"><span data-stu-id="e5fb9-191">System.Void</span></span>

## <span data-ttu-id="e5fb9-192">NOTES</span><span class="sxs-lookup"><span data-stu-id="e5fb9-192">NOTES</span></span>

## <span data-ttu-id="e5fb9-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5fb9-193">RELATED LINKS</span></span>

[<span data-ttu-id="e5fb9-194">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e5fb9-194">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e5fb9-195">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e5fb9-195">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="e5fb9-196">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e5fb9-196">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="e5fb9-197">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="e5fb9-197">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
