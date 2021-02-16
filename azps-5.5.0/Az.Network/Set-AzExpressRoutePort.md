---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: 2365729f3960e3652e2b4c0709ca14092fea3264
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118263"
---
# <span data-ttu-id="c3d8a-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c3d8a-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="c3d8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d8a-103">Modifica um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c3d8a-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="c3d8a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3d8a-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3d8a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3d8a-105">DESCRIPTION</span></span>
<span data-ttu-id="c3d8a-106">O cmdlet **Set-AzExpressRoutePort** salva o ExpressRoutePort modificado no Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d8a-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="c3d8a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c3d8a-107">EXAMPLES</span></span>

### <span data-ttu-id="c3d8a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3d8a-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="c3d8a-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c3d8a-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="c3d8a-110">Modifica o estado de administrador de um link de um ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c3d8a-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="c3d8a-111">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c3d8a-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="c3d8a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3d8a-112">PARAMETERS</span></span>

### <span data-ttu-id="c3d8a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3d8a-113">-AsJob</span></span>
<span data-ttu-id="c3d8a-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c3d8a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3d8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d8a-115">-DefaultProfile</span></span>
<span data-ttu-id="c3d8a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d8a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d8a-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c3d8a-117">-ExpressRoutePort</span></span>
<span data-ttu-id="c3d8a-118">O objeto ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c3d8a-118">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="c3d8a-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c3d8a-119">-Confirm</span></span>
<span data-ttu-id="c3d8a-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3d8a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3d8a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3d8a-121">-WhatIf</span></span>
<span data-ttu-id="c3d8a-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c3d8a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3d8a-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3d8a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3d8a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d8a-124">CommonParameters</span></span>
<span data-ttu-id="c3d8a-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d8a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d8a-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d8a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d8a-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="c3d8a-127">INPUTS</span></span>

### <span data-ttu-id="c3d8a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c3d8a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c3d8a-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="c3d8a-129">OUTPUTS</span></span>

### <span data-ttu-id="c3d8a-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c3d8a-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c3d8a-131">Notas</span><span class="sxs-lookup"><span data-stu-id="c3d8a-131">NOTES</span></span>

## <span data-ttu-id="c3d8a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3d8a-132">RELATED LINKS</span></span>

[<span data-ttu-id="c3d8a-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c3d8a-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="c3d8a-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c3d8a-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="c3d8a-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c3d8a-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
