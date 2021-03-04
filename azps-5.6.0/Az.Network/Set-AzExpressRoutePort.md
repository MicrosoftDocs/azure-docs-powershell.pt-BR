---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: c431b03c4dd417638f84fe3a483bcaf9eefcb837
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886883"
---
# <span data-ttu-id="80dc0-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="80dc0-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="80dc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="80dc0-103">Modifica um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="80dc0-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="80dc0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="80dc0-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80dc0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="80dc0-105">DESCRIPTION</span></span>
<span data-ttu-id="80dc0-106">O cmdlet **Set-AzExpressRoutePort** salva o ExpressRoutePort modificado para o Azure.</span><span class="sxs-lookup"><span data-stu-id="80dc0-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="80dc0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80dc0-107">EXAMPLES</span></span>

### <span data-ttu-id="80dc0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="80dc0-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="80dc0-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="80dc0-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="80dc0-110">Modifica o estado de administrador de um link de um ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="80dc0-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="80dc0-111">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="80dc0-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="80dc0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="80dc0-112">PARAMETERS</span></span>

### <span data-ttu-id="80dc0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80dc0-113">-AsJob</span></span>
<span data-ttu-id="80dc0-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="80dc0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80dc0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80dc0-115">-DefaultProfile</span></span>
<span data-ttu-id="80dc0-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80dc0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80dc0-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="80dc0-117">-ExpressRoutePort</span></span>
<span data-ttu-id="80dc0-118">O objeto ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="80dc0-118">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80dc0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80dc0-119">-Confirm</span></span>
<span data-ttu-id="80dc0-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80dc0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80dc0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80dc0-121">-WhatIf</span></span>
<span data-ttu-id="80dc0-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80dc0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80dc0-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80dc0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80dc0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80dc0-124">CommonParameters</span></span>
<span data-ttu-id="80dc0-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80dc0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80dc0-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80dc0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80dc0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80dc0-127">INPUTS</span></span>

### <span data-ttu-id="80dc0-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="80dc0-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="80dc0-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="80dc0-129">OUTPUTS</span></span>

### <span data-ttu-id="80dc0-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="80dc0-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="80dc0-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="80dc0-131">NOTES</span></span>

## <span data-ttu-id="80dc0-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80dc0-132">RELATED LINKS</span></span>

[<span data-ttu-id="80dc0-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="80dc0-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="80dc0-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="80dc0-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="80dc0-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="80dc0-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
