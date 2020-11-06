---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: 395ee4b20ae2c26d05ad66489b3c643d0f4245a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431380"
---
# <span data-ttu-id="e36b5-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e36b5-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="e36b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e36b5-102">SYNOPSIS</span></span>
<span data-ttu-id="e36b5-103">Atualiza um servidor de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="e36b5-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e36b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e36b5-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e36b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e36b5-105">DESCRIPTION</span></span>
<span data-ttu-id="e36b5-106">O cmdlet **set-AzureRmCdnOrigin** atualiza um servidor de origem da CDN (rede de distribuição de conteúdo) do Azure.</span><span class="sxs-lookup"><span data-stu-id="e36b5-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="e36b5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e36b5-107">EXAMPLES</span></span>

## <span data-ttu-id="e36b5-108">OS</span><span class="sxs-lookup"><span data-stu-id="e36b5-108">PARAMETERS</span></span>

### <span data-ttu-id="e36b5-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e36b5-109">-CdnOrigin</span></span>
<span data-ttu-id="e36b5-110">Especifica o servidor de origem no qual esse cmdlet é atualizado.</span><span class="sxs-lookup"><span data-stu-id="e36b5-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e36b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36b5-111">-DefaultProfile</span></span>
<span data-ttu-id="e36b5-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e36b5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e36b5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36b5-113">CommonParameters</span></span>
<span data-ttu-id="e36b5-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36b5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36b5-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e36b5-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36b5-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e36b5-116">INPUTS</span></span>

### <span data-ttu-id="e36b5-117">Microsoft. Azure. Commands. cdn. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="e36b5-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>
<span data-ttu-id="e36b5-118">Parâmetros: CdnOrigin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e36b5-118">Parameters: CdnOrigin (ByValue)</span></span>

## <span data-ttu-id="e36b5-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e36b5-119">OUTPUTS</span></span>

### <span data-ttu-id="e36b5-120">Microsoft. Azure. Commands. cdn. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="e36b5-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="e36b5-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e36b5-121">NOTES</span></span>

## <span data-ttu-id="e36b5-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e36b5-122">RELATED LINKS</span></span>

[<span data-ttu-id="e36b5-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e36b5-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


