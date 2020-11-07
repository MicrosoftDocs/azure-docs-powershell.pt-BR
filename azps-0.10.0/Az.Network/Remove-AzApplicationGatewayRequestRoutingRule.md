---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 3c034f3bbbd5edc77fb6f43c291b8bf7ca27cd38
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775319"
---
# <span data-ttu-id="1dacc-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1dacc-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="1dacc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1dacc-102">SYNOPSIS</span></span>
<span data-ttu-id="1dacc-103">Remove uma regra de roteamento de solicitação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1dacc-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="1dacc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dacc-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dacc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1dacc-105">DESCRIPTION</span></span>
<span data-ttu-id="1dacc-106">O cmdlet **Remove-AzApplicationGatewayRequestRoutingRule** remove uma regra de roteamento de solicitação de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="1dacc-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="1dacc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1dacc-107">EXAMPLES</span></span>

### <span data-ttu-id="1dacc-108">Exemplo 1: remover uma regra de roteamento de solicitação de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="1dacc-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="1dacc-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1dacc-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1dacc-110">O segundo comando Remove a regra de roteamento de solicitação chamada Rule02 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1dacc-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="1dacc-111">OS</span><span class="sxs-lookup"><span data-stu-id="1dacc-111">PARAMETERS</span></span>

### <span data-ttu-id="1dacc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1dacc-112">-ApplicationGateway</span></span>
<span data-ttu-id="1dacc-113">Especifica o gateway do aplicativo do qual remover uma regra de roteamento de solicitações.</span><span class="sxs-lookup"><span data-stu-id="1dacc-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dacc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dacc-114">-DefaultProfile</span></span>
<span data-ttu-id="1dacc-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1dacc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dacc-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dacc-116">-Name</span></span>
<span data-ttu-id="1dacc-117">Especifica o nome da regra de roteamento de solicitação para a qual esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="1dacc-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dacc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dacc-118">CommonParameters</span></span>
<span data-ttu-id="1dacc-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dacc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dacc-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dacc-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dacc-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1dacc-121">INPUTS</span></span>

### <span data-ttu-id="1dacc-122">System. String</span><span class="sxs-lookup"><span data-stu-id="1dacc-122">System.String</span></span>

## <span data-ttu-id="1dacc-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1dacc-123">OUTPUTS</span></span>

### <span data-ttu-id="1dacc-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1dacc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="1dacc-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1dacc-125">NOTES</span></span>

## <span data-ttu-id="1dacc-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dacc-126">RELATED LINKS</span></span>

[<span data-ttu-id="1dacc-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1dacc-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1dacc-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1dacc-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1dacc-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1dacc-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1dacc-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1dacc-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


