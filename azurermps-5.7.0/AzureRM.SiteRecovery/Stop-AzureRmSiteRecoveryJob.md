---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFEA76B4-684C-4C2A-9806-36DC133AEE80
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/stop-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 44875207b5a4317b2ceb9a0284a3818a6be36298
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426589"
---
# <span data-ttu-id="ed1d6-101">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ed1d6-101">Stop-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="ed1d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed1d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ed1d6-103">Interrompe um trabalho de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="ed1d6-103">Stops a Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed1d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed1d6-104">SYNTAX</span></span>

### <span data-ttu-id="ed1d6-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="ed1d6-105">ByObject (Default)</span></span>
```
Stop-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed1d6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ed1d6-106">ByName</span></span>
```
Stop-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed1d6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed1d6-107">DESCRIPTION</span></span>
<span data-ttu-id="ed1d6-108">O cmdlet **Stop-AzureRmSiteRecoveryJob** interrompe um trabalho de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed1d6-108">The **Stop-AzureRmSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="ed1d6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed1d6-109">EXAMPLES</span></span>

## <span data-ttu-id="ed1d6-110">OS</span><span class="sxs-lookup"><span data-stu-id="ed1d6-110">PARAMETERS</span></span>

### <span data-ttu-id="ed1d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed1d6-111">-DefaultProfile</span></span>
<span data-ttu-id="ed1d6-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed1d6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed1d6-113">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="ed1d6-113">-Job</span></span>
<span data-ttu-id="ed1d6-114">Especifica o objeto de trabalho de recuperação de site para parar.</span><span class="sxs-lookup"><span data-stu-id="ed1d6-114">Specifies the Site Recovery job object to stop.</span></span>

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

### <span data-ttu-id="ed1d6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed1d6-115">-Name</span></span>
<span data-ttu-id="ed1d6-116">Especifica o nome exclusivo para o trabalho de recuperação de site parar.</span><span class="sxs-lookup"><span data-stu-id="ed1d6-116">Specifies the unique name for the Site Recovery job to stop.</span></span>

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

### <span data-ttu-id="ed1d6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed1d6-117">CommonParameters</span></span>
<span data-ttu-id="ed1d6-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed1d6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed1d6-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed1d6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed1d6-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed1d6-120">INPUTS</span></span>

### <span data-ttu-id="ed1d6-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="ed1d6-121">ASRJob</span></span>
<span data-ttu-id="ed1d6-122">O parâmetro ' Job ' aceita o valor do tipo ' ASRJob ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="ed1d6-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="ed1d6-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed1d6-123">OUTPUTS</span></span>

### <span data-ttu-id="ed1d6-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ed1d6-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ed1d6-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed1d6-125">NOTES</span></span>

## <span data-ttu-id="ed1d6-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed1d6-126">RELATED LINKS</span></span>

[<span data-ttu-id="ed1d6-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ed1d6-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="ed1d6-128">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ed1d6-128">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="ed1d6-129">Currículo-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ed1d6-129">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)
