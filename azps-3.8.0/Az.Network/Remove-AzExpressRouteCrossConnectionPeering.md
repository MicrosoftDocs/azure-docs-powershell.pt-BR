---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: eb90b668bf0466c44e3fde0ef0a8d6777074fb37
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944055"
---
# <span data-ttu-id="b717a-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b717a-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="b717a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b717a-102">SYNOPSIS</span></span>
<span data-ttu-id="b717a-103">Remove uma configuração de emparelhamento de conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b717a-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="b717a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b717a-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b717a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b717a-105">DESCRIPTION</span></span>
<span data-ttu-id="b717a-106">O cmdlet **Remove-AzExpressRouteCrossConnectionPeering** remove uma configuração de emparelhamento de conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b717a-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="b717a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b717a-107">EXAMPLES</span></span>

### <span data-ttu-id="b717a-108">Exemplo 1: remover uma configuração de emparelhamento de uma conexão cruzada do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="b717a-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="b717a-109">OS</span><span class="sxs-lookup"><span data-stu-id="b717a-109">PARAMETERS</span></span>

### <span data-ttu-id="b717a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b717a-110">-DefaultProfile</span></span>
<span data-ttu-id="b717a-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b717a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b717a-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b717a-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="b717a-113">A conexão cruzada do ExpressRoute que contém a configuração de emparelhamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="b717a-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="b717a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b717a-114">-Force</span></span>
<span data-ttu-id="b717a-115">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="b717a-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b717a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b717a-116">-Name</span></span>
<span data-ttu-id="b717a-117">O nome da configuração de emparelhamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="b717a-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="b717a-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b717a-118">-PeerAddressType</span></span>
<span data-ttu-id="b717a-119">A família de endereços da correspondência</span><span class="sxs-lookup"><span data-stu-id="b717a-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="b717a-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b717a-120">-Confirm</span></span>
<span data-ttu-id="b717a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b717a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b717a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b717a-122">-WhatIf</span></span>
<span data-ttu-id="b717a-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b717a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b717a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b717a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b717a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b717a-125">CommonParameters</span></span>
<span data-ttu-id="b717a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b717a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b717a-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b717a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b717a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b717a-128">INPUTS</span></span>

### <span data-ttu-id="b717a-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b717a-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="b717a-130">O parâmetro ' ExpressRouteCrossConnection ' aceita o valor do tipo ' PSExpressRouteCrossConnection ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b717a-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="b717a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b717a-131">OUTPUTS</span></span>

### <span data-ttu-id="b717a-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b717a-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="b717a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b717a-133">NOTES</span></span>

## <span data-ttu-id="b717a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b717a-134">RELATED LINKS</span></span>

[<span data-ttu-id="b717a-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b717a-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="b717a-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b717a-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](New-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="b717a-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b717a-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="b717a-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b717a-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
