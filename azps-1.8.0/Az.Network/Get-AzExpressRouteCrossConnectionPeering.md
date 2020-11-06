---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 99142e3dd33d84e11f326258450d92a58fe70e20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600582"
---
# <span data-ttu-id="1c72f-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1c72f-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="1c72f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c72f-102">SYNOPSIS</span></span>
<span data-ttu-id="1c72f-103">Obtém uma configuração de emparelhamento de conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1c72f-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="1c72f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c72f-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c72f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c72f-105">DESCRIPTION</span></span>
<span data-ttu-id="1c72f-106">O cmdlet **Get-AzExpressRouteCrossConnectionPeering** recupera a configuração de uma relação de emparelhamento para uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1c72f-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="1c72f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c72f-107">EXAMPLES</span></span>

### <span data-ttu-id="1c72f-108">Exemplo 1: exibir a configuração de emparelhamento para uma conexão cruzada do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="1c72f-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="1c72f-109">OS</span><span class="sxs-lookup"><span data-stu-id="1c72f-109">PARAMETERS</span></span>

### <span data-ttu-id="1c72f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c72f-110">-DefaultProfile</span></span>
<span data-ttu-id="1c72f-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c72f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c72f-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1c72f-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="1c72f-113">O objeto de conexão Cruz expressa que contém a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="1c72f-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="1c72f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c72f-114">-Name</span></span>
<span data-ttu-id="1c72f-115">O nome da configuração de emparelhamento a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="1c72f-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="1c72f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c72f-116">CommonParameters</span></span>
<span data-ttu-id="1c72f-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c72f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c72f-118">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c72f-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c72f-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c72f-119">INPUTS</span></span>

### <span data-ttu-id="1c72f-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1c72f-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="1c72f-121">O parâmetro ' ExpressRouteCrossConnection ' aceita o valor do tipo ' PSExpressRouteCrossConnection ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1c72f-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="1c72f-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c72f-122">OUTPUTS</span></span>

### <span data-ttu-id="1c72f-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="1c72f-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="1c72f-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c72f-124">NOTES</span></span>

## <span data-ttu-id="1c72f-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c72f-125">RELATED LINKS</span></span>

[<span data-ttu-id="1c72f-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1c72f-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="1c72f-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="1c72f-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="1c72f-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1c72f-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="1c72f-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1c72f-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
