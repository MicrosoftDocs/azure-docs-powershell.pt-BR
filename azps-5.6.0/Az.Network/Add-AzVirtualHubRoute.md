---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: d90d25776f895bee47549dfb08a4588f0e446883
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888855"
---
# <span data-ttu-id="2aec5-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="2aec5-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="2aec5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aec5-102">SYNOPSIS</span></span>
<span data-ttu-id="2aec5-103">Cria um objeto VirtualHubRoute que pode ser passado como parâmetro para o Add-AzVirtualHubRouteTable comando.</span><span class="sxs-lookup"><span data-stu-id="2aec5-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="2aec5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2aec5-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aec5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2aec5-105">DESCRIPTION</span></span>
<span data-ttu-id="2aec5-106">Cria um objeto VirtualHubRoute.</span><span class="sxs-lookup"><span data-stu-id="2aec5-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="2aec5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2aec5-107">EXAMPLES</span></span>

### <span data-ttu-id="2aec5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2aec5-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="2aec5-109">O comando acima criará um objeto VirtualHubRoute que pode ser adicionado a um recurso VirtualHubRouteTable e definido como VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="2aec5-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="2aec5-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2aec5-110">PARAMETERS</span></span>

### <span data-ttu-id="2aec5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aec5-111">-DefaultProfile</span></span>
<span data-ttu-id="2aec5-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2aec5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aec5-113">-Destination</span><span class="sxs-lookup"><span data-stu-id="2aec5-113">-Destination</span></span>
<span data-ttu-id="2aec5-114">Lista de destinos.</span><span class="sxs-lookup"><span data-stu-id="2aec5-114">List of Destinations.</span></span>

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

### <span data-ttu-id="2aec5-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="2aec5-115">-DestinationType</span></span>
<span data-ttu-id="2aec5-116">Tipo de Destinos.</span><span class="sxs-lookup"><span data-stu-id="2aec5-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="2aec5-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="2aec5-117">-NextHop</span></span>
<span data-ttu-id="2aec5-118">Lista de próximos saltos.</span><span class="sxs-lookup"><span data-stu-id="2aec5-118">List of Next hops.</span></span>

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

### <span data-ttu-id="2aec5-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="2aec5-119">-NextHopType</span></span>
<span data-ttu-id="2aec5-120">O tipo Next Hop.</span><span class="sxs-lookup"><span data-stu-id="2aec5-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="2aec5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aec5-121">CommonParameters</span></span>
<span data-ttu-id="2aec5-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aec5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aec5-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2aec5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aec5-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2aec5-124">INPUTS</span></span>

### <span data-ttu-id="2aec5-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2aec5-125">None</span></span>

## <span data-ttu-id="2aec5-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2aec5-126">OUTPUTS</span></span>

### <span data-ttu-id="2aec5-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="2aec5-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="2aec5-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="2aec5-128">NOTES</span></span>

## <span data-ttu-id="2aec5-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2aec5-129">RELATED LINKS</span></span>
