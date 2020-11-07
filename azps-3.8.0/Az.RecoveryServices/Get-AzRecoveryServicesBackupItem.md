---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 75eb9975a578e1114e994b08949eda8d3dafda0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940890"
---
# <span data-ttu-id="81c39-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="81c39-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="81c39-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81c39-102">SYNOPSIS</span></span>

<span data-ttu-id="81c39-103">Obtém os itens de um contêiner no backup.</span><span class="sxs-lookup"><span data-stu-id="81c39-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="81c39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81c39-104">SYNTAX</span></span>

### <span data-ttu-id="81c39-105">GetItemsForContainer (padrão)</span><span class="sxs-lookup"><span data-stu-id="81c39-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81c39-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="81c39-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81c39-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="81c39-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81c39-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81c39-108">DESCRIPTION</span></span>

<span data-ttu-id="81c39-109">O cmdlet **Get-AzRecoveryServicesBackupItem** Obtém os itens em um contêiner ou um valor no Azure backup e o status de proteção dos itens.</span><span class="sxs-lookup"><span data-stu-id="81c39-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="81c39-110">Um contêiner que está registrado para um cofre de serviços de recuperação do Azure pode ter um ou mais itens que podem ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="81c39-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="81c39-111">Para máquinas virtuais do Azure, pode haver apenas um item de backup no contêiner da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="81c39-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="81c39-112">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="81c39-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="81c39-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81c39-113">EXAMPLES</span></span>

### <span data-ttu-id="81c39-114">Exemplo 1: obter um item de um contêiner de backup</span><span class="sxs-lookup"><span data-stu-id="81c39-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="81c39-115">O primeiro comando obtém o contêiner do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="81c39-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="81c39-116">O segundo comando obtém o item de backup chamado V2VM em $Container e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="81c39-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="81c39-117">Exemplo 2: obter um item de compartilhamento de arquivos do Azure de FriendlyName</span><span class="sxs-lookup"><span data-stu-id="81c39-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="81c39-118">O primeiro comando obtém o contêiner do tipo AzureStorage e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="81c39-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="81c39-119">O segundo comando obtém o item de backup cujo FriendlyName corresponde ao valor passado no parâmetro FriendlyName e o armazena na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="81c39-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="81c39-120">Usar o parâmetro FriendlyName pode resultar em retornar mais de um compartilhamento de arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="81c39-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="81c39-121">Nesse caso, use o parâmetro Name com valor de parâmetro como a propriedade Name retornada na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="81c39-121">In such cases use -Name parameter with parameter value as the Name property returned in $BackupItem variable.</span></span>

## <span data-ttu-id="81c39-122">OS</span><span class="sxs-lookup"><span data-stu-id="81c39-122">PARAMETERS</span></span>

### <span data-ttu-id="81c39-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="81c39-123">-BackupManagementType</span></span>

<span data-ttu-id="81c39-124">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="81c39-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="81c39-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="81c39-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81c39-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="81c39-126">AzureVM</span></span>
- <span data-ttu-id="81c39-127">Marte</span><span class="sxs-lookup"><span data-stu-id="81c39-127">MARS</span></span>
- <span data-ttu-id="81c39-128">SCDPM</span><span class="sxs-lookup"><span data-stu-id="81c39-128">SCDPM</span></span>
- <span data-ttu-id="81c39-129">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="81c39-129">AzureBackupServer</span></span>
- <span data-ttu-id="81c39-130">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="81c39-130">AzureSQL</span></span>
- <span data-ttu-id="81c39-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="81c39-131">AzureStorage</span></span>
- <span data-ttu-id="81c39-132">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="81c39-132">AzureWorkload</span></span>

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

### <span data-ttu-id="81c39-133">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="81c39-133">-Container</span></span>

<span data-ttu-id="81c39-134">Especifica um objeto de contêiner do qual este cmdlet obtém itens de backup.</span><span class="sxs-lookup"><span data-stu-id="81c39-134">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="81c39-135">Para obter um **AzureRmRecoveryServicesBackupContainer** , use o cmdlet **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="81c39-135">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="81c39-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c39-136">-DefaultProfile</span></span>

<span data-ttu-id="81c39-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81c39-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81c39-138">-Deletestate</span><span class="sxs-lookup"><span data-stu-id="81c39-138">-DeleteState</span></span>
<span data-ttu-id="81c39-139">Especifica o deletestate do item os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="81c39-139">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81c39-140">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="81c39-140">ToBeDeleted</span></span>
- <span data-ttu-id="81c39-141">Não excluído</span><span class="sxs-lookup"><span data-stu-id="81c39-141">NotDeleted</span></span>

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

