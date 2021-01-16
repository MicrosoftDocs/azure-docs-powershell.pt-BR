---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 92d3945e92dc4996fbbe3fc0abbcc296ab141621
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258575"
---
# <span data-ttu-id="ce711-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce711-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="ce711-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce711-102">SYNOPSIS</span></span>
<span data-ttu-id="ce711-103">Remove a configuração de autenticação de cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="ce711-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="ce711-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce711-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce711-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce711-105">DESCRIPTION</span></span>
<span data-ttu-id="ce711-106">O cmdlet **Remove-AzApplicationGatewayClientAuthConfiguration** remove a configuração de autenticação de cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="ce711-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="ce711-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce711-107">EXAMPLES</span></span>

### <span data-ttu-id="ce711-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce711-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="ce711-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ce711-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="ce711-110">O segundo comando obtém o perfil SSL chamado Profile01 para $AppGw e o armazena na variável $profile.</span><span class="sxs-lookup"><span data-stu-id="ce711-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="ce711-111">O último comando Remove a configuração de autenticação de cliente do perfil SSL armazenado em $profile.</span><span class="sxs-lookup"><span data-stu-id="ce711-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="ce711-112">OS</span><span class="sxs-lookup"><span data-stu-id="ce711-112">PARAMETERS</span></span>

### <span data-ttu-id="ce711-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce711-113">-DefaultProfile</span></span>
<span data-ttu-id="ce711-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce711-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce711-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="ce711-115">-SslProfile</span></span>
<span data-ttu-id="ce711-116">O perfil SSL</span><span class="sxs-lookup"><span data-stu-id="ce711-116">The ssl profile</span></span>

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

### <span data-ttu-id="ce711-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce711-117">CommonParameters</span></span>
<span data-ttu-id="ce711-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce711-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce711-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce711-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce711-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce711-120">INPUTS</span></span>

### <span data-ttu-id="ce711-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ce711-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="ce711-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce711-122">OUTPUTS</span></span>

### <span data-ttu-id="ce711-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ce711-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="ce711-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce711-124">NOTES</span></span>

## <span data-ttu-id="ce711-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce711-125">RELATED LINKS</span></span>

[<span data-ttu-id="ce711-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce711-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="ce711-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce711-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="ce711-128">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce711-128">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="ce711-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce711-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)