---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 73e4fb2dde10739176a1adfe55c22529e8ccdaaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429431"
---
# <span data-ttu-id="f5e1f-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f5e1f-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="f5e1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e1f-103">Remove um emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-103">Removes a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5e1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5e1f-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5e1f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5e1f-105">DESCRIPTION</span></span>
<span data-ttu-id="f5e1f-106">Remove um emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="f5e1f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5e1f-107">EXAMPLES</span></span>

### <span data-ttu-id="f5e1f-108">Exemplo 1: remover um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="f5e1f-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="f5e1f-109">OS</span><span class="sxs-lookup"><span data-stu-id="f5e1f-109">PARAMETERS</span></span>

### <span data-ttu-id="f5e1f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5e1f-110">-AsJob</span></span>
<span data-ttu-id="f5e1f-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f5e1f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5e1f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e1f-112">-DefaultProfile</span></span>
<span data-ttu-id="f5e1f-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e1f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f5e1f-114">-Force</span></span>
<span data-ttu-id="f5e1f-115">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f5e1f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5e1f-116">-Name</span></span>
<span data-ttu-id="f5e1f-117">O nome de emparelhamento da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="f5e1f-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5e1f-118">-PassThru</span></span>
<span data-ttu-id="f5e1f-119">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f5e1f-120">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f5e1f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e1f-121">-ResourceGroupName</span></span>
<span data-ttu-id="f5e1f-122">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f5e1f-122">The resource group name</span></span>

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

### <span data-ttu-id="f5e1f-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f5e1f-123">-VirtualNetworkName</span></span>
<span data-ttu-id="f5e1f-124">O nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-124">The virtual network name.</span></span>

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

### <span data-ttu-id="f5e1f-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5e1f-125">-Confirm</span></span>
<span data-ttu-id="f5e1f-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5e1f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5e1f-127">-WhatIf</span></span>
<span data-ttu-id="f5e1f-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5e1f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5e1f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e1f-130">CommonParameters</span></span>
<span data-ttu-id="f5e1f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e1f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e1f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e1f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5e1f-133">INPUTS</span></span>

### <span data-ttu-id="f5e1f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f5e1f-134">System.String</span></span>

## <span data-ttu-id="f5e1f-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5e1f-135">OUTPUTS</span></span>

### <span data-ttu-id="f5e1f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5e1f-136">System.Boolean</span></span>

## <span data-ttu-id="f5e1f-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5e1f-137">NOTES</span></span>

## <span data-ttu-id="f5e1f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5e1f-138">RELATED LINKS</span></span>
