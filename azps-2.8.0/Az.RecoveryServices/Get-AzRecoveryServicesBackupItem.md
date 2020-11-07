---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 2dfc4b8fd0491a9f8c2200876609ab0a8cb00cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773020"
---
# <span data-ttu-id="709ea-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="709ea-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="709ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="709ea-102">SYNOPSIS</span></span>

<span data-ttu-id="709ea-103">Obtém os itens de um contêiner no backup.</span><span class="sxs-lookup"><span data-stu-id="709ea-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="709ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="709ea-104">SYNTAX</span></span>

### <span data-ttu-id="709ea-105">GetItemsForContainer (padrão)</span><span class="sxs-lookup"><span data-stu-id="709ea-105">GetItemsForContainer (Default)</span></span>

```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="709ea-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="709ea-106">GetItemsForVault</span></span>

```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="709ea-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="709ea-107">GetItemsForPolicy</span></span>

```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [[-DeleteState] <ItemDeleteState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="709ea-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="709ea-108">DESCRIPTION</span></span>

<span data-ttu-id="709ea-109">O cmdlet **Get-AzRecoveryServicesBackupItem** Obtém os itens em um contêiner ou um valor no Azure backup e o status de proteção dos itens.</span><span class="sxs-lookup"><span data-stu-id="709ea-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="709ea-110">Um contêiner que está registrado para um cofre de serviços de recuperação do Azure pode ter um ou mais itens que podem ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="709ea-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="709ea-111">Para máquinas virtuais do Azure, pode haver apenas um item de backup no contêiner da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="709ea-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="709ea-112">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="709ea-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="709ea-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="709ea-113">EXAMPLES</span></span>

### <span data-ttu-id="709ea-114">Exemplo 1: obter um item de um contêiner de backup</span><span class="sxs-lookup"><span data-stu-id="709ea-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="709ea-115">O primeiro comando obtém o contêiner do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="709ea-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="709ea-116">O segundo comando obtém o item de backup chamado V2VM em $Container e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="709ea-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="709ea-117">OS</span><span class="sxs-lookup"><span data-stu-id="709ea-117">PARAMETERS</span></span>

### <span data-ttu-id="709ea-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="709ea-118">-BackupManagementType</span></span>

<span data-ttu-id="709ea-119">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="709ea-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="709ea-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="709ea-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="709ea-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="709ea-121">AzureVM</span></span>
- <span data-ttu-id="709ea-122">Marte</span><span class="sxs-lookup"><span data-stu-id="709ea-122">MARS</span></span>
- <span data-ttu-id="709ea-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="709ea-123">SCDPM</span></span>
- <span data-ttu-id="709ea-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="709ea-124">AzureBackupServer</span></span>
- <span data-ttu-id="709ea-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="709ea-125">AzureSQL</span></span>
- <span data-ttu-id="709ea-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="709ea-126">AzureStorage</span></span>
- <span data-ttu-id="709ea-127">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="709ea-127">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709ea-128">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="709ea-128">-Container</span></span>

<span data-ttu-id="709ea-129">Especifica um objeto de contêiner do qual este cmdlet obtém itens de backup.</span><span class="sxs-lookup"><span data-stu-id="709ea-129">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="709ea-130">Para obter um **AzureRmRecoveryServicesBackupContainer** , use o cmdlet **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="709ea-130">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: GetItemsForContainer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="709ea-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709ea-131">-DefaultProfile</span></span>

<span data-ttu-id="709ea-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="709ea-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="709ea-133">-Deletestate</span><span class="sxs-lookup"><span data-stu-id="709ea-133">-DeleteState</span></span>
<span data-ttu-id="709ea-134">Especifica o deletestate do item os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="709ea-134">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="709ea-135">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="709ea-135">ToBeDeleted</span></span>
- <span data-ttu-id="709ea-136">Não excluído</span><span class="sxs-lookup"><span data-stu-id="709ea-136">NotDeleted</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709ea-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="709ea-137">-Name</span></span>

<span data-ttu-id="709ea-138">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="709ea-138">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709ea-139">-Política</span><span class="sxs-lookup"><span data-stu-id="709ea-139">-Policy</span></span>

<span data-ttu-id="709ea-140">Objeto de política de proteção.</span><span class="sxs-lookup"><span data-stu-id="709ea-140">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709ea-141">-Protectionstate</span><span class="sxs-lookup"><span data-stu-id="709ea-141">-ProtectionState</span></span>

<span data-ttu-id="709ea-142">Especifica o estado de proteção.</span><span class="sxs-lookup"><span data-stu-id="709ea-142">Specifies the state of protection.</span></span>
<span data-ttu-id="709ea-143">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="709ea-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="709ea-144">IRPending.</span><span class="sxs-lookup"><span data-stu-id="709ea-144">IRPending.</span></span>
<span data-ttu-id="709ea-145">A sincronização inicial ainda não começou e ainda não há um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="709ea-145">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="709ea-146">Protegida.</span><span class="sxs-lookup"><span data-stu-id="709ea-146">Protected.</span></span>
<span data-ttu-id="709ea-147">A proteção está em andamento.</span><span class="sxs-lookup"><span data-stu-id="709ea-147">Protection is ongoing.</span></span>
- <span data-ttu-id="709ea-148">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="709ea-148">ProtectionError.</span></span>
<span data-ttu-id="709ea-149">Há um erro de proteção.</span><span class="sxs-lookup"><span data-stu-id="709ea-149">There is a protection error.</span></span>
- <span data-ttu-id="709ea-150">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="709ea-150">ProtectionStopped.</span></span>
<span data-ttu-id="709ea-151">A proteção está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="709ea-151">Protection is disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709ea-152">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="709ea-152">-ProtectionStatus</span></span>

<span data-ttu-id="709ea-153">Especifica o status geral da proteção de um item no contêiner.</span><span class="sxs-lookup"><span data-stu-id="709ea-153">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="709ea-154">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="709ea-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="709ea-155">Bom</span><span class="sxs-lookup"><span data-stu-id="709ea-155">Healthy</span></span>
- <span data-ttu-id="709ea-156">Não íntegro</span><span class="sxs-lookup"><span data-stu-id="709ea-156">Unhealthy</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709ea-157">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="709ea-157">-VaultId</span></span>

<span data-ttu-id="709ea-158">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="709ea-158">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="709ea-159">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="709ea-159">-WorkloadType</span></span>

<span data-ttu-id="709ea-160">Especifica o tipo de carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="709ea-160">Specifies the workload type.</span></span>
<span data-ttu-id="709ea-161">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="709ea-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="709ea-162">AzureVM</span><span class="sxs-lookup"><span data-stu-id="709ea-162">AzureVM</span></span>
- <span data-ttu-id="709ea-163">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="709ea-163">AzureSQLDatabase</span></span>
- <span data-ttu-id="709ea-164">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="709ea-164">AzureFiles</span></span>
- <span data-ttu-id="709ea-165">SERVIÇO</span><span class="sxs-lookup"><span data-stu-id="709ea-165">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709ea-166">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709ea-166">-CommonParameters</span></span>

<span data-ttu-id="709ea-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="709ea-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709ea-168">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="709ea-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709ea-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="709ea-169">INPUTS</span></span>

### <span data-ttu-id="709ea-170">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="709ea-170">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="709ea-171">System. String</span><span class="sxs-lookup"><span data-stu-id="709ea-171">System.String</span></span>

## <span data-ttu-id="709ea-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="709ea-172">OUTPUTS</span></span>

### <span data-ttu-id="709ea-173">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="709ea-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="709ea-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="709ea-174">NOTES</span></span>

## <span data-ttu-id="709ea-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="709ea-175">RELATED LINKS</span></span>

[<span data-ttu-id="709ea-176">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="709ea-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="709ea-177">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="709ea-177">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="709ea-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="709ea-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="709ea-179">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="709ea-179">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
