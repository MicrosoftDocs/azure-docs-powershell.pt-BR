---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 1c8d061dae3d2334b422e6f9e4e3c2b7bb75abcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440169"
---
# <span data-ttu-id="87530-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="87530-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="87530-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87530-102">SYNOPSIS</span></span>
<span data-ttu-id="87530-103">Obtém um mapeamento de classificação de armazenamento na recuperação do site.</span><span class="sxs-lookup"><span data-stu-id="87530-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87530-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87530-104">SYNTAX</span></span>

### <span data-ttu-id="87530-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="87530-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87530-106">ByName</span><span class="sxs-lookup"><span data-stu-id="87530-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87530-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87530-107">DESCRIPTION</span></span>
<span data-ttu-id="87530-108">O cmdlet **Get-AzureRmSiteRecoveryStorageClassificationMapping** Obtém um mapeamento de classificação de armazenamento no Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="87530-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="87530-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87530-109">EXAMPLES</span></span>

## <span data-ttu-id="87530-110">OS</span><span class="sxs-lookup"><span data-stu-id="87530-110">PARAMETERS</span></span>

### <span data-ttu-id="87530-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="87530-111">-Name</span></span>
<span data-ttu-id="87530-112">Especifica o nome do mapeamento de classificação de armazenamento que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="87530-112">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

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

### <span data-ttu-id="87530-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87530-113">-DefaultProfile</span></span>
<span data-ttu-id="87530-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87530-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87530-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87530-115">CommonParameters</span></span>
<span data-ttu-id="87530-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87530-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87530-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87530-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87530-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87530-118">INPUTS</span></span>

## <span data-ttu-id="87530-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87530-119">OUTPUTS</span></span>

### <span data-ttu-id="87530-120">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassificationMapping]</span><span class="sxs-lookup"><span data-stu-id="87530-120">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="87530-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87530-121">NOTES</span></span>

## <span data-ttu-id="87530-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87530-122">RELATED LINKS</span></span>

[<span data-ttu-id="87530-123">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="87530-123">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="87530-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="87530-124">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
