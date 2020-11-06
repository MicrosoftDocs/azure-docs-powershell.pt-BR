---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/restart-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 17486f4a22e488a147fcdd8a8e085c7900fc8147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426592"
---
# <span data-ttu-id="dc98c-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="dc98c-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="dc98c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc98c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc98c-103">Reinicia um trabalho do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="dc98c-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc98c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc98c-104">SYNTAX</span></span>

### <span data-ttu-id="dc98c-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="dc98c-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc98c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dc98c-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc98c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc98c-107">DESCRIPTION</span></span>
<span data-ttu-id="dc98c-108">O cmdlet **Restart-AzureRmSiteRecoveryJob** reinicia um trabalho de recuperação de site do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc98c-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="dc98c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc98c-109">EXAMPLES</span></span>

## <span data-ttu-id="dc98c-110">OS</span><span class="sxs-lookup"><span data-stu-id="dc98c-110">PARAMETERS</span></span>

### <span data-ttu-id="dc98c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc98c-111">-DefaultProfile</span></span>
<span data-ttu-id="dc98c-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc98c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc98c-113">-Trabalho</span><span class="sxs-lookup"><span data-stu-id="dc98c-113">-Job</span></span>
<span data-ttu-id="dc98c-114">Especifica o objeto de trabalho de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="dc98c-114">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="dc98c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc98c-115">-Name</span></span>
<span data-ttu-id="dc98c-116">Especifica o nome exclusivo para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="dc98c-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="dc98c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc98c-117">CommonParameters</span></span>
<span data-ttu-id="dc98c-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc98c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc98c-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc98c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc98c-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc98c-120">INPUTS</span></span>

### <span data-ttu-id="dc98c-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="dc98c-121">ASRJob</span></span>
<span data-ttu-id="dc98c-122">O parâmetro ' Job ' aceita o valor do tipo ' ASRJob ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="dc98c-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="dc98c-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc98c-123">OUTPUTS</span></span>

### <span data-ttu-id="dc98c-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="dc98c-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dc98c-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc98c-125">NOTES</span></span>

## <span data-ttu-id="dc98c-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc98c-126">RELATED LINKS</span></span>

[<span data-ttu-id="dc98c-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="dc98c-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="dc98c-128">Currículo-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="dc98c-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="dc98c-129">Parar-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="dc98c-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
