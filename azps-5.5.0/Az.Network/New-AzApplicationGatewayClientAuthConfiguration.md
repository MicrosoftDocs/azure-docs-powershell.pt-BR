---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 68ab3fbd87e5fe28fffdd0f6d769fb21d0ce9e6e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398080"
---
# <span data-ttu-id="03b58-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="03b58-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="03b58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03b58-102">SYNOPSIS</span></span>
<span data-ttu-id="03b58-103">Cria uma nova configuração de autenticação de cliente para perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="03b58-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="03b58-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03b58-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03b58-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="03b58-105">DESCRIPTION</span></span>
<span data-ttu-id="03b58-106">O cmdlet **New-AzApplicationGatewayClientAuthConfiguration** cria uma nova configuração de autenticação de cliente para o perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="03b58-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="03b58-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="03b58-107">EXAMPLES</span></span>

### <span data-ttu-id="03b58-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="03b58-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="03b58-109">O comando cria uma nova configuração de auth do cliente e a armazena $clientAuthConfig variável a ser usada em um perfil SSL.</span><span class="sxs-lookup"><span data-stu-id="03b58-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="03b58-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03b58-110">PARAMETERS</span></span>

### <span data-ttu-id="03b58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b58-111">-DefaultProfile</span></span>
<span data-ttu-id="03b58-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03b58-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03b58-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="03b58-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="03b58-114">Verificar o nome do emissor do certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="03b58-114">Verify client certificate issuer name.</span></span>

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

### <span data-ttu-id="03b58-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b58-115">CommonParameters</span></span>
<span data-ttu-id="03b58-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b58-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b58-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03b58-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b58-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="03b58-118">INPUTS</span></span>

### <span data-ttu-id="03b58-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="03b58-119">None</span></span>

## <span data-ttu-id="03b58-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="03b58-120">OUTPUTS</span></span>

### <span data-ttu-id="03b58-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="03b58-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="03b58-122">Notas</span><span class="sxs-lookup"><span data-stu-id="03b58-122">NOTES</span></span>

## <span data-ttu-id="03b58-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03b58-123">RELATED LINKS</span></span>


[<span data-ttu-id="03b58-124">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="03b58-124">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="03b58-125">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="03b58-125">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="03b58-126">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="03b58-126">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)
