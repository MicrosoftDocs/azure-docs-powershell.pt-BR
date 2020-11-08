---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 98b097e0be8d4b08ba16d5af06fbec1a2f3d66de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114798"
---
# <span data-ttu-id="7fcf5-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7fcf5-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="7fcf5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fcf5-102">SYNOPSIS</span></span>
<span data-ttu-id="7fcf5-103">Remove a conexão que descarrega a configuração de um objeto de configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="7fcf5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fcf5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fcf5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fcf5-105">DESCRIPTION</span></span>
<span data-ttu-id="7fcf5-106">O cmdlet **Remove-AzApplicationGatewayConnectionDraining** remove a configuração de descarga da configuração de um objeto de configurações http back-end.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="7fcf5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fcf5-107">EXAMPLES</span></span>

### <span data-ttu-id="7fcf5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7fcf5-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="7fcf5-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7fcf5-110">O segundo comando obtém as configurações HTTP back-end chamadas Settings01 para $AppGw e armazena as configurações na variável $Settings.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="7fcf5-111">O último comando Remove a conexão que descarrega a configuração das configurações HTTP de back-end armazenadas em $Settings.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="7fcf5-112">OS</span><span class="sxs-lookup"><span data-stu-id="7fcf5-112">PARAMETERS</span></span>

### <span data-ttu-id="7fcf5-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7fcf5-113">-BackendHttpSettings</span></span>
<span data-ttu-id="7fcf5-114">As configurações http de back-end</span><span class="sxs-lookup"><span data-stu-id="7fcf5-114">The backend http settings</span></span>

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

### <span data-ttu-id="7fcf5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fcf5-115">-DefaultProfile</span></span>
<span data-ttu-id="7fcf5-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fcf5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fcf5-117">CommonParameters</span></span>
<span data-ttu-id="7fcf5-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fcf5-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fcf5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fcf5-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fcf5-120">INPUTS</span></span>

### <span data-ttu-id="7fcf5-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7fcf5-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7fcf5-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fcf5-122">OUTPUTS</span></span>

### <span data-ttu-id="7fcf5-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7fcf5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7fcf5-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fcf5-124">NOTES</span></span>

## <span data-ttu-id="7fcf5-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fcf5-125">RELATED LINKS</span></span>

[<span data-ttu-id="7fcf5-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7fcf5-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="7fcf5-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7fcf5-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="7fcf5-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7fcf5-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="7fcf5-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7fcf5-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="7fcf5-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7fcf5-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

