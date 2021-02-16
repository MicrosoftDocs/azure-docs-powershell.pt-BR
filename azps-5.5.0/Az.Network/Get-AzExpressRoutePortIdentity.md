---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113506"
---
# <span data-ttu-id="3c511-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="3c511-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="3c511-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c511-102">SYNOPSIS</span></span>
<span data-ttu-id="3c511-103">Obter identidade atribuída a um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3c511-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="3c511-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c511-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c511-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c511-105">DESCRIPTION</span></span>
<span data-ttu-id="3c511-106">O cmdlet **Get-AzExpressRoutePortIdentity** recebe a identidade atribuída a um objeto local do Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="3c511-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="3c511-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3c511-107">EXAMPLES</span></span>

### <span data-ttu-id="3c511-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c511-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="3c511-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c511-109">PARAMETERS</span></span>

### <span data-ttu-id="3c511-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c511-110">-DefaultProfile</span></span>
<span data-ttu-id="3c511-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c511-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c511-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3c511-112">-ExpressRoutePort</span></span>
<span data-ttu-id="3c511-113">A Porta do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3c511-113">The ExpressRoute Port</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c511-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c511-114">CommonParameters</span></span>
<span data-ttu-id="3c511-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c511-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c511-116">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c511-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c511-117">Entradas</span><span class="sxs-lookup"><span data-stu-id="3c511-117">INPUTS</span></span>

### <span data-ttu-id="3c511-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="3c511-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="3c511-119">Saídas</span><span class="sxs-lookup"><span data-stu-id="3c511-119">OUTPUTS</span></span>

### <span data-ttu-id="3c511-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="3c511-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="3c511-121">Notas</span><span class="sxs-lookup"><span data-stu-id="3c511-121">NOTES</span></span>

## <span data-ttu-id="3c511-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c511-122">RELATED LINKS</span></span>
[<span data-ttu-id="3c511-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="3c511-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="3c511-124">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="3c511-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="3c511-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="3c511-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)