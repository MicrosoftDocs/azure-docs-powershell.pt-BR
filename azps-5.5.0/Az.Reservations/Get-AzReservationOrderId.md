---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 31cccc3c2bde38593bcc1b54d86940f07716a0db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112650"
---
# <span data-ttu-id="47721-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="47721-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="47721-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47721-102">SYNOPSIS</span></span>
<span data-ttu-id="47721-103">Obter lista de `ReservationOrder` IDs aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="47721-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="47721-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47721-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47721-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="47721-105">DESCRIPTION</span></span>
<span data-ttu-id="47721-106">Obter IDs dos `ReservationOrder` s aplicáveis que podem ser aplicadas a esta assinatura.</span><span class="sxs-lookup"><span data-stu-id="47721-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="47721-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47721-107">EXAMPLES</span></span>

### <span data-ttu-id="47721-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47721-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="47721-109">Aplicar-se `ReservationOrder` à assinatura padrão</span><span class="sxs-lookup"><span data-stu-id="47721-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="47721-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="47721-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="47721-111">Aplicar-se `ReservationOrder` à assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="47721-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="47721-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47721-112">PARAMETERS</span></span>

### <span data-ttu-id="47721-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47721-113">-DefaultProfile</span></span>
<span data-ttu-id="47721-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47721-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47721-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47721-115">-SubscriptionId</span></span>
<span data-ttu-id="47721-116">ID da assinatura para obter os `ReservationOrder` s aplicados</span><span class="sxs-lookup"><span data-stu-id="47721-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="47721-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47721-117">CommonParameters</span></span>
<span data-ttu-id="47721-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47721-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47721-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47721-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47721-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="47721-120">INPUTS</span></span>

### <span data-ttu-id="47721-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="47721-121">None</span></span>

## <span data-ttu-id="47721-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="47721-122">OUTPUTS</span></span>

### <span data-ttu-id="47721-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="47721-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="47721-124">Notas</span><span class="sxs-lookup"><span data-stu-id="47721-124">NOTES</span></span>

## <span data-ttu-id="47721-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47721-125">RELATED LINKS</span></span>
