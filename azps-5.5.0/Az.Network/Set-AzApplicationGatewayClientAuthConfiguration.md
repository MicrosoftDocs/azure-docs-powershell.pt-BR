---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: def44c0925239aed345eed84b4f34690d2db8746
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100395683"
---
# <span data-ttu-id="8603d-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8603d-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="8603d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8603d-102">SYNOPSIS</span></span>
<span data-ttu-id="8603d-103">Modifica a configuração de auth do cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="8603d-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="8603d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8603d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8603d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8603d-105">DESCRIPTION</span></span>
<span data-ttu-id="8603d-106">O cmdlet **Set-AzApplicationGatewayClientAuthConfiguration** modifica a configuração de auth do cliente de um objeto de perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="8603d-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="8603d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8603d-107">EXAMPLES</span></span>

### <span data-ttu-id="8603d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8603d-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="8603d-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8603d-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="8603d-110">O segundo comando obtém o perfil SSL chamado SslProfile01 para $AppGw e armazena as configurações na variável $profile.</span><span class="sxs-lookup"><span data-stu-id="8603d-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="8603d-111">O último comando modifica a configuração de auth do cliente do objeto de perfil ssl armazenado em $profile.</span><span class="sxs-lookup"><span data-stu-id="8603d-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="8603d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8603d-112">PARAMETERS</span></span>

### <span data-ttu-id="8603d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8603d-113">-DefaultProfile</span></span>
<span data-ttu-id="8603d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8603d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8603d-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="8603d-115">-SslProfile</span></span>
<span data-ttu-id="8603d-116">O perfil SSL</span><span class="sxs-lookup"><span data-stu-id="8603d-116">The ssl profile</span></span>

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

### <span data-ttu-id="8603d-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="8603d-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="8603d-118">Verificar o nome do emissor do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="8603d-118">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="8603d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8603d-119">CommonParameters</span></span>
<span data-ttu-id="8603d-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8603d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8603d-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8603d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8603d-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="8603d-122">INPUTS</span></span>

### <span data-ttu-id="8603d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8603d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="8603d-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="8603d-124">OUTPUTS</span></span>

### <span data-ttu-id="8603d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8603d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="8603d-126">Notas</span><span class="sxs-lookup"><span data-stu-id="8603d-126">NOTES</span></span>

## <span data-ttu-id="8603d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8603d-127">RELATED LINKS</span></span>


[<span data-ttu-id="8603d-128">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8603d-128">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="8603d-129">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8603d-129">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="8603d-130">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8603d-130">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)
