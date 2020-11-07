---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: ecee205ee831c5ba7a2fa78c00f005af3303a13a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785485"
---
# <span data-ttu-id="04e33-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="04e33-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="04e33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04e33-102">SYNOPSIS</span></span>
<span data-ttu-id="04e33-103">Remove uma porta de front-end de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="04e33-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04e33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04e33-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04e33-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04e33-105">DESCRIPTION</span></span>
<span data-ttu-id="04e33-106">O cmdlet **Remove-AzureRmApplicationGatewayFrontendPort** remove uma porta de front-end de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="04e33-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="04e33-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04e33-107">EXAMPLES</span></span>

### <span data-ttu-id="04e33-108">Exemplo: remover uma porta de front-end de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="04e33-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="04e33-109">O primeiro comando obtém um gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e armazena o gateway em $AppGw variável.</span><span class="sxs-lookup"><span data-stu-id="04e33-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="04e33-110">O segundo comando Remove a porta nomeada FrontEndPort02 do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04e33-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="04e33-111">OS</span><span class="sxs-lookup"><span data-stu-id="04e33-111">PARAMETERS</span></span>

### <span data-ttu-id="04e33-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04e33-112">-ApplicationGateway</span></span>
<span data-ttu-id="04e33-113">Especifica o gateway do aplicativo do qual você deseja remover uma porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="04e33-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="04e33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e33-114">-DefaultProfile</span></span>
<span data-ttu-id="04e33-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04e33-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04e33-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="04e33-116">-Name</span></span>
<span data-ttu-id="04e33-117">Especifica o nome da porta de front-end a ser removida.</span><span class="sxs-lookup"><span data-stu-id="04e33-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="04e33-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e33-118">CommonParameters</span></span>
<span data-ttu-id="04e33-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04e33-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e33-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04e33-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e33-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04e33-121">INPUTS</span></span>

### <span data-ttu-id="04e33-122">System. String</span><span class="sxs-lookup"><span data-stu-id="04e33-122">System.String</span></span>

## <span data-ttu-id="04e33-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04e33-123">OUTPUTS</span></span>

### <span data-ttu-id="04e33-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04e33-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="04e33-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04e33-125">NOTES</span></span>

## <span data-ttu-id="04e33-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04e33-126">RELATED LINKS</span></span>

[<span data-ttu-id="04e33-127">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="04e33-127">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="04e33-128">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="04e33-128">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="04e33-129">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="04e33-129">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="04e33-130">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="04e33-130">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


