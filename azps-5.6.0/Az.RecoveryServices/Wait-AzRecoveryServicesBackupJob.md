---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: e0b3dc87ffdfc86f39f201b6384f38ce8ca1c70a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886404"
---
# <span data-ttu-id="eea4c-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="eea4c-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="eea4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eea4c-102">SYNOPSIS</span></span>

<span data-ttu-id="eea4c-103">Aguarda a finalização de um trabalho de Backup.</span><span class="sxs-lookup"><span data-stu-id="eea4c-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="eea4c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eea4c-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eea4c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eea4c-105">DESCRIPTION</span></span>

<span data-ttu-id="eea4c-106">O cmdlet **Wait-AzRecoveryServicesBackupJob** aguarda a finalização de um trabalho de Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="eea4c-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="eea4c-107">Os trabalhos de backup podem levar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="eea4c-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="eea4c-108">Se você executar um trabalho de backup como parte de um script, talvez você queira forçar o script a aguardar o trabalho ser finalizado antes que ele continue para outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="eea4c-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="eea4c-109">Um script que inclui esse cmdlet pode ser mais simples do que um que sonda o serviço de Backup para o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="eea4c-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="eea4c-110">De definir o contexto do cofre usando o parâmetro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="eea4c-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="eea4c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eea4c-111">EXAMPLES</span></span>

### <span data-ttu-id="eea4c-112">Exemplo 1: aguarde a finalização de um trabalho</span><span class="sxs-lookup"><span data-stu-id="eea4c-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="eea4c-113">Este script sonda o primeiro trabalho que está em andamento até que o trabalho tenha concluído ou o período de tempo-de-tempo de 1 hora expirado.</span><span class="sxs-lookup"><span data-stu-id="eea4c-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="eea4c-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eea4c-114">PARAMETERS</span></span>

### <span data-ttu-id="eea4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea4c-115">-DefaultProfile</span></span>

<span data-ttu-id="eea4c-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="eea4c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eea4c-117">-Job</span><span class="sxs-lookup"><span data-stu-id="eea4c-117">-Job</span></span>

<span data-ttu-id="eea4c-118">Especifica o trabalho a ser aguardado.</span><span class="sxs-lookup"><span data-stu-id="eea4c-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="eea4c-119">Para obter um **objeto BackupJob,** use o cmdlet **Get-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="eea4c-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="eea4c-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="eea4c-120">-Timeout</span></span>

<span data-ttu-id="eea4c-121">Especifica o tempo máximo, em segundos, que este cmdlet aguarda o fim do trabalho.</span><span class="sxs-lookup"><span data-stu-id="eea4c-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="eea4c-122">É recomendável especificar um valor de tempo-de-tempo.</span><span class="sxs-lookup"><span data-stu-id="eea4c-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="eea4c-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="eea4c-123">-VaultId</span></span>

<span data-ttu-id="eea4c-124">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="eea4c-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="eea4c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea4c-125">CommonParameters</span></span>
<span data-ttu-id="eea4c-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea4c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea4c-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eea4c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea4c-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eea4c-128">INPUTS</span></span>

### <span data-ttu-id="eea4c-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="eea4c-129">System.Object</span></span>

### <span data-ttu-id="eea4c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="eea4c-130">System.String</span></span>

## <span data-ttu-id="eea4c-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eea4c-131">OUTPUTS</span></span>

### <span data-ttu-id="eea4c-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="eea4c-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="eea4c-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="eea4c-133">NOTES</span></span>

## <span data-ttu-id="eea4c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eea4c-134">RELATED LINKS</span></span>

[<span data-ttu-id="eea4c-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="eea4c-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
