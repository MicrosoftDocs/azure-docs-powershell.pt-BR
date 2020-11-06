---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F3E1BEB5-B565-4618-9AEF-DB85A1AB2163
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 869b22c881652680be31c541c6d70d95a45be43d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429075"
---
# <span data-ttu-id="19634-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="19634-101">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="19634-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19634-102">SYNOPSIS</span></span>
<span data-ttu-id="19634-103">Obtém mapeamentos de contêiner de proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="19634-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19634-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19634-104">SYNTAX</span></span>

### <span data-ttu-id="19634-105">ByObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="19634-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19634-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="19634-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19634-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19634-107">DESCRIPTION</span></span>
<span data-ttu-id="19634-108">O cmdlet **Get-AzureRmSiteRecoveryProtectionContainerMapping** Obtém informações sobre o contêiner de proteção para mapeamentos de política no cofre.</span><span class="sxs-lookup"><span data-stu-id="19634-108">The **Get-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet gets information about the Protection Container to Policy mappings in the vault.</span></span>

## <span data-ttu-id="19634-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19634-109">EXAMPLES</span></span>

## <span data-ttu-id="19634-110">OS</span><span class="sxs-lookup"><span data-stu-id="19634-110">PARAMETERS</span></span>

### <span data-ttu-id="19634-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="19634-111">-Name</span></span>
<span data-ttu-id="19634-112">Especifica o nome do mapeamento de contêiner de proteção.</span><span class="sxs-lookup"><span data-stu-id="19634-112">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19634-113">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="19634-113">-ProtectionContainer</span></span>
<span data-ttu-id="19634-114">Especifica o objeto contêiner da proteção do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="19634-114">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19634-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19634-115">-DefaultProfile</span></span>
<span data-ttu-id="19634-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19634-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19634-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19634-117">CommonParameters</span></span>
<span data-ttu-id="19634-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19634-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19634-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19634-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19634-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19634-120">INPUTS</span></span>

### <span data-ttu-id="19634-121">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="19634-121">ASRProtectionContainer</span></span>
<span data-ttu-id="19634-122">O parâmetro ' ProtectionContainer ' aceita o valor do tipo ' ASRProtectionContainer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="19634-122">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="19634-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19634-123">OUTPUTS</span></span>

### <span data-ttu-id="19634-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainerMapping, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="19634-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="19634-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19634-125">NOTES</span></span>

## <span data-ttu-id="19634-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19634-126">RELATED LINKS</span></span>

[<span data-ttu-id="19634-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="19634-127">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="19634-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="19634-128">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
