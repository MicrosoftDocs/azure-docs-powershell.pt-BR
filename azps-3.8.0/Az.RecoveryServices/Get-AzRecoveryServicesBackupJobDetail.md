---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 81c1aeded9b4bb40998448d61a5edbf35742bfcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940887"
---
# <span data-ttu-id="41265-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="41265-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="41265-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41265-102">SYNOPSIS</span></span>

<span data-ttu-id="41265-103">Obtém detalhes para um trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="41265-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="41265-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41265-104">SYNTAX</span></span>

### <span data-ttu-id="41265-105">JobFilterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="41265-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41265-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="41265-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41265-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41265-107">DESCRIPTION</span></span>

<span data-ttu-id="41265-108">O cmdlet **Get-AzRecoveryServicesBackupJobDetail** Obtém detalhes do trabalho de backup do Azure para um trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="41265-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="41265-109">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="41265-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="41265-110">Aviso: o alias **Get-AzRecoveryServicesBackupJobDetails** será removido em uma versão futura de alteração significativa.</span><span class="sxs-lookup"><span data-stu-id="41265-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="41265-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41265-111">EXAMPLES</span></span>

### <span data-ttu-id="41265-112">Exemplo 1: obter detalhes do trabalho de backup para trabalhos com falha</span><span class="sxs-lookup"><span data-stu-id="41265-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="41265-113">O primeiro comando obtém uma matriz de trabalhos com falha no cofre e, em seguida, armazena-os na matriz de $Jobs.</span><span class="sxs-lookup"><span data-stu-id="41265-113">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="41265-114">O segundo comando obtém os detalhes do trabalho para os trabalhos com falha no $Jobs e, em seguida, armazena-os na variável $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="41265-114">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="41265-115">O comando final exibe detalhes do erro para os trabalhos com falha.</span><span class="sxs-lookup"><span data-stu-id="41265-115">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="41265-116">OS</span><span class="sxs-lookup"><span data-stu-id="41265-116">PARAMETERS</span></span>

### <span data-ttu-id="41265-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41265-117">-DefaultProfile</span></span>

<span data-ttu-id="41265-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41265-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41265-119">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="41265-119">-Job</span></span>

<span data-ttu-id="41265-120">Especifica o trabalho a obter.</span><span class="sxs-lookup"><span data-stu-id="41265-120">Specifies the job to get.</span></span>
<span data-ttu-id="41265-121">Para obter um objeto **BackupJob** , use o cmdlet **Get-AzRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="41265-121">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="41265-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="41265-122">-JobId</span></span>

<span data-ttu-id="41265-123">Especifica a ID de um trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="41265-123">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="41265-124">A ID é a propriedade JobId de um objeto **Microsoft. Azure. Commands. recoveryservices. backup. cmdlets. Models. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="41265-124">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="41265-125">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="41265-125">-VaultId</span></span>

<span data-ttu-id="41265-126">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="41265-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="41265-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41265-127">CommonParameters</span></span>
<span data-ttu-id="41265-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41265-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41265-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41265-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41265-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41265-130">INPUTS</span></span>

### <span data-ttu-id="41265-131">System. String</span><span class="sxs-lookup"><span data-stu-id="41265-131">System.String</span></span>

## <span data-ttu-id="41265-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41265-132">OUTPUTS</span></span>

### <span data-ttu-id="41265-133">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="41265-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="41265-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41265-134">NOTES</span></span>

## <span data-ttu-id="41265-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41265-135">RELATED LINKS</span></span>

[<span data-ttu-id="41265-136">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="41265-136">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
