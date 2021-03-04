---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3d1df3262fa9cee55d5aa49c026b7b1e681b5c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891177"
---
# <span data-ttu-id="f62d0-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f62d0-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f62d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f62d0-102">SYNOPSIS</span></span>
<span data-ttu-id="f62d0-103">Obtém a configuração de esvaziamento de conexão de um objeto de configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="f62d0-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="f62d0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f62d0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f62d0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f62d0-105">DESCRIPTION</span></span>
<span data-ttu-id="f62d0-106">O cmdlet **Get-AzApplicationGatewayConnectionDraining** obtém a configuração de esvaziamento de conexão de um objeto de configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="f62d0-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="f62d0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f62d0-107">EXAMPLES</span></span>

### <span data-ttu-id="f62d0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f62d0-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="f62d0-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f62d0-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f62d0-110">O segundo comando obtém as configurações HTTP de back-end denominadas Settings01 para $AppGw e armazena as configurações na variável $Settings back-end.</span><span class="sxs-lookup"><span data-stu-id="f62d0-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="f62d0-111">O último comando obtém a configuração de esvaziamento de conexão das configurações HTTP de back-end $Settings e armazena-a na variável $ConnectionDraining back-end.</span><span class="sxs-lookup"><span data-stu-id="f62d0-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="f62d0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f62d0-112">PARAMETERS</span></span>

### <span data-ttu-id="f62d0-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f62d0-113">-BackendHttpSettings</span></span>
<span data-ttu-id="f62d0-114">As configurações http de back-end</span><span class="sxs-lookup"><span data-stu-id="f62d0-114">The backend http settings</span></span>

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

### <span data-ttu-id="f62d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f62d0-115">-DefaultProfile</span></span>
<span data-ttu-id="f62d0-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f62d0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f62d0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62d0-117">CommonParameters</span></span>
<span data-ttu-id="f62d0-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f62d0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62d0-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f62d0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62d0-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f62d0-120">INPUTS</span></span>

### <span data-ttu-id="f62d0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f62d0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f62d0-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f62d0-122">OUTPUTS</span></span>

### <span data-ttu-id="f62d0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f62d0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f62d0-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="f62d0-124">NOTES</span></span>

## <span data-ttu-id="f62d0-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f62d0-125">RELATED LINKS</span></span>

[<span data-ttu-id="f62d0-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f62d0-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="f62d0-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="f62d0-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="f62d0-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f62d0-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f62d0-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f62d0-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f62d0-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f62d0-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
