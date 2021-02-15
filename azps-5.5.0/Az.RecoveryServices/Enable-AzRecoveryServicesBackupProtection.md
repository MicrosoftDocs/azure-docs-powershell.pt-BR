---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 41ee67359d4545a5b69ec1f9c44ff8e37302837e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114980"
---
# <span data-ttu-id="669df-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="669df-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="669df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="669df-102">SYNOPSIS</span></span>
<span data-ttu-id="669df-103">Habilita o backup de um item com uma política de proteção de Backup especificada.</span><span class="sxs-lookup"><span data-stu-id="669df-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="669df-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="669df-104">SYNTAX</span></span>

### <span data-ttu-id="669df-105">AzureVMComputeEnableProtection (Padrão)</span><span class="sxs-lookup"><span data-stu-id="669df-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="669df-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="669df-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="669df-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="669df-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="669df-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="669df-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="669df-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="669df-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="669df-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="669df-110">DESCRIPTION</span></span>
<span data-ttu-id="669df-111">O cmdlet **Enable-AzRecoveryServicesBackupProtection** habilita o backup associando uma política de proteção ao item.</span><span class="sxs-lookup"><span data-stu-id="669df-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="669df-112">Se a ID de política não estiver presente ou se o item de backup não estiver associado a nenhuma política, então esse comando esperará uma ID de política.</span><span class="sxs-lookup"><span data-stu-id="669df-112">If policy ID is not present or the backup item is not associated with any policy, then this command will expect a policyID.</span></span>
<span data-ttu-id="669df-113">De definir o contexto do cofre usando o Set-AzRecoveryServicesVaultContext cmdlet antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="669df-113">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="669df-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="669df-114">EXAMPLES</span></span>

### <span data-ttu-id="669df-115">Exemplo 1: Habilitar a proteção de backup para um item</span><span class="sxs-lookup"><span data-stu-id="669df-115">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="669df-116">O primeiro cmdlet obtém um objeto de política padrão e o armazena na variável $Pol padrão.</span><span class="sxs-lookup"><span data-stu-id="669df-116">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="669df-117">O segundo cmdlet especifica os LUNs de disco que devem ser backup e armazena-os $inclusionDiskLUNS variável.</span><span class="sxs-lookup"><span data-stu-id="669df-117">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="669df-118">O terceiro cmdlet define a política de proteção de backup para a máquina virtual ARM chamada V2VM usando a política no $Pol.</span><span class="sxs-lookup"><span data-stu-id="669df-118">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="669df-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="669df-119">Example 2</span></span>

<span data-ttu-id="669df-120">Habilita o backup de um item com uma política de proteção de Backup especificada.</span><span class="sxs-lookup"><span data-stu-id="669df-120">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="669df-121">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="669df-121">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="669df-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="669df-122">PARAMETERS</span></span>

### <span data-ttu-id="669df-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="669df-123">-DefaultProfile</span></span>
<span data-ttu-id="669df-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="669df-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="669df-125">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="669df-125">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="669df-126">Opção para especificar somente os discos de backup do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="669df-126">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="669df-127">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="669df-127">-ExclusionDisksList</span></span>
<span data-ttu-id="669df-128">Lista de LUNs de Disco a serem excluídos no backup e o restante é incluído automaticamente.</span><span class="sxs-lookup"><span data-stu-id="669df-128">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

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

### <span data-ttu-id="669df-129">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="669df-129">-InclusionDisksList</span></span>
<span data-ttu-id="669df-130">Lista de LUNs de Disco a serem incluídos no backup e o restante é excluído automaticamente, exceto o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="669df-130">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

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

### <span data-ttu-id="669df-131">-Item</span><span class="sxs-lookup"><span data-stu-id="669df-131">-Item</span></span>
<span data-ttu-id="669df-132">Especifica o item backup para o qual este cmdlet habilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="669df-132">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="669df-133">Para obter um **cmdlet AzureRmRecoveryServicesBackupItem, use o cmdlet Get-AzRecoveryServicesBackupItem AzureRmRecoveryServicesBackupItem.**</span><span class="sxs-lookup"><span data-stu-id="669df-133">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="669df-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="669df-134">-Name</span></span>
<span data-ttu-id="669df-135">Especifica o nome do item backup.</span><span class="sxs-lookup"><span data-stu-id="669df-135">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="669df-136">-Política</span><span class="sxs-lookup"><span data-stu-id="669df-136">-Policy</span></span>
<span data-ttu-id="669df-137">Especifica a política de proteção que este cmdlet associa a um item.</span><span class="sxs-lookup"><span data-stu-id="669df-137">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="669df-138">Para obter um **objeto AzureRmRecoveryServicesBackupProtectionPolicy,** use Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="669df-138">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="669df-139">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="669df-139">-ProtectableItem</span></span>
<span data-ttu-id="669df-140">Especifica o item a ser protegido com a política determinada.</span><span class="sxs-lookup"><span data-stu-id="669df-140">Specifies the item to be protected with the given policy.</span></span>

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

### <span data-ttu-id="669df-141">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="669df-141">-ResetExclusionSettings</span></span>
<span data-ttu-id="669df-142">Especifica a configuração de exclusão de disco redefinida associada ao item</span><span class="sxs-lookup"><span data-stu-id="669df-142">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="669df-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="669df-143">-ResourceGroupName</span></span>
<span data-ttu-id="669df-144">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="669df-144">Specifies the name of the resource group.</span></span>
<span data-ttu-id="669df-145">Especifique este parâmetro somente para máquinas virtuais ARM.</span><span class="sxs-lookup"><span data-stu-id="669df-145">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="669df-146">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="669df-146">-StorageAccountName</span></span>
<span data-ttu-id="669df-147">Nome da conta de armazenamento de compartilhamento de arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="669df-147">Azure file share storage account name</span></span>

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

### <span data-ttu-id="669df-148">-VaultId</span><span class="sxs-lookup"><span data-stu-id="669df-148">-VaultId</span></span>
<span data-ttu-id="669df-149">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="669df-149">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="669df-150">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="669df-150">-Confirm</span></span>
<span data-ttu-id="669df-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="669df-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="669df-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="669df-152">-WhatIf</span></span>
<span data-ttu-id="669df-153">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="669df-153">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="669df-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669df-154">CommonParameters</span></span>
<span data-ttu-id="669df-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="669df-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669df-156">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="669df-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669df-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="669df-157">INPUTS</span></span>

### <span data-ttu-id="669df-158">System.String</span><span class="sxs-lookup"><span data-stu-id="669df-158">System.String</span></span>

### <span data-ttu-id="669df-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="669df-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="669df-160">Saídas</span><span class="sxs-lookup"><span data-stu-id="669df-160">OUTPUTS</span></span>

### <span data-ttu-id="669df-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="669df-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="669df-162">Notas</span><span class="sxs-lookup"><span data-stu-id="669df-162">NOTES</span></span>

## <span data-ttu-id="669df-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="669df-163">RELATED LINKS</span></span>

[<span data-ttu-id="669df-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="669df-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="669df-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="669df-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


