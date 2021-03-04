---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: c7b213fd041718de1f4f8a6c21979a6c0e7af964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889414"
---
# <span data-ttu-id="dee63-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="dee63-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="dee63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dee63-102">SYNOPSIS</span></span>

<span data-ttu-id="dee63-103">Obtém detalhes de um trabalho de Backup.</span><span class="sxs-lookup"><span data-stu-id="dee63-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="dee63-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dee63-104">SYNTAX</span></span>

### <span data-ttu-id="dee63-105">JobFilterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dee63-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dee63-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="dee63-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dee63-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dee63-107">DESCRIPTION</span></span>

<span data-ttu-id="dee63-108">O cmdlet **Get-AzRecoveryServicesBackupJobDetail** obtém detalhes do trabalho de Backup do Azure para um trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="dee63-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="dee63-109">De definir o contexto do cofre usando o parâmetro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="dee63-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="dee63-110">Aviso: o alias **Get-AzRecoveryServicesBackupJobDetails** será removido em uma versão de alteração futura.</span><span class="sxs-lookup"><span data-stu-id="dee63-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="dee63-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dee63-111">EXAMPLES</span></span>

### <span data-ttu-id="dee63-112">Exemplo 1: Obter detalhes do trabalho de backup para trabalhos com falha</span><span class="sxs-lookup"><span data-stu-id="dee63-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="dee63-113">O primeiro comando busca o cofre relevante.</span><span class="sxs-lookup"><span data-stu-id="dee63-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="dee63-114">O segundo comando obtém uma matriz de trabalhos com falha no cofre e os armazena na matriz $Jobs.</span><span class="sxs-lookup"><span data-stu-id="dee63-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="dee63-115">O terceiro comando obtém os detalhes do trabalho do 1º trabalho com falha no $Jobs e os armazena na variável $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="dee63-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="dee63-116">O comando final exibe detalhes de erro para os trabalhos com falha.</span><span class="sxs-lookup"><span data-stu-id="dee63-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="dee63-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dee63-117">PARAMETERS</span></span>

### <span data-ttu-id="dee63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee63-118">-DefaultProfile</span></span>

<span data-ttu-id="dee63-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="dee63-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dee63-120">-Job</span><span class="sxs-lookup"><span data-stu-id="dee63-120">-Job</span></span>

<span data-ttu-id="dee63-121">Especifica o trabalho a ser feito.</span><span class="sxs-lookup"><span data-stu-id="dee63-121">Specifies the job to get.</span></span>
<span data-ttu-id="dee63-122">Para obter um **objeto BackupJob,** use o cmdlet **Get-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="dee63-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="dee63-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="dee63-123">-JobId</span></span>

<span data-ttu-id="dee63-124">Especifica a ID de um trabalho de Backup.</span><span class="sxs-lookup"><span data-stu-id="dee63-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="dee63-125">A ID é a propriedade JobId de **um objeto Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase.**</span><span class="sxs-lookup"><span data-stu-id="dee63-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="dee63-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="dee63-126">-VaultId</span></span>

<span data-ttu-id="dee63-127">ARM ID do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="dee63-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="dee63-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee63-128">CommonParameters</span></span>
<span data-ttu-id="dee63-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dee63-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee63-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dee63-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee63-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dee63-131">INPUTS</span></span>

### <span data-ttu-id="dee63-132">System.String</span><span class="sxs-lookup"><span data-stu-id="dee63-132">System.String</span></span>

## <span data-ttu-id="dee63-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dee63-133">OUTPUTS</span></span>

### <span data-ttu-id="dee63-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="dee63-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="dee63-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="dee63-135">NOTES</span></span>

## <span data-ttu-id="dee63-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dee63-136">RELATED LINKS</span></span>

[<span data-ttu-id="dee63-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="dee63-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
