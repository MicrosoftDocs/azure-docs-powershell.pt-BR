---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262901"
---
# <span data-ttu-id="78f5f-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="78f5f-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="78f5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="78f5f-103">Excluir um recurso de tabela de rota de Hub virtual associado a um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="78f5f-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="78f5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78f5f-104">SYNTAX</span></span>

### <span data-ttu-id="78f5f-105">ByVirtualHubRouteTableName (padrão)</span><span class="sxs-lookup"><span data-stu-id="78f5f-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f5f-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="78f5f-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f5f-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="78f5f-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f5f-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="78f5f-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f5f-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78f5f-109">DESCRIPTION</span></span>
<span data-ttu-id="78f5f-110">Exclui a tabela de rotas especificada que está associada ao Hub virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="78f5f-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="78f5f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78f5f-111">EXAMPLES</span></span>

### <span data-ttu-id="78f5f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78f5f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="78f5f-113">Esse comando exclui o routeTable1 do Hub virtual westushub.</span><span class="sxs-lookup"><span data-stu-id="78f5f-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="78f5f-114">OS</span><span class="sxs-lookup"><span data-stu-id="78f5f-114">PARAMETERS</span></span>

### <span data-ttu-id="78f5f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78f5f-115">-AsJob</span></span>
<span data-ttu-id="78f5f-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="78f5f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78f5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f5f-117">-DefaultProfile</span></span>
<span data-ttu-id="78f5f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78f5f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78f5f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="78f5f-119">-Force</span></span>
<span data-ttu-id="78f5f-120">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="78f5f-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="78f5f-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="78f5f-121">-HubName</span></span>
<span data-ttu-id="78f5f-122">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="78f5f-122">The parent resource name.</span></span>

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

### <span data-ttu-id="78f5f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78f5f-123">-InputObject</span></span>
<span data-ttu-id="78f5f-124">O recurso virtualhubroutetable a ser removido.</span><span class="sxs-lookup"><span data-stu-id="78f5f-124">The virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="78f5f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="78f5f-125">-Name</span></span>
<span data-ttu-id="78f5f-126">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="78f5f-126">The resource name.</span></span>

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

### <span data-ttu-id="78f5f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78f5f-127">-PassThru</span></span>
<span data-ttu-id="78f5f-128">Retorna um objeto que representa o item em que essa operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="78f5f-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="78f5f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f5f-129">-ResourceGroupName</span></span>
<span data-ttu-id="78f5f-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="78f5f-130">The resource group name.</span></span>

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

### <span data-ttu-id="78f5f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78f5f-131">-ResourceId</span></span>
<span data-ttu-id="78f5f-132">A ID do recurso do recurso virtualhubroutetable a ser removido.</span><span class="sxs-lookup"><span data-stu-id="78f5f-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="78f5f-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="78f5f-133">-VirtualHub</span></span>
<span data-ttu-id="78f5f-134">{{Fill VirtualHub descrição}}</span><span class="sxs-lookup"><span data-stu-id="78f5f-134">{{ Fill VirtualHub Description }}</span></span>

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

### <span data-ttu-id="78f5f-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="78f5f-135">-Confirm</span></span>
<span data-ttu-id="78f5f-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78f5f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f5f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f5f-137">-WhatIf</span></span>
<span data-ttu-id="78f5f-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="78f5f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78f5f-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78f5f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78f5f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f5f-140">CommonParameters</span></span>
<span data-ttu-id="78f5f-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f5f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f5f-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78f5f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f5f-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78f5f-143">INPUTS</span></span>

### <span data-ttu-id="78f5f-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="78f5f-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="78f5f-145">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="78f5f-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="78f5f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="78f5f-146">System.String</span></span>

## <span data-ttu-id="78f5f-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78f5f-147">OUTPUTS</span></span>

### <span data-ttu-id="78f5f-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78f5f-148">System.Boolean</span></span>

## <span data-ttu-id="78f5f-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78f5f-149">NOTES</span></span>

## <span data-ttu-id="78f5f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78f5f-150">RELATED LINKS</span></span>
