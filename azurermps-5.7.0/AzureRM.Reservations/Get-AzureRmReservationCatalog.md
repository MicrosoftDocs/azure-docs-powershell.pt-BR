---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 4714b97773583197807d6ca54152ee25ab520909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429702"
---
# <span data-ttu-id="ea931-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="ea931-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="ea931-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea931-102">SYNOPSIS</span></span>
<span data-ttu-id="ea931-103">Obter o catálogo de reservas disponíveis</span><span class="sxs-lookup"><span data-stu-id="ea931-103">Get the catalog of available reservation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea931-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea931-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="ea931-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea931-105">DESCRIPTION</span></span>
<span data-ttu-id="ea931-106">Obtenha as regiões e SKUs disponíveis para a compra de instância reservada da assinatura do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="ea931-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="ea931-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea931-107">EXAMPLES</span></span>

### <span data-ttu-id="ea931-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea931-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog
```

<span data-ttu-id="ea931-109">Obter o catálogo para a assinatura padrão</span><span class="sxs-lookup"><span data-stu-id="ea931-109">Get the catalog for the default subscription</span></span>

### <span data-ttu-id="ea931-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ea931-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="ea931-111">Obter o catálogo para a assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="ea931-111">Get the catalog for the specified subscription</span></span>

## <span data-ttu-id="ea931-112">OS</span><span class="sxs-lookup"><span data-stu-id="ea931-112">PARAMETERS</span></span>

### <span data-ttu-id="ea931-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea931-113">-SubscriptionId</span></span>
<span data-ttu-id="ea931-114">ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="ea931-114">Id of the subscription</span></span>

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

### <span data-ttu-id="ea931-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea931-115">CommonParameters</span></span>
<span data-ttu-id="ea931-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea931-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea931-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea931-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea931-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea931-118">INPUTS</span></span>

### <span data-ttu-id="ea931-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ea931-119">None</span></span>

## <span data-ttu-id="ea931-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea931-120">OUTPUTS</span></span>

### <span data-ttu-id="ea931-121">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. reservas. Models. PSCatalog, Microsoft. Azure. Commands. reservas, Version = 1.0.0.0, Culture = neutro, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ea931-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSCatalog, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ea931-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea931-122">NOTES</span></span>

## <span data-ttu-id="ea931-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea931-123">RELATED LINKS</span></span>

