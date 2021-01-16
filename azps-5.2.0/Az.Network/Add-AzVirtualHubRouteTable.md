---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262581"
---
# <span data-ttu-id="23f3b-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="23f3b-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="23f3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="23f3b-103">Cria um recurso de tabela de rota de Hub virtual que é filho de VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="23f3b-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="23f3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23f3b-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23f3b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23f3b-105">DESCRIPTION</span></span>
<span data-ttu-id="23f3b-106">O recurso tabela de rota de Hub virtual contém a lista de rotas e uma lista de conexões às quais ela pode ser associada e é usada para direcionar o tráfego em um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="23f3b-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="23f3b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23f3b-107">EXAMPLES</span></span>

### <span data-ttu-id="23f3b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23f3b-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="23f3b-109">O comando acima criará um recurso de tabela de rota de Hub virtual a partir dos roteiros transmitidos a ele e esse objeto poderá ser usado para rotear o tráfego em um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="23f3b-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="23f3b-110">OS</span><span class="sxs-lookup"><span data-stu-id="23f3b-110">PARAMETERS</span></span>

### <span data-ttu-id="23f3b-111">-Conexão</span><span class="sxs-lookup"><span data-stu-id="23f3b-111">-Connection</span></span>
<span data-ttu-id="23f3b-112">Lista de conexões às quais esta tabela de rotas está anexada.</span><span class="sxs-lookup"><span data-stu-id="23f3b-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="23f3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f3b-113">-DefaultProfile</span></span>
<span data-ttu-id="23f3b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23f3b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23f3b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="23f3b-115">-Name</span></span>
<span data-ttu-id="23f3b-116">Nome da tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="23f3b-116">Name of the route table.</span></span>

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

### <span data-ttu-id="23f3b-117">-Rota</span><span class="sxs-lookup"><span data-stu-id="23f3b-117">-Route</span></span>
<span data-ttu-id="23f3b-118">Lista de rotas de Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="23f3b-118">List of virtual hub routes.</span></span>

```yaml
Type: PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f3b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f3b-119">CommonParameters</span></span>
<span data-ttu-id="23f3b-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f3b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f3b-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23f3b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f3b-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23f3b-122">INPUTS</span></span>

### <span data-ttu-id="23f3b-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="23f3b-123">None</span></span>

## <span data-ttu-id="23f3b-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23f3b-124">OUTPUTS</span></span>

### <span data-ttu-id="23f3b-125">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="23f3b-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="23f3b-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23f3b-126">NOTES</span></span>

## <span data-ttu-id="23f3b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23f3b-127">RELATED LINKS</span></span>
