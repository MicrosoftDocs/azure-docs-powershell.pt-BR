---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117196"
---
# <span data-ttu-id="c2ecd-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="c2ecd-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="c2ecd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ecd-103">Obter `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="c2ecd-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="c2ecd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2ecd-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2ecd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2ecd-105">DESCRIPTION</span></span>
<span data-ttu-id="c2ecd-106">Lista de todos os `ReservationOrder` s aos que o usuário tem acesso no locatário atual.</span><span class="sxs-lookup"><span data-stu-id="c2ecd-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="c2ecd-107">Se o parâmetro ReservationOrderId estiver definido, obter essa ReservationOrder específica.</span><span class="sxs-lookup"><span data-stu-id="c2ecd-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="c2ecd-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c2ecd-108">EXAMPLES</span></span>

### <span data-ttu-id="c2ecd-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c2ecd-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="c2ecd-110">Listar `ReservationOrder` tudo o que o usuário tem acesso no locatário atual</span><span class="sxs-lookup"><span data-stu-id="c2ecd-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="c2ecd-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c2ecd-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="c2ecd-112">Obter `ReservationOrder` com a ReservationOrderId especificada</span><span class="sxs-lookup"><span data-stu-id="c2ecd-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="c2ecd-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2ecd-113">PARAMETERS</span></span>

### <span data-ttu-id="c2ecd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ecd-114">-DefaultProfile</span></span>
<span data-ttu-id="c2ecd-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ecd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2ecd-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c2ecd-116">-ReservationOrderId</span></span>
<span data-ttu-id="c2ecd-117">ID da ReservationOrder específica que o usuário deseja ver</span><span class="sxs-lookup"><span data-stu-id="c2ecd-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="c2ecd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ecd-118">CommonParameters</span></span>
<span data-ttu-id="c2ecd-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ecd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ecd-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2ecd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ecd-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="c2ecd-121">INPUTS</span></span>

### <span data-ttu-id="c2ecd-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c2ecd-122">None</span></span>

## <span data-ttu-id="c2ecd-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="c2ecd-123">OUTPUTS</span></span>

### <span data-ttu-id="c2ecd-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="c2ecd-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="c2ecd-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="c2ecd-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="c2ecd-126">Notas</span><span class="sxs-lookup"><span data-stu-id="c2ecd-126">NOTES</span></span>

## <span data-ttu-id="c2ecd-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2ecd-127">RELATED LINKS</span></span>
