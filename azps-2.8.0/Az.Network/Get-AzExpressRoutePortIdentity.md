---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: f8b41145c29d0eb3b2485fb1eb6b969574686b08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771757"
---
# <span data-ttu-id="d6090-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="d6090-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="d6090-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6090-102">SYNOPSIS</span></span>
<span data-ttu-id="d6090-103">Obter identidade atribuída a um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d6090-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="d6090-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6090-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6090-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6090-105">DESCRIPTION</span></span>
<span data-ttu-id="d6090-106">O cmdlet **Get-AzExpressRoutePortIdentity** Obtém a identidade atribuída a um objeto do Azure ExpressRoutePort local.</span><span class="sxs-lookup"><span data-stu-id="d6090-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="d6090-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6090-107">EXAMPLES</span></span>

### <span data-ttu-id="d6090-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6090-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="d6090-109">OS</span><span class="sxs-lookup"><span data-stu-id="d6090-109">PARAMETERS</span></span>

### <span data-ttu-id="d6090-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6090-110">-DefaultProfile</span></span>
<span data-ttu-id="d6090-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6090-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6090-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d6090-112">-ExpressRoutePort</span></span>
<span data-ttu-id="d6090-113">A porta do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d6090-113">The ExpressRoute Port</span></span>

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

### <span data-ttu-id="d6090-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6090-114">CommonParameters</span></span>
<span data-ttu-id="d6090-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6090-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6090-116">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6090-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6090-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6090-117">INPUTS</span></span>

### <span data-ttu-id="d6090-118">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d6090-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="d6090-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6090-119">OUTPUTS</span></span>

### <span data-ttu-id="d6090-120">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="d6090-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="d6090-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6090-121">NOTES</span></span>

## <span data-ttu-id="d6090-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6090-122">RELATED LINKS</span></span>
[<span data-ttu-id="d6090-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="d6090-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="d6090-124">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="d6090-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="d6090-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="d6090-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)