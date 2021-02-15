---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114953"
---
# <span data-ttu-id="d119b-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="d119b-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="d119b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d119b-102">SYNOPSIS</span></span>
<span data-ttu-id="d119b-103">Esse comando construirá a configuração de recuperação de um item em backup, como SQL DB.</span><span class="sxs-lookup"><span data-stu-id="d119b-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="d119b-104">O objeto de configuração armazena todos os detalhes, como o modo de recuperação, destinos de destino para a restauração e parâmetros específicos do aplicativo, como caminhos físicos de destino para SQL.</span><span class="sxs-lookup"><span data-stu-id="d119b-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="d119b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d119b-105">SYNTAX</span></span>

### <span data-ttu-id="d119b-106">RessaltoParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d119b-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d119b-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d119b-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d119b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d119b-108">DESCRIPTION</span></span>
<span data-ttu-id="d119b-109">O comando retorna uma configuração de recuperação para itens do AzureWorkload que é passado para o cmdlet de restauração.</span><span class="sxs-lookup"><span data-stu-id="d119b-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="d119b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d119b-110">EXAMPLES</span></span>

### <span data-ttu-id="d119b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d119b-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="d119b-112">O primeiro cmdlet é usado para obter o objeto ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d119b-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="d119b-113">O segundo cmdlet cria um plano de recuperação para uma restauração de local original.</span><span class="sxs-lookup"><span data-stu-id="d119b-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="d119b-114">O terceiro cmdlet cria um plano de recuperação para uma restauração de local alternativa.</span><span class="sxs-lookup"><span data-stu-id="d119b-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="d119b-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d119b-115">Example 2</span></span>

<span data-ttu-id="d119b-116">Esse comando construirá a configuração de recuperação de um item em backup, como SQL DB.</span><span class="sxs-lookup"><span data-stu-id="d119b-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="d119b-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="d119b-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="d119b-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d119b-118">PARAMETERS</span></span>

### <span data-ttu-id="d119b-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="d119b-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="d119b-120">Especifica que o BD backup deve ser restaurado em outro servidor selecionado.</span><span class="sxs-lookup"><span data-stu-id="d119b-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="d119b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d119b-121">-DefaultProfile</span></span>
<span data-ttu-id="d119b-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d119b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d119b-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d119b-123">-FilePath</span></span>
<span data-ttu-id="d119b-124">Especifica o filepath que é usado para a operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="d119b-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="d119b-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="d119b-125">-FromFull</span></span>
<span data-ttu-id="d119b-126">Especifica o Full RecoveryPoint ao qual os backups de Log serão aplicados.</span><span class="sxs-lookup"><span data-stu-id="d119b-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="d119b-127">-Item</span><span class="sxs-lookup"><span data-stu-id="d119b-127">-Item</span></span>
<span data-ttu-id="d119b-128">Especifica o item de backup no qual a operação de restauração está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="d119b-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="d119b-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="d119b-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="d119b-130">Especifica que o BD em backup deve ser substituído com as informações db presentes no ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d119b-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="d119b-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="d119b-131">-PointInTime</span></span>
<span data-ttu-id="d119b-132">Hora de término do intervalo de tempo para o qual o ponto de recuperação precisa ser buscado</span><span class="sxs-lookup"><span data-stu-id="d119b-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="d119b-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d119b-133">-RecoveryPoint</span></span>
<span data-ttu-id="d119b-134">Objeto do ponto de recuperação a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="d119b-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="d119b-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="d119b-135">-RestoreAsFiles</span></span>
<span data-ttu-id="d119b-136">Especifica a restauração do Banco de Dados como arquivos em um computador.</span><span class="sxs-lookup"><span data-stu-id="d119b-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="d119b-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="d119b-137">-TargetContainer</span></span>
<span data-ttu-id="d119b-138">Especifica o computador de destino no qual os Arquivos DB precisam ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="d119b-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="d119b-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="d119b-139">-TargetItem</span></span>
<span data-ttu-id="d119b-140">Especifica o destino no qual o BD precisa ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="d119b-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="d119b-141">Para restaurações de SQL, ele precisa ser apenas do tipo de item protegido SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="d119b-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="d119b-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d119b-142">-VaultId</span></span>
<span data-ttu-id="d119b-143">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="d119b-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d119b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d119b-144">CommonParameters</span></span>
<span data-ttu-id="d119b-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d119b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d119b-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d119b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d119b-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="d119b-147">INPUTS</span></span>

### <span data-ttu-id="d119b-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="d119b-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="d119b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d119b-149">System.String</span></span>

## <span data-ttu-id="d119b-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="d119b-150">OUTPUTS</span></span>

### <span data-ttu-id="d119b-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="d119b-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="d119b-152">Notas</span><span class="sxs-lookup"><span data-stu-id="d119b-152">NOTES</span></span>

## <span data-ttu-id="d119b-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d119b-153">RELATED LINKS</span></span>
