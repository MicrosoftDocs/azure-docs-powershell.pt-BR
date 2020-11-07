---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 80fbb17d31c37dafd4ba16b059c1dda5a987bea4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772960"
---
# <span data-ttu-id="25407-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="25407-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="25407-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25407-102">SYNOPSIS</span></span>
<span data-ttu-id="25407-103">Cancela um trabalho em execução.</span><span class="sxs-lookup"><span data-stu-id="25407-103">Cancels a running job.</span></span>

## <span data-ttu-id="25407-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25407-104">SYNTAX</span></span>

### <span data-ttu-id="25407-105">JobFilterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="25407-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25407-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="25407-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25407-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25407-107">DESCRIPTION</span></span>
<span data-ttu-id="25407-108">O cmdlet **Stop-AzRecoveryServicesBackupJob** cancela um trabalho de backup do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="25407-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="25407-109">Use esse cmdlet para interromper um trabalho que leve muito tempo e bloqueie outras atividades.</span><span class="sxs-lookup"><span data-stu-id="25407-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="25407-110">Você pode cancelar somente os tipos de trabalho de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="25407-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="25407-111">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="25407-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="25407-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25407-112">EXAMPLES</span></span>

### <span data-ttu-id="25407-113">Exemplo 1: parar um trabalho de backup</span><span class="sxs-lookup"><span data-stu-id="25407-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="25407-114">O primeiro comando obtém um trabalho de backup e armazena o trabalho na variável $Job.</span><span class="sxs-lookup"><span data-stu-id="25407-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="25407-115">O último comando interrompe o trabalho especificando a ID da instância do trabalho de backup em $Job.</span><span class="sxs-lookup"><span data-stu-id="25407-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="25407-116">OS</span><span class="sxs-lookup"><span data-stu-id="25407-116">PARAMETERS</span></span>

### <span data-ttu-id="25407-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25407-117">-DefaultProfile</span></span>
<span data-ttu-id="25407-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25407-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25407-119">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="25407-119">-Job</span></span>
<span data-ttu-id="25407-120">Especifica um trabalho cancelado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25407-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="25407-121">Para obter um objeto **BackupJob** , use o cmdlet Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="25407-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="25407-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="25407-122">-JobId</span></span>
<span data-ttu-id="25407-123">Especifica a ID do trabalho a ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="25407-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="25407-124">A ID é a propriedade InstanceId de um objeto **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="25407-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="25407-125">Para obter um objeto **BackupJob** , use Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="25407-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="25407-126">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="25407-126">-VaultId</span></span>
<span data-ttu-id="25407-127">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="25407-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="25407-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="25407-128">-Confirm</span></span>
<span data-ttu-id="25407-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25407-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25407-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25407-130">-WhatIf</span></span>
<span data-ttu-id="25407-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25407-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25407-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25407-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25407-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25407-133">CommonParameters</span></span>
<span data-ttu-id="25407-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25407-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25407-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25407-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25407-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25407-136">INPUTS</span></span>

### <span data-ttu-id="25407-137">System. String</span><span class="sxs-lookup"><span data-stu-id="25407-137">System.String</span></span>

## <span data-ttu-id="25407-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25407-138">OUTPUTS</span></span>

### <span data-ttu-id="25407-139">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="25407-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="25407-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25407-140">NOTES</span></span>

## <span data-ttu-id="25407-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25407-141">RELATED LINKS</span></span>

[<span data-ttu-id="25407-142">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="25407-142">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="25407-143">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="25407-143">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


