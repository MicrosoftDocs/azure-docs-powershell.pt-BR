---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118271"
---
# <span data-ttu-id="4e010-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e010-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="4e010-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e010-102">SYNOPSIS</span></span>
<span data-ttu-id="4e010-103">Exclua um recurso de tabela de rotação de hub virtual associado a um hub virtual.</span><span class="sxs-lookup"><span data-stu-id="4e010-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="4e010-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e010-104">SYNTAX</span></span>

### <span data-ttu-id="4e010-105">ByVirtualHubRouteTableName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4e010-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e010-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="4e010-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e010-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="4e010-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e010-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="4e010-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e010-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e010-109">DESCRIPTION</span></span>
<span data-ttu-id="4e010-110">Exclui a tabela de rota especificada associada ao hub virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="4e010-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="4e010-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4e010-111">EXAMPLES</span></span>

### <span data-ttu-id="4e010-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4e010-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="4e010-113">Esse comando exclui a RoteadaTable1 do hub virtual westushub.</span><span class="sxs-lookup"><span data-stu-id="4e010-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="4e010-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e010-114">PARAMETERS</span></span>

### <span data-ttu-id="4e010-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e010-115">-AsJob</span></span>
<span data-ttu-id="4e010-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4e010-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e010-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e010-117">-DefaultProfile</span></span>
<span data-ttu-id="4e010-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e010-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e010-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4e010-119">-Force</span></span>
<span data-ttu-id="4e010-120">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="4e010-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4e010-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="4e010-121">-HubName</span></span>
<span data-ttu-id="4e010-122">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="4e010-122">The parent resource name.</span></span>

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

### <span data-ttu-id="4e010-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e010-123">-InputObject</span></span>
<span data-ttu-id="4e010-124">O recurso virtualhuutetable a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4e010-124">The virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="4e010-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e010-125">-Name</span></span>
<span data-ttu-id="4e010-126">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4e010-126">The resource name.</span></span>

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

### <span data-ttu-id="4e010-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e010-127">-PassThru</span></span>
<span data-ttu-id="4e010-128">Retorna um objeto que representa o item no qual esta operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="4e010-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="4e010-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e010-129">-ResourceGroupName</span></span>
<span data-ttu-id="4e010-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4e010-130">The resource group name.</span></span>

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

### <span data-ttu-id="4e010-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e010-131">-ResourceId</span></span>
<span data-ttu-id="4e010-132">A id de recurso do recurso virtualmenteeável a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4e010-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="4e010-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="4e010-133">-VirtualHub</span></span>
<span data-ttu-id="4e010-134">{{ Fill VirtualHub Description }}</span><span class="sxs-lookup"><span data-stu-id="4e010-134">{{ Fill VirtualHub Description }}</span></span>

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

### <span data-ttu-id="4e010-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4e010-135">-Confirm</span></span>
<span data-ttu-id="4e010-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e010-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e010-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e010-137">-WhatIf</span></span>
<span data-ttu-id="4e010-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4e010-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e010-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4e010-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e010-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e010-140">CommonParameters</span></span>
<span data-ttu-id="4e010-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e010-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e010-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e010-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e010-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="4e010-143">INPUTS</span></span>

### <span data-ttu-id="4e010-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4e010-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="4e010-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4e010-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="4e010-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4e010-146">System.String</span></span>

## <span data-ttu-id="4e010-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="4e010-147">OUTPUTS</span></span>

### <span data-ttu-id="4e010-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4e010-148">System.Boolean</span></span>

## <span data-ttu-id="4e010-149">Notas</span><span class="sxs-lookup"><span data-stu-id="4e010-149">NOTES</span></span>

## <span data-ttu-id="4e010-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e010-150">RELATED LINKS</span></span>
