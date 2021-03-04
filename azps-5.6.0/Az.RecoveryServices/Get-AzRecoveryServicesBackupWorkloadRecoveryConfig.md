---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: d608b4265435041a918ba71cdd68ae00892bcc20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886321"
---
# <span data-ttu-id="35832-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="35832-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="35832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35832-102">SYNOPSIS</span></span>
<span data-ttu-id="35832-103">Este comando constrói a configuração de recuperação de um item com backup, como SQL DB.</span><span class="sxs-lookup"><span data-stu-id="35832-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="35832-104">O objeto de configuração armazena todos os detalhes, como o modo de recuperação, destinos de destino para os parâmetros específicos de restauração e aplicativo, como caminhos físicos de destino para SQL.</span><span class="sxs-lookup"><span data-stu-id="35832-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="35832-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="35832-105">SYNTAX</span></span>

### <span data-ttu-id="35832-106">RpParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="35832-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35832-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="35832-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35832-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="35832-108">DESCRIPTION</span></span>
<span data-ttu-id="35832-109">O comando retorna uma configuração de recuperação para itens do AzureWorkload que é passado para o cmdlet de restauração.</span><span class="sxs-lookup"><span data-stu-id="35832-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="35832-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35832-110">EXAMPLES</span></span>

### <span data-ttu-id="35832-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="35832-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="35832-112">O primeiro cmdlet é usado para obter o objeto Ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="35832-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="35832-113">O segundo cmdlet cria um plano de recuperação para uma restauração de local original.</span><span class="sxs-lookup"><span data-stu-id="35832-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="35832-114">O terceiro cmdlet THe cria um plano de recuperação para uma restauração de local alternativo.</span><span class="sxs-lookup"><span data-stu-id="35832-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="35832-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="35832-115">Example 2</span></span>

<span data-ttu-id="35832-116">Este comando constrói a configuração de recuperação de um item com backup, como SQL DB.</span><span class="sxs-lookup"><span data-stu-id="35832-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="35832-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="35832-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="35832-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="35832-118">PARAMETERS</span></span>

### <span data-ttu-id="35832-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="35832-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="35832-120">Especifica que o DB com backup deve ser restaurado para outro servidor selecionado.</span><span class="sxs-lookup"><span data-stu-id="35832-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35832-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35832-121">-DefaultProfile</span></span>
<span data-ttu-id="35832-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35832-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35832-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="35832-123">-FilePath</span></span>
<span data-ttu-id="35832-124">Especifica o filepath usado para a operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="35832-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="35832-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="35832-125">-FromFull</span></span>
<span data-ttu-id="35832-126">Especifica o Full RecoveryPoint ao qual os backups de Log serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="35832-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35832-127">-Item</span><span class="sxs-lookup"><span data-stu-id="35832-127">-Item</span></span>
<span data-ttu-id="35832-128">Especifica o item de backup no qual a operação de restauração está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="35832-128">Specifies the backup item on which the restore operation is being performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35832-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="35832-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="35832-130">Especifica que o DB com backup deve ser substituído com as informações db presentes no ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="35832-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35832-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="35832-131">-PointInTime</span></span>
<span data-ttu-id="35832-132">Tempo de término do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="35832-132">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.DateTime
Parameter Sets: LogChainParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35832-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="35832-133">-RecoveryPoint</span></span>
<span data-ttu-id="35832-134">Objeto ponto de recuperação a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="35832-134">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: RpParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35832-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="35832-135">-RestoreAsFiles</span></span>
<span data-ttu-id="35832-136">Especifica a restauração do banco de dados como arquivos em um computador.</span><span class="sxs-lookup"><span data-stu-id="35832-136">Specifies to restore Database as files in a machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35832-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="35832-137">-TargetContainer</span></span>
<span data-ttu-id="35832-138">Especifica o computador de destino no qual os Arquivos DB precisam ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="35832-138">Specifies the target machine on which DB Files need to be restored.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35832-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="35832-139">-TargetItem</span></span>
<span data-ttu-id="35832-140">Especifica o destino no qual o DB precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="35832-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="35832-141">Para SQL restaurações, ele precisa ser apenas do tipo de item protegido SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="35832-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35832-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="35832-142">-VaultId</span></span>
<span data-ttu-id="35832-143">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="35832-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="35832-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35832-144">CommonParameters</span></span>
<span data-ttu-id="35832-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35832-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35832-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35832-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35832-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35832-147">INPUTS</span></span>

### <span data-ttu-id="35832-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="35832-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="35832-149">System.String</span><span class="sxs-lookup"><span data-stu-id="35832-149">System.String</span></span>

## <span data-ttu-id="35832-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="35832-150">OUTPUTS</span></span>

### <span data-ttu-id="35832-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="35832-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="35832-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="35832-152">NOTES</span></span>

## <span data-ttu-id="35832-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35832-153">RELATED LINKS</span></span>