### <span data-ttu-id="81c39-142">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="81c39-142">-FriendlyName</span></span>
<span data-ttu-id="81c39-143">FriendlyName do item de backup</span><span class="sxs-lookup"><span data-stu-id="81c39-143">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="81c39-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="81c39-144">-Name</span></span>

<span data-ttu-id="81c39-145">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="81c39-145">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="81c39-146">-Política</span><span class="sxs-lookup"><span data-stu-id="81c39-146">-Policy</span></span>

<span data-ttu-id="81c39-147">Objeto de política de proteção.</span><span class="sxs-lookup"><span data-stu-id="81c39-147">Protection policy object.</span></span>

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

### <span data-ttu-id="81c39-148">-Protectionstate</span><span class="sxs-lookup"><span data-stu-id="81c39-148">-ProtectionState</span></span>

<span data-ttu-id="81c39-149">Especifica o estado de proteção.</span><span class="sxs-lookup"><span data-stu-id="81c39-149">Specifies the state of protection.</span></span>
<span data-ttu-id="81c39-150">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="81c39-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81c39-151">IRPending.</span><span class="sxs-lookup"><span data-stu-id="81c39-151">IRPending.</span></span>
<span data-ttu-id="81c39-152">A sincronização inicial ainda não começou e ainda não há um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="81c39-152">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="81c39-153">Protegida.</span><span class="sxs-lookup"><span data-stu-id="81c39-153">Protected.</span></span>
<span data-ttu-id="81c39-154">A proteção está em andamento.</span><span class="sxs-lookup"><span data-stu-id="81c39-154">Protection is ongoing.</span></span>
- <span data-ttu-id="81c39-155">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="81c39-155">ProtectionError.</span></span>
<span data-ttu-id="81c39-156">Há um erro de proteção.</span><span class="sxs-lookup"><span data-stu-id="81c39-156">There is a protection error.</span></span>
- <span data-ttu-id="81c39-157">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="81c39-157">ProtectionStopped.</span></span>
<span data-ttu-id="81c39-158">A proteção está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="81c39-158">Protection is disabled.</span></span>

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

### <span data-ttu-id="81c39-159">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="81c39-159">-ProtectionStatus</span></span>

<span data-ttu-id="81c39-160">Especifica o status geral da proteção de um item no contêiner.</span><span class="sxs-lookup"><span data-stu-id="81c39-160">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="81c39-161">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="81c39-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81c39-162">Bom</span><span class="sxs-lookup"><span data-stu-id="81c39-162">Healthy</span></span>
- <span data-ttu-id="81c39-163">Não íntegro</span><span class="sxs-lookup"><span data-stu-id="81c39-163">Unhealthy</span></span>

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

### <span data-ttu-id="81c39-164">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="81c39-164">-VaultId</span></span>

<span data-ttu-id="81c39-165">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="81c39-165">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="81c39-166">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="81c39-166">-WorkloadType</span></span>

<span data-ttu-id="81c39-167">Especifica o tipo de carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="81c39-167">Specifies the workload type.</span></span>
<span data-ttu-id="81c39-168">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="81c39-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81c39-169">AzureVM</span><span class="sxs-lookup"><span data-stu-id="81c39-169">AzureVM</span></span>
- <span data-ttu-id="81c39-170">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="81c39-170">AzureSQLDatabase</span></span>
- <span data-ttu-id="81c39-171">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="81c39-171">AzureFiles</span></span>
- <span data-ttu-id="81c39-172">SERVIÇO</span><span class="sxs-lookup"><span data-stu-id="81c39-172">MSSQL</span></span>

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

### <span data-ttu-id="81c39-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c39-173">CommonParameters</span></span>
<span data-ttu-id="81c39-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81c39-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c39-175">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81c39-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c39-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81c39-176">INPUTS</span></span>

### <span data-ttu-id="81c39-177">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="81c39-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="81c39-178">System. String</span><span class="sxs-lookup"><span data-stu-id="81c39-178">System.String</span></span>

## <span data-ttu-id="81c39-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81c39-179">OUTPUTS</span></span>

### <span data-ttu-id="81c39-180">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="81c39-180">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="81c39-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81c39-181">NOTES</span></span>

## <span data-ttu-id="81c39-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81c39-182">RELATED LINKS</span></span>

[<span data-ttu-id="81c39-183">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="81c39-183">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="81c39-184">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="81c39-184">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="81c39-185">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="81c39-185">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="81c39-186">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="81c39-186">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
