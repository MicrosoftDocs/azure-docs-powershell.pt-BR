---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/wait-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: ce44ac04914419fa2551062b28108abeca9d4249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611050"
---
# <span data-ttu-id="49ec3-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="49ec3-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="49ec3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="49ec3-103">Aguarda o término do trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="49ec3-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49ec3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49ec3-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49ec3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="49ec3-106">O cmdlet **Wait-AzureRmBackupJob** aguarda a conclusão de um trabalho de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="49ec3-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="49ec3-107">Tarefas de backup podem levar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="49ec3-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="49ec3-108">Se você executar um trabalho de backup como parte de um script, talvez queira forçar o script a aguardar a conclusão do trabalho antes que ele continue para outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="49ec3-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="49ec3-109">Um script que inclui esse cmdlet pode ser mais simples que um que sonda o serviço de backup para o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="49ec3-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="49ec3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49ec3-110">EXAMPLES</span></span>

## <span data-ttu-id="49ec3-111">OS</span><span class="sxs-lookup"><span data-stu-id="49ec3-111">PARAMETERS</span></span>

### <span data-ttu-id="49ec3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ec3-112">-DefaultProfile</span></span>
<span data-ttu-id="49ec3-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="49ec3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ec3-114">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="49ec3-114">-Job</span></span>
<span data-ttu-id="49ec3-115">Especifica um trabalho cancelado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ec3-115">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="49ec3-116">Para obter um objeto **AzureRmBackupJob** , use o cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="49ec3-116">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ec3-117">-TimeOut</span><span class="sxs-lookup"><span data-stu-id="49ec3-117">-TimeOut</span></span>
<span data-ttu-id="49ec3-118">Especifica o tempo máximo, em segundos, que esse cmdlet aguarda para o trabalho terminar.</span><span class="sxs-lookup"><span data-stu-id="49ec3-118">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="49ec3-119">Recomendamos que você especifique um valor de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="49ec3-119">We recommend that you specify a time-out value.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ec3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ec3-120">CommonParameters</span></span>
<span data-ttu-id="49ec3-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ec3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ec3-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ec3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ec3-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49ec3-123">INPUTS</span></span>

### <span data-ttu-id="49ec3-124">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="49ec3-124">AzureRmBackupJob</span></span>

## <span data-ttu-id="49ec3-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49ec3-125">OUTPUTS</span></span>

### <span data-ttu-id="49ec3-126">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="49ec3-126">AzureRmBackupJob[]</span></span>

## <span data-ttu-id="49ec3-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49ec3-127">NOTES</span></span>

## <span data-ttu-id="49ec3-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49ec3-128">RELATED LINKS</span></span>

[<span data-ttu-id="49ec3-129">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="49ec3-129">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="49ec3-130">Parar-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="49ec3-130">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


