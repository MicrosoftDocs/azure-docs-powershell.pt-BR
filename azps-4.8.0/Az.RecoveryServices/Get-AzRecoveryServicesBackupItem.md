---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 358d3da36996c9b020db3a805889b7098b9c36ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114702"
---
# <span data-ttu-id="35baf-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="35baf-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="35baf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35baf-102">SYNOPSIS</span></span>

<span data-ttu-id="35baf-103">Obtém os itens de um contêiner no backup.</span><span class="sxs-lookup"><span data-stu-id="35baf-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="35baf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35baf-104">SYNTAX</span></span>

### <span data-ttu-id="35baf-105">GetItemsForContainer (padrão)</span><span class="sxs-lookup"><span data-stu-id="35baf-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35baf-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="35baf-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35baf-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="35baf-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35baf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35baf-108">DESCRIPTION</span></span>

<span data-ttu-id="35baf-109">O cmdlet **Get-AzRecoveryServicesBackupItem** Obtém a lista de itens protegidos em um contêiner e o status de proteção dos itens.</span><span class="sxs-lookup"><span data-stu-id="35baf-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="35baf-110">Um contêiner que está registrado para um cofre de serviços de recuperação do Azure pode ter um ou mais itens que podem ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="35baf-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="35baf-111">Para máquinas virtuais do Azure, pode haver apenas um item de backup no contêiner da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35baf-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="35baf-112">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="35baf-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="35baf-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35baf-113">EXAMPLES</span></span>

### <span data-ttu-id="35baf-114">Exemplo 1: obter um item de um contêiner de backup</span><span class="sxs-lookup"><span data-stu-id="35baf-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="35baf-115">O primeiro comando obtém o contêiner do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="35baf-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="35baf-116">O segundo comando obtém o item de backup chamado V2VM em $Container e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="35baf-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="35baf-117">Exemplo 2: obter um item de compartilhamento de arquivos do Azure de FriendlyName</span><span class="sxs-lookup"><span data-stu-id="35baf-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="35baf-118">O primeiro comando obtém o contêiner do tipo AzureStorage e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="35baf-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="35baf-119">O segundo comando obtém o item de backup cujo FriendlyName corresponde ao valor passado no parâmetro FriendlyName e o armazena na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="35baf-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="35baf-120">Usar o parâmetro FriendlyName pode resultar em retornar mais de um compartilhamento de arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="35baf-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="35baf-121">Nesses casos, execute o cmdlet passando o valor do parâmetro-Name como a propriedade Name retornada no conjunto de resultados de $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="35baf-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="35baf-122">OS</span><span class="sxs-lookup"><span data-stu-id="35baf-122">PARAMETERS</span></span>

### <span data-ttu-id="35baf-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="35baf-123">-BackupManagementType</span></span>

<span data-ttu-id="35baf-124">A classe de recursos que estão sendo protegidos.</span><span class="sxs-lookup"><span data-stu-id="35baf-124">The class of resources being protected.</span></span> <span data-ttu-id="35baf-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35baf-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35baf-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="35baf-126">AzureVM</span></span>
- <span data-ttu-id="35baf-127">MAB</span><span class="sxs-lookup"><span data-stu-id="35baf-127">MAB</span></span>
- <span data-ttu-id="35baf-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="35baf-128">AzureStorage</span></span>
- <span data-ttu-id="35baf-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="35baf-129">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35baf-130">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="35baf-130">-Container</span></span>

<span data-ttu-id="35baf-131">Especifica um objeto de contêiner do qual este cmdlet obtém itens de backup.</span><span class="sxs-lookup"><span data-stu-id="35baf-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="35baf-132">Para obter um **AzureRmRecoveryServicesBackupContainer** , use o cmdlet **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="35baf-132">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="35baf-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35baf-133">-DefaultProfile</span></span>

<span data-ttu-id="35baf-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35baf-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35baf-135">-Deletestate</span><span class="sxs-lookup"><span data-stu-id="35baf-135">-DeleteState</span></span>
<span data-ttu-id="35baf-136">Especifica o deletestate do item os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35baf-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35baf-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="35baf-137">ToBeDeleted</span></span>
- <span data-ttu-id="35baf-138">Não excluído</span><span class="sxs-lookup"><span data-stu-id="35baf-138">NotDeleted</span></span>

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

