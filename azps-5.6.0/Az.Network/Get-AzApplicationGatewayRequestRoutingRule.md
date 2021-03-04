---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 04c7ef7dd041ce26802f23117edab79353816283
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890819"
---
# <span data-ttu-id="90c0f-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90c0f-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="90c0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="90c0f-103">Obtém a regra de roteamento de solicitação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="90c0f-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="90c0f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="90c0f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90c0f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="90c0f-105">DESCRIPTION</span></span>
<span data-ttu-id="90c0f-106">O cmdlet **Get-AzApplicationGatewayRequestRoutingRule** obtém a regra de roteamento de solicitação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="90c0f-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="90c0f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90c0f-107">EXAMPLES</span></span>

### <span data-ttu-id="90c0f-108">Exemplo 1: Obter uma regra de roteamento de solicitação específica</span><span class="sxs-lookup"><span data-stu-id="90c0f-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="90c0f-109">O primeiro comando obtém o Gateway de Aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="90c0f-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="90c0f-110">O segundo comando obtém a regra de roteamento de solicitação chamada Rule01 do Gateway de Aplicativo armazenado na variável denominada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="90c0f-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="90c0f-111">Exemplo 2: Obter uma lista de regras de roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="90c0f-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="90c0f-112">O primeiro comando obtém o Gateway de Aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="90c0f-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="90c0f-113">O segundo comando obtém uma lista de regras de roteamento de solicitação do Gateway de Aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="90c0f-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="90c0f-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="90c0f-114">PARAMETERS</span></span>

### <span data-ttu-id="90c0f-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90c0f-115">-ApplicationGateway</span></span>
<span data-ttu-id="90c0f-116">Especifica o objeto gateway de aplicativo que contém a regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="90c0f-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="90c0f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c0f-117">-DefaultProfile</span></span>
<span data-ttu-id="90c0f-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="90c0f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90c0f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="90c0f-119">-Name</span></span>
<span data-ttu-id="90c0f-120">Especifica o nome da regra de roteamento de solicitação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="90c0f-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="90c0f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c0f-121">CommonParameters</span></span>
<span data-ttu-id="90c0f-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90c0f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c0f-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90c0f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c0f-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90c0f-124">INPUTS</span></span>

### <span data-ttu-id="90c0f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90c0f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="90c0f-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="90c0f-126">OUTPUTS</span></span>

### <span data-ttu-id="90c0f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90c0f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="90c0f-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="90c0f-128">NOTES</span></span>

## <span data-ttu-id="90c0f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90c0f-129">RELATED LINKS</span></span>

[<span data-ttu-id="90c0f-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90c0f-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="90c0f-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90c0f-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="90c0f-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90c0f-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="90c0f-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90c0f-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


