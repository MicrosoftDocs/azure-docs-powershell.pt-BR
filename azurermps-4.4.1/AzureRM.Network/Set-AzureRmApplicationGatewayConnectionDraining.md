---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 9da0f53f6dbea616a1f1cbea7ef08e71b05df17b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441008"
---
# <span data-ttu-id="48878-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="48878-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="48878-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48878-102">SYNOPSIS</span></span>
<span data-ttu-id="48878-103">Modifica a configuração de descarga da conexão de um objeto de configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="48878-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48878-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48878-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48878-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48878-105">DESCRIPTION</span></span>
<span data-ttu-id="48878-106">O cmdlet **set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** modifica a configuração de descarga da configuração de um objeto de configurações http back-end.</span><span class="sxs-lookup"><span data-stu-id="48878-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="48878-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48878-107">EXAMPLES</span></span>

### <span data-ttu-id="48878-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="48878-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="48878-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="48878-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="48878-110">O segundo comando obtém as configurações HTTP back-end chamadas Settings01 para $AppGw e armazena as configurações na variável $Settings.</span><span class="sxs-lookup"><span data-stu-id="48878-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="48878-111">O último comando modifica a configuração de descarga da configuração do objeto de configurações HTTP back-end armazenado no $Settings definindo Enabled como false e DrainTimeoutInSec como 3600.</span><span class="sxs-lookup"><span data-stu-id="48878-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="48878-112">OS</span><span class="sxs-lookup"><span data-stu-id="48878-112">PARAMETERS</span></span>

### <span data-ttu-id="48878-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="48878-113">-BackendHttpSettings</span></span>
<span data-ttu-id="48878-114">As configurações http de back-end</span><span class="sxs-lookup"><span data-stu-id="48878-114">The backend http settings</span></span>

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

### <span data-ttu-id="48878-115">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="48878-115">-DrainTimeoutInSec</span></span>
<span data-ttu-id="48878-116">O número de segundos que a conexão drenada está ativa.</span><span class="sxs-lookup"><span data-stu-id="48878-116">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="48878-117">Os valores aceitáveis variam de 1 segundo a 3600 segundos.</span><span class="sxs-lookup"><span data-stu-id="48878-117">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="48878-118">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="48878-118">-Enabled</span></span>
<span data-ttu-id="48878-119">Se a descarga de conexão está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="48878-119">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="48878-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48878-120">-DefaultProfile</span></span>
<span data-ttu-id="48878-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48878-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48878-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48878-122">CommonParameters</span></span>
<span data-ttu-id="48878-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48878-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48878-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48878-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48878-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48878-125">INPUTS</span></span>

### <span data-ttu-id="48878-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="48878-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="48878-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48878-127">OUTPUTS</span></span>

### <span data-ttu-id="48878-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="48878-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="48878-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48878-129">NOTES</span></span>

## <span data-ttu-id="48878-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48878-130">RELATED LINKS</span></span>

[<span data-ttu-id="48878-131">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48878-131">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="48878-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="48878-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="48878-133">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="48878-133">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="48878-134">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="48878-134">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="48878-135">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="48878-135">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