### <span data-ttu-id="35baf-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="35baf-139">-FriendlyName</span></span>
<span data-ttu-id="35baf-140">FriendlyName do item de backup</span><span class="sxs-lookup"><span data-stu-id="35baf-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="35baf-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="35baf-141">-Name</span></span>

<span data-ttu-id="35baf-142">Especifica o nome do item de backup.</span><span class="sxs-lookup"><span data-stu-id="35baf-142">Specifies the name of backup item.</span></span> <span data-ttu-id="35baf-143">Para compartilhamento de arquivos, especifique a ID exclusiva do compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="35baf-143">For file share, specify the unique ID of protected file share.</span></span>

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

### <span data-ttu-id="35baf-144">-Política</span><span class="sxs-lookup"><span data-stu-id="35baf-144">-Policy</span></span>

<span data-ttu-id="35baf-145">Objeto de política de proteção.</span><span class="sxs-lookup"><span data-stu-id="35baf-145">Protection policy object.</span></span>

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

### <span data-ttu-id="35baf-146">-Protectionstate</span><span class="sxs-lookup"><span data-stu-id="35baf-146">-ProtectionState</span></span>

<span data-ttu-id="35baf-147">Especifica o estado de proteção.</span><span class="sxs-lookup"><span data-stu-id="35baf-147">Specifies the state of protection.</span></span>
<span data-ttu-id="35baf-148">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35baf-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35baf-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="35baf-149">IRPending.</span></span>
<span data-ttu-id="35baf-150">A sincronização inicial ainda não começou e ainda não há um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="35baf-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="35baf-151">Protegida.</span><span class="sxs-lookup"><span data-stu-id="35baf-151">Protected.</span></span>
<span data-ttu-id="35baf-152">A proteção está em andamento.</span><span class="sxs-lookup"><span data-stu-id="35baf-152">Protection is ongoing.</span></span>
- <span data-ttu-id="35baf-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="35baf-153">ProtectionError.</span></span>
<span data-ttu-id="35baf-154">Há um erro de proteção.</span><span class="sxs-lookup"><span data-stu-id="35baf-154">There is a protection error.</span></span>
- <span data-ttu-id="35baf-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="35baf-155">ProtectionStopped.</span></span>
<span data-ttu-id="35baf-156">A proteção está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="35baf-156">Protection is disabled.</span></span>

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

### <span data-ttu-id="35baf-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="35baf-157">-ProtectionStatus</span></span>

<span data-ttu-id="35baf-158">Especifica o status geral da proteção de um item no contêiner.</span><span class="sxs-lookup"><span data-stu-id="35baf-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="35baf-159">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35baf-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35baf-160">Bom</span><span class="sxs-lookup"><span data-stu-id="35baf-160">Healthy</span></span>
- <span data-ttu-id="35baf-161">Não íntegro</span><span class="sxs-lookup"><span data-stu-id="35baf-161">Unhealthy</span></span>

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

### <span data-ttu-id="35baf-162">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="35baf-162">-VaultId</span></span>

<span data-ttu-id="35baf-163">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="35baf-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="35baf-164">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="35baf-164">-WorkloadType</span></span>

<span data-ttu-id="35baf-165">Tipo de carga de trabalho do recurso.</span><span class="sxs-lookup"><span data-stu-id="35baf-165">Workload type of the resource.</span></span> <span data-ttu-id="35baf-166">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35baf-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35baf-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="35baf-167">AzureVM</span></span>
- <span data-ttu-id="35baf-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="35baf-168">AzureFiles</span></span>
- <span data-ttu-id="35baf-169">SERVIÇO</span><span class="sxs-lookup"><span data-stu-id="35baf-169">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35baf-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35baf-170">CommonParameters</span></span>
<span data-ttu-id="35baf-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35baf-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35baf-172">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35baf-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35baf-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35baf-173">INPUTS</span></span>

### <span data-ttu-id="35baf-174">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="35baf-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="35baf-175">System. String</span><span class="sxs-lookup"><span data-stu-id="35baf-175">System.String</span></span>

## <span data-ttu-id="35baf-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35baf-176">OUTPUTS</span></span>

### <span data-ttu-id="35baf-177">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="35baf-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="35baf-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35baf-178">NOTES</span></span>

## <span data-ttu-id="35baf-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35baf-179">RELATED LINKS</span></span>

[<span data-ttu-id="35baf-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="35baf-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="35baf-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="35baf-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="35baf-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="35baf-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="35baf-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="35baf-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
