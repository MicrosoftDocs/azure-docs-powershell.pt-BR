---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: 56f0eb8362cef287cea326ea30a559d7efc70573
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885630"
---
# <span data-ttu-id="11ec3-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="11ec3-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="11ec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="11ec3-103">Obtém uma Tabela de Rota de Hub Virtual em um hub virtual ou lista todas as tabelas de rota em um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="11ec3-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="11ec3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="11ec3-104">SYNTAX</span></span>

### <span data-ttu-id="11ec3-105">ByVirtualHubName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="11ec3-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11ec3-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="11ec3-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11ec3-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="11ec3-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11ec3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="11ec3-108">DESCRIPTION</span></span>
<span data-ttu-id="11ec3-109">Obtém uma Tabela de Rota de Hub Virtual em um hub virtual ou lista todas as tabelas de rota em um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="11ec3-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="11ec3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11ec3-110">EXAMPLES</span></span>

### <span data-ttu-id="11ec3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11ec3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="11ec3-112">Este cmdlet recupera um recurso de tabela de rota usando o nome do grupo de recursos, o nome do hub e o nome da tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="11ec3-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="11ec3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="11ec3-113">Example 2</span></span>
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

<span data-ttu-id="11ec3-114">Este cmdlet lista todas as tabelas de rota presentes em um hub virtual usando o nome do grupo de recursos e o nome do hub.</span><span class="sxs-lookup"><span data-stu-id="11ec3-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="11ec3-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="11ec3-115">PARAMETERS</span></span>

### <span data-ttu-id="11ec3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ec3-116">-DefaultProfile</span></span>
<span data-ttu-id="11ec3-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11ec3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11ec3-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="11ec3-118">-HubName</span></span>
<span data-ttu-id="11ec3-119">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="11ec3-119">The parent resource name.</span></span>

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

### <span data-ttu-id="11ec3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="11ec3-120">-Name</span></span>
<span data-ttu-id="11ec3-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="11ec3-121">The resource name.</span></span>

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

### <span data-ttu-id="11ec3-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="11ec3-122">-ParentResourceId</span></span>
<span data-ttu-id="11ec3-123">A ID do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="11ec3-123">The parent resource id.</span></span>

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

### <span data-ttu-id="11ec3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ec3-124">-ResourceGroupName</span></span>
<span data-ttu-id="11ec3-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="11ec3-125">The resource group name.</span></span>

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

### <span data-ttu-id="11ec3-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="11ec3-126">-VirtualHub</span></span>
<span data-ttu-id="11ec3-127">O recurso pai.</span><span class="sxs-lookup"><span data-stu-id="11ec3-127">The parent resource.</span></span>

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

### <span data-ttu-id="11ec3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ec3-128">CommonParameters</span></span>
<span data-ttu-id="11ec3-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11ec3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ec3-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11ec3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ec3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11ec3-131">INPUTS</span></span>

### <span data-ttu-id="11ec3-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="11ec3-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="11ec3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="11ec3-133">System.String</span></span>

## <span data-ttu-id="11ec3-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="11ec3-134">OUTPUTS</span></span>

### <span data-ttu-id="11ec3-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="11ec3-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="11ec3-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="11ec3-136">NOTES</span></span>

## <span data-ttu-id="11ec3-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11ec3-137">RELATED LINKS</span></span>
