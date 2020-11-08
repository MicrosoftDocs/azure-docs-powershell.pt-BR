---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: bc93ba739a622a97f418dd7e01d4bbdc7d6824dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124519"
---
# <span data-ttu-id="555cd-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="555cd-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="555cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="555cd-102">SYNOPSIS</span></span>
<span data-ttu-id="555cd-103">Obtém uma tabela de rota de Hub virtual em um hub virtual ou lista todas as tabelas de rotas em um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="555cd-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="555cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="555cd-104">SYNTAX</span></span>

### <span data-ttu-id="555cd-105">ByVirtualHubName (padrão)</span><span class="sxs-lookup"><span data-stu-id="555cd-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="555cd-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="555cd-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="555cd-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="555cd-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="555cd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="555cd-108">DESCRIPTION</span></span>
<span data-ttu-id="555cd-109">Obtém uma tabela de rota de Hub virtual em um hub virtual ou lista todas as tabelas de rotas em um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="555cd-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="555cd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="555cd-110">EXAMPLES</span></span>

### <span data-ttu-id="555cd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="555cd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="555cd-112">Este cmdlet recupera um recurso de tabela de rota usando o nome do grupo de recursos, o nome do Hub e o nome da tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="555cd-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="555cd-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="555cd-113">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded

Name                : routeTable2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable2
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Branches}
ProvisioningState   : Succeeded
```

<span data-ttu-id="555cd-114">Esse cmdlet lista todas as tabelas de rota presentes em um hub virtual usando o nome do grupo de recursos e o nome do Hub.</span><span class="sxs-lookup"><span data-stu-id="555cd-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="555cd-115">OS</span><span class="sxs-lookup"><span data-stu-id="555cd-115">PARAMETERS</span></span>

### <span data-ttu-id="555cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="555cd-116">-DefaultProfile</span></span>
<span data-ttu-id="555cd-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="555cd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="555cd-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="555cd-118">-HubName</span></span>
<span data-ttu-id="555cd-119">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="555cd-119">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555cd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="555cd-120">-Name</span></span>
<span data-ttu-id="555cd-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="555cd-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555cd-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="555cd-122">-ParentResourceId</span></span>
<span data-ttu-id="555cd-123">A ID do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="555cd-123">The parent resource id.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="555cd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="555cd-124">-ResourceGroupName</span></span>
<span data-ttu-id="555cd-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="555cd-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555cd-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="555cd-126">-VirtualHub</span></span>
<span data-ttu-id="555cd-127">O recurso pai.</span><span class="sxs-lookup"><span data-stu-id="555cd-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentObject, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="555cd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555cd-128">CommonParameters</span></span>
<span data-ttu-id="555cd-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="555cd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555cd-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="555cd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555cd-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="555cd-131">INPUTS</span></span>

### <span data-ttu-id="555cd-132">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="555cd-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="555cd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="555cd-133">System.String</span></span>

## <span data-ttu-id="555cd-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="555cd-134">OUTPUTS</span></span>

### <span data-ttu-id="555cd-135">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="555cd-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="555cd-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="555cd-136">NOTES</span></span>

## <span data-ttu-id="555cd-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="555cd-137">RELATED LINKS</span></span>
