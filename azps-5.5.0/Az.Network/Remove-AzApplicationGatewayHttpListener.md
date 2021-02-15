---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 81b750188a85add491e519c023c765f302e31dea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114666"
---
# <span data-ttu-id="56d76-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="56d76-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="56d76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56d76-102">SYNOPSIS</span></span>
<span data-ttu-id="56d76-103">Remove um ouvinte HTTP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="56d76-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="56d76-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56d76-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56d76-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="56d76-105">DESCRIPTION</span></span>
<span data-ttu-id="56d76-106">O cmdlet **Remove-AzApplicationGatewayHttpListener** remove um ouvinte HTTP de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="56d76-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="56d76-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="56d76-107">EXAMPLES</span></span>

### <span data-ttu-id="56d76-108">Exemplo 1: Remover um ouvinte HTTP do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="56d76-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="56d76-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="56d76-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="56d76-110">O segundo comando remove o ouvinte HTTP chamado Ouvinte02 do gateway de aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="56d76-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="56d76-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56d76-111">PARAMETERS</span></span>

### <span data-ttu-id="56d76-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56d76-112">-ApplicationGateway</span></span>
<span data-ttu-id="56d76-113">Especifica o gateway do aplicativo do qual remover um ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="56d76-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="56d76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d76-114">-DefaultProfile</span></span>
<span data-ttu-id="56d76-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="56d76-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56d76-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="56d76-116">-Name</span></span>
<span data-ttu-id="56d76-117">Especifica o nome do ouvinte HTTP que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="56d76-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="56d76-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d76-118">CommonParameters</span></span>
<span data-ttu-id="56d76-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d76-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d76-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d76-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d76-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="56d76-121">INPUTS</span></span>

### <span data-ttu-id="56d76-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56d76-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="56d76-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="56d76-123">OUTPUTS</span></span>

### <span data-ttu-id="56d76-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="56d76-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="56d76-125">Notas</span><span class="sxs-lookup"><span data-stu-id="56d76-125">NOTES</span></span>

## <span data-ttu-id="56d76-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56d76-126">RELATED LINKS</span></span>

[<span data-ttu-id="56d76-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="56d76-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="56d76-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="56d76-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="56d76-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="56d76-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="56d76-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="56d76-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


