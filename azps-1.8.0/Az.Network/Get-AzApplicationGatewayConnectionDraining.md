---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 1630b0177efbccbf4d1cba674f0cf11ab457307e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402109"
---
# <span data-ttu-id="72048-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="72048-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="72048-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72048-102">SYNOPSIS</span></span>
<span data-ttu-id="72048-103">Obtém a configuração de esgotamento de conexão de um objeto de configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="72048-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="72048-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72048-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72048-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="72048-105">DESCRIPTION</span></span>
<span data-ttu-id="72048-106">O cmdlet **Get-AzApplicationGatewayConnectionConnectionDraining** obtém a configuração de drenamento de conexão de um objeto de configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="72048-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="72048-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="72048-107">EXAMPLES</span></span>

### <span data-ttu-id="72048-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="72048-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="72048-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="72048-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="72048-110">O segundo comando obtém as configurações HTTP de back-end chamadas Configurações01 para $AppGw e armazena as configurações na variável $Settings back-end.</span><span class="sxs-lookup"><span data-stu-id="72048-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="72048-111">O último comando obtém a configuração de consumo de conexão das configurações HTTP de back-end $Settings e a armazena na variável $ConnectionDraining back-end.</span><span class="sxs-lookup"><span data-stu-id="72048-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="72048-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72048-112">PARAMETERS</span></span>

### <span data-ttu-id="72048-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="72048-113">-BackendHttpSettings</span></span>
<span data-ttu-id="72048-114">As configurações de http back-end</span><span class="sxs-lookup"><span data-stu-id="72048-114">The backend http settings</span></span>

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

### <span data-ttu-id="72048-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72048-115">-DefaultProfile</span></span>
<span data-ttu-id="72048-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="72048-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72048-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72048-117">CommonParameters</span></span>
<span data-ttu-id="72048-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72048-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72048-119">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72048-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72048-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="72048-120">INPUTS</span></span>

### <span data-ttu-id="72048-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="72048-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="72048-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="72048-122">OUTPUTS</span></span>

### <span data-ttu-id="72048-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="72048-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="72048-124">Notas</span><span class="sxs-lookup"><span data-stu-id="72048-124">NOTES</span></span>

## <span data-ttu-id="72048-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72048-125">RELATED LINKS</span></span>

[<span data-ttu-id="72048-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72048-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="72048-127">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="72048-127">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="72048-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="72048-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="72048-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="72048-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
