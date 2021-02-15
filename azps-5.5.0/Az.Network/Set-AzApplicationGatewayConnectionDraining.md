---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: e2cecb2061b605c5380597c51cb72860596690cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114634"
---
# <span data-ttu-id="0da6a-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0da6a-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="0da6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0da6a-102">SYNOPSIS</span></span>
<span data-ttu-id="0da6a-103">Modifica a configuração de drenamento de conexão de um objeto de configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="0da6a-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="0da6a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0da6a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0da6a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0da6a-105">DESCRIPTION</span></span>
<span data-ttu-id="0da6a-106">O cmdlet **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** modifica a configuração de esgotamento de conexão de um objeto de configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="0da6a-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="0da6a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0da6a-107">EXAMPLES</span></span>

### <span data-ttu-id="0da6a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0da6a-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="0da6a-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0da6a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0da6a-110">O segundo comando obtém as configurações HTTP de back-end chamadas Configurações01 para $AppGw e armazena as configurações na variável $Settings back-end.</span><span class="sxs-lookup"><span data-stu-id="0da6a-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="0da6a-111">O último comando modifica a configuração de esgotamento de conexão do objeto de configurações HTTP de back-end armazenado no $Settings configurando Habilitado para False e DrainTimeoutInSec como 3600.</span><span class="sxs-lookup"><span data-stu-id="0da6a-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="0da6a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0da6a-112">PARAMETERS</span></span>

### <span data-ttu-id="0da6a-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0da6a-113">-BackendHttpSettings</span></span>
<span data-ttu-id="0da6a-114">As configurações de http back-end</span><span class="sxs-lookup"><span data-stu-id="0da6a-114">The backend http settings</span></span>

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

### <span data-ttu-id="0da6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da6a-115">-DefaultProfile</span></span>
<span data-ttu-id="0da6a-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0da6a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0da6a-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="0da6a-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="0da6a-118">O número de segundos de estouros de conexão está ativo.</span><span class="sxs-lookup"><span data-stu-id="0da6a-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="0da6a-119">Valores aceitáveis variam de 1 segundo a 3600 segundos.</span><span class="sxs-lookup"><span data-stu-id="0da6a-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="0da6a-120">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="0da6a-120">-Enabled</span></span>
<span data-ttu-id="0da6a-121">Se a conexão está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="0da6a-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="0da6a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da6a-122">CommonParameters</span></span>
<span data-ttu-id="0da6a-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da6a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da6a-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da6a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da6a-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="0da6a-125">INPUTS</span></span>

### <span data-ttu-id="0da6a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0da6a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0da6a-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="0da6a-127">OUTPUTS</span></span>

### <span data-ttu-id="0da6a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0da6a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0da6a-129">Notas</span><span class="sxs-lookup"><span data-stu-id="0da6a-129">NOTES</span></span>

## <span data-ttu-id="0da6a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0da6a-130">RELATED LINKS</span></span>

[<span data-ttu-id="0da6a-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0da6a-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="0da6a-132">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0da6a-132">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="0da6a-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0da6a-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0da6a-134">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0da6a-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0da6a-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0da6a-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

