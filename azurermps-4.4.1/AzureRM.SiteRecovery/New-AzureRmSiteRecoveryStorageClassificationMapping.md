---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2520dd90eed1362f4d499eb88ce88dec33f1338c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427773"
---
# <span data-ttu-id="2060d-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2060d-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="2060d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2060d-102">SYNOPSIS</span></span>
<span data-ttu-id="2060d-103">Cria um mapeamento de classificação de armazenamento na recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="2060d-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2060d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2060d-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2060d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2060d-105">DESCRIPTION</span></span>
<span data-ttu-id="2060d-106">O cmdlet **New-AzureRmSiteRecoveryStorageClassificationMapping** cria um mapeamento de classificação de armazenamento no Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2060d-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="2060d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2060d-107">EXAMPLES</span></span>

## <span data-ttu-id="2060d-108">OS</span><span class="sxs-lookup"><span data-stu-id="2060d-108">PARAMETERS</span></span>

### <span data-ttu-id="2060d-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="2060d-109">-Name</span></span>
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

### <span data-ttu-id="2060d-110">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2060d-110">-PrimaryStorageClassification</span></span>
<span data-ttu-id="2060d-111">Especifica o mapeamento de classificação de armazenamento principal.</span><span class="sxs-lookup"><span data-stu-id="2060d-111">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2060d-112">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2060d-112">-RecoveryStorageClassification</span></span>
<span data-ttu-id="2060d-113">Especifica um mapeamento de classificação de armazenamento de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2060d-113">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2060d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2060d-114">-DefaultProfile</span></span>
<span data-ttu-id="2060d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2060d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2060d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2060d-116">CommonParameters</span></span>
<span data-ttu-id="2060d-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2060d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2060d-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2060d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2060d-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2060d-119">INPUTS</span></span>

### <span data-ttu-id="2060d-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="2060d-120">ASRStorageClassification</span></span>
<span data-ttu-id="2060d-121">O parâmetro ' PrimaryStorageClassification ' aceita o valor do tipo ' ASRStorageClassification ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2060d-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="2060d-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2060d-122">OUTPUTS</span></span>

### <span data-ttu-id="2060d-123">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2060d-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2060d-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2060d-124">NOTES</span></span>

## <span data-ttu-id="2060d-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2060d-125">RELATED LINKS</span></span>

[<span data-ttu-id="2060d-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2060d-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="2060d-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="2060d-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
