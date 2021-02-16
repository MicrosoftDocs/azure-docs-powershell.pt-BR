---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113515"
---
# <span data-ttu-id="297f6-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="297f6-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="297f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="297f6-102">SYNOPSIS</span></span>
<span data-ttu-id="297f6-103">Obtém uma configuração de peering de conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="297f6-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="297f6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="297f6-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="297f6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="297f6-105">DESCRIPTION</span></span>
<span data-ttu-id="297f6-106">O cmdlet **Get-AzExpressRouteCrossConnectionPeering** recupera a configuração de uma relação de pares para uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="297f6-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="297f6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="297f6-107">EXAMPLES</span></span>

### <span data-ttu-id="297f6-108">Exemplo 1: Exibir a configuração de peering de uma conexão cruzada do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="297f6-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="297f6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="297f6-109">PARAMETERS</span></span>

### <span data-ttu-id="297f6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="297f6-110">-DefaultProfile</span></span>
<span data-ttu-id="297f6-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="297f6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="297f6-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="297f6-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="297f6-113">O objeto de conexão cruzada do ExpressRoute que contém a configuração de peering.</span><span class="sxs-lookup"><span data-stu-id="297f6-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="297f6-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="297f6-114">-Name</span></span>
<span data-ttu-id="297f6-115">O nome da configuração de peering a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="297f6-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="297f6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297f6-116">CommonParameters</span></span>
<span data-ttu-id="297f6-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="297f6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297f6-118">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="297f6-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297f6-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="297f6-119">INPUTS</span></span>

### <span data-ttu-id="297f6-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="297f6-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="297f6-121">Parâmetro 'ExpressRouteCrossConnection' aceita o valor do tipo 'PSExpressRouteCrossConnection' do pipeline</span><span class="sxs-lookup"><span data-stu-id="297f6-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="297f6-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="297f6-122">OUTPUTS</span></span>

### <span data-ttu-id="297f6-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="297f6-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="297f6-124">Notas</span><span class="sxs-lookup"><span data-stu-id="297f6-124">NOTES</span></span>

## <span data-ttu-id="297f6-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="297f6-125">RELATED LINKS</span></span>

[<span data-ttu-id="297f6-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="297f6-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="297f6-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="297f6-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="297f6-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="297f6-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="297f6-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="297f6-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
