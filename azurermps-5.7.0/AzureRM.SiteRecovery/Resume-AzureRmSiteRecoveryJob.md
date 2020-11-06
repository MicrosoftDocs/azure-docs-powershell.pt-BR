---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/resume-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: aae0bf7c2ec4a166d48edb032d6c21918dc3ae6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429674"
---
# <span data-ttu-id="58656-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="58656-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="58656-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58656-102">SYNOPSIS</span></span>
<span data-ttu-id="58656-103">Retoma um trabalho suspenso de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="58656-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58656-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58656-104">SYNTAX</span></span>

### <span data-ttu-id="58656-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="58656-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58656-106">ByName</span><span class="sxs-lookup"><span data-stu-id="58656-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58656-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58656-107">DESCRIPTION</span></span>
<span data-ttu-id="58656-108">O cmdlet **resume-AzureRmSiteRecoveryJob** retoma um trabalho suspenso do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="58656-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="58656-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58656-109">EXAMPLES</span></span>

## <span data-ttu-id="58656-110">OS</span><span class="sxs-lookup"><span data-stu-id="58656-110">PARAMETERS</span></span>

### <span data-ttu-id="58656-111">-Comentários</span><span class="sxs-lookup"><span data-stu-id="58656-111">-Comments</span></span>
<span data-ttu-id="58656-112">Especifica os comentários para o log de trabalho.</span><span class="sxs-lookup"><span data-stu-id="58656-112">Specifies the comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58656-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58656-113">-DefaultProfile</span></span>
<span data-ttu-id="58656-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58656-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58656-115">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="58656-115">-Job</span></span>
<span data-ttu-id="58656-116">Especifica o objeto de trabalho de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="58656-116">Specifies the Site Recovery job object.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58656-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="58656-117">-Name</span></span>
<span data-ttu-id="58656-118">Especifica o nome exclusivo para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="58656-118">Specifies the unique name for the job.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58656-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58656-119">CommonParameters</span></span>
<span data-ttu-id="58656-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58656-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58656-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58656-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58656-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58656-122">INPUTS</span></span>

### <span data-ttu-id="58656-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="58656-123">ASRJob</span></span>
<span data-ttu-id="58656-124">O parâmetro ' Job ' aceita o valor do tipo ' ASRJob ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="58656-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="58656-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58656-125">OUTPUTS</span></span>

### <span data-ttu-id="58656-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="58656-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="58656-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58656-127">NOTES</span></span>

## <span data-ttu-id="58656-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58656-128">RELATED LINKS</span></span>

[<span data-ttu-id="58656-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="58656-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="58656-130">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="58656-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="58656-131">Parar-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="58656-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
