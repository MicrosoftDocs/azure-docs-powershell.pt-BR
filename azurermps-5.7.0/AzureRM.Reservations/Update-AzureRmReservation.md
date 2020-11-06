---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 76abdc2f7a7099529af87f69af8e37319685aea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429693"
---
# <span data-ttu-id="16172-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="16172-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="16172-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16172-102">SYNOPSIS</span></span>
<span data-ttu-id="16172-103">Atualizar um `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="16172-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16172-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16172-104">SYNTAX</span></span>

### <span data-ttu-id="16172-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="16172-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -AppliedScopeType <String>
 [-AppliedScope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16172-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="16172-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16172-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16172-107">DESCRIPTION</span></span>
<span data-ttu-id="16172-108">Atualiza os escopos aplicados do `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="16172-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="16172-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16172-109">EXAMPLES</span></span>

### <span data-ttu-id="16172-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16172-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="16172-111">Atualiza o AppliedScopeType da reserva especificada para Single</span><span class="sxs-lookup"><span data-stu-id="16172-111">Updates the AppliedScopeType of the specified reservation to Single</span></span>

### <span data-ttu-id="16172-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="16172-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared"
```

<span data-ttu-id="16172-113">Atualiza o AppliedScopeType da reserva especificada para compartilhada</span><span class="sxs-lookup"><span data-stu-id="16172-113">Updates the AppliedScopeType of the specified reservation to Shared</span></span>

## <span data-ttu-id="16172-114">OS</span><span class="sxs-lookup"><span data-stu-id="16172-114">PARAMETERS</span></span>

### <span data-ttu-id="16172-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="16172-115">-AppliedScope</span></span>
<span data-ttu-id="16172-116">SubscriptionId para `Reservation` ser aplicada</span><span class="sxs-lookup"><span data-stu-id="16172-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="16172-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="16172-117">-AppliedScopeType</span></span>
<span data-ttu-id="16172-118">Tipo de a `Reservation` ser atualizado</span><span class="sxs-lookup"><span data-stu-id="16172-118">Type of the `Reservation` to be updated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Single, Shared

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16172-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16172-119">-DefaultProfile</span></span>
<span data-ttu-id="16172-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16172-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16172-121">-Reserva</span><span class="sxs-lookup"><span data-stu-id="16172-121">-Reservation</span></span>
<span data-ttu-id="16172-122">Parâmetro do objeto pipe para `Reservation`</span><span class="sxs-lookup"><span data-stu-id="16172-122">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16172-123">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="16172-123">-ReservationId</span></span>
<span data-ttu-id="16172-124">ID do `Reservation` a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="16172-124">Id of the `Reservation` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16172-125">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="16172-125">-ReservationOrderId</span></span>
<span data-ttu-id="16172-126">ID do `ReservationOrder` a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="16172-126">Id of the `ReservationOrder` to update</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16172-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="16172-127">-Confirm</span></span>
<span data-ttu-id="16172-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16172-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16172-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16172-129">-WhatIf</span></span>
<span data-ttu-id="16172-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16172-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16172-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16172-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16172-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16172-132">CommonParameters</span></span>
<span data-ttu-id="16172-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16172-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16172-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16172-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16172-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16172-135">INPUTS</span></span>

### <span data-ttu-id="16172-136">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="16172-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="16172-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16172-137">OUTPUTS</span></span>

### <span data-ttu-id="16172-138">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="16172-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="16172-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16172-139">NOTES</span></span>

## <span data-ttu-id="16172-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16172-140">RELATED LINKS</span></span>

