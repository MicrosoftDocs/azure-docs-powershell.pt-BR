---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: f542783ce1edcebf0c0c4e70116423836ddff736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429454"
---
# <span data-ttu-id="99c3d-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="99c3d-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="99c3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="99c3d-103">Remove uma configuração de redirecionamento de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="99c3d-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99c3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99c3d-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99c3d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="99c3d-106">O cmdlet **Remove-AzureRmApplicationGatewayRedirectConfiguration** remove uma configuração de redirecionamento de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="99c3d-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="99c3d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99c3d-107">EXAMPLES</span></span>

### <span data-ttu-id="99c3d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="99c3d-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="99c3d-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="99c3d-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="99c3d-110">O segundo comando Remove a configuração de redirecionamento chamada Redirect01 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="99c3d-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="99c3d-111">OS</span><span class="sxs-lookup"><span data-stu-id="99c3d-111">PARAMETERS</span></span>

### <span data-ttu-id="99c3d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99c3d-112">-ApplicationGateway</span></span>
<span data-ttu-id="99c3d-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="99c3d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="99c3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c3d-114">-DefaultProfile</span></span>
<span data-ttu-id="99c3d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99c3d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99c3d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="99c3d-116">-Name</span></span>
<span data-ttu-id="99c3d-117">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="99c3d-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="99c3d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c3d-118">CommonParameters</span></span>
<span data-ttu-id="99c3d-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99c3d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c3d-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99c3d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c3d-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99c3d-121">INPUTS</span></span>

### <span data-ttu-id="99c3d-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99c3d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="99c3d-123">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="99c3d-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="99c3d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99c3d-124">OUTPUTS</span></span>

### <span data-ttu-id="99c3d-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99c3d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99c3d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99c3d-126">NOTES</span></span>

## <span data-ttu-id="99c3d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99c3d-127">RELATED LINKS</span></span>
