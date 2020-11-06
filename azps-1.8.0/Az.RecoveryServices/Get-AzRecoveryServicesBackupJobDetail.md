---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: f38029a85cac1b6771a546b120714823f5b02927
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599704"
---
# <span data-ttu-id="73d3b-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="73d3b-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="73d3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="73d3b-103">Obtém detalhes para um trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="73d3b-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="73d3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73d3b-104">SYNTAX</span></span>

### <span data-ttu-id="73d3b-105">JobFilterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="73d3b-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73d3b-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="73d3b-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73d3b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73d3b-107">DESCRIPTION</span></span>
<span data-ttu-id="73d3b-108">O cmdlet **Get-AzRecoveryServicesBackupJobDetail** Obtém detalhes do trabalho de backup do Azure para um trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="73d3b-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="73d3b-109">Defina o contexto do cofre usando o cmdlet Set-AzRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="73d3b-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="73d3b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73d3b-110">EXAMPLES</span></span>

### <span data-ttu-id="73d3b-111">Exemplo 1: obter detalhes do trabalho de backup para trabalhos com falha</span><span class="sxs-lookup"><span data-stu-id="73d3b-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="73d3b-112">O primeiro comando obtém uma matriz de trabalhos com falha no cofre e, em seguida, armazena-os na matriz de $Jobs.</span><span class="sxs-lookup"><span data-stu-id="73d3b-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="73d3b-113">O segundo comando obtém os detalhes do trabalho para os trabalhos com falha no $Jobs e, em seguida, armazena-os na variável $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="73d3b-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="73d3b-114">O comando final exibe detalhes do erro para os trabalhos com falha.</span><span class="sxs-lookup"><span data-stu-id="73d3b-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="73d3b-115">OS</span><span class="sxs-lookup"><span data-stu-id="73d3b-115">PARAMETERS</span></span>

### <span data-ttu-id="73d3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73d3b-116">-DefaultProfile</span></span>
<span data-ttu-id="73d3b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73d3b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73d3b-118">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="73d3b-118">-Job</span></span>
<span data-ttu-id="73d3b-119">Especifica o trabalho a obter.</span><span class="sxs-lookup"><span data-stu-id="73d3b-119">Specifies the job to get.</span></span>
<span data-ttu-id="73d3b-120">Para obter um objeto **BackupJob** , use o cmdlet Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="73d3b-120">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="73d3b-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="73d3b-121">-JobId</span></span>
<span data-ttu-id="73d3b-122">Especifica a ID de um trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="73d3b-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="73d3b-123">A ID é a propriedade InstanceId de um objeto **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="73d3b-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="73d3b-124">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="73d3b-124">-VaultId</span></span>
<span data-ttu-id="73d3b-125">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="73d3b-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="73d3b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d3b-126">CommonParameters</span></span>
<span data-ttu-id="73d3b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73d3b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d3b-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73d3b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d3b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73d3b-129">INPUTS</span></span>

### <span data-ttu-id="73d3b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="73d3b-130">System.String</span></span>

## <span data-ttu-id="73d3b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73d3b-131">OUTPUTS</span></span>

### <span data-ttu-id="73d3b-132">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="73d3b-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="73d3b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73d3b-133">NOTES</span></span>

## <span data-ttu-id="73d3b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73d3b-134">RELATED LINKS</span></span>

[<span data-ttu-id="73d3b-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="73d3b-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)


