---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261358"
---
# <span data-ttu-id="f94cf-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f94cf-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f94cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f94cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f94cf-103">Obtém a regra de roteamento de solicitação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f94cf-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="f94cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f94cf-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f94cf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f94cf-105">DESCRIPTION</span></span>
<span data-ttu-id="f94cf-106">O cmdlet **Get-AzApplicationGatewayRequestRoutingRule** Obtém a regra de roteamento de solicitação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f94cf-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="f94cf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f94cf-107">EXAMPLES</span></span>

### <span data-ttu-id="f94cf-108">Exemplo 1: obter uma regra específica de roteamento de solicitações</span><span class="sxs-lookup"><span data-stu-id="f94cf-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="f94cf-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f94cf-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="f94cf-110">O segundo comando obtém a regra de roteamento de solicitação chamada Rule01 do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f94cf-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="f94cf-111">Exemplo 2: obter uma lista de regras de roteamento de solicitações</span><span class="sxs-lookup"><span data-stu-id="f94cf-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="f94cf-112">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f94cf-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="f94cf-113">O segundo comando obtém uma lista de regras de roteamento de solicitações do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f94cf-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="f94cf-114">OS</span><span class="sxs-lookup"><span data-stu-id="f94cf-114">PARAMETERS</span></span>

### <span data-ttu-id="f94cf-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f94cf-115">-ApplicationGateway</span></span>
<span data-ttu-id="f94cf-116">Especifica o objeto do gateway do aplicativo que contém a regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="f94cf-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="f94cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f94cf-117">-DefaultProfile</span></span>
<span data-ttu-id="f94cf-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f94cf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f94cf-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f94cf-119">-Name</span></span>
<span data-ttu-id="f94cf-120">Especifica o nome da regra de roteamento de solicitação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f94cf-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="f94cf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f94cf-121">CommonParameters</span></span>
<span data-ttu-id="f94cf-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f94cf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f94cf-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f94cf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f94cf-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f94cf-124">INPUTS</span></span>

### <span data-ttu-id="f94cf-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f94cf-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f94cf-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f94cf-126">OUTPUTS</span></span>

### <span data-ttu-id="f94cf-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f94cf-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f94cf-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f94cf-128">NOTES</span></span>

## <span data-ttu-id="f94cf-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f94cf-129">RELATED LINKS</span></span>

[<span data-ttu-id="f94cf-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f94cf-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f94cf-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f94cf-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f94cf-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f94cf-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f94cf-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f94cf-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


