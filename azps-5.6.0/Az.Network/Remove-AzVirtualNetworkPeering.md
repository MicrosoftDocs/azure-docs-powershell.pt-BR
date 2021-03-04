---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: f47b1bcc571337de8a64c591383367568cf7d67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890740"
---
# <span data-ttu-id="1d367-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1d367-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="1d367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d367-102">SYNOPSIS</span></span>
<span data-ttu-id="1d367-103">Remove um par de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="1d367-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="1d367-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1d367-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d367-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1d367-105">DESCRIPTION</span></span>
<span data-ttu-id="1d367-106">Remove um par de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="1d367-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="1d367-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d367-107">EXAMPLES</span></span>

### <span data-ttu-id="1d367-108">Exemplo 1: Remover um par de rede virtual</span><span class="sxs-lookup"><span data-stu-id="1d367-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="1d367-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1d367-109">PARAMETERS</span></span>

### <span data-ttu-id="1d367-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d367-110">-AsJob</span></span>
<span data-ttu-id="1d367-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1d367-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d367-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d367-112">-DefaultProfile</span></span>
<span data-ttu-id="1d367-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1d367-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d367-114">-Force</span><span class="sxs-lookup"><span data-stu-id="1d367-114">-Force</span></span>
<span data-ttu-id="1d367-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1d367-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1d367-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1d367-116">-Name</span></span>
<span data-ttu-id="1d367-117">O nome de paração de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="1d367-117">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d367-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d367-118">-PassThru</span></span>
<span data-ttu-id="1d367-119">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="1d367-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1d367-120">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1d367-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1d367-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d367-121">-ResourceGroupName</span></span>
<span data-ttu-id="1d367-122">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1d367-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d367-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1d367-123">-VirtualNetworkName</span></span>
<span data-ttu-id="1d367-124">O nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="1d367-124">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d367-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d367-125">-Confirm</span></span>
<span data-ttu-id="1d367-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d367-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d367-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d367-127">-WhatIf</span></span>
<span data-ttu-id="1d367-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1d367-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d367-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1d367-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d367-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d367-130">CommonParameters</span></span>
<span data-ttu-id="1d367-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d367-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d367-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d367-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d367-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d367-133">INPUTS</span></span>

### <span data-ttu-id="1d367-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1d367-134">System.String</span></span>

## <span data-ttu-id="1d367-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1d367-135">OUTPUTS</span></span>

### <span data-ttu-id="1d367-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1d367-136">System.Boolean</span></span>

## <span data-ttu-id="1d367-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="1d367-137">NOTES</span></span>

## <span data-ttu-id="1d367-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d367-138">RELATED LINKS</span></span>

[<span data-ttu-id="1d367-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1d367-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="1d367-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1d367-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="1d367-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1d367-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
