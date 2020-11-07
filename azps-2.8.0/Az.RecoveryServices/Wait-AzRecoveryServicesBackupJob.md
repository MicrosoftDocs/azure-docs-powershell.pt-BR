---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 9a8f972d9a1107517fa151a714540d4758619913
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772947"
---
# <span data-ttu-id="e2f7e-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="e2f7e-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="e2f7e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2f7e-102">SYNOPSIS</span></span>

<span data-ttu-id="e2f7e-103">Aguarda o término do trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="e2f7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2f7e-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2f7e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2f7e-105">DESCRIPTION</span></span>

<span data-ttu-id="e2f7e-106">O cmdlet **Wait-AzRecoveryServicesBackupJob** aguarda a conclusão de um trabalho de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="e2f7e-107">Tarefas de backup podem levar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="e2f7e-108">Se você executar um trabalho de backup como parte de um script, talvez queira forçar o script a aguardar a conclusão do trabalho antes que ele continue para outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="e2f7e-109">Um script que inclui esse cmdlet pode ser mais simples que um que sonda o serviço de backup para o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="e2f7e-110">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="e2f7e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2f7e-111">EXAMPLES</span></span>

### <span data-ttu-id="e2f7e-112">Exemplo 1: Aguarde a conclusão do trabalho</span><span class="sxs-lookup"><span data-stu-id="e2f7e-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="e2f7e-113">Este script sonda o primeiro trabalho que está em andamento até que o trabalho seja concluído ou o período de tempo limite de 1 hora venceu.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="e2f7e-114">OS</span><span class="sxs-lookup"><span data-stu-id="e2f7e-114">PARAMETERS</span></span>

### <span data-ttu-id="e2f7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f7e-115">-DefaultProfile</span></span>

<span data-ttu-id="e2f7e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2f7e-117">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="e2f7e-117">-Job</span></span>

<span data-ttu-id="e2f7e-118">Especifica o trabalho a ser aguardado.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="e2f7e-119">Para obter um objeto **BackupJob** , use o cmdlet **Get-AzRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="e2f7e-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="e2f7e-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="e2f7e-120">-Timeout</span></span>

<span data-ttu-id="e2f7e-121">Especifica o tempo máximo, em segundos, que esse cmdlet aguarda para o trabalho terminar.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="e2f7e-122">É recomendável especificar um valor de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="e2f7e-123">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="e2f7e-123">-VaultId</span></span>

<span data-ttu-id="e2f7e-124">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e2f7e-125">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f7e-125">-CommonParameters</span></span>

<span data-ttu-id="e2f7e-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2f7e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f7e-127">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2f7e-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f7e-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2f7e-128">INPUTS</span></span>

### <span data-ttu-id="e2f7e-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="e2f7e-129">System.Object</span></span>

### <span data-ttu-id="e2f7e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e2f7e-130">System.String</span></span>

## <span data-ttu-id="e2f7e-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2f7e-131">OUTPUTS</span></span>

### <span data-ttu-id="e2f7e-132">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="e2f7e-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="e2f7e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2f7e-133">NOTES</span></span>

## <span data-ttu-id="e2f7e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2f7e-134">RELATED LINKS</span></span>

[<span data-ttu-id="e2f7e-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="e2f7e-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)