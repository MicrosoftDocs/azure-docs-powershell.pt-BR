---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: a0188236a5ce0b4da29a61b38d7c1889bc909968
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892397"
---
# <span data-ttu-id="2da69-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2da69-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="2da69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2da69-102">SYNOPSIS</span></span>
<span data-ttu-id="2da69-103">Remove um toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2da69-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="2da69-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2da69-104">SYNTAX</span></span>

### <span data-ttu-id="2da69-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2da69-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2da69-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2da69-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2da69-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2da69-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2da69-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2da69-108">DESCRIPTION</span></span>
<span data-ttu-id="2da69-109">O cmdlet **Remove-AzVirtualNetworkTap** remove um toque de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="2da69-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="2da69-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2da69-110">EXAMPLES</span></span>

### <span data-ttu-id="2da69-111">Exemplo 1: Remover um toque de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2da69-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="2da69-112">Este comando remove o VirtualNetworkTap1 no grupo de recursos ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="2da69-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="2da69-113">Como o *parâmetro Force* não é usado, o usuário será solicitado a confirmar essa ação.</span><span class="sxs-lookup"><span data-stu-id="2da69-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="2da69-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2da69-114">PARAMETERS</span></span>

### <span data-ttu-id="2da69-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2da69-115">-AsJob</span></span>
<span data-ttu-id="2da69-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2da69-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da69-117">-DefaultProfile</span></span>
<span data-ttu-id="2da69-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2da69-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da69-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2da69-119">-Force</span></span>
<span data-ttu-id="2da69-120">Não peça confirmação se você deseja excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="2da69-120">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da69-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2da69-121">-InputObject</span></span>
<span data-ttu-id="2da69-122">Referência ao recurso VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2da69-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2da69-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2da69-123">-Name</span></span>
<span data-ttu-id="2da69-124">O nome do toque.</span><span class="sxs-lookup"><span data-stu-id="2da69-124">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da69-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2da69-125">-PassThru</span></span>
<span data-ttu-id="2da69-126">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="2da69-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2da69-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="2da69-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da69-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da69-128">-ResourceGroupName</span></span>
<span data-ttu-id="2da69-129">O nome do grupo de recursos do toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2da69-129">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da69-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2da69-130">-ResourceId</span></span>
<span data-ttu-id="2da69-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="2da69-131">VirtualNetworkTap resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da69-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2da69-132">-Confirm</span></span>
<span data-ttu-id="2da69-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2da69-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da69-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2da69-134">-WhatIf</span></span>
<span data-ttu-id="2da69-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2da69-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2da69-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2da69-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da69-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da69-137">CommonParameters</span></span>
<span data-ttu-id="2da69-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2da69-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da69-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2da69-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da69-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2da69-140">INPUTS</span></span>

### <span data-ttu-id="2da69-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2da69-141">System.String</span></span>

### <span data-ttu-id="2da69-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2da69-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="2da69-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2da69-143">OUTPUTS</span></span>

### <span data-ttu-id="2da69-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2da69-144">System.Boolean</span></span>

## <span data-ttu-id="2da69-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="2da69-145">NOTES</span></span>

## <span data-ttu-id="2da69-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2da69-146">RELATED LINKS</span></span>

[<span data-ttu-id="2da69-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2da69-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="2da69-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2da69-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="2da69-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2da69-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
