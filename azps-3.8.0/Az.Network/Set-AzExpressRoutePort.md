---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: b5170ef175b93bc977ba047d4188d51de2858e63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941329"
---
# <span data-ttu-id="c6b20-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c6b20-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="c6b20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6b20-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b20-103">Modifica um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c6b20-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="c6b20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6b20-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6b20-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6b20-105">DESCRIPTION</span></span>
<span data-ttu-id="c6b20-106">O cmdlet **set-AzExpressRoutePort** salva o ExpressRoutePort modificado no Azure.</span><span class="sxs-lookup"><span data-stu-id="c6b20-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="c6b20-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6b20-107">EXAMPLES</span></span>

### <span data-ttu-id="c6b20-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6b20-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="c6b20-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c6b20-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="c6b20-110">Modifica o estado do administrador de um link de um ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c6b20-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="c6b20-111">OS</span><span class="sxs-lookup"><span data-stu-id="c6b20-111">PARAMETERS</span></span>

### <span data-ttu-id="c6b20-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6b20-112">-AsJob</span></span>
<span data-ttu-id="c6b20-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c6b20-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6b20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6b20-114">-DefaultProfile</span></span>
<span data-ttu-id="c6b20-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6b20-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6b20-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c6b20-116">-ExpressRoutePort</span></span>
<span data-ttu-id="c6b20-117">O objeto ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c6b20-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="c6b20-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c6b20-118">-Confirm</span></span>
<span data-ttu-id="c6b20-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6b20-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6b20-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6b20-120">-WhatIf</span></span>
<span data-ttu-id="c6b20-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c6b20-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6b20-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c6b20-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6b20-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b20-123">CommonParameters</span></span>
<span data-ttu-id="c6b20-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6b20-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b20-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6b20-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b20-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6b20-126">INPUTS</span></span>

### <span data-ttu-id="c6b20-127">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c6b20-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c6b20-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6b20-128">OUTPUTS</span></span>

### <span data-ttu-id="c6b20-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c6b20-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c6b20-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6b20-130">NOTES</span></span>

## <span data-ttu-id="c6b20-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6b20-131">RELATED LINKS</span></span>

[<span data-ttu-id="c6b20-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c6b20-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="c6b20-133">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c6b20-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="c6b20-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c6b20-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
