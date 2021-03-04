---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 0eaabc025a9252cdd48500f294fab699e7ebea1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891771"
---
# <span data-ttu-id="63e49-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="63e49-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="63e49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63e49-102">SYNOPSIS</span></span>
<span data-ttu-id="63e49-103">Cancela um trabalho em execução.</span><span class="sxs-lookup"><span data-stu-id="63e49-103">Cancels a running job.</span></span>

## <span data-ttu-id="63e49-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="63e49-104">SYNTAX</span></span>

### <span data-ttu-id="63e49-105">JobFilterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="63e49-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e49-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="63e49-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e49-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="63e49-107">DESCRIPTION</span></span>
<span data-ttu-id="63e49-108">O cmdlet **Stop-AzRecoveryServicesBackupJob** cancela um trabalho de Backup do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="63e49-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="63e49-109">Use este cmdlet para interromper um trabalho que leva muito tempo e bloqueia outras atividades.</span><span class="sxs-lookup"><span data-stu-id="63e49-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="63e49-110">Você pode cancelar apenas tipos de trabalho de Backup e Restauração.</span><span class="sxs-lookup"><span data-stu-id="63e49-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="63e49-111">De definir o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="63e49-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="63e49-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63e49-112">EXAMPLES</span></span>

### <span data-ttu-id="63e49-113">Exemplo 1: Interromper um trabalho de backup</span><span class="sxs-lookup"><span data-stu-id="63e49-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="63e49-114">O primeiro comando obtém um trabalho de backup e armazena o trabalho na variável $Job.</span><span class="sxs-lookup"><span data-stu-id="63e49-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="63e49-115">O último comando interrompe o trabalho especificando a ID de Instância do trabalho de backup $Job.</span><span class="sxs-lookup"><span data-stu-id="63e49-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="63e49-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="63e49-116">PARAMETERS</span></span>

### <span data-ttu-id="63e49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e49-117">-DefaultProfile</span></span>
<span data-ttu-id="63e49-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="63e49-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63e49-119">-Job</span><span class="sxs-lookup"><span data-stu-id="63e49-119">-Job</span></span>
<span data-ttu-id="63e49-120">Especifica um trabalho que esse cmdlet cancela.</span><span class="sxs-lookup"><span data-stu-id="63e49-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="63e49-121">Para obter um **objeto BackupJob,** use Get-AzRecoveryServicesBackupJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e49-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e49-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="63e49-122">-JobId</span></span>
<span data-ttu-id="63e49-123">Especifica a ID do trabalho a ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="63e49-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="63e49-124">A ID é a propriedade InstanceId de um **objeto BackupJob.**</span><span class="sxs-lookup"><span data-stu-id="63e49-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="63e49-125">Para obter um **objeto BackupJob,** use Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="63e49-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e49-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="63e49-126">-VaultId</span></span>
<span data-ttu-id="63e49-127">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="63e49-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="63e49-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63e49-128">-Confirm</span></span>
<span data-ttu-id="63e49-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e49-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e49-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e49-130">-WhatIf</span></span>
<span data-ttu-id="63e49-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="63e49-131">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="63e49-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e49-132">CommonParameters</span></span>
<span data-ttu-id="63e49-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e49-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e49-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63e49-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e49-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63e49-135">INPUTS</span></span>

### <span data-ttu-id="63e49-136">System.String</span><span class="sxs-lookup"><span data-stu-id="63e49-136">System.String</span></span>

## <span data-ttu-id="63e49-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="63e49-137">OUTPUTS</span></span>

### <span data-ttu-id="63e49-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="63e49-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="63e49-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="63e49-139">NOTES</span></span>

## <span data-ttu-id="63e49-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63e49-140">RELATED LINKS</span></span>

[<span data-ttu-id="63e49-141">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="63e49-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="63e49-142">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="63e49-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


