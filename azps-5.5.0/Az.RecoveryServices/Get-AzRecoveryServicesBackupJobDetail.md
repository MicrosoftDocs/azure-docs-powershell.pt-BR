---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 6c12cccff6305c96bf2df037e32b8af35170454a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114963"
---
# <span data-ttu-id="8f7c5-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="8f7c5-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="8f7c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f7c5-102">SYNOPSIS</span></span>

<span data-ttu-id="8f7c5-103">Obtém detalhes sobre um trabalho de Backup.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="8f7c5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f7c5-104">SYNTAX</span></span>

### <span data-ttu-id="8f7c5-105">JobFilterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f7c5-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f7c5-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="8f7c5-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f7c5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f7c5-107">DESCRIPTION</span></span>

<span data-ttu-id="8f7c5-108">O cmdlet **Get-AzRecoveryServicesBackupServiceDetail** obtém detalhes do trabalho do Azure Backup para um trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="8f7c5-109">De definir o contexto do cofre usando o parâmetro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="8f7c5-110">Aviso: o alias **Get-AzRecoveryServicesBackupServiceDetails** será removido em uma versão futura de alteração de quebra.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="8f7c5-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f7c5-111">EXAMPLES</span></span>

### <span data-ttu-id="8f7c5-112">Exemplo 1: Obter detalhes do trabalho de backup para trabalhos com falha</span><span class="sxs-lookup"><span data-stu-id="8f7c5-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="8f7c5-113">O primeiro comando busca o cofre relevante.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="8f7c5-114">O segundo comando obtém uma matriz de trabalhos com falha no cofre e os armazena na matriz $Jobs dados.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="8f7c5-115">O terceiro comando obtém os detalhes do trabalho do 1º trabalho com falha no $Jobs e, em seguida, os armazena na variável $JobDetails trabalho.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="8f7c5-116">O comando final exibe detalhes de erro para os trabalhos com falha.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="8f7c5-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f7c5-117">PARAMETERS</span></span>

### <span data-ttu-id="8f7c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7c5-118">-DefaultProfile</span></span>

<span data-ttu-id="8f7c5-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f7c5-120">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="8f7c5-120">-Job</span></span>

<span data-ttu-id="8f7c5-121">Especifica o trabalho a ser feito.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-121">Specifies the job to get.</span></span>
<span data-ttu-id="8f7c5-122">Para obter um **objeto BackupService,** use o cmdlet **Get-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="8f7c5-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="8f7c5-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="8f7c5-123">-JobId</span></span>

<span data-ttu-id="8f7c5-124">Especifica a ID de um trabalho de Backup.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="8f7c5-125">A ID é a propriedade JobId de um objeto **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase.**</span><span class="sxs-lookup"><span data-stu-id="8f7c5-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="8f7c5-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8f7c5-126">-VaultId</span></span>

<span data-ttu-id="8f7c5-127">ID arm do Cofre de Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8f7c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7c5-128">CommonParameters</span></span>
<span data-ttu-id="8f7c5-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7c5-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f7c5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7c5-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="8f7c5-131">INPUTS</span></span>

### <span data-ttu-id="8f7c5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8f7c5-132">System.String</span></span>

## <span data-ttu-id="8f7c5-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="8f7c5-133">OUTPUTS</span></span>

### <span data-ttu-id="8f7c5-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="8f7c5-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8f7c5-135">Notas</span><span class="sxs-lookup"><span data-stu-id="8f7c5-135">NOTES</span></span>

## <span data-ttu-id="8f7c5-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f7c5-136">RELATED LINKS</span></span>

[<span data-ttu-id="8f7c5-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8f7c5-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
