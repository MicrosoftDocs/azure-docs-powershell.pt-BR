---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112671"
---
# <span data-ttu-id="efcf7-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="efcf7-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="efcf7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efcf7-102">SYNOPSIS</span></span>

<span data-ttu-id="efcf7-103">Aguarda a finalização de um trabalho de Backup.</span><span class="sxs-lookup"><span data-stu-id="efcf7-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="efcf7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efcf7-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efcf7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="efcf7-105">DESCRIPTION</span></span>

<span data-ttu-id="efcf7-106">O cmdlet **Wait-AzRecoveryServicesBackup Job** aguarda a finalização de um trabalho de Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="efcf7-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="efcf7-107">Trabalhos de backup podem levar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="efcf7-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="efcf7-108">Se você executar um trabalho de backup como parte de um script, talvez queira forçar o script a aguardar até que o trabalho seja finalizado antes que ele continue em outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="efcf7-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="efcf7-109">Um script que inclui esse cmdlet pode ser mais simples do que um que vota no serviço backup para o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="efcf7-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="efcf7-110">De definir o contexto do cofre usando o parâmetro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="efcf7-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="efcf7-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="efcf7-111">EXAMPLES</span></span>

### <span data-ttu-id="efcf7-112">Exemplo 1: Aguarde até que um trabalho termine</span><span class="sxs-lookup"><span data-stu-id="efcf7-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="efcf7-113">Este script vota no primeiro trabalho em andamento até que o trabalho tenha concluído ou o período de tempo de 1 hora expirado.</span><span class="sxs-lookup"><span data-stu-id="efcf7-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="efcf7-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efcf7-114">PARAMETERS</span></span>

### <span data-ttu-id="efcf7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efcf7-115">-DefaultProfile</span></span>

<span data-ttu-id="efcf7-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="efcf7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efcf7-117">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="efcf7-117">-Job</span></span>

<span data-ttu-id="efcf7-118">Especifica o trabalho pelo que esperar.</span><span class="sxs-lookup"><span data-stu-id="efcf7-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="efcf7-119">Para obter um **objeto BackupService,** use o cmdlet **Get-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="efcf7-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efcf7-120">-Tempo de tempo</span><span class="sxs-lookup"><span data-stu-id="efcf7-120">-Timeout</span></span>

<span data-ttu-id="efcf7-121">Especifica o tempo máximo, em segundos, que este cmdlet espera o trabalho terminar.</span><span class="sxs-lookup"><span data-stu-id="efcf7-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="efcf7-122">É recomendável especificar um valor de tempo de tempo.</span><span class="sxs-lookup"><span data-stu-id="efcf7-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efcf7-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="efcf7-123">-VaultId</span></span>

<span data-ttu-id="efcf7-124">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="efcf7-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="efcf7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efcf7-125">CommonParameters</span></span>
<span data-ttu-id="efcf7-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efcf7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efcf7-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efcf7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efcf7-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="efcf7-128">INPUTS</span></span>

### <span data-ttu-id="efcf7-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="efcf7-129">System.Object</span></span>

### <span data-ttu-id="efcf7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="efcf7-130">System.String</span></span>

## <span data-ttu-id="efcf7-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="efcf7-131">OUTPUTS</span></span>

### <span data-ttu-id="efcf7-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="efcf7-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="efcf7-133">Notas</span><span class="sxs-lookup"><span data-stu-id="efcf7-133">NOTES</span></span>

## <span data-ttu-id="efcf7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efcf7-134">RELATED LINKS</span></span>

[<span data-ttu-id="efcf7-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="efcf7-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
