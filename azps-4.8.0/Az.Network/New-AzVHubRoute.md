---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 7dce18ce266bbd2e92f09039b1772acfc618dbdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110504"
---
# <span data-ttu-id="b310f-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="b310f-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="b310f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b310f-102">SYNOPSIS</span></span>
<span data-ttu-id="b310f-103">Cria um objeto VHubRoute que pode ser passado como parâmetro para o comando New-AzVHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="b310f-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="b310f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b310f-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b310f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b310f-105">DESCRIPTION</span></span>

<span data-ttu-id="b310f-106">Cria um objeto VHubRoute.</span><span class="sxs-lookup"><span data-stu-id="b310f-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="b310f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b310f-107">EXAMPLES</span></span>

### <span data-ttu-id="b310f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b310f-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="b310f-109">O comando acima criará um objeto VHubRoute com nextHop como o firewall especificado que pode ser adicionado a um recurso do VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="b310f-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="b310f-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b310f-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="b310f-111">O comando acima criará um objeto VHubRoute com nextHop como o hubVnetConnection especificado que pode então ser adicionado a um recurso VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="b310f-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>

## <span data-ttu-id="b310f-112">OS</span><span class="sxs-lookup"><span data-stu-id="b310f-112">PARAMETERS</span></span>

### <span data-ttu-id="b310f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b310f-113">-DefaultProfile</span></span>
<span data-ttu-id="b310f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b310f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b310f-115">-Destino</span><span class="sxs-lookup"><span data-stu-id="b310f-115">-Destination</span></span>
<span data-ttu-id="b310f-116">Lista de destinos.</span><span class="sxs-lookup"><span data-stu-id="b310f-116">List of Destinations.</span></span>

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

### <span data-ttu-id="b310f-117">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="b310f-117">-DestinationType</span></span>
<span data-ttu-id="b310f-118">Tipo de destinos.</span><span class="sxs-lookup"><span data-stu-id="b310f-118">Type of Destinations.</span></span>

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

### <span data-ttu-id="b310f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b310f-119">-Name</span></span>
<span data-ttu-id="b310f-120">O nome da rota.</span><span class="sxs-lookup"><span data-stu-id="b310f-120">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b310f-121">-NextHop</span><span class="sxs-lookup"><span data-stu-id="b310f-121">-NextHop</span></span>
<span data-ttu-id="b310f-122">O próximo nó.</span><span class="sxs-lookup"><span data-stu-id="b310f-122">The next hop.</span></span>

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

### <span data-ttu-id="b310f-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="b310f-123">-NextHopType</span></span>
<span data-ttu-id="b310f-124">O próximo tipo de salto.</span><span class="sxs-lookup"><span data-stu-id="b310f-124">The Next Hop type.</span></span>

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

### <span data-ttu-id="b310f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b310f-125">CommonParameters</span></span>
<span data-ttu-id="b310f-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b310f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b310f-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b310f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b310f-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b310f-128">INPUTS</span></span>

### <span data-ttu-id="b310f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b310f-129">System.String</span></span>

## <span data-ttu-id="b310f-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b310f-130">OUTPUTS</span></span>

### <span data-ttu-id="b310f-131">Microsoft. Azure. Commands. Network. Models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="b310f-131">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="b310f-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b310f-132">NOTES</span></span>

## <span data-ttu-id="b310f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b310f-133">RELATED LINKS</span></span>

[<span data-ttu-id="b310f-134">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b310f-134">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="b310f-135">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b310f-135">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="b310f-136">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b310f-136">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="b310f-137">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b310f-137">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)