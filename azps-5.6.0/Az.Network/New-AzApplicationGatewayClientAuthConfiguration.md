---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 002fdabfb01a0b12d36c69b0a8a75ddf91880012
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887093"
---
# <span data-ttu-id="46279-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46279-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="46279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46279-102">SYNOPSIS</span></span>
<span data-ttu-id="46279-103">Cria uma nova configuração de autenticação de cliente para perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="46279-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="46279-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="46279-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46279-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="46279-105">DESCRIPTION</span></span>
<span data-ttu-id="46279-106">O cmdlet **New-AzApplicationGatewayClientAuthConfiguration** cria uma nova configuração de autenticação de cliente para o perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="46279-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="46279-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46279-107">EXAMPLES</span></span>

### <span data-ttu-id="46279-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46279-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="46279-109">O comando cria uma nova configuração de auth do cliente e a armazena $clientAuthConfig variável a ser usada em um perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="46279-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="46279-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="46279-110">PARAMETERS</span></span>

### <span data-ttu-id="46279-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46279-111">-DefaultProfile</span></span>
<span data-ttu-id="46279-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46279-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46279-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="46279-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="46279-114">Verifique o nome do emissor do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="46279-114">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="46279-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46279-115">CommonParameters</span></span>
<span data-ttu-id="46279-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46279-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46279-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46279-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46279-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46279-118">INPUTS</span></span>

### <span data-ttu-id="46279-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="46279-119">None</span></span>

## <span data-ttu-id="46279-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="46279-120">OUTPUTS</span></span>

### <span data-ttu-id="46279-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46279-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="46279-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="46279-122">NOTES</span></span>

## <span data-ttu-id="46279-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46279-123">RELATED LINKS</span></span>

[<span data-ttu-id="46279-124">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46279-124">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="46279-125">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46279-125">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="46279-126">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46279-126">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="46279-127">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46279-127">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)