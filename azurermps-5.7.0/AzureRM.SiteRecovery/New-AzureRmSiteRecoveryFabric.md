---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 38a7f8ee32f02db10dc971d5be2016d5dea0b538
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426605"
---
# <span data-ttu-id="07a79-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="07a79-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="07a79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07a79-102">SYNOPSIS</span></span>
<span data-ttu-id="07a79-103">Cria uma malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="07a79-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07a79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07a79-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07a79-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07a79-105">DESCRIPTION</span></span>
<span data-ttu-id="07a79-106">O cmdlet **New-AzureRmSiteRecoveryFabric** cria uma malha de recuperação de site do Azure do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="07a79-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="07a79-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07a79-107">EXAMPLES</span></span>

## <span data-ttu-id="07a79-108">OS</span><span class="sxs-lookup"><span data-stu-id="07a79-108">PARAMETERS</span></span>

### <span data-ttu-id="07a79-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a79-109">-DefaultProfile</span></span>
<span data-ttu-id="07a79-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07a79-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07a79-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="07a79-111">-Name</span></span>
<span data-ttu-id="07a79-112">Especifica o nome da malha de recuperação do site do Azure</span><span class="sxs-lookup"><span data-stu-id="07a79-112">Specifies the name of the Azure Site Recovery Fabric</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a79-113">-Digite</span><span class="sxs-lookup"><span data-stu-id="07a79-113">-Type</span></span>
<span data-ttu-id="07a79-114">Especifica o tipo de malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="07a79-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a79-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a79-115">CommonParameters</span></span>
<span data-ttu-id="07a79-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07a79-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a79-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a79-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a79-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07a79-118">INPUTS</span></span>

### <span data-ttu-id="07a79-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="07a79-119">None</span></span>
<span data-ttu-id="07a79-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="07a79-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07a79-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07a79-121">OUTPUTS</span></span>

### <span data-ttu-id="07a79-122">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="07a79-122">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="07a79-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07a79-123">NOTES</span></span>

## <span data-ttu-id="07a79-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07a79-124">RELATED LINKS</span></span>

[<span data-ttu-id="07a79-125">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="07a79-125">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="07a79-126">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="07a79-126">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
