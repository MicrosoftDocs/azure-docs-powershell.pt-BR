---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264074"
---
# <span data-ttu-id="c2e17-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="c2e17-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="c2e17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2e17-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e17-103">Obter o catálogo de reservas disponíveis</span><span class="sxs-lookup"><span data-stu-id="c2e17-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="c2e17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2e17-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2e17-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2e17-105">DESCRIPTION</span></span>
<span data-ttu-id="c2e17-106">Obtenha as regiões e SKUs disponíveis para a compra de instância reservada da assinatura do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="c2e17-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="c2e17-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2e17-107">EXAMPLES</span></span>

### <span data-ttu-id="c2e17-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c2e17-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="c2e17-109">Obter o catálogo VirtualMachines no oesteus para a assinatura padrão</span><span class="sxs-lookup"><span data-stu-id="c2e17-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="c2e17-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c2e17-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="c2e17-111">Obter o catálogo SuseLinux para a assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="c2e17-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="c2e17-112">OS</span><span class="sxs-lookup"><span data-stu-id="c2e17-112">PARAMETERS</span></span>

### <span data-ttu-id="c2e17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e17-113">-DefaultProfile</span></span>
<span data-ttu-id="c2e17-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2e17-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2e17-115">-Local</span><span class="sxs-lookup"><span data-stu-id="c2e17-115">-Location</span></span>
<span data-ttu-id="c2e17-116">Especifica o local dos recursos reservados no catálogo</span><span class="sxs-lookup"><span data-stu-id="c2e17-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="c2e17-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="c2e17-117">-ReservedResourceType</span></span>
<span data-ttu-id="c2e17-118">Especifica o tipo dos recursos reservados no catálogo</span><span class="sxs-lookup"><span data-stu-id="c2e17-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="c2e17-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2e17-119">-SubscriptionId</span></span>
<span data-ttu-id="c2e17-120">ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="c2e17-120">Id of the subscription</span></span>

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

### <span data-ttu-id="c2e17-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e17-121">CommonParameters</span></span>
<span data-ttu-id="c2e17-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2e17-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e17-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2e17-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e17-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2e17-124">INPUTS</span></span>

### <span data-ttu-id="c2e17-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c2e17-125">None</span></span>

## <span data-ttu-id="c2e17-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2e17-126">OUTPUTS</span></span>

### <span data-ttu-id="c2e17-127">Microsoft. Azure. Commands. reservas. Models. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="c2e17-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="c2e17-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2e17-128">NOTES</span></span>

## <span data-ttu-id="c2e17-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2e17-129">RELATED LINKS</span></span>
