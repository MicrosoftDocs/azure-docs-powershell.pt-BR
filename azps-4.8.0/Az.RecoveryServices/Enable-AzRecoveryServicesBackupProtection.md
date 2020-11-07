---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: f0147cea03d4b535102efd53af1a4d5f88338530
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947704"
---
# <span data-ttu-id="c751c-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c751c-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="c751c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c751c-102">SYNOPSIS</span></span>
<span data-ttu-id="c751c-103">Habilita o backup para um item com uma política de proteção de backup especificada.</span><span class="sxs-lookup"><span data-stu-id="c751c-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="c751c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c751c-104">SYNTAX</span></span>

### <span data-ttu-id="c751c-105">AzureVMComputeEnableProtection (padrão)</span><span class="sxs-lookup"><span data-stu-id="c751c-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c751c-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="c751c-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c751c-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="c751c-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c751c-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="c751c-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c751c-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="c751c-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c751c-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c751c-110">DESCRIPTION</span></span>
<span data-ttu-id="c751c-111">O cmdlet **Enable-AzRecoveryServicesBackupProtection** permite o backup associando uma política de proteção ao item.</span><span class="sxs-lookup"><span data-stu-id="c751c-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="c751c-112">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="c751c-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c751c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c751c-113">EXAMPLES</span></span>

### <span data-ttu-id="c751c-114">Exemplo 1: habilitar a proteção de backup para um item</span><span class="sxs-lookup"><span data-stu-id="c751c-114">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="c751c-115">O primeiro cmdlet obtém um objeto de política padrão e, em seguida, armazena-o na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="c751c-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="c751c-116">O segundo cmdlet especifica os LUNs de disco dos quais fazer backup e os armazena em $inclusionDiskLUNS variável.</span><span class="sxs-lookup"><span data-stu-id="c751c-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="c751c-117">O terceiro cmdlet define a política de proteção de backup para a máquina virtual ARM chamada V2VM usando a política em $Pol.</span><span class="sxs-lookup"><span data-stu-id="c751c-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="c751c-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c751c-118">Example 2</span></span>

<span data-ttu-id="c751c-119">Habilita o backup para um item com uma política de proteção de backup especificada.</span><span class="sxs-lookup"><span data-stu-id="c751c-119">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="c751c-120">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="c751c-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="c751c-121">OS</span><span class="sxs-lookup"><span data-stu-id="c751c-121">PARAMETERS</span></span>

### <span data-ttu-id="c751c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c751c-122">-DefaultProfile</span></span>
<span data-ttu-id="c751c-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c751c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c751c-124">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="c751c-124">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="c751c-125">Opção para especificar somente para OS discos do so de backup</span><span class="sxs-lookup"><span data-stu-id="c751c-125">Option to specify to backup OS disks only</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c751c-126">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="c751c-126">-ExclusionDisksList</span></span>
<span data-ttu-id="c751c-127">A lista de LUNs de disco a ser excluída no backup e o restante são automaticamente incluídas.</span><span class="sxs-lookup"><span data-stu-id="c751c-127">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c751c-128">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="c751c-128">-InclusionDisksList</span></span>
<span data-ttu-id="c751c-129">Lista de LUNs de disco a serem incluídos no backup e o restante são excluídos automaticamente, exceto o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c751c-129">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c751c-130">-Item</span><span class="sxs-lookup"><span data-stu-id="c751c-130">-Item</span></span>
<span data-ttu-id="c751c-131">Especifica o item de backup para o qual esse cmdlet habilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="c751c-131">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="c751c-132">Para obter um **AzureRmRecoveryServicesBackupItem** , use o cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="c751c-132">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c751c-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="c751c-133">-Name</span></span>
<span data-ttu-id="c751c-134">Especifica o nome do item de backup.</span><span class="sxs-lookup"><span data-stu-id="c751c-134">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c751c-135">-Política</span><span class="sxs-lookup"><span data-stu-id="c751c-135">-Policy</span></span>
<span data-ttu-id="c751c-136">Especifica a política de proteção que este cmdlet associa a um item.</span><span class="sxs-lookup"><span data-stu-id="c751c-136">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="c751c-137">Para obter um objeto **AzureRmRecoveryServicesBackupProtectionPolicy** , use o cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="c751c-137">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c751c-138">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c751c-138">-ProtectableItem</span></span>
<span data-ttu-id="c751c-139">Especifica o item a ser protegido com a política fornecida.</span><span class="sxs-lookup"><span data-stu-id="c751c-139">Specifies the item to be protected with the given policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: AzureWorkloadEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c751c-140">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="c751c-140">-ResetExclusionSettings</span></span>
<span data-ttu-id="c751c-141">Especifica a redefinição da configuração de exclusão de disco associada ao item</span><span class="sxs-lookup"><span data-stu-id="c751c-141">Specifies to reset disk exclusion setting associated with the item</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c751c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c751c-142">-ResourceGroupName</span></span>
<span data-ttu-id="c751c-143">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c751c-143">Specifies the name of the resource group.</span></span>
<span data-ttu-id="c751c-144">Especifique esse parâmetro somente para máquinas virtuais ARM.</span><span class="sxs-lookup"><span data-stu-id="c751c-144">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c751c-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c751c-145">-StorageAccountName</span></span>
<span data-ttu-id="c751c-146">Nome da conta de armazenamento do Azure File Share</span><span class="sxs-lookup"><span data-stu-id="c751c-146">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c751c-147">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="c751c-147">-VaultId</span></span>
<span data-ttu-id="c751c-148">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="c751c-148">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c751c-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c751c-149">-Confirm</span></span>
<span data-ttu-id="c751c-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c751c-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c751c-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c751c-151">-WhatIf</span></span>
<span data-ttu-id="c751c-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c751c-152">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="c751c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c751c-153">CommonParameters</span></span>
<span data-ttu-id="c751c-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c751c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c751c-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c751c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c751c-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c751c-156">INPUTS</span></span>

### <span data-ttu-id="c751c-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c751c-157">System.String</span></span>

### <span data-ttu-id="c751c-158">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="c751c-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="c751c-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c751c-159">OUTPUTS</span></span>

### <span data-ttu-id="c751c-160">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="c751c-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c751c-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c751c-161">NOTES</span></span>

## <span data-ttu-id="c751c-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c751c-162">RELATED LINKS</span></span>

[<span data-ttu-id="c751c-163">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c751c-163">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="c751c-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c751c-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


