---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955388"
---
# <span data-ttu-id="2e1bd-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e1bd-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="2e1bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="2e1bd-103">Remove uma configuração de privateLink de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="2e1bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e1bd-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e1bd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e1bd-105">DESCRIPTION</span></span>
<span data-ttu-id="2e1bd-106">O cmdlet **Remove-AzApplicationGatewayPrivateLinkConfiguration** remove uma configuração privateLink de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="2e1bd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e1bd-107">EXAMPLES</span></span>

### <span data-ttu-id="2e1bd-108">Exemplo 1: remover uma configuração de PrivateLink do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="2e1bd-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="2e1bd-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2e1bd-110">O segundo comando Remove a configuração privateLink chamada privateLinkConfig01 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2e1bd-111">OS</span><span class="sxs-lookup"><span data-stu-id="2e1bd-111">PARAMETERS</span></span>

### <span data-ttu-id="2e1bd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e1bd-112">-ApplicationGateway</span></span>
<span data-ttu-id="2e1bd-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e1bd-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2e1bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e1bd-114">-DefaultProfile</span></span>
<span data-ttu-id="2e1bd-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1bd-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e1bd-116">-Name</span></span>
<span data-ttu-id="2e1bd-117">O nome da configuração de privateLink do gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="2e1bd-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="2e1bd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e1bd-118">CommonParameters</span></span>
<span data-ttu-id="2e1bd-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e1bd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e1bd-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e1bd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e1bd-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e1bd-121">INPUTS</span></span>

### <span data-ttu-id="2e1bd-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e1bd-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2e1bd-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e1bd-123">OUTPUTS</span></span>

### <span data-ttu-id="2e1bd-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e1bd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2e1bd-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e1bd-125">NOTES</span></span>

## <span data-ttu-id="2e1bd-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e1bd-126">RELATED LINKS</span></span>

[<span data-ttu-id="2e1bd-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e1bd-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2e1bd-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e1bd-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2e1bd-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e1bd-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2e1bd-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2e1bd-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)