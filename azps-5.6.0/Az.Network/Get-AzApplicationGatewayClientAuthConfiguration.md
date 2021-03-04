---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 74fba2cf4e91d939f4e88b66b47d92e0bc5c0730
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888674"
---
# <span data-ttu-id="c8c75-101">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c75-101">Get-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="c8c75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8c75-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c75-103">Obtém a configuração de autenticação do cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="c8c75-103">Gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="c8c75-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c8c75-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8c75-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c8c75-105">DESCRIPTION</span></span>
<span data-ttu-id="c8c75-106">O cmdlet **Get-AzApplicationGatewayClientAuthConfiguration** obtém a configuração de autenticação do cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="c8c75-106">The **Get-AzApplicationGatewayClientAuthConfiguration** cmdlet gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="c8c75-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8c75-107">EXAMPLES</span></span>

### <span data-ttu-id="c8c75-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8c75-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

<span data-ttu-id="c8c75-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c8c75-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="c8c75-110">O segundo comando obtém o perfil SSL chamado SslProfile01 para $AppGw e o armazena $SslProfile variável.</span><span class="sxs-lookup"><span data-stu-id="c8c75-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="c8c75-111">O último comando obtém a configuração de autenticação do cliente $SslProfile perfil SSL e armazena-a na variável $ClientAuthConfig cliente.</span><span class="sxs-lookup"><span data-stu-id="c8c75-111">The last command gets the client authentication configuration from the SSL profile $SslProfile and stores it in the $ClientAuthConfig variable.</span></span>

## <span data-ttu-id="c8c75-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c8c75-112">PARAMETERS</span></span>

### <span data-ttu-id="c8c75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c75-113">-DefaultProfile</span></span>
<span data-ttu-id="c8c75-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c75-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8c75-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="c8c75-115">-SslProfile</span></span>
<span data-ttu-id="c8c75-116">O perfil ssl</span><span class="sxs-lookup"><span data-stu-id="c8c75-116">The ssl profile</span></span>

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

### <span data-ttu-id="c8c75-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c75-117">CommonParameters</span></span>
<span data-ttu-id="c8c75-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c75-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c75-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8c75-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c75-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8c75-120">INPUTS</span></span>

### <span data-ttu-id="c8c75-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c8c75-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c8c75-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c8c75-122">OUTPUTS</span></span>

### <span data-ttu-id="c8c75-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c75-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="c8c75-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="c8c75-124">NOTES</span></span>

## <span data-ttu-id="c8c75-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8c75-125">RELATED LINKS</span></span>

[<span data-ttu-id="c8c75-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c75-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="c8c75-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c75-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="c8c75-128">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c75-128">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="c8c75-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8c75-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)