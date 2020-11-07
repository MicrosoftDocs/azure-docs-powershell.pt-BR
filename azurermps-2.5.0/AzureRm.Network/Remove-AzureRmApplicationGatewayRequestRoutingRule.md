---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 859ef684424069bb5fc4c5b45de3e722f0921705
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785479"
---
# <span data-ttu-id="1b996-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1b996-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="1b996-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b996-102">SYNOPSIS</span></span>
<span data-ttu-id="1b996-103">Remove uma regra de roteamento de solicitação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1b996-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b996-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b996-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b996-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b996-105">DESCRIPTION</span></span>
<span data-ttu-id="1b996-106">O cmdlet **Remove-AzureRmApplicationGatewayRequestRoutingRule** remove uma regra de roteamento de solicitação de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b996-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="1b996-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b996-107">EXAMPLES</span></span>

### <span data-ttu-id="1b996-108">Exemplo 1: remover uma regra de roteamento de solicitação de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="1b996-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="1b996-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1b996-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1b996-110">O segundo comando Remove a regra de roteamento de solicitação chamada Rule02 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1b996-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="1b996-111">OS</span><span class="sxs-lookup"><span data-stu-id="1b996-111">PARAMETERS</span></span>

### <span data-ttu-id="1b996-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b996-112">-ApplicationGateway</span></span>
<span data-ttu-id="1b996-113">Especifica o gateway do aplicativo do qual remover uma regra de roteamento de solicitações.</span><span class="sxs-lookup"><span data-stu-id="1b996-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="1b996-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b996-114">-DefaultProfile</span></span>
<span data-ttu-id="1b996-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b996-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b996-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b996-116">-Name</span></span>
<span data-ttu-id="1b996-117">Especifica o nome da regra de roteamento de solicitação para a qual esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="1b996-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="1b996-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b996-118">CommonParameters</span></span>
<span data-ttu-id="1b996-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b996-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b996-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b996-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b996-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b996-121">INPUTS</span></span>

### <span data-ttu-id="1b996-122">System. String</span><span class="sxs-lookup"><span data-stu-id="1b996-122">System.String</span></span>

## <span data-ttu-id="1b996-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b996-123">OUTPUTS</span></span>

### <span data-ttu-id="1b996-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1b996-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="1b996-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b996-125">NOTES</span></span>

## <span data-ttu-id="1b996-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b996-126">RELATED LINKS</span></span>

[<span data-ttu-id="1b996-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1b996-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1b996-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1b996-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1b996-129">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1b996-129">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1b996-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1b996-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


