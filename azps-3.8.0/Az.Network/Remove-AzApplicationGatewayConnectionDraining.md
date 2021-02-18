---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 4b0eb6188f75b71e3e56107138b6d5e2f9fc7b93
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406062"
---
# <span data-ttu-id="9d4dc-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9d4dc-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9d4dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="9d4dc-103">Remove a configuração de drenamento de conexão de um objeto de configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="9d4dc-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="9d4dc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d4dc-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d4dc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d4dc-105">DESCRIPTION</span></span>
<span data-ttu-id="9d4dc-106">O cmdlet **Remove-AzApplicationGatewayConnectionDraining** remove a configuração de drenamento de conexão de um objeto de configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="9d4dc-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="9d4dc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9d4dc-107">EXAMPLES</span></span>

### <span data-ttu-id="9d4dc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9d4dc-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="9d4dc-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9d4dc-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9d4dc-110">O segundo comando obtém as configurações HTTP de back-end chamadas Configurações01 para $AppGw e armazena as configurações na variável $Settings back-end.</span><span class="sxs-lookup"><span data-stu-id="9d4dc-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="9d4dc-111">O último comando remove a configuração de esgotamento de conexão das configurações HTTP de back-end armazenadas no $Settings.</span><span class="sxs-lookup"><span data-stu-id="9d4dc-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="9d4dc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d4dc-112">PARAMETERS</span></span>

### <span data-ttu-id="9d4dc-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9d4dc-113">-BackendHttpSettings</span></span>
<span data-ttu-id="9d4dc-114">As configurações de http back-end</span><span class="sxs-lookup"><span data-stu-id="9d4dc-114">The backend http settings</span></span>

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

### <span data-ttu-id="9d4dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d4dc-115">-DefaultProfile</span></span>
<span data-ttu-id="9d4dc-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9d4dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d4dc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d4dc-117">CommonParameters</span></span>
<span data-ttu-id="9d4dc-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d4dc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d4dc-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d4dc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d4dc-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="9d4dc-120">INPUTS</span></span>

### <span data-ttu-id="9d4dc-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9d4dc-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="9d4dc-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="9d4dc-122">OUTPUTS</span></span>

### <span data-ttu-id="9d4dc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9d4dc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="9d4dc-124">Notas</span><span class="sxs-lookup"><span data-stu-id="9d4dc-124">NOTES</span></span>

## <span data-ttu-id="9d4dc-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d4dc-125">RELATED LINKS</span></span>

[<span data-ttu-id="9d4dc-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d4dc-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="9d4dc-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9d4dc-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9d4dc-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9d4dc-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9d4dc-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9d4dc-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

