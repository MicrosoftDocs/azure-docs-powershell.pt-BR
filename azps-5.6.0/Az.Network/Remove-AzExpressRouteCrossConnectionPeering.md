---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 26e924bc94258480e0ae91f30d61c9cfd2adb72c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890777"
---
# <span data-ttu-id="20464-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="20464-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="20464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20464-102">SYNOPSIS</span></span>
<span data-ttu-id="20464-103">Remove uma configuração de peering de conexão cruzada expressRoute.</span><span class="sxs-lookup"><span data-stu-id="20464-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="20464-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="20464-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20464-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="20464-105">DESCRIPTION</span></span>
<span data-ttu-id="20464-106">O cmdlet **Remove-AzExpressRouteCrossConnectionPeering** remove uma configuração de peering de conexão cruzada expressRoute.</span><span class="sxs-lookup"><span data-stu-id="20464-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="20464-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20464-107">EXAMPLES</span></span>

### <span data-ttu-id="20464-108">Exemplo 1: Remover uma configuração de peering de uma conexão cruzada expressRoute</span><span class="sxs-lookup"><span data-stu-id="20464-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="20464-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="20464-109">PARAMETERS</span></span>

### <span data-ttu-id="20464-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20464-110">-DefaultProfile</span></span>
<span data-ttu-id="20464-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="20464-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20464-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="20464-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="20464-113">A conexão cruzada ExpressRoute que contém a configuração de paração a ser removida.</span><span class="sxs-lookup"><span data-stu-id="20464-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20464-114">-Force</span><span class="sxs-lookup"><span data-stu-id="20464-114">-Force</span></span>
<span data-ttu-id="20464-115">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="20464-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="20464-116">-Name</span><span class="sxs-lookup"><span data-stu-id="20464-116">-Name</span></span>
<span data-ttu-id="20464-117">O nome da configuração de paração a ser removida.</span><span class="sxs-lookup"><span data-stu-id="20464-117">The name of the peering configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20464-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="20464-118">-PeerAddressType</span></span>
<span data-ttu-id="20464-119">A família address do paring</span><span class="sxs-lookup"><span data-stu-id="20464-119">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20464-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20464-120">-Confirm</span></span>
<span data-ttu-id="20464-121">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20464-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20464-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20464-122">-WhatIf</span></span>
<span data-ttu-id="20464-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20464-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20464-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20464-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20464-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20464-125">CommonParameters</span></span>
<span data-ttu-id="20464-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20464-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20464-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20464-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20464-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20464-128">INPUTS</span></span>

### <span data-ttu-id="20464-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="20464-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="20464-130">Parâmetro 'ExpressRouteCrossConnection' aceita o valor do tipo 'PSExpressRouteCrossConnection' do pipeline</span><span class="sxs-lookup"><span data-stu-id="20464-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="20464-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="20464-131">OUTPUTS</span></span>

### <span data-ttu-id="20464-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="20464-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="20464-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="20464-133">NOTES</span></span>

## <span data-ttu-id="20464-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20464-134">RELATED LINKS</span></span>

[<span data-ttu-id="20464-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="20464-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="20464-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="20464-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](./Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="20464-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="20464-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="20464-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="20464-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
