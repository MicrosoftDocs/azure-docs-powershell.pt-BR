---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 7d39ce49a76d8519f2eacf0649c52051290274f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427222"
---
# <span data-ttu-id="169b7-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="169b7-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="169b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="169b7-102">SYNOPSIS</span></span>
<span data-ttu-id="169b7-103">Obtém detalhes para um trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="169b7-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="169b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="169b7-104">SYNTAX</span></span>

### <span data-ttu-id="169b7-105">JobFilterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="169b7-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="169b7-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="169b7-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="169b7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="169b7-107">DESCRIPTION</span></span>
<span data-ttu-id="169b7-108">O cmdlet **Get-AzureRmRecoveryServicesBackupJobDetails** Obtém detalhes do trabalho de backup do Azure para um trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="169b7-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="169b7-109">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="169b7-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="169b7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="169b7-110">EXAMPLES</span></span>

### <span data-ttu-id="169b7-111">Exemplo 1: obter detalhes do trabalho de backup para trabalhos com falha</span><span class="sxs-lookup"><span data-stu-id="169b7-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="169b7-112">O primeiro comando obtém uma matriz de trabalhos com falha no cofre e, em seguida, armazena-os na matriz de $Jobs.</span><span class="sxs-lookup"><span data-stu-id="169b7-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="169b7-113">O segundo comando obtém os detalhes do trabalho para os trabalhos com falha no $Jobs e, em seguida, armazena-os na variável $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="169b7-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="169b7-114">O comando final exibe detalhes do erro para os trabalhos com falha.</span><span class="sxs-lookup"><span data-stu-id="169b7-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="169b7-115">OS</span><span class="sxs-lookup"><span data-stu-id="169b7-115">PARAMETERS</span></span>

### <span data-ttu-id="169b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169b7-116">-DefaultProfile</span></span>
<span data-ttu-id="169b7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="169b7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169b7-118">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="169b7-118">-Job</span></span>
<span data-ttu-id="169b7-119">Especifica o trabalho a obter.</span><span class="sxs-lookup"><span data-stu-id="169b7-119">Specifies the job to get.</span></span>
<span data-ttu-id="169b7-120">Para obter um objeto **BackupJob** , use o cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="169b7-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="169b7-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="169b7-121">-JobId</span></span>
<span data-ttu-id="169b7-122">Especifica a ID de um trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="169b7-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="169b7-123">A ID é a propriedade InstanceId de um objeto **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="169b7-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="169b7-124">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="169b7-124">-VaultId</span></span>
<span data-ttu-id="169b7-125">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="169b7-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="169b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169b7-126">CommonParameters</span></span>
<span data-ttu-id="169b7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="169b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169b7-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="169b7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169b7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="169b7-129">INPUTS</span></span>

### <span data-ttu-id="169b7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="169b7-130">System.String</span></span>
<span data-ttu-id="169b7-131">Parâmetros: Vaultid (ByValue)</span><span class="sxs-lookup"><span data-stu-id="169b7-131">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="169b7-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="169b7-132">OUTPUTS</span></span>

### <span data-ttu-id="169b7-133">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="169b7-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="169b7-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="169b7-134">NOTES</span></span>

## <span data-ttu-id="169b7-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="169b7-135">RELATED LINKS</span></span>

[<span data-ttu-id="169b7-136">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="169b7-136">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


