---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428935"
---
# <span data-ttu-id="61be1-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="61be1-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="61be1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61be1-102">SYNOPSIS</span></span>
<span data-ttu-id="61be1-103">Remove uma identidade de um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="61be1-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="61be1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61be1-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61be1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61be1-105">DESCRIPTION</span></span>
<span data-ttu-id="61be1-106">O cmdlet **Remove-AzExpressRoutePortIdentity** remove a identidade de um objeto ExpressRoutePort do Azure local.</span><span class="sxs-lookup"><span data-stu-id="61be1-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="61be1-107">Use **Remove-AzExpressRoutePort** para removê-lo do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="61be1-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="61be1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61be1-108">EXAMPLES</span></span>

### <span data-ttu-id="61be1-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61be1-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="61be1-110">OS</span><span class="sxs-lookup"><span data-stu-id="61be1-110">PARAMETERS</span></span>

### <span data-ttu-id="61be1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61be1-111">-DefaultProfile</span></span>
<span data-ttu-id="61be1-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61be1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61be1-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="61be1-113">-ExpressRoutePort</span></span>
<span data-ttu-id="61be1-114">O ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="61be1-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="61be1-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="61be1-115">-Confirm</span></span>
<span data-ttu-id="61be1-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61be1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61be1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61be1-117">-WhatIf</span></span>
<span data-ttu-id="61be1-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="61be1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61be1-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="61be1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61be1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61be1-120">CommonParameters</span></span>
<span data-ttu-id="61be1-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61be1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61be1-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61be1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="61be1-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61be1-123">INPUTS</span></span>

### <span data-ttu-id="61be1-124">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="61be1-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="61be1-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61be1-125">OUTPUTS</span></span>

### <span data-ttu-id="61be1-126">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="61be1-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="61be1-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61be1-127">NOTES</span></span>

## <span data-ttu-id="61be1-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61be1-128">RELATED LINKS</span></span>
[<span data-ttu-id="61be1-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="61be1-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="61be1-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="61be1-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="61be1-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="61be1-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
