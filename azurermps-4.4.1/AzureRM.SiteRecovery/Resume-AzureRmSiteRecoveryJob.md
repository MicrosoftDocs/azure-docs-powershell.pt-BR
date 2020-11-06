---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 5514d7cec58c2ecad7a4b9c79b3d4d2ad77a5ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603310"
---
# <span data-ttu-id="88541-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="88541-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="88541-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88541-102">SYNOPSIS</span></span>
<span data-ttu-id="88541-103">Retoma um trabalho suspenso de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="88541-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88541-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88541-104">SYNTAX</span></span>

### <span data-ttu-id="88541-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="88541-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88541-106">ByName</span><span class="sxs-lookup"><span data-stu-id="88541-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88541-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88541-107">DESCRIPTION</span></span>
<span data-ttu-id="88541-108">O cmdlet **resume-AzureRmSiteRecoveryJob** retoma um trabalho suspenso do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="88541-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="88541-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88541-109">EXAMPLES</span></span>

## <span data-ttu-id="88541-110">OS</span><span class="sxs-lookup"><span data-stu-id="88541-110">PARAMETERS</span></span>

### <span data-ttu-id="88541-111">-Comentários</span><span class="sxs-lookup"><span data-stu-id="88541-111">-Comments</span></span>
<span data-ttu-id="88541-112">Especifica os comentários para o log de trabalho.</span><span class="sxs-lookup"><span data-stu-id="88541-112">Specifies the comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88541-113">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="88541-113">-Job</span></span>
<span data-ttu-id="88541-114">Especifica o objeto de trabalho de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="88541-114">Specifies the Site Recovery job object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88541-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="88541-115">-Name</span></span>
<span data-ttu-id="88541-116">Especifica o nome exclusivo para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="88541-116">Specifies the unique name for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88541-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88541-117">-DefaultProfile</span></span>
<span data-ttu-id="88541-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88541-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88541-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88541-119">CommonParameters</span></span>
<span data-ttu-id="88541-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88541-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88541-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88541-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88541-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88541-122">INPUTS</span></span>

### <span data-ttu-id="88541-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="88541-123">ASRJob</span></span>
<span data-ttu-id="88541-124">O parâmetro ' Job ' aceita o valor do tipo ' ASRJob ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="88541-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="88541-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88541-125">OUTPUTS</span></span>

### <span data-ttu-id="88541-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="88541-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="88541-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88541-127">NOTES</span></span>

## <span data-ttu-id="88541-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88541-128">RELATED LINKS</span></span>

[<span data-ttu-id="88541-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="88541-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="88541-130">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="88541-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="88541-131">Parar-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="88541-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
