---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: a1037f742fab47ae84edae6e1558e313e563c25a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609758"
---
# <span data-ttu-id="bc214-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="bc214-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="bc214-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc214-102">SYNOPSIS</span></span>
<span data-ttu-id="bc214-103">Obtém os itens de um contêiner no backup.</span><span class="sxs-lookup"><span data-stu-id="bc214-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc214-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc214-104">SYNTAX</span></span>

### <span data-ttu-id="bc214-105">GetItemsForContainer (padrão)</span><span class="sxs-lookup"><span data-stu-id="bc214-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc214-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="bc214-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc214-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="bc214-107">GetItemsForPolicy</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc214-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc214-108">DESCRIPTION</span></span>
<span data-ttu-id="bc214-109">O cmdlet **Get-AzureRmRecoveryServicesBackupItem** Obtém os itens em um contêiner ou um valor no Azure backup e o status de proteção dos itens.</span><span class="sxs-lookup"><span data-stu-id="bc214-109">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="bc214-110">Um contêiner que está registrado para um cofre de serviços de recuperação do Azure pode ter um ou mais itens que podem ser protegidos.</span><span class="sxs-lookup"><span data-stu-id="bc214-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="bc214-111">Para máquinas virtuais do Azure, pode haver apenas um item de backup no contêiner da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bc214-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="bc214-112">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="bc214-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bc214-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc214-113">EXAMPLES</span></span>

### <span data-ttu-id="bc214-114">Exemplo 1: obter um item de um contêiner de backup</span><span class="sxs-lookup"><span data-stu-id="bc214-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="bc214-115">O primeiro comando obtém o contêiner do tipo AzureVM e, em seguida, armazena-o na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="bc214-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="bc214-116">O segundo comando obtém o item de backup chamado V2VM em $Container e, em seguida, armazena-o na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="bc214-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="bc214-117">OS</span><span class="sxs-lookup"><span data-stu-id="bc214-117">PARAMETERS</span></span>

### <span data-ttu-id="bc214-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="bc214-118">-BackupManagementType</span></span>
<span data-ttu-id="bc214-119">Especifica o tipo de gerenciamento de backup.</span><span class="sxs-lookup"><span data-stu-id="bc214-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="bc214-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bc214-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc214-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="bc214-121">AzureVM</span></span> 
- <span data-ttu-id="bc214-122">Marte</span><span class="sxs-lookup"><span data-stu-id="bc214-122">MARS</span></span> 
- <span data-ttu-id="bc214-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="bc214-123">SCDPM</span></span> 
- <span data-ttu-id="bc214-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="bc214-124">AzureBackupServer</span></span> 
- <span data-ttu-id="bc214-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="bc214-125">AzureSQL</span></span>
- <span data-ttu-id="bc214-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="bc214-126">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc214-127">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="bc214-127">-Container</span></span>
<span data-ttu-id="bc214-128">Especifica um objeto de contêiner do qual este cmdlet obtém itens de backup.</span><span class="sxs-lookup"><span data-stu-id="bc214-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="bc214-129">Para obter um **AzureRmRecoveryServicesBackupContainer** , use o cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="bc214-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="bc214-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc214-130">-DefaultProfile</span></span>
<span data-ttu-id="bc214-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc214-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc214-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc214-132">-Name</span></span>
<span data-ttu-id="bc214-133">Especifica o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="bc214-133">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="bc214-134">-Política</span><span class="sxs-lookup"><span data-stu-id="bc214-134">-Policy</span></span>
<span data-ttu-id="bc214-135">Objeto de política de proteção.</span><span class="sxs-lookup"><span data-stu-id="bc214-135">Protection policy object.</span></span>

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

### <span data-ttu-id="bc214-136">-Protectionstate</span><span class="sxs-lookup"><span data-stu-id="bc214-136">-ProtectionState</span></span>
<span data-ttu-id="bc214-137">Especifica o estado de proteção.</span><span class="sxs-lookup"><span data-stu-id="bc214-137">Specifies the state of protection.</span></span>
<span data-ttu-id="bc214-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bc214-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc214-139">IRPending.</span><span class="sxs-lookup"><span data-stu-id="bc214-139">IRPending.</span></span>
<span data-ttu-id="bc214-140">A sincronização inicial ainda não começou e ainda não há um ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="bc214-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="bc214-141">Protegida.</span><span class="sxs-lookup"><span data-stu-id="bc214-141">Protected.</span></span>
<span data-ttu-id="bc214-142">A proteção está em andamento.</span><span class="sxs-lookup"><span data-stu-id="bc214-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="bc214-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="bc214-143">ProtectionError.</span></span>
<span data-ttu-id="bc214-144">Há um erro de proteção.</span><span class="sxs-lookup"><span data-stu-id="bc214-144">There is a protection error.</span></span>
- <span data-ttu-id="bc214-145">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="bc214-145">ProtectionStopped.</span></span>
<span data-ttu-id="bc214-146">A proteção está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="bc214-146">Protection is disabled.</span></span>

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

### <span data-ttu-id="bc214-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="bc214-147">-ProtectionStatus</span></span>
<span data-ttu-id="bc214-148">Especifica o status geral da proteção de um item no contêiner.</span><span class="sxs-lookup"><span data-stu-id="bc214-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="bc214-149">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bc214-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc214-150">Bom</span><span class="sxs-lookup"><span data-stu-id="bc214-150">Healthy</span></span>
- <span data-ttu-id="bc214-151">Não íntegro</span><span class="sxs-lookup"><span data-stu-id="bc214-151">Unhealthy</span></span>

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

### <span data-ttu-id="bc214-152">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="bc214-152">-VaultId</span></span>
<span data-ttu-id="bc214-153">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="bc214-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="bc214-154">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="bc214-154">-WorkloadType</span></span>
<span data-ttu-id="bc214-155">Especifica o tipo de carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bc214-155">Specifies the workload type.</span></span> <span data-ttu-id="bc214-156">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bc214-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc214-157">AzureVM</span><span class="sxs-lookup"><span data-stu-id="bc214-157">AzureVM</span></span> 
- <span data-ttu-id="bc214-158">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="bc214-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="bc214-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="bc214-159">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc214-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc214-160">CommonParameters</span></span>
<span data-ttu-id="bc214-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc214-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc214-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc214-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc214-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc214-163">INPUTS</span></span>

### <span data-ttu-id="bc214-164">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="bc214-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="bc214-165">System. String</span><span class="sxs-lookup"><span data-stu-id="bc214-165">System.String</span></span>
<span data-ttu-id="bc214-166">Parâmetros: Vaultid (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bc214-166">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="bc214-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc214-167">OUTPUTS</span></span>

### <span data-ttu-id="bc214-168">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. dobase</span><span class="sxs-lookup"><span data-stu-id="bc214-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="bc214-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc214-169">NOTES</span></span>

## <span data-ttu-id="bc214-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc214-170">RELATED LINKS</span></span>

[<span data-ttu-id="bc214-171">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="bc214-171">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="bc214-172">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="bc214-172">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="bc214-173">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="bc214-173">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="bc214-174">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="bc214-174">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


