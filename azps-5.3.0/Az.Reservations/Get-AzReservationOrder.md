---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428770"
---
# <span data-ttu-id="40907-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="40907-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="40907-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40907-102">SYNOPSIS</span></span>
<span data-ttu-id="40907-103">Obter `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="40907-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="40907-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40907-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40907-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40907-105">DESCRIPTION</span></span>
<span data-ttu-id="40907-106">Lista de todos os `ReservationOrder` s aos quais o usuário tem acesso no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="40907-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="40907-107">Se o parâmetro ReservationOrderId estiver definido, obtenha essa ReservationOrder específica.</span><span class="sxs-lookup"><span data-stu-id="40907-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="40907-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40907-108">EXAMPLES</span></span>

### <span data-ttu-id="40907-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40907-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="40907-110">Listar todos os `ReservationOrder` usuários que o usuário tem acesso ao locatário atual</span><span class="sxs-lookup"><span data-stu-id="40907-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="40907-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="40907-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="40907-112">Obter `ReservationOrder` com o ReservationOrderId especificado</span><span class="sxs-lookup"><span data-stu-id="40907-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="40907-113">OS</span><span class="sxs-lookup"><span data-stu-id="40907-113">PARAMETERS</span></span>

### <span data-ttu-id="40907-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40907-114">-DefaultProfile</span></span>
<span data-ttu-id="40907-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40907-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40907-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="40907-116">-ReservationOrderId</span></span>
<span data-ttu-id="40907-117">ID do ReservationOrder específico que o usuário quer ver</span><span class="sxs-lookup"><span data-stu-id="40907-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="40907-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40907-118">CommonParameters</span></span>
<span data-ttu-id="40907-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40907-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40907-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40907-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40907-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40907-121">INPUTS</span></span>

### <span data-ttu-id="40907-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="40907-122">None</span></span>

## <span data-ttu-id="40907-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40907-123">OUTPUTS</span></span>

### <span data-ttu-id="40907-124">Microsoft. Azure. Commands. reservas. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="40907-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="40907-125">Microsoft. Azure. Commands. reservas. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="40907-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="40907-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40907-126">NOTES</span></span>

## <span data-ttu-id="40907-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40907-127">RELATED LINKS</span></span>
