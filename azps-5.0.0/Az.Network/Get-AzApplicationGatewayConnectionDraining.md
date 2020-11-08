---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b6fe7d8be92e2d82762557a05bf88ef053e0d407
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118353"
---
# <span data-ttu-id="fafea-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fafea-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="fafea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fafea-102">SYNOPSIS</span></span>
<span data-ttu-id="fafea-103">Obtém a conexão que descarrega a configuração de um objeto de configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="fafea-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="fafea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fafea-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fafea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fafea-105">DESCRIPTION</span></span>
<span data-ttu-id="fafea-106">O cmdlet **Get-AzApplicationGatewayConnectionDraining** Obtém a configuração de descarga da configuração de um objeto de configurações http back-end.</span><span class="sxs-lookup"><span data-stu-id="fafea-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="fafea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fafea-107">EXAMPLES</span></span>

### <span data-ttu-id="fafea-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fafea-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="fafea-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="fafea-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fafea-110">O segundo comando obtém as configurações HTTP back-end chamadas Settings01 para $AppGw e armazena as configurações na variável $Settings.</span><span class="sxs-lookup"><span data-stu-id="fafea-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="fafea-111">O último comando obtém a conexão que descarrega a configuração das configurações HTTP back-end $Settings e a armazena na variável $ConnectionDraining.</span><span class="sxs-lookup"><span data-stu-id="fafea-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="fafea-112">OS</span><span class="sxs-lookup"><span data-stu-id="fafea-112">PARAMETERS</span></span>

### <span data-ttu-id="fafea-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fafea-113">-BackendHttpSettings</span></span>
<span data-ttu-id="fafea-114">As configurações http de back-end</span><span class="sxs-lookup"><span data-stu-id="fafea-114">The backend http settings</span></span>

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

### <span data-ttu-id="fafea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fafea-115">-DefaultProfile</span></span>
<span data-ttu-id="fafea-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fafea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fafea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fafea-117">CommonParameters</span></span>
<span data-ttu-id="fafea-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fafea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fafea-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fafea-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fafea-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fafea-120">INPUTS</span></span>

### <span data-ttu-id="fafea-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fafea-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="fafea-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fafea-122">OUTPUTS</span></span>

### <span data-ttu-id="fafea-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fafea-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="fafea-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fafea-124">NOTES</span></span>

## <span data-ttu-id="fafea-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fafea-125">RELATED LINKS</span></span>

[<span data-ttu-id="fafea-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fafea-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="fafea-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="fafea-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="fafea-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fafea-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="fafea-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fafea-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="fafea-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fafea-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
