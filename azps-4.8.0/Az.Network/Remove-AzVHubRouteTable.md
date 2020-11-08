---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114349"
---
# <span data-ttu-id="043a6-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="043a6-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="043a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="043a6-102">SYNOPSIS</span></span>
<span data-ttu-id="043a6-103">Excluir um recurso de tabela de rota de Hub associado a um VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="043a6-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="043a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="043a6-104">SYNTAX</span></span>

### <span data-ttu-id="043a6-105">ByVHubRouteTableName (padrão)</span><span class="sxs-lookup"><span data-stu-id="043a6-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="043a6-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="043a6-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="043a6-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="043a6-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="043a6-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="043a6-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="043a6-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="043a6-109">DESCRIPTION</span></span>
<span data-ttu-id="043a6-110">Exclui a tabela de rota de Hub especificada que está associada ao Hub virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="043a6-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="043a6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="043a6-111">EXAMPLES</span></span>

### <span data-ttu-id="043a6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="043a6-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="043a6-113">Esse comando exclui a tabela de rota do Hub do Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="043a6-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="043a6-114">OS</span><span class="sxs-lookup"><span data-stu-id="043a6-114">PARAMETERS</span></span>

### <span data-ttu-id="043a6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="043a6-115">-AsJob</span></span>
<span data-ttu-id="043a6-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="043a6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="043a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="043a6-117">-DefaultProfile</span></span>
<span data-ttu-id="043a6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="043a6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="043a6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="043a6-119">-Force</span></span>
<span data-ttu-id="043a6-120">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="043a6-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="043a6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="043a6-121">-InputObject</span></span>
<span data-ttu-id="043a6-122">O recurso vhubroutetable a ser removido.</span><span class="sxs-lookup"><span data-stu-id="043a6-122">The vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="043a6-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="043a6-123">-Name</span></span>
<span data-ttu-id="043a6-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="043a6-124">The resource name.</span></span>

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

### <span data-ttu-id="043a6-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="043a6-125">-ParentObject</span></span>
<span data-ttu-id="043a6-126">O objeto Hub virtual pai deste recurso.</span><span class="sxs-lookup"><span data-stu-id="043a6-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="043a6-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="043a6-127">-ParentResourceName</span></span>
<span data-ttu-id="043a6-128">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="043a6-128">The parent resource name.</span></span>

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

### <span data-ttu-id="043a6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="043a6-129">-PassThru</span></span>
<span data-ttu-id="043a6-130">Retorna um objeto que representa o item em que essa operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="043a6-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="043a6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="043a6-131">-ResourceGroupName</span></span>
<span data-ttu-id="043a6-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="043a6-132">The resource group name.</span></span>

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

### <span data-ttu-id="043a6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="043a6-133">-ResourceId</span></span>
<span data-ttu-id="043a6-134">A ID do recurso do recurso vhubroutetable a ser removido.</span><span class="sxs-lookup"><span data-stu-id="043a6-134">The resource id of the vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="043a6-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="043a6-135">-Confirm</span></span>
<span data-ttu-id="043a6-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="043a6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="043a6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="043a6-137">-WhatIf</span></span>
<span data-ttu-id="043a6-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="043a6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="043a6-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="043a6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="043a6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="043a6-140">CommonParameters</span></span>
<span data-ttu-id="043a6-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="043a6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="043a6-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="043a6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="043a6-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="043a6-143">INPUTS</span></span>

### <span data-ttu-id="043a6-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="043a6-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="043a6-145">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="043a6-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="043a6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="043a6-146">System.String</span></span>

## <span data-ttu-id="043a6-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="043a6-147">OUTPUTS</span></span>

### <span data-ttu-id="043a6-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="043a6-148">System.Boolean</span></span>

## <span data-ttu-id="043a6-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="043a6-149">NOTES</span></span>

## <span data-ttu-id="043a6-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="043a6-150">RELATED LINKS</span></span>

[<span data-ttu-id="043a6-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="043a6-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="043a6-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="043a6-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="043a6-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="043a6-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="043a6-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="043a6-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)