---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: bd9ab62406d033eefe3fb3723d2a2ebf2f9dbb8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430734"
---
# <span data-ttu-id="872f7-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="872f7-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="872f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="872f7-102">SYNOPSIS</span></span>
<span data-ttu-id="872f7-103">Remove uma configuração de redirecionamento de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="872f7-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="872f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="872f7-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="872f7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="872f7-105">DESCRIPTION</span></span>
<span data-ttu-id="872f7-106">O cmdlet **Remove-AzureRmApplicationGatewayRedirectConfiguration** remove uma configuração de redirecionamento de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="872f7-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="872f7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="872f7-107">EXAMPLES</span></span>

### <span data-ttu-id="872f7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="872f7-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="872f7-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="872f7-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="872f7-110">O segundo comando Remove a configuração de redirecionamento chamada Redirect01 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="872f7-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="872f7-111">OS</span><span class="sxs-lookup"><span data-stu-id="872f7-111">PARAMETERS</span></span>

### <span data-ttu-id="872f7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="872f7-112">-ApplicationGateway</span></span>
<span data-ttu-id="872f7-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="872f7-113">The applicationGateway</span></span>

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

### <span data-ttu-id="872f7-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="872f7-114">-Name</span></span>
<span data-ttu-id="872f7-115">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="872f7-115">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="872f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872f7-116">-DefaultProfile</span></span>
<span data-ttu-id="872f7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="872f7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872f7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872f7-118">CommonParameters</span></span>
<span data-ttu-id="872f7-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="872f7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872f7-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="872f7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872f7-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="872f7-121">INPUTS</span></span>

### <span data-ttu-id="872f7-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="872f7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="872f7-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="872f7-123">OUTPUTS</span></span>

### <span data-ttu-id="872f7-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="872f7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="872f7-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="872f7-125">NOTES</span></span>

## <span data-ttu-id="872f7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="872f7-126">RELATED LINKS</span></span>

