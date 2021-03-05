---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: fb7a9933a30760fe3bc33f296b93d6bc739c18eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901600"
---
# <span data-ttu-id="b14e6-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b14e6-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="b14e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b14e6-102">SYNOPSIS</span></span>
<span data-ttu-id="b14e6-103">Exclua um recurso de tabela de rota de hub associado a um VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b14e6-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="b14e6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b14e6-104">SYNTAX</span></span>

### <span data-ttu-id="b14e6-105">ByVHubRouteTableName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b14e6-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b14e6-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="b14e6-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b14e6-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="b14e6-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b14e6-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="b14e6-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b14e6-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b14e6-109">DESCRIPTION</span></span>
<span data-ttu-id="b14e6-110">Exclui a tabela de rota de hub especificada associada ao hub virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="b14e6-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="b14e6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b14e6-111">EXAMPLES</span></span>

### <span data-ttu-id="b14e6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b14e6-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="b14e6-113">Esse comando exclui a tabela de rota do hub do hub virtual.</span><span class="sxs-lookup"><span data-stu-id="b14e6-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="b14e6-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b14e6-114">PARAMETERS</span></span>

### <span data-ttu-id="b14e6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b14e6-115">-AsJob</span></span>
<span data-ttu-id="b14e6-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b14e6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b14e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b14e6-117">-DefaultProfile</span></span>
<span data-ttu-id="b14e6-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b14e6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b14e6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b14e6-119">-Force</span></span>
<span data-ttu-id="b14e6-120">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="b14e6-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b14e6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b14e6-121">-InputObject</span></span>
<span data-ttu-id="b14e6-122">O recurso vhubroutetable a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b14e6-122">The vhubroutetable resource to remove.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b14e6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b14e6-123">-Name</span></span>
<span data-ttu-id="b14e6-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b14e6-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14e6-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b14e6-125">-ParentObject</span></span>
<span data-ttu-id="b14e6-126">O objeto hub virtual pai desse recurso.</span><span class="sxs-lookup"><span data-stu-id="b14e6-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b14e6-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b14e6-127">-ParentResourceName</span></span>
<span data-ttu-id="b14e6-128">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="b14e6-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14e6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b14e6-129">-PassThru</span></span>
<span data-ttu-id="b14e6-130">Retorna um objeto que representa o item no qual esta operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="b14e6-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="b14e6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b14e6-131">-ResourceGroupName</span></span>
<span data-ttu-id="b14e6-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b14e6-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14e6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b14e6-133">-ResourceId</span></span>
<span data-ttu-id="b14e6-134">A id de recurso do recurso vhubroutetable a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b14e6-134">The resource id of the vhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14e6-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b14e6-135">-Confirm</span></span>
<span data-ttu-id="b14e6-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b14e6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b14e6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b14e6-137">-WhatIf</span></span>
<span data-ttu-id="b14e6-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b14e6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b14e6-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b14e6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b14e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b14e6-140">CommonParameters</span></span>
<span data-ttu-id="b14e6-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b14e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b14e6-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b14e6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b14e6-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b14e6-143">INPUTS</span></span>

### <span data-ttu-id="b14e6-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b14e6-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="b14e6-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b14e6-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="b14e6-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b14e6-146">System.String</span></span>

## <span data-ttu-id="b14e6-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b14e6-147">OUTPUTS</span></span>

### <span data-ttu-id="b14e6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b14e6-148">System.Boolean</span></span>

## <span data-ttu-id="b14e6-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="b14e6-149">NOTES</span></span>

## <span data-ttu-id="b14e6-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b14e6-150">RELATED LINKS</span></span>

[<span data-ttu-id="b14e6-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b14e6-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="b14e6-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="b14e6-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="b14e6-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b14e6-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="b14e6-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="b14e6-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)