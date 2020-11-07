---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: c3bc83f3f38c8a9b3c34e990e5729648a3677dd8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775324"
---
# <span data-ttu-id="4ebcb-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4ebcb-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4ebcb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ebcb-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebcb-103">Remove um ouvinte HTTP de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="4ebcb-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="4ebcb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ebcb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ebcb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ebcb-105">DESCRIPTION</span></span>
<span data-ttu-id="4ebcb-106">O cmdlet **Remove-AzApplicationGatewayHttpListener** remove um ouvinte HTTP de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ebcb-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="4ebcb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ebcb-107">EXAMPLES</span></span>

### <span data-ttu-id="4ebcb-108">Exemplo 1: remover um ouvinte HTTP do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="4ebcb-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="4ebcb-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4ebcb-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4ebcb-110">O segundo comando Remove o ouvinte HTTP chamado Listener02 do gateway do aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4ebcb-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4ebcb-111">OS</span><span class="sxs-lookup"><span data-stu-id="4ebcb-111">PARAMETERS</span></span>

### <span data-ttu-id="4ebcb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ebcb-112">-ApplicationGateway</span></span>
<span data-ttu-id="4ebcb-113">Especifica o gateway do aplicativo do qual remover um ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="4ebcb-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="4ebcb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebcb-114">-DefaultProfile</span></span>
<span data-ttu-id="4ebcb-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ebcb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ebcb-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ebcb-116">-Name</span></span>
<span data-ttu-id="4ebcb-117">Especifica o nome da escuta HTTP que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="4ebcb-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4ebcb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebcb-118">CommonParameters</span></span>
<span data-ttu-id="4ebcb-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ebcb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebcb-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ebcb-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebcb-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ebcb-121">INPUTS</span></span>

### <span data-ttu-id="4ebcb-122">System. String</span><span class="sxs-lookup"><span data-stu-id="4ebcb-122">System.String</span></span>

## <span data-ttu-id="4ebcb-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ebcb-123">OUTPUTS</span></span>

### <span data-ttu-id="4ebcb-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4ebcb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4ebcb-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ebcb-125">NOTES</span></span>

## <span data-ttu-id="4ebcb-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ebcb-126">RELATED LINKS</span></span>

[<span data-ttu-id="4ebcb-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4ebcb-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4ebcb-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4ebcb-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4ebcb-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4ebcb-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4ebcb-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4ebcb-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)

