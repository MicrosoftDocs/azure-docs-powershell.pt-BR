---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118131"
---
# <span data-ttu-id="758f9-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="758f9-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="758f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="758f9-102">SYNOPSIS</span></span>
<span data-ttu-id="758f9-103">Obtém uma configuração de emparelhamento de conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="758f9-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="758f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="758f9-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="758f9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="758f9-105">DESCRIPTION</span></span>
<span data-ttu-id="758f9-106">O cmdlet **Get-AzExpressRouteCrossConnectionPeering** recupera a configuração de uma relação de emparelhamento para uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="758f9-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="758f9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="758f9-107">EXAMPLES</span></span>

### <span data-ttu-id="758f9-108">Exemplo 1: exibir a configuração de emparelhamento para uma conexão cruzada do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="758f9-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="758f9-109">OS</span><span class="sxs-lookup"><span data-stu-id="758f9-109">PARAMETERS</span></span>

### <span data-ttu-id="758f9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758f9-110">-DefaultProfile</span></span>
<span data-ttu-id="758f9-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="758f9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="758f9-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="758f9-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="758f9-113">O objeto de conexão Cruz expressa que contém a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="758f9-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="758f9-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="758f9-114">-Name</span></span>
<span data-ttu-id="758f9-115">O nome da configuração de emparelhamento a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="758f9-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="758f9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758f9-116">CommonParameters</span></span>
<span data-ttu-id="758f9-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="758f9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758f9-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="758f9-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758f9-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="758f9-119">INPUTS</span></span>

### <span data-ttu-id="758f9-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="758f9-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="758f9-121">O parâmetro ' ExpressRouteCrossConnection ' aceita o valor do tipo ' PSExpressRouteCrossConnection ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="758f9-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="758f9-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="758f9-122">OUTPUTS</span></span>

### <span data-ttu-id="758f9-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="758f9-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="758f9-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="758f9-124">NOTES</span></span>

## <span data-ttu-id="758f9-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="758f9-125">RELATED LINKS</span></span>

[<span data-ttu-id="758f9-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="758f9-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="758f9-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="758f9-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="758f9-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="758f9-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="758f9-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="758f9-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
