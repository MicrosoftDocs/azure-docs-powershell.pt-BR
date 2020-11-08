---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125829"
---
# <span data-ttu-id="e0709-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e0709-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="e0709-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0709-102">SYNOPSIS</span></span>
<span data-ttu-id="e0709-103">Cria um objeto VirtualHubRoute que pode ser passado como parâmetro para o comando Add-AzVirtualHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="e0709-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="e0709-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0709-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0709-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0709-105">DESCRIPTION</span></span>
<span data-ttu-id="e0709-106">Cria um objeto VirtualHubRoute.</span><span class="sxs-lookup"><span data-stu-id="e0709-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="e0709-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0709-107">EXAMPLES</span></span>

### <span data-ttu-id="e0709-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0709-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="e0709-109">O comando acima criará um objeto VirtualHubRoute que pode ser adicionado a um recurso VirtualHubRouteTable e definido como um VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="e0709-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="e0709-110">OS</span><span class="sxs-lookup"><span data-stu-id="e0709-110">PARAMETERS</span></span>

### <span data-ttu-id="e0709-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0709-111">-DefaultProfile</span></span>
<span data-ttu-id="e0709-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0709-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0709-113">-Destino</span><span class="sxs-lookup"><span data-stu-id="e0709-113">-Destination</span></span>
<span data-ttu-id="e0709-114">Lista de destinos.</span><span class="sxs-lookup"><span data-stu-id="e0709-114">List of Destinations.</span></span>

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

### <span data-ttu-id="e0709-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="e0709-115">-DestinationType</span></span>
<span data-ttu-id="e0709-116">Tipo de destinos.</span><span class="sxs-lookup"><span data-stu-id="e0709-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="e0709-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="e0709-117">-NextHop</span></span>
<span data-ttu-id="e0709-118">Lista de próximos saltos.</span><span class="sxs-lookup"><span data-stu-id="e0709-118">List of Next hops.</span></span>

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

### <span data-ttu-id="e0709-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="e0709-119">-NextHopType</span></span>
<span data-ttu-id="e0709-120">O próximo tipo de salto.</span><span class="sxs-lookup"><span data-stu-id="e0709-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="e0709-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0709-121">CommonParameters</span></span>
<span data-ttu-id="e0709-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0709-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0709-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0709-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0709-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0709-124">INPUTS</span></span>

### <span data-ttu-id="e0709-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e0709-125">None</span></span>

## <span data-ttu-id="e0709-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0709-126">OUTPUTS</span></span>

### <span data-ttu-id="e0709-127">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e0709-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="e0709-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0709-128">NOTES</span></span>

## <span data-ttu-id="e0709-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0709-129">RELATED LINKS</span></span>
