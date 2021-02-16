---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 074ad4103128b9fd3943ebe4f450a04b74c28a75
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403554"
---
# <span data-ttu-id="5d70a-101">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d70a-101">Get-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="5d70a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d70a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d70a-103">Obtém a configuração de autenticação do cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="5d70a-103">Gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="5d70a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d70a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d70a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d70a-105">DESCRIPTION</span></span>
<span data-ttu-id="5d70a-106">O cmdlet **Get-AzApplicationGatewayClientAuthConfiguration** obtém a configuração de autenticação do cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="5d70a-106">The **Get-AzApplicationGatewayClientAuthConfiguration** cmdlet gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="5d70a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5d70a-107">EXAMPLES</span></span>

### <span data-ttu-id="5d70a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5d70a-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

<span data-ttu-id="5d70a-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5d70a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="5d70a-110">O segundo comando obtém o perfil SSL chamado SslProfile01 para $AppGw e o armazena $SslProfile variável.</span><span class="sxs-lookup"><span data-stu-id="5d70a-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="5d70a-111">O último comando obtém a configuração de autenticação do cliente do perfil SSL $SslProfile armazena-a na variável $ClientAuthConfig cliente.</span><span class="sxs-lookup"><span data-stu-id="5d70a-111">The last command gets the client authentication configuration from the SSL profile $SslProfile and stores it in the $ClientAuthConfig variable.</span></span>

## <span data-ttu-id="5d70a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d70a-112">PARAMETERS</span></span>

### <span data-ttu-id="5d70a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d70a-113">-DefaultProfile</span></span>
<span data-ttu-id="5d70a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d70a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70a-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="5d70a-115">-SslProfile</span></span>
<span data-ttu-id="5d70a-116">O perfil SSL</span><span class="sxs-lookup"><span data-stu-id="5d70a-116">The ssl profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d70a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d70a-117">CommonParameters</span></span>
<span data-ttu-id="5d70a-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d70a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d70a-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d70a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d70a-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="5d70a-120">INPUTS</span></span>

### <span data-ttu-id="5d70a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5d70a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="5d70a-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="5d70a-122">OUTPUTS</span></span>

### <span data-ttu-id="5d70a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d70a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="5d70a-124">Notas</span><span class="sxs-lookup"><span data-stu-id="5d70a-124">NOTES</span></span>

## <span data-ttu-id="5d70a-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d70a-125">RELATED LINKS</span></span>

[<span data-ttu-id="5d70a-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d70a-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)


[<span data-ttu-id="5d70a-127">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d70a-127">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="5d70a-128">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d70a-128">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
