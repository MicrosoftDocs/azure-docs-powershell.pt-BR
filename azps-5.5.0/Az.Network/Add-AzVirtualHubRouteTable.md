---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115203"
---
# <span data-ttu-id="678ee-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="678ee-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="678ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="678ee-102">SYNOPSIS</span></span>
<span data-ttu-id="678ee-103">Cria um recurso de Tabela de Rota do Hub Virtual, que é filho do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="678ee-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="678ee-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="678ee-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="678ee-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="678ee-105">DESCRIPTION</span></span>
<span data-ttu-id="678ee-106">O recurso de tabela de rota do hub virtual contém a lista de rotas e uma lista de conexões às quais ele pode ser anexado e é usado para rotear o tráfego em um Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="678ee-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="678ee-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="678ee-107">EXAMPLES</span></span>

### <span data-ttu-id="678ee-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="678ee-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="678ee-109">O comando acima criará um recurso tabela de rota do Hub Virtual a partir das rotas passadas para ele e esse objeto pode ser usado para rotear o tráfego em um Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="678ee-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="678ee-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="678ee-110">PARAMETERS</span></span>

### <span data-ttu-id="678ee-111">-Conexão</span><span class="sxs-lookup"><span data-stu-id="678ee-111">-Connection</span></span>
<span data-ttu-id="678ee-112">Lista de conexões às que esta tabela de rota está anexada.</span><span class="sxs-lookup"><span data-stu-id="678ee-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="678ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678ee-113">-DefaultProfile</span></span>
<span data-ttu-id="678ee-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="678ee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="678ee-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="678ee-115">-Name</span></span>
<span data-ttu-id="678ee-116">Nome da tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="678ee-116">Name of the route table.</span></span>

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

### <span data-ttu-id="678ee-117">-Rota</span><span class="sxs-lookup"><span data-stu-id="678ee-117">-Route</span></span>
<span data-ttu-id="678ee-118">Lista de rotas do hub virtual.</span><span class="sxs-lookup"><span data-stu-id="678ee-118">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="678ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678ee-119">CommonParameters</span></span>
<span data-ttu-id="678ee-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="678ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678ee-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="678ee-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678ee-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="678ee-122">INPUTS</span></span>

### <span data-ttu-id="678ee-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="678ee-123">None</span></span>

## <span data-ttu-id="678ee-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="678ee-124">OUTPUTS</span></span>

### <span data-ttu-id="678ee-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="678ee-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="678ee-126">Notas</span><span class="sxs-lookup"><span data-stu-id="678ee-126">NOTES</span></span>

## <span data-ttu-id="678ee-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="678ee-127">RELATED LINKS</span></span>
