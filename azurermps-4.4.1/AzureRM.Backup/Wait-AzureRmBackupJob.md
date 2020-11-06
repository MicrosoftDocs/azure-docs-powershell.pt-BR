---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: 6ee1319881b200b3fcae56e433f81460bfc90274
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439977"
---
# <span data-ttu-id="f07cb-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f07cb-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="f07cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f07cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f07cb-103">Aguarda o término do trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="f07cb-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f07cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f07cb-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f07cb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f07cb-105">DESCRIPTION</span></span>
<span data-ttu-id="f07cb-106">O cmdlet **Wait-AzureRmBackupJob** aguarda a conclusão de um trabalho de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="f07cb-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="f07cb-107">Tarefas de backup podem levar muito tempo.</span><span class="sxs-lookup"><span data-stu-id="f07cb-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="f07cb-108">Se você executar um trabalho de backup como parte de um script, talvez queira forçar o script a aguardar a conclusão do trabalho antes que ele continue para outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="f07cb-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="f07cb-109">Um script que inclui esse cmdlet pode ser mais simples que um que sonda o serviço de backup para o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="f07cb-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="f07cb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f07cb-110">EXAMPLES</span></span>

## <span data-ttu-id="f07cb-111">OS</span><span class="sxs-lookup"><span data-stu-id="f07cb-111">PARAMETERS</span></span>

### <span data-ttu-id="f07cb-112">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="f07cb-112">-Job</span></span>
<span data-ttu-id="f07cb-113">Especifica um trabalho cancelado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f07cb-113">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="f07cb-114">Para obter um objeto **AzureRmBackupJob** , use o cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="f07cb-114">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f07cb-115">-TimeOut</span><span class="sxs-lookup"><span data-stu-id="f07cb-115">-TimeOut</span></span>
<span data-ttu-id="f07cb-116">Especifica o tempo máximo, em segundos, que esse cmdlet aguarda para o trabalho terminar.</span><span class="sxs-lookup"><span data-stu-id="f07cb-116">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="f07cb-117">Recomendamos que você especifique um valor de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="f07cb-117">We recommend that you specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f07cb-118">-DefaultProfile</span></span>
<span data-ttu-id="f07cb-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f07cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f07cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f07cb-120">CommonParameters</span></span>
<span data-ttu-id="f07cb-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f07cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f07cb-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f07cb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f07cb-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f07cb-123">INPUTS</span></span>

### <span data-ttu-id="f07cb-124">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f07cb-124">AzureRmBackupJob</span></span>

## <span data-ttu-id="f07cb-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f07cb-125">OUTPUTS</span></span>

### <span data-ttu-id="f07cb-126">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="f07cb-126">AzureRmBackupJob[]</span></span>

## <span data-ttu-id="f07cb-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f07cb-127">NOTES</span></span>

## <span data-ttu-id="f07cb-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f07cb-128">RELATED LINKS</span></span>

[<span data-ttu-id="f07cb-129">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f07cb-129">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="f07cb-130">Parar-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f07cb-130">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


