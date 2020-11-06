---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 59ae0324a5e42e87192e655352fce074413907ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603315"
---
# <span data-ttu-id="92986-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="92986-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="92986-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92986-102">SYNOPSIS</span></span>
<span data-ttu-id="92986-103">Remove um mapeamento de classificação de armazenamento da recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="92986-103">Removes a storage classification mapping from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92986-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92986-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92986-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92986-105">DESCRIPTION</span></span>
<span data-ttu-id="92986-106">O cmdlet **Remove-AzureRmSiteRecoveryStorageClassificationMapping** remove um mapeamento de classificação de armazenamento do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="92986-106">The **Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet removes a storage classification mapping from Azure Site Recovery.</span></span>

## <span data-ttu-id="92986-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92986-107">EXAMPLES</span></span>

## <span data-ttu-id="92986-108">OS</span><span class="sxs-lookup"><span data-stu-id="92986-108">PARAMETERS</span></span>

### <span data-ttu-id="92986-109">-StorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="92986-109">-StorageClassificationMapping</span></span>
<span data-ttu-id="92986-110">Especifica um mapeamento de classificação de armazenamento que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="92986-110">Specifies a storage classification mapping that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92986-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92986-111">-DefaultProfile</span></span>
<span data-ttu-id="92986-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92986-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92986-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92986-113">CommonParameters</span></span>
<span data-ttu-id="92986-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92986-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92986-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92986-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92986-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92986-116">INPUTS</span></span>

### <span data-ttu-id="92986-117">ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="92986-117">ASRStorageClassificationMapping</span></span>
<span data-ttu-id="92986-118">O parâmetro ' StorageClassificationMapping ' aceita o valor do tipo ' ASRStorageClassificationMapping ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="92986-118">Parameter 'StorageClassificationMapping' accepts value of type 'ASRStorageClassificationMapping' from the pipeline</span></span>

## <span data-ttu-id="92986-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92986-119">OUTPUTS</span></span>

### <span data-ttu-id="92986-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="92986-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="92986-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92986-121">NOTES</span></span>

## <span data-ttu-id="92986-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92986-122">RELATED LINKS</span></span>

[<span data-ttu-id="92986-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="92986-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="92986-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="92986-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)
