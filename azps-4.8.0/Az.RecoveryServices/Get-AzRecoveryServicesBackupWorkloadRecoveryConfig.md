---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112725"
---
# <span data-ttu-id="cc998-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="cc998-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="cc998-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc998-102">SYNOPSIS</span></span>
<span data-ttu-id="cc998-103">Esse comando cria a configuração de recuperação de um item em backup, como SQL DB.</span><span class="sxs-lookup"><span data-stu-id="cc998-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="cc998-104">O objeto de configuração armazena todos os detalhes, como o modo de recuperação, destinos de destino para os parâmetros específicos para restauração e aplicativo, como caminhos físicos de destino para SQL.</span><span class="sxs-lookup"><span data-stu-id="cc998-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="cc998-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc998-105">SYNTAX</span></span>

### <span data-ttu-id="cc998-106">RpParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc998-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc998-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc998-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc998-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc998-108">DESCRIPTION</span></span>
<span data-ttu-id="cc998-109">O comando retorna uma configuração de recuperação para itens AzureWorkload que é passado para o cmdlet Restore.</span><span class="sxs-lookup"><span data-stu-id="cc998-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="cc998-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc998-110">EXAMPLES</span></span>

### <span data-ttu-id="cc998-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc998-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="cc998-112">O primeiro cmdlet é usado para obter o objeto de ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="cc998-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="cc998-113">O segundo cmdlet cria um plano de recuperação para uma restauração de local original.</span><span class="sxs-lookup"><span data-stu-id="cc998-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="cc998-114">O terceiro cmdlet cria um plano de recuperação para uma restauração de local alternativo.</span><span class="sxs-lookup"><span data-stu-id="cc998-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="cc998-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cc998-115">Example 2</span></span>

<span data-ttu-id="cc998-116">Esse comando cria a configuração de recuperação de um item em backup, como SQL DB.</span><span class="sxs-lookup"><span data-stu-id="cc998-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="cc998-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="cc998-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="cc998-118">OS</span><span class="sxs-lookup"><span data-stu-id="cc998-118">PARAMETERS</span></span>

### <span data-ttu-id="cc998-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="cc998-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="cc998-120">Especifica que o banco de banco de backup deve ser restaurado em outro servidor selecionado.</span><span class="sxs-lookup"><span data-stu-id="cc998-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="cc998-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc998-121">-DefaultProfile</span></span>
<span data-ttu-id="cc998-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc998-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc998-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="cc998-123">-FilePath</span></span>
<span data-ttu-id="cc998-124">Especifica o filePath que é usado para a operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="cc998-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="cc998-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="cc998-125">-FromFull</span></span>
<span data-ttu-id="cc998-126">Especifica a RecoveryPoint completa à qual os backups de log serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="cc998-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="cc998-127">-Item</span><span class="sxs-lookup"><span data-stu-id="cc998-127">-Item</span></span>
<span data-ttu-id="cc998-128">Especifica o item de backup no qual a operação de restauração está sendo realizada.</span><span class="sxs-lookup"><span data-stu-id="cc998-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="cc998-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="cc998-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="cc998-130">Especifica que o banco de dados de backup deve ser substituído pelas informações de banco de dados presentes no ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="cc998-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="cc998-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="cc998-131">-PointInTime</span></span>
<span data-ttu-id="cc998-132">Hora de término do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="cc998-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="cc998-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="cc998-133">-RecoveryPoint</span></span>
<span data-ttu-id="cc998-134">Objeto de ponto de recuperação a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="cc998-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="cc998-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="cc998-135">-RestoreAsFiles</span></span>
<span data-ttu-id="cc998-136">Especifica a restauração do banco de dados como arquivos em um computador.</span><span class="sxs-lookup"><span data-stu-id="cc998-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="cc998-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="cc998-137">-TargetContainer</span></span>
<span data-ttu-id="cc998-138">Especifica o computador de destino em que os arquivos de BD precisam ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="cc998-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="cc998-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="cc998-139">-TargetItem</span></span>
<span data-ttu-id="cc998-140">Especifica o destino no qual o banco de BD precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="cc998-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="cc998-141">Para restaurações do SQL, ele precisa ter apenas SQLInstance do tipo de item de proteção.</span><span class="sxs-lookup"><span data-stu-id="cc998-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="cc998-142">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="cc998-142">-VaultId</span></span>
<span data-ttu-id="cc998-143">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="cc998-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="cc998-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc998-144">CommonParameters</span></span>
<span data-ttu-id="cc998-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc998-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc998-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc998-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc998-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc998-147">INPUTS</span></span>

### <span data-ttu-id="cc998-148">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="cc998-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="cc998-149">System. String</span><span class="sxs-lookup"><span data-stu-id="cc998-149">System.String</span></span>

## <span data-ttu-id="cc998-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc998-150">OUTPUTS</span></span>

### <span data-ttu-id="cc998-151">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="cc998-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="cc998-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc998-152">NOTES</span></span>

## <span data-ttu-id="cc998-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc998-153">RELATED LINKS</span></span>
