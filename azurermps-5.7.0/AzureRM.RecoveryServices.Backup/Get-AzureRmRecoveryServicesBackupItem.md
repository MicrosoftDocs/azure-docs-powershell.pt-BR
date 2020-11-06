---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9b836a4c4c056699e2c74bcb4d5b373f5bfe170e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427501"
---
# <span data-ttu-id="2b6d5-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2b6d5-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="2b6d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b6d5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6d5-103">Obtém os itens de um contêiner no backup.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b6d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b6d5-104">SYNTAX</span></span>

### <span data-ttu-id="2b6d5-105">GetItemsForContainer (padrão)</span><span class="sxs-lookup"><span data-stu-id="2b6d5-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b6d5-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="2b6d5-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b6d5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b6d5-107">DESCRIPTION</span></span>
<span data-ttu-id="2b6d5-108">O cmdlet **Get-AzureRmRecoveryServicesBackupItem** Obtém os itens em um contêiner ou um valor no Azure backup e o status de proteção dos itens.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="2b6d5-109">Um contêiner que está registrado para um cofre de serviços de recuperação do Azure pode ter um ou mais itens que podem ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="2b6d5-110">Para máquinas virtuais do Azure, pode haver apenas um item de backup no contêiner da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="2b6d5-111">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2b6d5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b6d5-112">EXAMPLES</span></span>

### <span data-ttu-id="2b6d5-113">Exemplo 1: obter um item de um contêiner de backup</span><span class="sxs-lookup"><span data-stu-id="2b6d5-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="2b6d5-114">O primeiro comando obtém o contêiner do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="2b6d5-115">O segundo comando obtém o item de backup chamado V2VM em $Container e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="2b6d5-116">OS</span><span class="sxs-lookup"><span data-stu-id="2b6d5-116">PARAMETERS</span></span>

### <span data-ttu-id="2b6d5-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="2b6d5-117">-BackupManagementType</span></span>
<span data-ttu-id="2b6d5-118">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="2b6d5-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2b6d5-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b6d5-120">AzureVM</span><span class="sxs-lookup"><span data-stu-id="2b6d5-120">AzureVM</span></span> 
- <span data-ttu-id="2b6d5-121">Marte</span><span class="sxs-lookup"><span data-stu-id="2b6d5-121">MARS</span></span> 
- <span data-ttu-id="2b6d5-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="2b6d5-122">SCDPM</span></span> 
- <span data-ttu-id="2b6d5-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="2b6d5-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6d5-124">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="2b6d5-124">-Container</span></span>
<span data-ttu-id="2b6d5-125">Especifica um objeto de contêiner do qual este cmdlet obtém itens de backup.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="2b6d5-126">Para obter um **AzureRmRecoveryServicesBackupContainer** , use o cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: GetItemsForContainer
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b6d5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6d5-127">-DefaultProfile</span></span>
<span data-ttu-id="2b6d5-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6d5-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b6d5-129">-Name</span></span>
<span data-ttu-id="2b6d5-130">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-130">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6d5-131">-Protectionstate</span><span class="sxs-lookup"><span data-stu-id="2b6d5-131">-ProtectionState</span></span>
<span data-ttu-id="2b6d5-132">Especifica o estado de proteção.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-132">Specifies the state of protection.</span></span>
<span data-ttu-id="2b6d5-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2b6d5-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b6d5-134">IRPending.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-134">IRPending.</span></span>
<span data-ttu-id="2b6d5-135">A sincronização inicial ainda não começou e ainda não há um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-135">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="2b6d5-136">Protegida.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-136">Protected.</span></span>
<span data-ttu-id="2b6d5-137">A proteção está em andamento.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-137">Protection is ongoing.</span></span> 
- <span data-ttu-id="2b6d5-138">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-138">ProtectionError.</span></span>
<span data-ttu-id="2b6d5-139">Há um erro de proteção.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-139">There is a protection error.</span></span>
- <span data-ttu-id="2b6d5-140">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-140">ProtectionStopped.</span></span>
<span data-ttu-id="2b6d5-141">A proteção está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-141">Protection is disabled.</span></span>

```yaml
Type: ItemProtectionState
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6d5-142">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="2b6d5-142">-ProtectionStatus</span></span>
<span data-ttu-id="2b6d5-143">Especifica o status geral da proteção de um item no contêiner.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-143">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="2b6d5-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2b6d5-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b6d5-145">Bom</span><span class="sxs-lookup"><span data-stu-id="2b6d5-145">Healthy</span></span>
- <span data-ttu-id="2b6d5-146">Não íntegro</span><span class="sxs-lookup"><span data-stu-id="2b6d5-146">Unhealthy</span></span>

```yaml
Type: ItemProtectionStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6d5-147">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="2b6d5-147">-WorkloadType</span></span>
<span data-ttu-id="2b6d5-148">Especifica o tipo de carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-148">Specifies the workload type.</span></span> <span data-ttu-id="2b6d5-149">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2b6d5-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b6d5-150">AzureVM</span><span class="sxs-lookup"><span data-stu-id="2b6d5-150">AzureVM</span></span> 
- <span data-ttu-id="2b6d5-151">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="2b6d5-151">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6d5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6d5-152">CommonParameters</span></span>
<span data-ttu-id="2b6d5-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6d5-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b6d5-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6d5-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b6d5-155">INPUTS</span></span>

### <span data-ttu-id="2b6d5-156">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2b6d5-156">None</span></span>
<span data-ttu-id="2b6d5-157">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2b6d5-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b6d5-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b6d5-158">OUTPUTS</span></span>

### <span data-ttu-id="2b6d5-159">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="2b6d5-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="2b6d5-160">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase]</span><span class="sxs-lookup"><span data-stu-id="2b6d5-160">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="2b6d5-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b6d5-161">NOTES</span></span>

## <span data-ttu-id="2b6d5-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b6d5-162">RELATED LINKS</span></span>

[<span data-ttu-id="2b6d5-163">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2b6d5-163">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="2b6d5-164">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2b6d5-164">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="2b6d5-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2b6d5-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="2b6d5-166">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2b6d5-166">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


