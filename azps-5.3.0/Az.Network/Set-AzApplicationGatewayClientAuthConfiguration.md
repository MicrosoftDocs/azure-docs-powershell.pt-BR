---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 9512d2d2a51e70b2a0b5e7aa2e8240a8aeb1be1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434650"
---
# <span data-ttu-id="69d5a-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="69d5a-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="69d5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="69d5a-103">Modifica a configuração de autenticação de cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="69d5a-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="69d5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69d5a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69d5a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69d5a-105">DESCRIPTION</span></span>
<span data-ttu-id="69d5a-106">O cmdlet **set-AzApplicationGatewayClientAuthConfiguration** modifica a configuração de autenticação de cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="69d5a-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="69d5a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69d5a-107">EXAMPLES</span></span>

### <span data-ttu-id="69d5a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69d5a-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="69d5a-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="69d5a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="69d5a-110">O segundo comando obtém o perfil SSL chamado SslProfile01 para $AppGw e armazena as configurações na variável $profile.</span><span class="sxs-lookup"><span data-stu-id="69d5a-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="69d5a-111">O último comando modifica a configuração de autenticação de cliente do objeto de perfil SSL armazenado em $profile.</span><span class="sxs-lookup"><span data-stu-id="69d5a-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="69d5a-112">OS</span><span class="sxs-lookup"><span data-stu-id="69d5a-112">PARAMETERS</span></span>

### <span data-ttu-id="69d5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69d5a-113">-DefaultProfile</span></span>
<span data-ttu-id="69d5a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69d5a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69d5a-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="69d5a-115">-SslProfile</span></span>
<span data-ttu-id="69d5a-116">O perfil SSL</span><span class="sxs-lookup"><span data-stu-id="69d5a-116">The ssl profile</span></span>

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

### <span data-ttu-id="69d5a-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="69d5a-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="69d5a-118">Verifique o nome do emissor do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="69d5a-118">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69d5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d5a-119">CommonParameters</span></span>
<span data-ttu-id="69d5a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69d5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d5a-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69d5a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d5a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69d5a-122">INPUTS</span></span>

### <span data-ttu-id="69d5a-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="69d5a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="69d5a-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69d5a-124">OUTPUTS</span></span>

### <span data-ttu-id="69d5a-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="69d5a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="69d5a-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69d5a-126">NOTES</span></span>

## <span data-ttu-id="69d5a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69d5a-127">RELATED LINKS</span></span>

[<span data-ttu-id="69d5a-128">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="69d5a-128">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="69d5a-129">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="69d5a-129">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="69d5a-130">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="69d5a-130">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="69d5a-131">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="69d5a-131">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)