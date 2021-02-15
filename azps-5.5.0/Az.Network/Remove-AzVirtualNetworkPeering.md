---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111583"
---
# <span data-ttu-id="0eca0-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0eca0-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="0eca0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0eca0-102">SYNOPSIS</span></span>
<span data-ttu-id="0eca0-103">Remove um peering de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0eca0-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="0eca0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0eca0-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eca0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0eca0-105">DESCRIPTION</span></span>
<span data-ttu-id="0eca0-106">Remove um peering de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0eca0-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="0eca0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0eca0-107">EXAMPLES</span></span>

### <span data-ttu-id="0eca0-108">Exemplo 1: Remover um par de rede virtual</span><span class="sxs-lookup"><span data-stu-id="0eca0-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="0eca0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0eca0-109">PARAMETERS</span></span>

### <span data-ttu-id="0eca0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0eca0-110">-AsJob</span></span>
<span data-ttu-id="0eca0-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0eca0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0eca0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eca0-112">-DefaultProfile</span></span>
<span data-ttu-id="0eca0-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0eca0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eca0-114">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0eca0-114">-Force</span></span>
<span data-ttu-id="0eca0-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0eca0-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0eca0-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0eca0-116">-Name</span></span>
<span data-ttu-id="0eca0-117">O nome de paridade de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0eca0-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="0eca0-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0eca0-118">-PassThru</span></span>
<span data-ttu-id="0eca0-119">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="0eca0-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0eca0-120">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="0eca0-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0eca0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eca0-121">-ResourceGroupName</span></span>
<span data-ttu-id="0eca0-122">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0eca0-122">The resource group name</span></span>

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

### <span data-ttu-id="0eca0-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0eca0-123">-VirtualNetworkName</span></span>
<span data-ttu-id="0eca0-124">O nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0eca0-124">The virtual network name.</span></span>

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

### <span data-ttu-id="0eca0-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0eca0-125">-Confirm</span></span>
<span data-ttu-id="0eca0-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eca0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eca0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eca0-127">-WhatIf</span></span>
<span data-ttu-id="0eca0-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0eca0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eca0-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0eca0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eca0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eca0-130">CommonParameters</span></span>
<span data-ttu-id="0eca0-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eca0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eca0-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eca0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eca0-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="0eca0-133">INPUTS</span></span>

### <span data-ttu-id="0eca0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0eca0-134">System.String</span></span>

## <span data-ttu-id="0eca0-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="0eca0-135">OUTPUTS</span></span>

### <span data-ttu-id="0eca0-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0eca0-136">System.Boolean</span></span>

## <span data-ttu-id="0eca0-137">Notas</span><span class="sxs-lookup"><span data-stu-id="0eca0-137">NOTES</span></span>

## <span data-ttu-id="0eca0-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0eca0-138">RELATED LINKS</span></span>

[<span data-ttu-id="0eca0-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0eca0-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="0eca0-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0eca0-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="0eca0-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0eca0-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
