---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114690"
---
# <span data-ttu-id="fd676-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="fd676-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="fd676-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd676-102">SYNOPSIS</span></span>
<span data-ttu-id="fd676-103">Obter o catálogo de reservas disponíveis</span><span class="sxs-lookup"><span data-stu-id="fd676-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="fd676-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd676-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd676-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd676-105">DESCRIPTION</span></span>
<span data-ttu-id="fd676-106">Obtenha as regiões e SKUs disponíveis para a compra de instância reservada da assinatura do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="fd676-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="fd676-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd676-107">EXAMPLES</span></span>

### <span data-ttu-id="fd676-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd676-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="fd676-109">Obter o catálogo VirtualMachines no oesteus para a assinatura padrão</span><span class="sxs-lookup"><span data-stu-id="fd676-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="fd676-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fd676-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="fd676-111">Obter o catálogo SuseLinux para a assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="fd676-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="fd676-112">OS</span><span class="sxs-lookup"><span data-stu-id="fd676-112">PARAMETERS</span></span>

### <span data-ttu-id="fd676-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd676-113">-DefaultProfile</span></span>
<span data-ttu-id="fd676-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd676-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd676-115">-Local</span><span class="sxs-lookup"><span data-stu-id="fd676-115">-Location</span></span>
<span data-ttu-id="fd676-116">Especifica o local dos recursos reservados no catálogo</span><span class="sxs-lookup"><span data-stu-id="fd676-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="fd676-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="fd676-117">-ReservedResourceType</span></span>
<span data-ttu-id="fd676-118">Especifica o tipo dos recursos reservados no catálogo</span><span class="sxs-lookup"><span data-stu-id="fd676-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="fd676-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd676-119">-SubscriptionId</span></span>
<span data-ttu-id="fd676-120">ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="fd676-120">Id of the subscription</span></span>

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

### <span data-ttu-id="fd676-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd676-121">CommonParameters</span></span>
<span data-ttu-id="fd676-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd676-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd676-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd676-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd676-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd676-124">INPUTS</span></span>

### <span data-ttu-id="fd676-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fd676-125">None</span></span>

## <span data-ttu-id="fd676-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd676-126">OUTPUTS</span></span>

### <span data-ttu-id="fd676-127">Microsoft. Azure. Commands. reservas. Models. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="fd676-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="fd676-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd676-128">NOTES</span></span>

## <span data-ttu-id="fd676-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd676-129">RELATED LINKS</span></span>
