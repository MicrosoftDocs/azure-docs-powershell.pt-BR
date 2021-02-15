---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 98b097e0be8d4b08ba16d5af06fbec1a2f3d66de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112802"
---
# <span data-ttu-id="b8220-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8220-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="b8220-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8220-102">SYNOPSIS</span></span>
<span data-ttu-id="b8220-103">Remove a configuração de drenamento de conexão de um objeto de configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="b8220-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="b8220-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8220-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8220-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8220-105">DESCRIPTION</span></span>
<span data-ttu-id="b8220-106">O cmdlet **Remove-AzApplicationGatewayConnectionDraining** remove a configuração de drenamento de conexão de um objeto de configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="b8220-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="b8220-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b8220-107">EXAMPLES</span></span>

### <span data-ttu-id="b8220-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8220-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="b8220-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b8220-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b8220-110">O segundo comando obtém as configurações HTTP de back-end chamadas Configurações01 para $AppGw e armazena as configurações na variável $Settings back-end.</span><span class="sxs-lookup"><span data-stu-id="b8220-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="b8220-111">O último comando remove a configuração de esgotamento de conexão das configurações HTTP de back-end armazenadas no $Settings.</span><span class="sxs-lookup"><span data-stu-id="b8220-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="b8220-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8220-112">PARAMETERS</span></span>

### <span data-ttu-id="b8220-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b8220-113">-BackendHttpSettings</span></span>
<span data-ttu-id="b8220-114">As configurações de http back-end</span><span class="sxs-lookup"><span data-stu-id="b8220-114">The backend http settings</span></span>

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

### <span data-ttu-id="b8220-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8220-115">-DefaultProfile</span></span>
<span data-ttu-id="b8220-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b8220-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8220-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8220-117">CommonParameters</span></span>
<span data-ttu-id="b8220-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8220-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8220-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8220-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8220-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="b8220-120">INPUTS</span></span>

### <span data-ttu-id="b8220-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b8220-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b8220-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="b8220-122">OUTPUTS</span></span>

### <span data-ttu-id="b8220-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b8220-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b8220-124">Notas</span><span class="sxs-lookup"><span data-stu-id="b8220-124">NOTES</span></span>

## <span data-ttu-id="b8220-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8220-125">RELATED LINKS</span></span>

[<span data-ttu-id="b8220-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8220-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="b8220-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="b8220-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="b8220-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8220-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b8220-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8220-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b8220-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b8220-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

