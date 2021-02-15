---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112912"
---
# <span data-ttu-id="a7296-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a7296-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="a7296-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7296-102">SYNOPSIS</span></span>
<span data-ttu-id="a7296-103">Cria um objeto VirtualHubRoute que pode ser passado como parâmetro para o Add-AzVirtualHubRouteTable comando.</span><span class="sxs-lookup"><span data-stu-id="a7296-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="a7296-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7296-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7296-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7296-105">DESCRIPTION</span></span>
<span data-ttu-id="a7296-106">Cria um objeto VirtualHubRoute.</span><span class="sxs-lookup"><span data-stu-id="a7296-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="a7296-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7296-107">EXAMPLES</span></span>

### <span data-ttu-id="a7296-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7296-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="a7296-109">O comando acima criará um objeto VirtualHubRoute que pode ser adicionado a um recurso VirtualHubRouteTable e definido como um VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="a7296-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="a7296-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7296-110">PARAMETERS</span></span>

### <span data-ttu-id="a7296-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7296-111">-DefaultProfile</span></span>
<span data-ttu-id="a7296-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7296-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-113">-Destino</span><span class="sxs-lookup"><span data-stu-id="a7296-113">-Destination</span></span>
<span data-ttu-id="a7296-114">Lista de Destinos.</span><span class="sxs-lookup"><span data-stu-id="a7296-114">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="a7296-115">-DestinationType</span></span>
<span data-ttu-id="a7296-116">Tipo de Destinos.</span><span class="sxs-lookup"><span data-stu-id="a7296-116">Type of Destinations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="a7296-117">-NextHop</span></span>
<span data-ttu-id="a7296-118">Lista de próximos saltos.</span><span class="sxs-lookup"><span data-stu-id="a7296-118">List of Next hops.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-119">-NextType</span><span class="sxs-lookup"><span data-stu-id="a7296-119">-NextHopType</span></span>
<span data-ttu-id="a7296-120">O tipo Próximo Salto.</span><span class="sxs-lookup"><span data-stu-id="a7296-120">The Next Hop type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7296-121">CommonParameters</span></span>
<span data-ttu-id="a7296-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7296-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7296-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7296-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7296-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="a7296-124">INPUTS</span></span>

### <span data-ttu-id="a7296-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a7296-125">None</span></span>

## <span data-ttu-id="a7296-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="a7296-126">OUTPUTS</span></span>

### <span data-ttu-id="a7296-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="a7296-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="a7296-128">Notas</span><span class="sxs-lookup"><span data-stu-id="a7296-128">NOTES</span></span>

## <span data-ttu-id="a7296-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7296-129">RELATED LINKS</span></span>
