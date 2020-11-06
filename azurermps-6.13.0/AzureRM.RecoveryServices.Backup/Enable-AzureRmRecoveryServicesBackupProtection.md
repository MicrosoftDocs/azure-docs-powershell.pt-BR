---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 357256d1c1a754915cbebc978e5c4ccf4440ccf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609760"
---
# <span data-ttu-id="065b1-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="065b1-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="065b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="065b1-102">SYNOPSIS</span></span>
<span data-ttu-id="065b1-103">Habilita o backup para um item com uma política de proteção de backup especificada.</span><span class="sxs-lookup"><span data-stu-id="065b1-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="065b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="065b1-104">SYNTAX</span></span>

### <span data-ttu-id="065b1-105">AzureVMComputeEnableProtection (padrão)</span><span class="sxs-lookup"><span data-stu-id="065b1-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="065b1-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="065b1-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="065b1-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="065b1-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 -StorageAccountName <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="065b1-108">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="065b1-108">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="065b1-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="065b1-109">DESCRIPTION</span></span>
<span data-ttu-id="065b1-110">O cmdlet **Enable-AzureRmRecoveryServicesBackupProtection** define a política de proteção de backup do Azure em um item.</span><span class="sxs-lookup"><span data-stu-id="065b1-110">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="065b1-111">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="065b1-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="065b1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="065b1-112">EXAMPLES</span></span>

### <span data-ttu-id="065b1-113">Exemplo 1: habilitar a proteção de backup para um item</span><span class="sxs-lookup"><span data-stu-id="065b1-113">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="065b1-114">O primeiro cmdlet obtém um objeto de política padrão e, em seguida, armazena-o na variável $Pol.</span><span class="sxs-lookup"><span data-stu-id="065b1-114">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="065b1-115">O segundo cmdlet define a política de proteção de backup para a máquina virtual ARM chamada V2VM usando a política em $Pol.</span><span class="sxs-lookup"><span data-stu-id="065b1-115">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="065b1-116">OS</span><span class="sxs-lookup"><span data-stu-id="065b1-116">PARAMETERS</span></span>

### <span data-ttu-id="065b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="065b1-117">-DefaultProfile</span></span>
<span data-ttu-id="065b1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="065b1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="065b1-119">-Item</span><span class="sxs-lookup"><span data-stu-id="065b1-119">-Item</span></span>
<span data-ttu-id="065b1-120">Especifica o item de backup para o qual esse cmdlet habilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="065b1-120">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="065b1-121">Para obter um **AzureRmRecoveryServicesBackupItem** , use o cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="065b1-121">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="065b1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="065b1-122">-Name</span></span>
<span data-ttu-id="065b1-123">Especifica o nome do item de backup.</span><span class="sxs-lookup"><span data-stu-id="065b1-123">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="065b1-124">-Política</span><span class="sxs-lookup"><span data-stu-id="065b1-124">-Policy</span></span>
<span data-ttu-id="065b1-125">Especifica a política de proteção que este cmdlet associa a um item.</span><span class="sxs-lookup"><span data-stu-id="065b1-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="065b1-126">Para obter um objeto **AzureRmRecoveryServicesBackupProtectionPolicy** , use o cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="065b1-126">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="065b1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="065b1-127">-ResourceGroupName</span></span>
<span data-ttu-id="065b1-128">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="065b1-128">Specifies the name of the resource group.</span></span>
<span data-ttu-id="065b1-129">Especifique esse parâmetro somente para máquinas virtuais ARM.</span><span class="sxs-lookup"><span data-stu-id="065b1-129">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="065b1-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="065b1-130">-ServiceName</span></span>
<span data-ttu-id="065b1-131">Especifica o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="065b1-131">Specifies the service name.</span></span>
<span data-ttu-id="065b1-132">Especifique esse parâmetro somente para máquinas virtuais ASM.</span><span class="sxs-lookup"><span data-stu-id="065b1-132">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="065b1-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="065b1-133">-StorageAccountName</span></span>
<span data-ttu-id="065b1-134">Nome da conta de armazenamento do Azure File Share</span><span class="sxs-lookup"><span data-stu-id="065b1-134">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="065b1-135">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="065b1-135">-VaultId</span></span>
<span data-ttu-id="065b1-136">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="065b1-136">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="065b1-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="065b1-137">-Confirm</span></span>
<span data-ttu-id="065b1-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="065b1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="065b1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="065b1-139">-WhatIf</span></span>
<span data-ttu-id="065b1-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="065b1-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="065b1-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="065b1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="065b1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="065b1-142">CommonParameters</span></span>
<span data-ttu-id="065b1-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="065b1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="065b1-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="065b1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="065b1-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="065b1-145">INPUTS</span></span>

### <span data-ttu-id="065b1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="065b1-146">System.String</span></span>
<span data-ttu-id="065b1-147">Parâmetros: Vaultid (ByValue)</span><span class="sxs-lookup"><span data-stu-id="065b1-147">Parameters: VaultId (ByValue)</span></span>

### <span data-ttu-id="065b1-148">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="065b1-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="065b1-149">Parâmetros: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="065b1-149">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="065b1-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="065b1-150">OUTPUTS</span></span>

### <span data-ttu-id="065b1-151">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="065b1-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="065b1-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="065b1-152">NOTES</span></span>

## <span data-ttu-id="065b1-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="065b1-153">RELATED LINKS</span></span>

[<span data-ttu-id="065b1-154">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="065b1-154">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="065b1-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="065b1-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


