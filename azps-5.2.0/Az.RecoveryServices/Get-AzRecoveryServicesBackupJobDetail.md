---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259893"
---
# <span data-ttu-id="b3d83-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="b3d83-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="b3d83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3d83-102">SYNOPSIS</span></span>

<span data-ttu-id="b3d83-103">Obtém detalhes para um trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="b3d83-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="b3d83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3d83-104">SYNTAX</span></span>

### <span data-ttu-id="b3d83-105">JobFilterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b3d83-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3d83-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="b3d83-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3d83-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3d83-107">DESCRIPTION</span></span>

<span data-ttu-id="b3d83-108">O cmdlet **Get-AzRecoveryServicesBackupJobDetail** Obtém detalhes do trabalho de backup do Azure para um trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="b3d83-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="b3d83-109">Defina o contexto do cofre usando o parâmetro-Cofreid.</span><span class="sxs-lookup"><span data-stu-id="b3d83-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="b3d83-110">Aviso: o alias **Get-AzRecoveryServicesBackupJobDetails** será removido em uma versão futura de alteração significativa.</span><span class="sxs-lookup"><span data-stu-id="b3d83-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="b3d83-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3d83-111">EXAMPLES</span></span>

### <span data-ttu-id="b3d83-112">Exemplo 1: obter detalhes do trabalho de backup para trabalhos com falha</span><span class="sxs-lookup"><span data-stu-id="b3d83-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="b3d83-113">O primeiro comando busca o cofre relevante.</span><span class="sxs-lookup"><span data-stu-id="b3d83-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="b3d83-114">O segundo comando obtém uma matriz de trabalhos com falha no cofre e, em seguida, armazena-os na matriz de $Jobs.</span><span class="sxs-lookup"><span data-stu-id="b3d83-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="b3d83-115">O terceiro comando obtém os detalhes do trabalho para o primeiro trabalho com falha no $Jobs e, em seguida, os armazena na variável $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="b3d83-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="b3d83-116">O comando final exibe detalhes do erro para os trabalhos com falha.</span><span class="sxs-lookup"><span data-stu-id="b3d83-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="b3d83-117">OS</span><span class="sxs-lookup"><span data-stu-id="b3d83-117">PARAMETERS</span></span>

### <span data-ttu-id="b3d83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d83-118">-DefaultProfile</span></span>

<span data-ttu-id="b3d83-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3d83-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3d83-120">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="b3d83-120">-Job</span></span>

<span data-ttu-id="b3d83-121">Especifica o trabalho a obter.</span><span class="sxs-lookup"><span data-stu-id="b3d83-121">Specifies the job to get.</span></span>
<span data-ttu-id="b3d83-122">Para obter um objeto **BackupJob** , use o cmdlet **Get-AzRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="b3d83-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="b3d83-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="b3d83-123">-JobId</span></span>

<span data-ttu-id="b3d83-124">Especifica a ID de um trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="b3d83-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="b3d83-125">A ID é a propriedade JobId de um objeto **Microsoft. Azure. Commands. recoveryservices. backup. cmdlets. Models. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="b3d83-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="b3d83-126">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="b3d83-126">-VaultId</span></span>

<span data-ttu-id="b3d83-127">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b3d83-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b3d83-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d83-128">CommonParameters</span></span>
<span data-ttu-id="b3d83-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d83-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d83-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3d83-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d83-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3d83-131">INPUTS</span></span>

### <span data-ttu-id="b3d83-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b3d83-132">System.String</span></span>

## <span data-ttu-id="b3d83-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3d83-133">OUTPUTS</span></span>

### <span data-ttu-id="b3d83-134">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="b3d83-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b3d83-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3d83-135">NOTES</span></span>

## <span data-ttu-id="b3d83-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3d83-136">RELATED LINKS</span></span>

[<span data-ttu-id="b3d83-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="b3d83-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
