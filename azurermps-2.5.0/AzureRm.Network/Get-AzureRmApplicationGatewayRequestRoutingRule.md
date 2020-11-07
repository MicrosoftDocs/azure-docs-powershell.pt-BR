---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: de019ffd1bc3be0e66cef6e8a15912f18b05f770
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786475"
---
# <span data-ttu-id="7a031-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7a031-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="7a031-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a031-102">SYNOPSIS</span></span>
<span data-ttu-id="7a031-103">Obtém a regra de roteamento de solicitação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7a031-103">Gets the request routing rule of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a031-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a031-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a031-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a031-105">DESCRIPTION</span></span>
<span data-ttu-id="7a031-106">O cmdlet **Get-AzureRmApplicationGatewayRequestRoutingRule** Obtém a regra de roteamento de solicitação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7a031-106">The **Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="7a031-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a031-107">EXAMPLES</span></span>

### <span data-ttu-id="7a031-108">Exemplo 1: obter uma regra específica de roteamento de solicitações</span><span class="sxs-lookup"><span data-stu-id="7a031-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzureRmApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="7a031-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7a031-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="7a031-110">O segundo comando obtém a regra de roteamento de solicitação chamada Rule01 do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7a031-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="7a031-111">Exemplo 2: obter uma lista de regras de roteamento de solicitações</span><span class="sxs-lookup"><span data-stu-id="7a031-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="7a031-112">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7a031-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="7a031-113">O segundo comando obtém uma lista de regras de roteamento de solicitações do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7a031-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="7a031-114">OS</span><span class="sxs-lookup"><span data-stu-id="7a031-114">PARAMETERS</span></span>

### <span data-ttu-id="7a031-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a031-115">-ApplicationGateway</span></span>
<span data-ttu-id="7a031-116">Especifica o objeto do gateway do aplicativo que contém a regra de roteamento de solicitação.</span><span class="sxs-lookup"><span data-stu-id="7a031-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="7a031-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a031-117">-DefaultProfile</span></span>
<span data-ttu-id="7a031-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a031-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a031-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a031-119">-Name</span></span>
<span data-ttu-id="7a031-120">Especifica o nome da regra de roteamento de solicitação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="7a031-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a031-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a031-121">CommonParameters</span></span>
<span data-ttu-id="7a031-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a031-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a031-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a031-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a031-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a031-124">INPUTS</span></span>

### <span data-ttu-id="7a031-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7a031-125">System.String</span></span>

## <span data-ttu-id="7a031-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a031-126">OUTPUTS</span></span>

### <span data-ttu-id="7a031-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7a031-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="7a031-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a031-128">NOTES</span></span>

## <span data-ttu-id="7a031-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a031-129">RELATED LINKS</span></span>

[<span data-ttu-id="7a031-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7a031-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7a031-131">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7a031-131">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7a031-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7a031-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7a031-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7a031-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


