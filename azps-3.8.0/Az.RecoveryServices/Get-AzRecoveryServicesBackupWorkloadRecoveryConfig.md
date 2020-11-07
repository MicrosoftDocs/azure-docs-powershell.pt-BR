---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6033421b9a78e7cb531d2a33eabba1e97010c4f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944720"
---
# <span data-ttu-id="7574f-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="7574f-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="7574f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7574f-102">SYNOPSIS</span></span>
<span data-ttu-id="7574f-103">Esse comando cria a configuração de recuperação de um item em backup, como SQL DB.</span><span class="sxs-lookup"><span data-stu-id="7574f-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="7574f-104">O objeto de configuração armazena todos os detalhes, como o modo de recuperação, destinos de destino para os parâmetros específicos para restauração e aplicativo, como caminhos físicos de destino para SQL.</span><span class="sxs-lookup"><span data-stu-id="7574f-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="7574f-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7574f-105">SYNTAX</span></span>

### <span data-ttu-id="7574f-106">RpParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7574f-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7574f-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="7574f-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7574f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7574f-108">DESCRIPTION</span></span>
<span data-ttu-id="7574f-109">O comando retorna uma configuração de recuperação para itens AzureWorkload que é passado para o cmdlet Restore.</span><span class="sxs-lookup"><span data-stu-id="7574f-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="7574f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7574f-110">EXAMPLES</span></span>

### <span data-ttu-id="7574f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7574f-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="7574f-112">O primeiro cmdlet é usado para obter o objeto de ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7574f-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="7574f-113">O segundo cmdlet cria um plano de recuperação para uma restauração de local original.</span><span class="sxs-lookup"><span data-stu-id="7574f-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="7574f-114">O terceiro cmdlet cria um plano de recuperação para uma restauração de local alternativo.</span><span class="sxs-lookup"><span data-stu-id="7574f-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="7574f-115">OS</span><span class="sxs-lookup"><span data-stu-id="7574f-115">PARAMETERS</span></span>

### <span data-ttu-id="7574f-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="7574f-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="7574f-117">Especifica que o banco de dados de backup deve ser substituído pelas informações de banco de dados presentes no ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7574f-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="7574f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7574f-118">-DefaultProfile</span></span>
<span data-ttu-id="7574f-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7574f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7574f-120">-FilePath</span><span class="sxs-lookup"><span data-stu-id="7574f-120">-FilePath</span></span>
<span data-ttu-id="7574f-121">Especifica o filePath para a operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="7574f-121">Specifies the filepath for restore operation.</span></span>

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

### <span data-ttu-id="7574f-122">-FromFull</span><span class="sxs-lookup"><span data-stu-id="7574f-122">-FromFull</span></span>
<span data-ttu-id="7574f-123">Especifica a RecoveryPoint completa à qual os backups de log serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="7574f-123">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="7574f-124">-Item</span><span class="sxs-lookup"><span data-stu-id="7574f-124">-Item</span></span>
<span data-ttu-id="7574f-125">Especifica o item de backup no qual a operação de restauração está sendo realizada.</span><span class="sxs-lookup"><span data-stu-id="7574f-125">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="7574f-126">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="7574f-126">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="7574f-127">Especifica que o banco de dados de backup deve ser substituído pelas informações de banco de dados presentes no ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7574f-127">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="7574f-128">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="7574f-128">-PointInTime</span></span>
<span data-ttu-id="7574f-129">Hora de término do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="7574f-129">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="7574f-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="7574f-130">-RecoveryPoint</span></span>
<span data-ttu-id="7574f-131">Objeto de ponto de recuperação a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="7574f-131">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="7574f-132">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="7574f-132">-RestoreAsFiles</span></span>
<span data-ttu-id="7574f-133">Especifica a restauração do banco de dados como arquivos em um computador.</span><span class="sxs-lookup"><span data-stu-id="7574f-133">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="7574f-134">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="7574f-134">-TargetContainer</span></span>
<span data-ttu-id="7574f-135">Especifica o computador de destino em que os arquivos de BD precisam ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="7574f-135">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="7574f-136">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="7574f-136">-TargetItem</span></span>
<span data-ttu-id="7574f-137">Especifica o destino no qual o banco de BD precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="7574f-137">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="7574f-138">Para restaurações do SQL, ele precisa ter apenas SQLInstance do tipo de item de proteção.</span><span class="sxs-lookup"><span data-stu-id="7574f-138">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="7574f-139">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="7574f-139">-VaultId</span></span>
<span data-ttu-id="7574f-140">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7574f-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7574f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7574f-141">CommonParameters</span></span>
<span data-ttu-id="7574f-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7574f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7574f-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7574f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7574f-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7574f-144">INPUTS</span></span>

### <span data-ttu-id="7574f-145">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="7574f-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="7574f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7574f-146">System.String</span></span>

## <span data-ttu-id="7574f-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7574f-147">OUTPUTS</span></span>

### <span data-ttu-id="7574f-148">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="7574f-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="7574f-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7574f-149">NOTES</span></span>

## <span data-ttu-id="7574f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7574f-150">RELATED LINKS</span></span>
