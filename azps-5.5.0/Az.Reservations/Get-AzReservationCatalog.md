---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118142"
---
# <span data-ttu-id="af53c-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="af53c-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="af53c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af53c-102">SYNOPSIS</span></span>
<span data-ttu-id="af53c-103">Obter o catálogo de reservas disponíveis</span><span class="sxs-lookup"><span data-stu-id="af53c-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="af53c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af53c-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af53c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="af53c-105">DESCRIPTION</span></span>
<span data-ttu-id="af53c-106">Obter as regiões e SKUs que estão disponíveis para compra de Instância Reservada para a assinatura especificada do Azure.</span><span class="sxs-lookup"><span data-stu-id="af53c-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="af53c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="af53c-107">EXAMPLES</span></span>

### <span data-ttu-id="af53c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af53c-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="af53c-109">Obter o catálogo VirtualMachines em westus para a assinatura padrão</span><span class="sxs-lookup"><span data-stu-id="af53c-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="af53c-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="af53c-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="af53c-111">Obter o catálogo SuseLinux para a assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="af53c-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="af53c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af53c-112">PARAMETERS</span></span>

### <span data-ttu-id="af53c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af53c-113">-DefaultProfile</span></span>
<span data-ttu-id="af53c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af53c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af53c-115">-Local</span><span class="sxs-lookup"><span data-stu-id="af53c-115">-Location</span></span>
<span data-ttu-id="af53c-116">Especifica o local dos recursos reservados no catálogo</span><span class="sxs-lookup"><span data-stu-id="af53c-116">Specifies the location of the reserved resources in the catalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af53c-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="af53c-117">-ReservedResourceType</span></span>
<span data-ttu-id="af53c-118">Especifica o tipo de recursos reservados no catálogo</span><span class="sxs-lookup"><span data-stu-id="af53c-118">Specifies the type of the reserved resources in the catalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af53c-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af53c-119">-SubscriptionId</span></span>
<span data-ttu-id="af53c-120">ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="af53c-120">Id of the subscription</span></span>

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

### <span data-ttu-id="af53c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af53c-121">CommonParameters</span></span>
<span data-ttu-id="af53c-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af53c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af53c-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af53c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af53c-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="af53c-124">INPUTS</span></span>

### <span data-ttu-id="af53c-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="af53c-125">None</span></span>

## <span data-ttu-id="af53c-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="af53c-126">OUTPUTS</span></span>

### <span data-ttu-id="af53c-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span><span class="sxs-lookup"><span data-stu-id="af53c-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="af53c-128">Notas</span><span class="sxs-lookup"><span data-stu-id="af53c-128">NOTES</span></span>

## <span data-ttu-id="af53c-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af53c-129">RELATED LINKS</span></span>
