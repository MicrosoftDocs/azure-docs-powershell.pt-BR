---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 91658fc0772dfa2752d7f12f93efc62d57330891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603337"
---
# <span data-ttu-id="64e25-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="64e25-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="64e25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64e25-102">SYNOPSIS</span></span>
<span data-ttu-id="64e25-103">Obtém detalhes para um trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="64e25-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64e25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64e25-104">SYNTAX</span></span>

### <span data-ttu-id="64e25-105">JobFilterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="64e25-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64e25-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="64e25-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64e25-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64e25-107">DESCRIPTION</span></span>
<span data-ttu-id="64e25-108">O cmdlet **Get-AzureRmRecoveryServicesBackupJobDetails** Obtém detalhes do trabalho de backup do Azure para um trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="64e25-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="64e25-109">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="64e25-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="64e25-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64e25-110">EXAMPLES</span></span>

### <span data-ttu-id="64e25-111">Exemplo 1: obter detalhes do trabalho de backup para trabalhos com falha</span><span class="sxs-lookup"><span data-stu-id="64e25-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="64e25-112">O primeiro comando obtém uma matriz de trabalhos com falha no cofre e, em seguida, armazena-os na matriz de $Jobs.</span><span class="sxs-lookup"><span data-stu-id="64e25-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="64e25-113">O segundo comando obtém os detalhes do trabalho para os trabalhos com falha no $Jobs e, em seguida, armazena-os na variável $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="64e25-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="64e25-114">O comando final exibe detalhes do erro para os trabalhos com falha.</span><span class="sxs-lookup"><span data-stu-id="64e25-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="64e25-115">OS</span><span class="sxs-lookup"><span data-stu-id="64e25-115">PARAMETERS</span></span>

### <span data-ttu-id="64e25-116">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="64e25-116">-Job</span></span>
<span data-ttu-id="64e25-117">Especifica o trabalho a obter.</span><span class="sxs-lookup"><span data-stu-id="64e25-117">Specifies the job to get.</span></span>
<span data-ttu-id="64e25-118">Para obter um objeto **BackupJob** , use o cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="64e25-118">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="64e25-119">-JobId</span><span class="sxs-lookup"><span data-stu-id="64e25-119">-JobId</span></span>
<span data-ttu-id="64e25-120">Especifica a ID de um trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="64e25-120">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="64e25-121">A ID é a propriedade InstanceId de um objeto **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="64e25-121">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="64e25-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64e25-122">-DefaultProfile</span></span>
<span data-ttu-id="64e25-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64e25-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64e25-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64e25-124">CommonParameters</span></span>
<span data-ttu-id="64e25-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64e25-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64e25-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64e25-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64e25-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64e25-127">INPUTS</span></span>

## <span data-ttu-id="64e25-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64e25-128">OUTPUTS</span></span>

### <span data-ttu-id="64e25-129">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="64e25-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="64e25-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64e25-130">NOTES</span></span>

## <span data-ttu-id="64e25-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64e25-131">RELATED LINKS</span></span>

[<span data-ttu-id="64e25-132">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="64e25-132">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


