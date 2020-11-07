---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7f29c0bef53d75be4f5b253e3a15bf78cbacd04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773060"
---
# <span data-ttu-id="5c89e-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="5c89e-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="5c89e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c89e-102">SYNOPSIS</span></span>
<span data-ttu-id="5c89e-103">Habilita o backup para um item com uma política de proteção de backup especificada.</span><span class="sxs-lookup"><span data-stu-id="5c89e-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="5c89e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c89e-104">SYNTAX</span></span>

### <span data-ttu-id="5c89e-105">AzureVMComputeEnableProtection (padrão)</span><span class="sxs-lookup"><span data-stu-id="5c89e-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ResourceGroupName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c89e-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="5c89e-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c89e-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="5c89e-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c89e-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="5c89e-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c89e-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="5c89e-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c89e-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c89e-110">DESCRIPTION</span></span>
<span data-ttu-id="5c89e-111">O cmdlet **Enable-AzRecoveryServicesBackupProtection** define a política de proteção de backup do Azure em um item.</span><span class="sxs-lookup"><span data-stu-id="5c89e-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="5c89e-112">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="5c89e-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5c89e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c89e-113">EXAMPLES</span></span>

### <span data-ttu-id="5c89e-114">Exemplo 1: habilitar a proteção de backup para um item</span><span class="sxs-lookup"><span data-stu-id="5c89e-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="5c89e-115">O primeiro cmdlet obtém um objeto de política padrão e, em seguida, armazena-o na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="5c89e-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="5c89e-116">O segundo cmdlet define a política de proteção de backup para a máquina virtual ARM chamada V2VM usando a política em $Pol.</span><span class="sxs-lookup"><span data-stu-id="5c89e-116">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="5c89e-117">OS</span><span class="sxs-lookup"><span data-stu-id="5c89e-117">PARAMETERS</span></span>

### <span data-ttu-id="5c89e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c89e-118">-DefaultProfile</span></span>
<span data-ttu-id="5c89e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c89e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c89e-120">-Item</span><span class="sxs-lookup"><span data-stu-id="5c89e-120">-Item</span></span>
<span data-ttu-id="5c89e-121">Especifica o item de backup para o qual esse cmdlet habilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="5c89e-121">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="5c89e-122">Para obter um **AzureRmRecoveryServicesBackupItem** , use o cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="5c89e-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="5c89e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c89e-123">-Name</span></span>
<span data-ttu-id="5c89e-124">Especifica o nome do item de backup.</span><span class="sxs-lookup"><span data-stu-id="5c89e-124">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="5c89e-125">-Política</span><span class="sxs-lookup"><span data-stu-id="5c89e-125">-Policy</span></span>
<span data-ttu-id="5c89e-126">Especifica a política de proteção que este cmdlet associa a um item.</span><span class="sxs-lookup"><span data-stu-id="5c89e-126">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="5c89e-127">Para obter um objeto **AzureRmRecoveryServicesBackupProtectionPolicy** , use o cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="5c89e-127">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c89e-128">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5c89e-128">-ProtectableItem</span></span>
<span data-ttu-id="5c89e-129">Valor do filtro para o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="5c89e-129">Filter value for status of job.</span></span>

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

### <span data-ttu-id="5c89e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c89e-130">-ResourceGroupName</span></span>
<span data-ttu-id="5c89e-131">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5c89e-131">Specifies the name of the resource group.</span></span>
<span data-ttu-id="5c89e-132">Especifique esse parâmetro somente para máquinas virtuais ARM.</span><span class="sxs-lookup"><span data-stu-id="5c89e-132">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="5c89e-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5c89e-133">-ServiceName</span></span>
<span data-ttu-id="5c89e-134">Especifica o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="5c89e-134">Specifies the service name.</span></span>
<span data-ttu-id="5c89e-135">Especifique esse parâmetro somente para máquinas virtuais ASM.</span><span class="sxs-lookup"><span data-stu-id="5c89e-135">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c89e-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5c89e-136">-StorageAccountName</span></span>
<span data-ttu-id="5c89e-137">Nome da conta de armazenamento do Azure File Share</span><span class="sxs-lookup"><span data-stu-id="5c89e-137">Azure file share storage account name</span></span>

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

### <span data-ttu-id="5c89e-138">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="5c89e-138">-VaultId</span></span>
<span data-ttu-id="5c89e-139">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="5c89e-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5c89e-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5c89e-140">-Confirm</span></span>
<span data-ttu-id="5c89e-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c89e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c89e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c89e-142">-WhatIf</span></span>
<span data-ttu-id="5c89e-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c89e-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c89e-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c89e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c89e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c89e-145">CommonParameters</span></span>
<span data-ttu-id="5c89e-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c89e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c89e-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c89e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c89e-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c89e-148">INPUTS</span></span>

### <span data-ttu-id="5c89e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5c89e-149">System.String</span></span>

### <span data-ttu-id="5c89e-150">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="5c89e-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="5c89e-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c89e-151">OUTPUTS</span></span>

### <span data-ttu-id="5c89e-152">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="5c89e-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5c89e-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c89e-153">NOTES</span></span>

## <span data-ttu-id="5c89e-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c89e-154">RELATED LINKS</span></span>

[<span data-ttu-id="5c89e-155">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="5c89e-155">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="5c89e-156">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c89e-156">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


