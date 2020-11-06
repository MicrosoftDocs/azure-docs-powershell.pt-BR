---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 1f67da2d15aca003853bcb21846535bad4e2a066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599676"
---
# <span data-ttu-id="79344-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="79344-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="79344-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79344-102">SYNOPSIS</span></span>
<span data-ttu-id="79344-103">Cria um objeto de mapeamento de disco para discos de máquina virtual do Azure a serem replicados.</span><span class="sxs-lookup"><span data-stu-id="79344-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="79344-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79344-104">SYNTAX</span></span>

### <span data-ttu-id="79344-105">AzureToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="79344-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79344-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="79344-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79344-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79344-107">DESCRIPTION</span></span>
<span data-ttu-id="79344-108">Cria um objeto de mapeamento de disco que mapeia um disco da máquina virtual do Azure para a conta de armazenamento do cache e a conta de armazenamento de destino (região de recuperação) a ser usada para replicar o disco.</span><span class="sxs-lookup"><span data-stu-id="79344-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="79344-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79344-109">EXAMPLES</span></span>

### <span data-ttu-id="79344-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="79344-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="79344-111">Crie um objeto de mapeamento de disco para discos de máquina virtual do Azure a serem replicados. Usado durante a operação do Azure to Azure EnableD e do reprotect.</span><span class="sxs-lookup"><span data-stu-id="79344-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="79344-112">OS</span><span class="sxs-lookup"><span data-stu-id="79344-112">PARAMETERS</span></span>

### <span data-ttu-id="79344-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79344-113">-DefaultProfile</span></span>
<span data-ttu-id="79344-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79344-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79344-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="79344-115">-DiskId</span></span>
<span data-ttu-id="79344-116">Especifica a identificação do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="79344-116">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79344-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="79344-117">-LogStorageAccountId</span></span>
<span data-ttu-id="79344-118">Especifica o log ou a ID da conta de armazenamento do cache a ser usada para armazenar logs de replicação.</span><span class="sxs-lookup"><span data-stu-id="79344-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="79344-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="79344-119">-ManagedDisk</span></span>
<span data-ttu-id="79344-120">Especifica a entrada para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="79344-120">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79344-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="79344-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="79344-122">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="79344-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79344-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="79344-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="79344-124">Especifica o tipo de conta de disco gerenciado replicado.</span><span class="sxs-lookup"><span data-stu-id="79344-124">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79344-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="79344-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="79344-126">Especifica a ID do grupo de recursos de recuperação para o disco gerenciado replicado.</span><span class="sxs-lookup"><span data-stu-id="79344-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79344-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="79344-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="79344-128">Especifica o disco de destino de recuperação para disco gerenciado replicado.</span><span class="sxs-lookup"><span data-stu-id="79344-128">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79344-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="79344-129">-VhdUri</span></span>
<span data-ttu-id="79344-130">Especifique o URI do VHD do disco ao qual esse mapeamento corresponde.</span><span class="sxs-lookup"><span data-stu-id="79344-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79344-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="79344-131">-Confirm</span></span>
<span data-ttu-id="79344-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79344-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79344-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79344-133">-WhatIf</span></span>
<span data-ttu-id="79344-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="79344-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79344-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79344-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79344-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79344-136">CommonParameters</span></span>
<span data-ttu-id="79344-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79344-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79344-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79344-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79344-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79344-139">INPUTS</span></span>

### <span data-ttu-id="79344-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="79344-140">None</span></span>

## <span data-ttu-id="79344-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79344-141">OUTPUTS</span></span>

### <span data-ttu-id="79344-142">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="79344-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="79344-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79344-143">NOTES</span></span>

## <span data-ttu-id="79344-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79344-144">RELATED LINKS</span></span>
