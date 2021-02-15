---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fdd461ea2908e59ba824b09a49bed3b6b8f4d38f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111603"
---
# <span data-ttu-id="e2b8f-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2b8f-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e2b8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b8f-103">Remove uma configuração de redirecionamento de um Gateway de Aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="e2b8f-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="e2b8f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2b8f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2b8f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2b8f-105">DESCRIPTION</span></span>
<span data-ttu-id="e2b8f-106">O cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** remove uma configuração de redirecionamento de um Gateway de Aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="e2b8f-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="e2b8f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e2b8f-107">EXAMPLES</span></span>

### <span data-ttu-id="e2b8f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e2b8f-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="e2b8f-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2b8f-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e2b8f-110">O segundo comando remove a configuração de redirecionamento chamada Redirecionamento01 do gateway de aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e2b8f-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="e2b8f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2b8f-111">PARAMETERS</span></span>

### <span data-ttu-id="e2b8f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2b8f-112">-ApplicationGateway</span></span>
<span data-ttu-id="e2b8f-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2b8f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e2b8f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b8f-114">-DefaultProfile</span></span>
<span data-ttu-id="e2b8f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e2b8f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2b8f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2b8f-116">-Name</span></span>
<span data-ttu-id="e2b8f-117">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="e2b8f-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="e2b8f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b8f-118">CommonParameters</span></span>
<span data-ttu-id="e2b8f-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2b8f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b8f-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2b8f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b8f-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="e2b8f-121">INPUTS</span></span>

### <span data-ttu-id="e2b8f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2b8f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2b8f-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="e2b8f-123">OUTPUTS</span></span>

### <span data-ttu-id="e2b8f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2b8f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2b8f-125">Notas</span><span class="sxs-lookup"><span data-stu-id="e2b8f-125">NOTES</span></span>

## <span data-ttu-id="e2b8f-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2b8f-126">RELATED LINKS</span></span>

[<span data-ttu-id="e2b8f-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2b8f-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="e2b8f-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2b8f-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="e2b8f-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2b8f-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="e2b8f-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2b8f-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
