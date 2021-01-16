---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 6e8c3cdbfa1242cba19d3aa3250c4bf4e381ae92
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260619"
---
# <span data-ttu-id="0b4fb-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b4fb-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="0b4fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b4fb-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4fb-103">Cria uma nova configuração de autenticação de cliente para o perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="0b4fb-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="0b4fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b4fb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b4fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b4fb-105">DESCRIPTION</span></span>
<span data-ttu-id="0b4fb-106">O cmdlet **New-AzApplicationGatewayClientAuthConfiguration** cria uma nova configuração de autenticação de cliente para o perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="0b4fb-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="0b4fb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b4fb-107">EXAMPLES</span></span>

### <span data-ttu-id="0b4fb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0b4fb-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="0b4fb-109">O comando cria uma nova configuração de autenticação de cliente e a armazena em $clientAuthConfig variável para ser usada em um perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="0b4fb-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="0b4fb-110">OS</span><span class="sxs-lookup"><span data-stu-id="0b4fb-110">PARAMETERS</span></span>

### <span data-ttu-id="0b4fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4fb-111">-DefaultProfile</span></span>
<span data-ttu-id="0b4fb-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4fb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b4fb-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="0b4fb-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="0b4fb-114">Verifique o nome do emissor do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="0b4fb-114">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="0b4fb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4fb-115">CommonParameters</span></span>
<span data-ttu-id="0b4fb-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b4fb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4fb-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b4fb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4fb-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b4fb-118">INPUTS</span></span>

### <span data-ttu-id="0b4fb-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0b4fb-119">None</span></span>

## <span data-ttu-id="0b4fb-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b4fb-120">OUTPUTS</span></span>

### <span data-ttu-id="0b4fb-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b4fb-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="0b4fb-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b4fb-122">NOTES</span></span>

## <span data-ttu-id="0b4fb-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b4fb-123">RELATED LINKS</span></span>

[<span data-ttu-id="0b4fb-124">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b4fb-124">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="0b4fb-125">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b4fb-125">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="0b4fb-126">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b4fb-126">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="0b4fb-127">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b4fb-127">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)