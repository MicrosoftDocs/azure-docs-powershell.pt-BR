---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429685"
---
# <span data-ttu-id="61fb5-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="61fb5-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="61fb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="61fb5-103">Esse comando cria a configuração de recuperação de um item em backup, como SQL DB.</span><span class="sxs-lookup"><span data-stu-id="61fb5-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="61fb5-104">O objeto de configuração armazena todos os detalhes, como o modo de recuperação, destinos de destino para os parâmetros específicos para restauração e aplicativo, como caminhos físicos de destino para SQL.</span><span class="sxs-lookup"><span data-stu-id="61fb5-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="61fb5-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61fb5-105">SYNTAX</span></span>

### <span data-ttu-id="61fb5-106">RpParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="61fb5-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61fb5-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="61fb5-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61fb5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61fb5-108">DESCRIPTION</span></span>
<span data-ttu-id="61fb5-109">O comando retorna uma configuração de recuperação para itens AzureWorkload que é passado para o cmdlet Restore.</span><span class="sxs-lookup"><span data-stu-id="61fb5-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="61fb5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61fb5-110">EXAMPLES</span></span>

### <span data-ttu-id="61fb5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61fb5-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="61fb5-112">O primeiro cmdlet é usado para obter o objeto de ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="61fb5-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="61fb5-113">O segundo cmdlet cria um plano de recuperação para uma restauração de local original.</span><span class="sxs-lookup"><span data-stu-id="61fb5-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="61fb5-114">O terceiro cmdlet cria um plano de recuperação para uma restauração de local alternativo.</span><span class="sxs-lookup"><span data-stu-id="61fb5-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="61fb5-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="61fb5-115">Example 2</span></span>

<span data-ttu-id="61fb5-116">Esse comando cria a configuração de recuperação de um item em backup, como SQL DB.</span><span class="sxs-lookup"><span data-stu-id="61fb5-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="61fb5-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="61fb5-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="61fb5-118">OS</span><span class="sxs-lookup"><span data-stu-id="61fb5-118">PARAMETERS</span></span>

### <span data-ttu-id="61fb5-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="61fb5-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="61fb5-120">Especifica que o banco de banco de backup deve ser restaurado em outro servidor selecionado.</span><span class="sxs-lookup"><span data-stu-id="61fb5-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="61fb5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61fb5-121">-DefaultProfile</span></span>
<span data-ttu-id="61fb5-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61fb5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61fb5-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="61fb5-123">-FilePath</span></span>
<span data-ttu-id="61fb5-124">Especifica o filePath que é usado para a operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="61fb5-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="61fb5-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="61fb5-125">-FromFull</span></span>
<span data-ttu-id="61fb5-126">Especifica a RecoveryPoint completa à qual os backups de log serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="61fb5-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="61fb5-127">-Item</span><span class="sxs-lookup"><span data-stu-id="61fb5-127">-Item</span></span>
<span data-ttu-id="61fb5-128">Especifica o item de backup no qual a operação de restauração está sendo realizada.</span><span class="sxs-lookup"><span data-stu-id="61fb5-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="61fb5-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="61fb5-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="61fb5-130">Especifica que o banco de dados de backup deve ser substituído pelas informações de banco de dados presentes no ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="61fb5-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="61fb5-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="61fb5-131">-PointInTime</span></span>
<span data-ttu-id="61fb5-132">Hora de término do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="61fb5-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="61fb5-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="61fb5-133">-RecoveryPoint</span></span>
<span data-ttu-id="61fb5-134">Objeto de ponto de recuperação a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="61fb5-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="61fb5-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="61fb5-135">-RestoreAsFiles</span></span>
<span data-ttu-id="61fb5-136">Especifica a restauração do banco de dados como arquivos em um computador.</span><span class="sxs-lookup"><span data-stu-id="61fb5-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="61fb5-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="61fb5-137">-TargetContainer</span></span>
<span data-ttu-id="61fb5-138">Especifica o computador de destino em que os arquivos de BD precisam ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="61fb5-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="61fb5-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="61fb5-139">-TargetItem</span></span>
<span data-ttu-id="61fb5-140">Especifica o destino no qual o banco de BD precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="61fb5-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="61fb5-141">Para restaurações do SQL, ele precisa ter apenas SQLInstance do tipo de item de proteção.</span><span class="sxs-lookup"><span data-stu-id="61fb5-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="61fb5-142">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="61fb5-142">-VaultId</span></span>
<span data-ttu-id="61fb5-143">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="61fb5-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="61fb5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61fb5-144">CommonParameters</span></span>
<span data-ttu-id="61fb5-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61fb5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61fb5-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61fb5-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61fb5-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61fb5-147">INPUTS</span></span>

### <span data-ttu-id="61fb5-148">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="61fb5-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="61fb5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="61fb5-149">System.String</span></span>

## <span data-ttu-id="61fb5-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61fb5-150">OUTPUTS</span></span>

### <span data-ttu-id="61fb5-151">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="61fb5-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="61fb5-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61fb5-152">NOTES</span></span>

## <span data-ttu-id="61fb5-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61fb5-153">RELATED LINKS</span></span>
