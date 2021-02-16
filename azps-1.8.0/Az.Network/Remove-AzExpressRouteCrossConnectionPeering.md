---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: fe7c4550e3f54268e600414f8516095132b72115
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402279"
---
# <span data-ttu-id="64286-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="64286-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="64286-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64286-102">SYNOPSIS</span></span>
<span data-ttu-id="64286-103">Remove uma configuração de peering de conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="64286-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="64286-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64286-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64286-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="64286-105">DESCRIPTION</span></span>
<span data-ttu-id="64286-106">O cmdlet **Remove-AzExpressRouteCrossConnectionPeering** remove uma configuração de peering de conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="64286-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="64286-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="64286-107">EXAMPLES</span></span>

### <span data-ttu-id="64286-108">Exemplo 1: Remover uma configuração de peering de uma conexão cruzada do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="64286-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="64286-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64286-109">PARAMETERS</span></span>

### <span data-ttu-id="64286-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64286-110">-DefaultProfile</span></span>
<span data-ttu-id="64286-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="64286-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64286-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="64286-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="64286-113">A conexão cruzada do ExpressRoute contendo a configuração de peering a ser removida.</span><span class="sxs-lookup"><span data-stu-id="64286-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="64286-114">-Forçar</span><span class="sxs-lookup"><span data-stu-id="64286-114">-Force</span></span>
<span data-ttu-id="64286-115">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="64286-115">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="64286-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="64286-116">-Name</span></span>
<span data-ttu-id="64286-117">O nome da configuração de peering a ser removida.</span><span class="sxs-lookup"><span data-stu-id="64286-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="64286-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="64286-118">-PeerAddressType</span></span>
<span data-ttu-id="64286-119">A família Endereço do peering</span><span class="sxs-lookup"><span data-stu-id="64286-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="64286-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="64286-120">-Confirm</span></span>
<span data-ttu-id="64286-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64286-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64286-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64286-122">-WhatIf</span></span>
<span data-ttu-id="64286-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="64286-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64286-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64286-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64286-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64286-125">CommonParameters</span></span>
<span data-ttu-id="64286-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64286-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64286-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64286-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64286-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="64286-128">INPUTS</span></span>

### <span data-ttu-id="64286-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="64286-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="64286-130">O parâmetro 'ExpressRouteCrossConnection' aceita o valor do tipo 'PSExpressRouteCrossConnection' do pipeline</span><span class="sxs-lookup"><span data-stu-id="64286-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="64286-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="64286-131">OUTPUTS</span></span>

### <span data-ttu-id="64286-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="64286-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="64286-133">Notas</span><span class="sxs-lookup"><span data-stu-id="64286-133">NOTES</span></span>

## <span data-ttu-id="64286-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64286-134">RELATED LINKS</span></span>

[<span data-ttu-id="64286-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="64286-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)



[<span data-ttu-id="64286-136">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="64286-136">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="64286-137">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="64286-137">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
