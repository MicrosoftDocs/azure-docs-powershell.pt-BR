---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: bc93ba739a622a97f418dd7e01d4bbdc7d6824dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115147"
---
# <span data-ttu-id="de618-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="de618-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="de618-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de618-102">SYNOPSIS</span></span>
<span data-ttu-id="de618-103">Obtém uma Tabela de Rota do Hub Virtual em um hub virtual ou lista todas as tabelas de rota em um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="de618-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="de618-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de618-104">SYNTAX</span></span>

### <span data-ttu-id="de618-105">ByVirtualHubName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="de618-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de618-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="de618-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de618-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="de618-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de618-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="de618-108">DESCRIPTION</span></span>
<span data-ttu-id="de618-109">Obtém uma Tabela de Rota do Hub Virtual em um hub virtual ou lista todas as tabelas de rota em um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="de618-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="de618-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="de618-110">EXAMPLES</span></span>

### <span data-ttu-id="de618-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de618-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="de618-112">Esse cmdlet recupera um recurso de tabela de rota usando o nome do grupo de recursos, o nome do hub e o nome da tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="de618-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="de618-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="de618-113">Example 2</span></span>
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

<span data-ttu-id="de618-114">Este cmdlet lista todas as tabelas de rota presentes em um hub virtual usando o nome do grupo de recursos e o nome do hub.</span><span class="sxs-lookup"><span data-stu-id="de618-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="de618-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de618-115">PARAMETERS</span></span>

### <span data-ttu-id="de618-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de618-116">-DefaultProfile</span></span>
<span data-ttu-id="de618-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de618-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de618-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="de618-118">-HubName</span></span>
<span data-ttu-id="de618-119">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="de618-119">The parent resource name.</span></span>

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

### <span data-ttu-id="de618-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="de618-120">-Name</span></span>
<span data-ttu-id="de618-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="de618-121">The resource name.</span></span>

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

### <span data-ttu-id="de618-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="de618-122">-ParentResourceId</span></span>
<span data-ttu-id="de618-123">A ID do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="de618-123">The parent resource id.</span></span>

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

### <span data-ttu-id="de618-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de618-124">-ResourceGroupName</span></span>
<span data-ttu-id="de618-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de618-125">The resource group name.</span></span>

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

### <span data-ttu-id="de618-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="de618-126">-VirtualHub</span></span>
<span data-ttu-id="de618-127">O recurso pai.</span><span class="sxs-lookup"><span data-stu-id="de618-127">The parent resource.</span></span>

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

### <span data-ttu-id="de618-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de618-128">CommonParameters</span></span>
<span data-ttu-id="de618-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de618-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de618-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de618-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de618-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="de618-131">INPUTS</span></span>

### <span data-ttu-id="de618-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="de618-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="de618-133">System.String</span><span class="sxs-lookup"><span data-stu-id="de618-133">System.String</span></span>

## <span data-ttu-id="de618-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="de618-134">OUTPUTS</span></span>

### <span data-ttu-id="de618-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="de618-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="de618-136">Notas</span><span class="sxs-lookup"><span data-stu-id="de618-136">NOTES</span></span>

## <span data-ttu-id="de618-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de618-137">RELATED LINKS</span></span>
