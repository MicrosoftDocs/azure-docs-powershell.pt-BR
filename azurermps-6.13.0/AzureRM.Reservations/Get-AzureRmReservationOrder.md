---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 12e76c3412f54ba840528f9ff1a40acd388cd109
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428392"
---
# <span data-ttu-id="cc112-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="cc112-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="cc112-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc112-102">SYNOPSIS</span></span>
<span data-ttu-id="cc112-103">Obter `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="cc112-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc112-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc112-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc112-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc112-105">DESCRIPTION</span></span>
<span data-ttu-id="cc112-106">Lista de todos os `ReservationOrder` s aos quais o usuário tem acesso no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="cc112-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="cc112-107">Se o parâmetro ReservationOrderId estiver definido, obtenha essa ReservationOrder específica.</span><span class="sxs-lookup"><span data-stu-id="cc112-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="cc112-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc112-108">EXAMPLES</span></span>

### <span data-ttu-id="cc112-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cc112-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="cc112-110">Listar todos os `ReservationOrder` usuários que o usuário tem acesso ao locatário atual</span><span class="sxs-lookup"><span data-stu-id="cc112-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="cc112-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cc112-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="cc112-112">Obter `ReservationOrder` com o ReservationOrderId especificado</span><span class="sxs-lookup"><span data-stu-id="cc112-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="cc112-113">OS</span><span class="sxs-lookup"><span data-stu-id="cc112-113">PARAMETERS</span></span>

### <span data-ttu-id="cc112-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc112-114">-DefaultProfile</span></span>
<span data-ttu-id="cc112-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc112-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc112-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="cc112-116">-ReservationOrderId</span></span>
<span data-ttu-id="cc112-117">ID do ReservationOrder específico que o usuário quer ver</span><span class="sxs-lookup"><span data-stu-id="cc112-117">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc112-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc112-118">CommonParameters</span></span>
<span data-ttu-id="cc112-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc112-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc112-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc112-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc112-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc112-121">INPUTS</span></span>

### <span data-ttu-id="cc112-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cc112-122">None</span></span>

## <span data-ttu-id="cc112-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc112-123">OUTPUTS</span></span>

### <span data-ttu-id="cc112-124">Microsoft. Azure. Commands. reservas. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="cc112-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="cc112-125">Microsoft. Azure. Commands. reservas. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="cc112-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="cc112-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc112-126">NOTES</span></span>

## <span data-ttu-id="cc112-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc112-127">RELATED LINKS</span></span>
