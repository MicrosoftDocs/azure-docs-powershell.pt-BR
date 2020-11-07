---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e965f2cdbd9909003a07ea6c6addd198110e456f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775323"
---
# <span data-ttu-id="61c49-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="61c49-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="61c49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61c49-102">SYNOPSIS</span></span>
<span data-ttu-id="61c49-103">Remove uma configuração de redirecionamento de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="61c49-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="61c49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61c49-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61c49-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61c49-105">DESCRIPTION</span></span>
<span data-ttu-id="61c49-106">O cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** remove uma configuração de redirecionamento de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="61c49-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="61c49-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61c49-107">EXAMPLES</span></span>

### <span data-ttu-id="61c49-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61c49-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="61c49-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="61c49-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="61c49-110">O segundo comando Remove a configuração de redirecionamento chamada Redirect01 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="61c49-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="61c49-111">OS</span><span class="sxs-lookup"><span data-stu-id="61c49-111">PARAMETERS</span></span>

### <span data-ttu-id="61c49-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61c49-112">-ApplicationGateway</span></span>
<span data-ttu-id="61c49-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="61c49-113">The applicationGateway</span></span>

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

### <span data-ttu-id="61c49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c49-114">-DefaultProfile</span></span>
<span data-ttu-id="61c49-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61c49-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61c49-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="61c49-116">-Name</span></span>
<span data-ttu-id="61c49-117">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="61c49-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="61c49-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c49-118">CommonParameters</span></span>
<span data-ttu-id="61c49-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61c49-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c49-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c49-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c49-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61c49-121">INPUTS</span></span>

### <span data-ttu-id="61c49-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61c49-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="61c49-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61c49-123">OUTPUTS</span></span>

### <span data-ttu-id="61c49-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61c49-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="61c49-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61c49-125">NOTES</span></span>

## <span data-ttu-id="61c49-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61c49-126">RELATED LINKS</span></span>

