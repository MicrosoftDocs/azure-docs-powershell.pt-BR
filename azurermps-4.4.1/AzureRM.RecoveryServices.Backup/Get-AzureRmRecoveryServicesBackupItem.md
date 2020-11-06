---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 03da361f8dd68d345782568dc243d4438cad1d77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610476"
---
# <span data-ttu-id="d1fb4-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d1fb4-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="d1fb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fb4-103">Obtém os itens de um contêiner no backup.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1fb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1fb4-104">SYNTAX</span></span>

### <span data-ttu-id="d1fb4-105">GetItemsForContainer (padrão)</span><span class="sxs-lookup"><span data-stu-id="d1fb4-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1fb4-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="d1fb4-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1fb4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1fb4-107">DESCRIPTION</span></span>
<span data-ttu-id="d1fb4-108">O cmdlet **Get-AzureRmRecoveryServicesBackupItem** Obtém os itens em um contêiner ou um valor no Azure backup e o status de proteção dos itens.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="d1fb4-109">Um contêiner que está registrado para um cofre de serviços de recuperação do Azure pode ter um ou mais itens que podem ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="d1fb4-110">Para máquinas virtuais do Azure, pode haver apenas um item de backup no contêiner da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="d1fb4-111">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d1fb4-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1fb4-112">EXAMPLES</span></span>

### <span data-ttu-id="d1fb4-113">Exemplo 1: obter um item de um contêiner de backup</span><span class="sxs-lookup"><span data-stu-id="d1fb4-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="d1fb4-114">O primeiro comando obtém o contêiner do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="d1fb4-115">O segundo comando obtém o item de backup chamado V2VM em $Container e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="d1fb4-116">OS</span><span class="sxs-lookup"><span data-stu-id="d1fb4-116">PARAMETERS</span></span>

### <span data-ttu-id="d1fb4-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d1fb4-117">-BackupManagementType</span></span>
<span data-ttu-id="d1fb4-118">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="d1fb4-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d1fb4-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1fb4-120">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d1fb4-120">AzureVM</span></span> 
- <span data-ttu-id="d1fb4-121">Marte</span><span class="sxs-lookup"><span data-stu-id="d1fb4-121">MARS</span></span> 
- <span data-ttu-id="d1fb4-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="d1fb4-122">SCDPM</span></span> 
- <span data-ttu-id="d1fb4-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="d1fb4-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1fb4-124">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="d1fb4-124">-Container</span></span>
<span data-ttu-id="d1fb4-125">Especifica um objeto de contêiner do qual este cmdlet obtém itens de backup.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="d1fb4-126">Para obter um **AzureRmRecoveryServicesBackupContainer** , use o cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="d1fb4-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1fb4-127">-Name</span></span>
<span data-ttu-id="d1fb4-128">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-128">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="d1fb4-129">-Protectionstate</span><span class="sxs-lookup"><span data-stu-id="d1fb4-129">-ProtectionState</span></span>
<span data-ttu-id="d1fb4-130">Especifica o estado de proteção.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-130">Specifies the state of protection.</span></span>
<span data-ttu-id="d1fb4-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d1fb4-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1fb4-132">IRPending.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-132">IRPending.</span></span>
<span data-ttu-id="d1fb4-133">A sincronização inicial ainda não começou e ainda não há um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-133">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="d1fb4-134">Protegida.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-134">Protected.</span></span>
<span data-ttu-id="d1fb4-135">A proteção está em andamento.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-135">Protection is ongoing.</span></span> 
- <span data-ttu-id="d1fb4-136">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-136">ProtectionError.</span></span>
<span data-ttu-id="d1fb4-137">Há um erro de proteção.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-137">There is a protection error.</span></span>
- <span data-ttu-id="d1fb4-138">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-138">ProtectionStopped.</span></span>
<span data-ttu-id="d1fb4-139">A proteção está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-139">Protection is disabled.</span></span>

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

### <span data-ttu-id="d1fb4-140">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="d1fb4-140">-ProtectionStatus</span></span>
<span data-ttu-id="d1fb4-141">Especifica o status geral da proteção de um item no contêiner.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-141">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="d1fb4-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d1fb4-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1fb4-143">Bom</span><span class="sxs-lookup"><span data-stu-id="d1fb4-143">Healthy</span></span>
- <span data-ttu-id="d1fb4-144">Não íntegro</span><span class="sxs-lookup"><span data-stu-id="d1fb4-144">Unhealthy</span></span>

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

### <span data-ttu-id="d1fb4-145">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="d1fb4-145">-WorkloadType</span></span>
<span data-ttu-id="d1fb4-146">Especifica o tipo de carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-146">Specifies the workload type.</span></span> <span data-ttu-id="d1fb4-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d1fb4-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1fb4-148">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d1fb4-148">AzureVM</span></span> 
- <span data-ttu-id="d1fb4-149">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="d1fb4-149">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1fb4-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1fb4-150">-DefaultProfile</span></span>
<span data-ttu-id="d1fb4-151">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1fb4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fb4-152">CommonParameters</span></span>
<span data-ttu-id="d1fb4-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1fb4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fb4-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1fb4-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fb4-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1fb4-155">INPUTS</span></span>

## <span data-ttu-id="d1fb4-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1fb4-156">OUTPUTS</span></span>

### <span data-ttu-id="d1fb4-157">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="d1fb4-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="d1fb4-158">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase]</span><span class="sxs-lookup"><span data-stu-id="d1fb4-158">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="d1fb4-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1fb4-159">NOTES</span></span>

## <span data-ttu-id="d1fb4-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1fb4-160">RELATED LINKS</span></span>

[<span data-ttu-id="d1fb4-161">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d1fb4-161">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="d1fb4-162">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d1fb4-162">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="d1fb4-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d1fb4-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="d1fb4-164">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d1fb4-164">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


