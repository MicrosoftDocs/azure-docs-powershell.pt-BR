---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: ddcec36e8561196b31dd94eb15d99a7e2a92a378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886896"
---
# <span data-ttu-id="b81be-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b81be-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="b81be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b81be-102">SYNOPSIS</span></span>
<span data-ttu-id="b81be-103">Remove a configuração de esvaziamento de conexão de um objeto de configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="b81be-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="b81be-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b81be-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b81be-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b81be-105">DESCRIPTION</span></span>
<span data-ttu-id="b81be-106">O cmdlet **Remove-AzApplicationGatewayConnectionDraining** remove a configuração de esvaziamento de conexão de um objeto de configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="b81be-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="b81be-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b81be-107">EXAMPLES</span></span>

### <span data-ttu-id="b81be-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b81be-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="b81be-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b81be-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b81be-110">O segundo comando obtém as configurações HTTP de back-end denominadas Settings01 para $AppGw e armazena as configurações na variável $Settings back-end.</span><span class="sxs-lookup"><span data-stu-id="b81be-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="b81be-111">O último comando remove a configuração de esvaziamento de conexão das configurações HTTP de back-end armazenadas $Settings.</span><span class="sxs-lookup"><span data-stu-id="b81be-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="b81be-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b81be-112">PARAMETERS</span></span>

### <span data-ttu-id="b81be-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b81be-113">-BackendHttpSettings</span></span>
<span data-ttu-id="b81be-114">As configurações http de back-end</span><span class="sxs-lookup"><span data-stu-id="b81be-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b81be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b81be-115">-DefaultProfile</span></span>
<span data-ttu-id="b81be-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b81be-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b81be-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b81be-117">CommonParameters</span></span>
<span data-ttu-id="b81be-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b81be-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b81be-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b81be-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b81be-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b81be-120">INPUTS</span></span>

### <span data-ttu-id="b81be-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b81be-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b81be-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b81be-122">OUTPUTS</span></span>

### <span data-ttu-id="b81be-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b81be-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b81be-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="b81be-124">NOTES</span></span>

## <span data-ttu-id="b81be-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b81be-125">RELATED LINKS</span></span>

[<span data-ttu-id="b81be-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b81be-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="b81be-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b81be-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="b81be-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b81be-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b81be-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b81be-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b81be-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b81be-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

