---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
ms.openlocfilehash: 46f73d2a58fe5f1109de6a15a5cb39e3b568a4b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432282"
---
# <span data-ttu-id="28781-101">Set-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="28781-101">Set-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="28781-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28781-102">SYNOPSIS</span></span>
<span data-ttu-id="28781-103">Modifica um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="28781-103">Modifies an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28781-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28781-104">SYNTAX</span></span>

```
Set-AzureRmExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28781-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28781-105">DESCRIPTION</span></span>
<span data-ttu-id="28781-106">O cmdlet **set-AzureRmExpressRoutePort** salva o ExpressRoutePort modificado no Azure.</span><span class="sxs-lookup"><span data-stu-id="28781-106">The **Set-AzureRmExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="28781-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28781-107">EXAMPLES</span></span>

### <span data-ttu-id="28781-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28781-108">Example 1</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="28781-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="28781-109">Example 2</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -InputObject $erport
```

<span data-ttu-id="28781-110">Modifica o estado do administrador de um link de um ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="28781-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="28781-111">OS</span><span class="sxs-lookup"><span data-stu-id="28781-111">PARAMETERS</span></span>

### <span data-ttu-id="28781-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28781-112">-AsJob</span></span>
<span data-ttu-id="28781-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="28781-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28781-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28781-114">-DefaultProfile</span></span>
<span data-ttu-id="28781-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28781-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28781-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="28781-116">-ExpressRoutePort</span></span>
<span data-ttu-id="28781-117">O objeto ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="28781-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="28781-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="28781-118">-Confirm</span></span>
<span data-ttu-id="28781-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28781-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28781-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28781-120">-WhatIf</span></span>
<span data-ttu-id="28781-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28781-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28781-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28781-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28781-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28781-123">CommonParameters</span></span>
<span data-ttu-id="28781-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28781-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28781-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28781-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28781-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28781-126">INPUTS</span></span>

### <span data-ttu-id="28781-127">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="28781-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="28781-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28781-128">OUTPUTS</span></span>

### <span data-ttu-id="28781-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="28781-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="28781-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28781-130">NOTES</span></span>

## <span data-ttu-id="28781-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28781-131">RELATED LINKS</span></span>
