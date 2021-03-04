---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: ecec3482c06c77063ebac71788d5bf2058c9ce64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892413"
---
# <span data-ttu-id="2aea5-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2aea5-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="2aea5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aea5-102">SYNOPSIS</span></span>
<span data-ttu-id="2aea5-103">Exclua um recurso de tabela de rota de hub virtual associado a um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="2aea5-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="2aea5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2aea5-104">SYNTAX</span></span>

### <span data-ttu-id="2aea5-105">ByVirtualHubRouteTableName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2aea5-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aea5-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="2aea5-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aea5-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="2aea5-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aea5-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="2aea5-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aea5-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2aea5-109">DESCRIPTION</span></span>
<span data-ttu-id="2aea5-110">Exclui a tabela de rota especificada associada ao hub virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="2aea5-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="2aea5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2aea5-111">EXAMPLES</span></span>

### <span data-ttu-id="2aea5-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2aea5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="2aea5-113">Este comando exclui o routeTable1 do hub virtual westushub.</span><span class="sxs-lookup"><span data-stu-id="2aea5-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="2aea5-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2aea5-114">PARAMETERS</span></span>

### <span data-ttu-id="2aea5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2aea5-115">-AsJob</span></span>
<span data-ttu-id="2aea5-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2aea5-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aea5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aea5-117">-DefaultProfile</span></span>
<span data-ttu-id="2aea5-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2aea5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aea5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2aea5-119">-Force</span></span>
<span data-ttu-id="2aea5-120">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="2aea5-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aea5-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="2aea5-121">-HubName</span></span>
<span data-ttu-id="2aea5-122">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="2aea5-122">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aea5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aea5-123">-InputObject</span></span>
<span data-ttu-id="2aea5-124">O recurso virtualhubroutetable a ser removido.</span><span class="sxs-lookup"><span data-stu-id="2aea5-124">The virtualhubroutetable resource to remove.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: ByVirtualHubRouteTableObject
Aliases: VirtualHubRouteTable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aea5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2aea5-125">-Name</span></span>
<span data-ttu-id="2aea5-126">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="2aea5-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VirtualHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aea5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2aea5-127">-PassThru</span></span>
<span data-ttu-id="2aea5-128">Retorna um objeto que representa o item no qual esta operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="2aea5-128">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aea5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aea5-129">-ResourceGroupName</span></span>
<span data-ttu-id="2aea5-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2aea5-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aea5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aea5-131">-ResourceId</span></span>
<span data-ttu-id="2aea5-132">A id de recurso do recurso virtualhubroutetable a ser removido.</span><span class="sxs-lookup"><span data-stu-id="2aea5-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableResourceId
Aliases: VirtualHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aea5-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="2aea5-133">-VirtualHub</span></span>
<span data-ttu-id="2aea5-134">{{ Fill VirtualHub Description }}</span><span class="sxs-lookup"><span data-stu-id="2aea5-134">{{ Fill VirtualHub Description }}</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, ParentObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aea5-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2aea5-135">-Confirm</span></span>
<span data-ttu-id="2aea5-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aea5-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aea5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aea5-137">-WhatIf</span></span>
<span data-ttu-id="2aea5-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2aea5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aea5-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2aea5-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aea5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aea5-140">CommonParameters</span></span>
<span data-ttu-id="2aea5-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aea5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aea5-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2aea5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aea5-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2aea5-143">INPUTS</span></span>

### <span data-ttu-id="2aea5-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2aea5-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="2aea5-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2aea5-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="2aea5-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2aea5-146">System.String</span></span>

## <span data-ttu-id="2aea5-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2aea5-147">OUTPUTS</span></span>

### <span data-ttu-id="2aea5-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2aea5-148">System.Boolean</span></span>

## <span data-ttu-id="2aea5-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="2aea5-149">NOTES</span></span>

## <span data-ttu-id="2aea5-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2aea5-150">RELATED LINKS</span></span>
