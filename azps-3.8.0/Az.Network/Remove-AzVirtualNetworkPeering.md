---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943972"
---
# <span data-ttu-id="20822-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="20822-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="20822-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20822-102">SYNOPSIS</span></span>
<span data-ttu-id="20822-103">Remove um emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="20822-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="20822-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20822-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20822-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20822-105">DESCRIPTION</span></span>
<span data-ttu-id="20822-106">Remove um emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="20822-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="20822-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20822-107">EXAMPLES</span></span>

### <span data-ttu-id="20822-108">Exemplo 1: remover um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="20822-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="20822-109">OS</span><span class="sxs-lookup"><span data-stu-id="20822-109">PARAMETERS</span></span>

### <span data-ttu-id="20822-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20822-110">-AsJob</span></span>
<span data-ttu-id="20822-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="20822-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20822-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20822-112">-DefaultProfile</span></span>
<span data-ttu-id="20822-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20822-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20822-114">-Force</span><span class="sxs-lookup"><span data-stu-id="20822-114">-Force</span></span>
<span data-ttu-id="20822-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="20822-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="20822-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="20822-116">-Name</span></span>
<span data-ttu-id="20822-117">O nome de emparelhamento da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="20822-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="20822-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20822-118">-PassThru</span></span>
<span data-ttu-id="20822-119">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="20822-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="20822-120">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="20822-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="20822-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20822-121">-ResourceGroupName</span></span>
<span data-ttu-id="20822-122">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="20822-122">The resource group name</span></span>

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

### <span data-ttu-id="20822-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="20822-123">-VirtualNetworkName</span></span>
<span data-ttu-id="20822-124">O nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="20822-124">The virtual network name.</span></span>

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

### <span data-ttu-id="20822-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="20822-125">-Confirm</span></span>
<span data-ttu-id="20822-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20822-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20822-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20822-127">-WhatIf</span></span>
<span data-ttu-id="20822-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20822-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20822-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20822-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20822-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20822-130">CommonParameters</span></span>
<span data-ttu-id="20822-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20822-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20822-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20822-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20822-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20822-133">INPUTS</span></span>

### <span data-ttu-id="20822-134">System. String</span><span class="sxs-lookup"><span data-stu-id="20822-134">System.String</span></span>

## <span data-ttu-id="20822-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20822-135">OUTPUTS</span></span>

### <span data-ttu-id="20822-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20822-136">System.Boolean</span></span>

## <span data-ttu-id="20822-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20822-137">NOTES</span></span>

## <span data-ttu-id="20822-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20822-138">RELATED LINKS</span></span>

[<span data-ttu-id="20822-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="20822-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="20822-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="20822-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="20822-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="20822-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
