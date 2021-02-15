---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c1c630c39039d39b1957ccab78bb96d8f085176c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111604"
---
# <span data-ttu-id="dd75a-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dd75a-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="dd75a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd75a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd75a-103">Remove uma regra de roteamento de solicitação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dd75a-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="dd75a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd75a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd75a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd75a-105">DESCRIPTION</span></span>
<span data-ttu-id="dd75a-106">O cmdlet **Remove-AzApplicationGatewayRequestRoutingRule** remove uma regra de roteamento de solicitação de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd75a-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="dd75a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dd75a-107">EXAMPLES</span></span>

### <span data-ttu-id="dd75a-108">Exemplo 1: Remover uma regra de roteamento de solicitação de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="dd75a-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="dd75a-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dd75a-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dd75a-110">O segundo comando remove a regra de roteamento de solicitação chamada Rule02 do gateway de aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="dd75a-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="dd75a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd75a-111">PARAMETERS</span></span>

### <span data-ttu-id="dd75a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dd75a-112">-ApplicationGateway</span></span>
<span data-ttu-id="dd75a-113">Especifica o gateway de aplicativo do qual remover uma regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="dd75a-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd75a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd75a-114">-DefaultProfile</span></span>
<span data-ttu-id="dd75a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="dd75a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd75a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd75a-116">-Name</span></span>
<span data-ttu-id="dd75a-117">Especifica o nome da regra de roteamento de solicitação para a qual este cmdlet é removido.</span><span class="sxs-lookup"><span data-stu-id="dd75a-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd75a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd75a-118">CommonParameters</span></span>
<span data-ttu-id="dd75a-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd75a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd75a-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd75a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd75a-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="dd75a-121">INPUTS</span></span>

### <span data-ttu-id="dd75a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dd75a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dd75a-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="dd75a-123">OUTPUTS</span></span>

### <span data-ttu-id="dd75a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dd75a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="dd75a-125">Notas</span><span class="sxs-lookup"><span data-stu-id="dd75a-125">NOTES</span></span>

## <span data-ttu-id="dd75a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd75a-126">RELATED LINKS</span></span>

[<span data-ttu-id="dd75a-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dd75a-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="dd75a-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dd75a-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="dd75a-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dd75a-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="dd75a-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dd75a-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


