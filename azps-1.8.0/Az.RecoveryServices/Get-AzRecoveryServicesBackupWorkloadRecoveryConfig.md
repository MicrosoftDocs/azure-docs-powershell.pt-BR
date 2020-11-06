---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6b0f2e2c5b2e9579a92b2cee7387a19fda498fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599683"
---
# <span data-ttu-id="78c63-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="78c63-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="78c63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78c63-102">SYNOPSIS</span></span>
<span data-ttu-id="78c63-103">Esse comando cria a configuração de recuperação de um item em backup, como SQL DB.</span><span class="sxs-lookup"><span data-stu-id="78c63-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="78c63-104">O objeto de configuração armazena todos os detalhes, como o modo de recuperação, destinos de destino para os parâmetros específicos para restauração e aplicativo, como caminhos físicos de destino para SQL.</span><span class="sxs-lookup"><span data-stu-id="78c63-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="78c63-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78c63-105">SYNTAX</span></span>

### <span data-ttu-id="78c63-106">RpParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="78c63-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78c63-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="78c63-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78c63-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78c63-108">DESCRIPTION</span></span>
<span data-ttu-id="78c63-109">O comando retorna uma configuração de recuperação para itens AzureWorkload que é passado para o cmdlet Restore.</span><span class="sxs-lookup"><span data-stu-id="78c63-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="78c63-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78c63-110">EXAMPLES</span></span>

### <span data-ttu-id="78c63-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78c63-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="78c63-112">O primeiro cmdlet é usado para obter o objeto de ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="78c63-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="78c63-113">O segundo cmdlet cria um plano de recuperação para uma restauração de local original.</span><span class="sxs-lookup"><span data-stu-id="78c63-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="78c63-114">O terceiro cmdlet crreats um plano de recuperação para uma restauração de local alternativo.</span><span class="sxs-lookup"><span data-stu-id="78c63-114">THe third cmdlet crreats a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="78c63-115">OS</span><span class="sxs-lookup"><span data-stu-id="78c63-115">PARAMETERS</span></span>

### <span data-ttu-id="78c63-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="78c63-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="78c63-117">Especifica que o banco de dados de backup deve ser substituído pelas informações de banco de dados presentes no ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="78c63-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="78c63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c63-118">-DefaultProfile</span></span>
<span data-ttu-id="78c63-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78c63-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78c63-120">-Item</span><span class="sxs-lookup"><span data-stu-id="78c63-120">-Item</span></span>
<span data-ttu-id="78c63-121">Especifica o item de backup no qual a operação de restauração está sendo realizada.</span><span class="sxs-lookup"><span data-stu-id="78c63-121">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="78c63-122">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="78c63-122">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="78c63-123">Especifica que o banco de dados de backup deve ser substituído pelas informações de banco de dados presentes no ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="78c63-123">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="78c63-124">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="78c63-124">-PointInTime</span></span>
<span data-ttu-id="78c63-125">Hora de término do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="78c63-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="78c63-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="78c63-126">-RecoveryPoint</span></span>
<span data-ttu-id="78c63-127">Objeto de ponto de recuperação a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="78c63-127">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="78c63-128">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="78c63-128">-TargetItem</span></span>
<span data-ttu-id="78c63-129">Especifica o destino no qual o banco de BD precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="78c63-129">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="78c63-130">Para restaurações do SQL, ele precisa ter apenas SQLInstance do tipo de item de proteção.</span><span class="sxs-lookup"><span data-stu-id="78c63-130">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="78c63-131">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="78c63-131">-VaultId</span></span>
<span data-ttu-id="78c63-132">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="78c63-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="78c63-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="78c63-133">-Confirm</span></span>
<span data-ttu-id="78c63-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78c63-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c63-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78c63-135">-WhatIf</span></span>
<span data-ttu-id="78c63-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="78c63-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78c63-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78c63-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c63-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c63-138">CommonParameters</span></span>
<span data-ttu-id="78c63-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78c63-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c63-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78c63-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c63-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78c63-141">INPUTS</span></span>

### <span data-ttu-id="78c63-142">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="78c63-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="78c63-143">System. String</span><span class="sxs-lookup"><span data-stu-id="78c63-143">System.String</span></span>

## <span data-ttu-id="78c63-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78c63-144">OUTPUTS</span></span>

### <span data-ttu-id="78c63-145">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="78c63-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="78c63-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78c63-146">NOTES</span></span>

## <span data-ttu-id="78c63-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78c63-147">RELATED LINKS</span></span>