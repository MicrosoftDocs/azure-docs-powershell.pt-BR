---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 92d3945e92dc4996fbbe3fc0abbcc296ab141621
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271694"
---
# <span data-ttu-id="2c5bd-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c5bd-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="2c5bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c5bd-102">SYNOPSIS</span></span>
<span data-ttu-id="2c5bd-103">Remove a configuração de autenticação de cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="2c5bd-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="2c5bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c5bd-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c5bd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c5bd-105">DESCRIPTION</span></span>
<span data-ttu-id="2c5bd-106">O cmdlet **Remove-AzApplicationGatewayClientAuthConfiguration** remove a configuração de autenticação de cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="2c5bd-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="2c5bd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c5bd-107">EXAMPLES</span></span>

### <span data-ttu-id="2c5bd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c5bd-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="2c5bd-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2c5bd-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="2c5bd-110">O segundo comando obtém o perfil SSL chamado Profile01 para $AppGw e o armazena na variável $profile.</span><span class="sxs-lookup"><span data-stu-id="2c5bd-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="2c5bd-111">O último comando Remove a configuração de autenticação de cliente do perfil SSL armazenado em $profile.</span><span class="sxs-lookup"><span data-stu-id="2c5bd-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="2c5bd-112">OS</span><span class="sxs-lookup"><span data-stu-id="2c5bd-112">PARAMETERS</span></span>

### <span data-ttu-id="2c5bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c5bd-113">-DefaultProfile</span></span>
<span data-ttu-id="2c5bd-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c5bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c5bd-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="2c5bd-115">-SslProfile</span></span>
<span data-ttu-id="2c5bd-116">O perfil SSL</span><span class="sxs-lookup"><span data-stu-id="2c5bd-116">The ssl profile</span></span>

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

### <span data-ttu-id="2c5bd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c5bd-117">CommonParameters</span></span>
<span data-ttu-id="2c5bd-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c5bd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c5bd-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c5bd-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c5bd-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c5bd-120">INPUTS</span></span>

### <span data-ttu-id="2c5bd-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2c5bd-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="2c5bd-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c5bd-122">OUTPUTS</span></span>

### <span data-ttu-id="2c5bd-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="2c5bd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="2c5bd-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c5bd-124">NOTES</span></span>

## <span data-ttu-id="2c5bd-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c5bd-125">RELATED LINKS</span></span>

[<span data-ttu-id="2c5bd-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c5bd-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="2c5bd-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c5bd-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="2c5bd-128">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c5bd-128">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="2c5bd-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c5bd-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)