---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 92d3945e92dc4996fbbe3fc0abbcc296ab141621
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113466"
---
# <span data-ttu-id="46436-101">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46436-101">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="46436-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46436-102">SYNOPSIS</span></span>
<span data-ttu-id="46436-103">Remove a configuração de autenticação do cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="46436-103">Removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="46436-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46436-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46436-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="46436-105">DESCRIPTION</span></span>
<span data-ttu-id="46436-106">O cmdlet **Remove-AzApplicationGatewayClientAuthConfiguration** remove a configuração de autenticação do cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="46436-106">The **Remove-AzApplicationGatewayClientAuthConfiguration** cmdlet removes the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="46436-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46436-107">EXAMPLES</span></span>

### <span data-ttu-id="46436-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46436-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile
```

<span data-ttu-id="46436-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="46436-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="46436-110">O segundo comando obtém o perfil SSL chamado Perfil01 para $AppGw e o armazena na variável $profile usuário.</span><span class="sxs-lookup"><span data-stu-id="46436-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="46436-111">O último comando remove a configuração de autenticação do cliente do perfil SSL armazenado no $profile.</span><span class="sxs-lookup"><span data-stu-id="46436-111">The last command removes the client authentication configuration of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="46436-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46436-112">PARAMETERS</span></span>

### <span data-ttu-id="46436-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46436-113">-DefaultProfile</span></span>
<span data-ttu-id="46436-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46436-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46436-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="46436-115">-SslProfile</span></span>
<span data-ttu-id="46436-116">O perfil SSL</span><span class="sxs-lookup"><span data-stu-id="46436-116">The ssl profile</span></span>

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

### <span data-ttu-id="46436-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46436-117">CommonParameters</span></span>
<span data-ttu-id="46436-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46436-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46436-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46436-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46436-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="46436-120">INPUTS</span></span>

### <span data-ttu-id="46436-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="46436-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="46436-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="46436-122">OUTPUTS</span></span>

### <span data-ttu-id="46436-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="46436-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="46436-124">Notas</span><span class="sxs-lookup"><span data-stu-id="46436-124">NOTES</span></span>

## <span data-ttu-id="46436-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46436-125">RELATED LINKS</span></span>

[<span data-ttu-id="46436-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46436-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="46436-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46436-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="46436-128">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46436-128">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="46436-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46436-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)