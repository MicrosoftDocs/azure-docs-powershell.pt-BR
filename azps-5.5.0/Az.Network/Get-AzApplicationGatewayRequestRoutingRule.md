---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112906"
---
# <span data-ttu-id="1399a-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1399a-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="1399a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1399a-102">SYNOPSIS</span></span>
<span data-ttu-id="1399a-103">Obtém a regra de roteamento de solicitação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1399a-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="1399a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1399a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1399a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1399a-105">DESCRIPTION</span></span>
<span data-ttu-id="1399a-106">O cmdlet **Get-AzApplicationGatewayRequestRoutingRule** obtém a regra de roteamento de solicitação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1399a-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="1399a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1399a-107">EXAMPLES</span></span>

### <span data-ttu-id="1399a-108">Exemplo 1: Obter uma regra de roteamento de solicitação específica</span><span class="sxs-lookup"><span data-stu-id="1399a-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="1399a-109">O primeiro comando obtém o Gateway de Aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1399a-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="1399a-110">O segundo comando obtém a regra de roteamento de solicitação chamada Rule01 do Gateway de Aplicativo armazenada na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1399a-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="1399a-111">Exemplo 2: Obter uma lista de regras de roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="1399a-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="1399a-112">O primeiro comando obtém o Gateway de Aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1399a-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="1399a-113">O segundo comando obtém uma lista de regras de roteamento de solicitação do Gateway de Aplicativo armazenadas na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1399a-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="1399a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1399a-114">PARAMETERS</span></span>

### <span data-ttu-id="1399a-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1399a-115">-ApplicationGateway</span></span>
<span data-ttu-id="1399a-116">Especifica o objeto do gateway de aplicativo que contém a regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="1399a-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="1399a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1399a-117">-DefaultProfile</span></span>
<span data-ttu-id="1399a-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1399a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1399a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1399a-119">-Name</span></span>
<span data-ttu-id="1399a-120">Especifica o nome da regra de roteamento de solicitação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="1399a-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="1399a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1399a-121">CommonParameters</span></span>
<span data-ttu-id="1399a-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1399a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1399a-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1399a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1399a-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="1399a-124">INPUTS</span></span>

### <span data-ttu-id="1399a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1399a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1399a-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="1399a-126">OUTPUTS</span></span>

### <span data-ttu-id="1399a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1399a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="1399a-128">Notas</span><span class="sxs-lookup"><span data-stu-id="1399a-128">NOTES</span></span>

## <span data-ttu-id="1399a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1399a-129">RELATED LINKS</span></span>

[<span data-ttu-id="1399a-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1399a-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1399a-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1399a-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1399a-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1399a-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1399a-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1399a-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


