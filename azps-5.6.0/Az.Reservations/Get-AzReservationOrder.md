---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 1878237544cc1b44b5e47814f455638c168e2412
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891686"
---
# <span data-ttu-id="5f0e2-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="5f0e2-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="5f0e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f0e2-102">SYNOPSIS</span></span>
<span data-ttu-id="5f0e2-103">Obter `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="5f0e2-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="5f0e2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5f0e2-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f0e2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5f0e2-105">DESCRIPTION</span></span>
<span data-ttu-id="5f0e2-106">Lista de todos os `ReservationOrder` s aos que o usuário tem acesso no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="5f0e2-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="5f0e2-107">Se o parâmetro ReservationOrderId estiver definido, obter esse ReservationOrder específico.</span><span class="sxs-lookup"><span data-stu-id="5f0e2-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="5f0e2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f0e2-108">EXAMPLES</span></span>

### <span data-ttu-id="5f0e2-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5f0e2-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="5f0e2-110">Listar `ReservationOrder` tudo o que o usuário tem acesso no locatário atual</span><span class="sxs-lookup"><span data-stu-id="5f0e2-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="5f0e2-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5f0e2-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="5f0e2-112">Obter `ReservationOrder` com o ReservationOrderId especificado</span><span class="sxs-lookup"><span data-stu-id="5f0e2-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="5f0e2-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5f0e2-113">PARAMETERS</span></span>

### <span data-ttu-id="5f0e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f0e2-114">-DefaultProfile</span></span>
<span data-ttu-id="5f0e2-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f0e2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0e2-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="5f0e2-116">-ReservationOrderId</span></span>
<span data-ttu-id="5f0e2-117">Id do ReservationOrder específico que o usuário deseja ver</span><span class="sxs-lookup"><span data-stu-id="5f0e2-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="5f0e2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f0e2-118">CommonParameters</span></span>
<span data-ttu-id="5f0e2-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f0e2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f0e2-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f0e2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f0e2-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f0e2-121">INPUTS</span></span>

### <span data-ttu-id="5f0e2-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5f0e2-122">None</span></span>

## <span data-ttu-id="5f0e2-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5f0e2-123">OUTPUTS</span></span>

### <span data-ttu-id="5f0e2-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="5f0e2-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="5f0e2-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="5f0e2-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="5f0e2-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="5f0e2-126">NOTES</span></span>

## <span data-ttu-id="5f0e2-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f0e2-127">RELATED LINKS</span></span>
