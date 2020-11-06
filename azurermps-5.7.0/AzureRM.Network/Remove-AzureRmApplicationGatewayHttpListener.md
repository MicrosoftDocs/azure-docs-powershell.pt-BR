---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: e42e13b0bb1d2cbe62ebd88b8ca5badc27143094
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93441595"
---
# <span data-ttu-id="bfc51-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bfc51-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bfc51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfc51-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc51-103">Remove um ouvinte HTTP de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="bfc51-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfc51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfc51-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfc51-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfc51-105">DESCRIPTION</span></span>
<span data-ttu-id="bfc51-106">O cmdlet **Remove-AzureRmApplicationGatewayHttpListener** remove um ouvinte HTTP de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc51-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="bfc51-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfc51-107">EXAMPLES</span></span>

### <span data-ttu-id="bfc51-108">Exemplo 1: remover um ouvinte HTTP do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="bfc51-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="bfc51-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bfc51-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="bfc51-110">O segundo comando Remove o ouvinte HTTP chamado Listener02 do gateway do aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bfc51-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="bfc51-111">OS</span><span class="sxs-lookup"><span data-stu-id="bfc51-111">PARAMETERS</span></span>

### <span data-ttu-id="bfc51-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bfc51-112">-ApplicationGateway</span></span>
<span data-ttu-id="bfc51-113">Especifica o gateway do aplicativo do qual remover um ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="bfc51-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="bfc51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc51-114">-DefaultProfile</span></span>
<span data-ttu-id="bfc51-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc51-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfc51-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfc51-116">-Name</span></span>
<span data-ttu-id="bfc51-117">Especifica o nome da escuta HTTP que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="bfc51-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bfc51-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc51-118">CommonParameters</span></span>
<span data-ttu-id="bfc51-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfc51-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc51-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfc51-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc51-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfc51-121">INPUTS</span></span>

### <span data-ttu-id="bfc51-122">System. String</span><span class="sxs-lookup"><span data-stu-id="bfc51-122">System.String</span></span>

## <span data-ttu-id="bfc51-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfc51-123">OUTPUTS</span></span>

### <span data-ttu-id="bfc51-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bfc51-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bfc51-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfc51-125">NOTES</span></span>

## <span data-ttu-id="bfc51-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfc51-126">RELATED LINKS</span></span>

[<span data-ttu-id="bfc51-127">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bfc51-127">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="bfc51-128">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bfc51-128">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="bfc51-129">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bfc51-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="bfc51-130">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bfc51-130">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


