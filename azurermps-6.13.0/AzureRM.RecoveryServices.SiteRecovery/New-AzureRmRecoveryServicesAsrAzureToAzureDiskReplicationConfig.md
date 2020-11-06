---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 19ba256176c47b5841b9d124d186f376f0ecce7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602105"
---
# <span data-ttu-id="a5d5c-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="a5d5c-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="a5d5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d5c-103">Cria um objeto de mapeamento de disco para discos de máquina virtual do Azure a serem replicados.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5d5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5d5c-104">SYNTAX</span></span>

### <span data-ttu-id="a5d5c-105">AzureToAzure (padrão)</span><span class="sxs-lookup"><span data-stu-id="a5d5c-105">AzureToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5d5c-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a5d5c-106">AzureToAzureManagedDisk</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5d5c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5d5c-107">DESCRIPTION</span></span>
<span data-ttu-id="a5d5c-108">Cria um objeto de mapeamento de disco que mapeia um disco da máquina virtual do Azure para a conta de armazenamento do cache e a conta de armazenamento de destino (região de recuperação) a ser usada para replicar o disco.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="a5d5c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5d5c-109">EXAMPLES</span></span>

### <span data-ttu-id="a5d5c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5d5c-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="a5d5c-111">Crie um objeto de mapeamento de disco para discos de máquina virtual do Azure a serem replicados. Usado durante a operação do Azure to Azure EnableD e do reprotect.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="a5d5c-112">OS</span><span class="sxs-lookup"><span data-stu-id="a5d5c-112">PARAMETERS</span></span>

### <span data-ttu-id="a5d5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d5c-113">-DefaultProfile</span></span>
<span data-ttu-id="a5d5c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5d5c-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="a5d5c-115">-DiskId</span></span>
<span data-ttu-id="a5d5c-116">Especifica a identificação do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-116">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="a5d5c-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a5d5c-117">-LogStorageAccountId</span></span>
<span data-ttu-id="a5d5c-118">Especifica o log ou a ID da conta de armazenamento do cache a ser usada para armazenar logs de replicação.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="a5d5c-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a5d5c-119">-ManagedDisk</span></span>
<span data-ttu-id="a5d5c-120">Especifica a entrada para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-120">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="a5d5c-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a5d5c-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="a5d5c-122">Especifica a ID da conta de armazenamento do Azure a ser replicada.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="a5d5c-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="a5d5c-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="a5d5c-124">Especifica o tipo de conta de disco gerenciado replicado.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-124">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="a5d5c-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="a5d5c-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="a5d5c-126">Especifica a ID do grupo de recursos de recuperação para o disco gerenciado replicado.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="a5d5c-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="a5d5c-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="a5d5c-128">Especifica o disco de destino de recuperação para disco gerenciado replicado.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-128">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="a5d5c-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="a5d5c-129">-VhdUri</span></span>
<span data-ttu-id="a5d5c-130">Especifique o URI do VHD do disco ao qual esse mapeamento corresponde.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="a5d5c-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a5d5c-131">-Confirm</span></span>
<span data-ttu-id="a5d5c-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d5c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d5c-133">-WhatIf</span></span>
<span data-ttu-id="a5d5c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d5c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d5c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d5c-136">CommonParameters</span></span>
<span data-ttu-id="a5d5c-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d5c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d5c-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d5c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d5c-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5d5c-139">INPUTS</span></span>

### <span data-ttu-id="a5d5c-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a5d5c-140">None</span></span>

## <span data-ttu-id="a5d5c-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5d5c-141">OUTPUTS</span></span>

### <span data-ttu-id="a5d5c-142">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="a5d5c-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="a5d5c-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5d5c-143">NOTES</span></span>

## <span data-ttu-id="a5d5c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5d5c-144">RELATED LINKS</span></span>
