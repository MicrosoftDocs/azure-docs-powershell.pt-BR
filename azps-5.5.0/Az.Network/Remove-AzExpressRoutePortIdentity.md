---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112792"
---
# <span data-ttu-id="71546-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="71546-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="71546-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71546-102">SYNOPSIS</span></span>
<span data-ttu-id="71546-103">Remove uma identidade de um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="71546-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="71546-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71546-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71546-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="71546-105">DESCRIPTION</span></span>
<span data-ttu-id="71546-106">O cmdlet **Remove-AzExpressRoutePortIdentity** remove a identidade de um objeto local do Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="71546-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="71546-107">Use **Remove-AzExpressRoutePort** para removê-lo do ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="71546-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="71546-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71546-108">EXAMPLES</span></span>

### <span data-ttu-id="71546-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71546-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="71546-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71546-110">PARAMETERS</span></span>

### <span data-ttu-id="71546-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71546-111">-DefaultProfile</span></span>
<span data-ttu-id="71546-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71546-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71546-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71546-113">-ExpressRoutePort</span></span>
<span data-ttu-id="71546-114">O ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71546-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="71546-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="71546-115">-Confirm</span></span>
<span data-ttu-id="71546-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71546-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71546-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71546-117">-WhatIf</span></span>
<span data-ttu-id="71546-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="71546-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71546-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71546-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71546-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71546-120">CommonParameters</span></span>
<span data-ttu-id="71546-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71546-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71546-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71546-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="71546-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="71546-123">INPUTS</span></span>

### <span data-ttu-id="71546-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71546-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="71546-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="71546-125">OUTPUTS</span></span>

### <span data-ttu-id="71546-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="71546-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="71546-127">Notas</span><span class="sxs-lookup"><span data-stu-id="71546-127">NOTES</span></span>

## <span data-ttu-id="71546-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71546-128">RELATED LINKS</span></span>
[<span data-ttu-id="71546-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="71546-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="71546-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="71546-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="71546-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="71546-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
