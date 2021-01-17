---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: e2cecb2061b605c5380597c51cb72860596690cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428878"
---
# <span data-ttu-id="b06d4-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b06d4-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="b06d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b06d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b06d4-103">Modifica a configuração de descarga da conexão de um objeto de configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="b06d4-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="b06d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b06d4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b06d4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b06d4-105">DESCRIPTION</span></span>
<span data-ttu-id="b06d4-106">O cmdlet **set-AzApplicationGatewayWebApplicationFirewallConfiguration** modifica a configuração de descarga da configuração de um objeto de configurações http back-end.</span><span class="sxs-lookup"><span data-stu-id="b06d4-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="b06d4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b06d4-107">EXAMPLES</span></span>

### <span data-ttu-id="b06d4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b06d4-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="b06d4-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b06d4-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b06d4-110">O segundo comando obtém as configurações HTTP back-end chamadas Settings01 para $AppGw e armazena as configurações na variável $Settings.</span><span class="sxs-lookup"><span data-stu-id="b06d4-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="b06d4-111">O último comando modifica a configuração de descarga da configuração do objeto de configurações HTTP back-end armazenado no $Settings definindo Enabled como false e DrainTimeoutInSec como 3600.</span><span class="sxs-lookup"><span data-stu-id="b06d4-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="b06d4-112">OS</span><span class="sxs-lookup"><span data-stu-id="b06d4-112">PARAMETERS</span></span>

### <span data-ttu-id="b06d4-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b06d4-113">-BackendHttpSettings</span></span>
<span data-ttu-id="b06d4-114">As configurações http de back-end</span><span class="sxs-lookup"><span data-stu-id="b06d4-114">The backend http settings</span></span>

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

### <span data-ttu-id="b06d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b06d4-115">-DefaultProfile</span></span>
<span data-ttu-id="b06d4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b06d4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b06d4-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="b06d4-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="b06d4-118">O número de segundos que a conexão drenada está ativa.</span><span class="sxs-lookup"><span data-stu-id="b06d4-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="b06d4-119">Os valores aceitáveis variam de 1 segundo a 3600 segundos.</span><span class="sxs-lookup"><span data-stu-id="b06d4-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06d4-120">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="b06d4-120">-Enabled</span></span>
<span data-ttu-id="b06d4-121">Se a descarga de conexão está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="b06d4-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06d4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06d4-122">CommonParameters</span></span>
<span data-ttu-id="b06d4-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b06d4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b06d4-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b06d4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06d4-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b06d4-125">INPUTS</span></span>

### <span data-ttu-id="b06d4-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b06d4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b06d4-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b06d4-127">OUTPUTS</span></span>

### <span data-ttu-id="b06d4-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b06d4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b06d4-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b06d4-129">NOTES</span></span>

## <span data-ttu-id="b06d4-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b06d4-130">RELATED LINKS</span></span>

[<span data-ttu-id="b06d4-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b06d4-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="b06d4-132">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b06d4-132">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="b06d4-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b06d4-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b06d4-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b06d4-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b06d4-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b06d4-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

