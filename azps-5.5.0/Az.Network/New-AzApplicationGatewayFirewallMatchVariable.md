---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117425"
---
# <span data-ttu-id="bff2a-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="bff2a-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="bff2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bff2a-102">SYNOPSIS</span></span>
<span data-ttu-id="bff2a-103">Cria uma variável de match para a condição de firewall.</span><span class="sxs-lookup"><span data-stu-id="bff2a-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="bff2a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bff2a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bff2a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bff2a-105">DESCRIPTION</span></span>
<span data-ttu-id="bff2a-106">O **New-AzApplicationGatewayFirewallMatchVariable** cria uma variável de match para a condição de firewall.</span><span class="sxs-lookup"><span data-stu-id="bff2a-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="bff2a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bff2a-107">EXAMPLES</span></span>

### <span data-ttu-id="bff2a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bff2a-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="bff2a-109">O comando cria uma nova variável de match com o nome dos títulos de solicitação e o seletor é o campo Comprimento do Conteúdo.</span><span class="sxs-lookup"><span data-stu-id="bff2a-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="bff2a-110">A nova variável de match é salva em $variable.</span><span class="sxs-lookup"><span data-stu-id="bff2a-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="bff2a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bff2a-111">PARAMETERS</span></span>

### <span data-ttu-id="bff2a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff2a-112">-DefaultProfile</span></span>
<span data-ttu-id="bff2a-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bff2a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff2a-114">-Seletor</span><span class="sxs-lookup"><span data-stu-id="bff2a-114">-Selector</span></span>
<span data-ttu-id="bff2a-115">Descreve o campo da coleção matchVariable.</span><span class="sxs-lookup"><span data-stu-id="bff2a-115">Describes field of the matchVariable collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff2a-116">-Nome Variável</span><span class="sxs-lookup"><span data-stu-id="bff2a-116">-VariableName</span></span>
<span data-ttu-id="bff2a-117">Corresponder Variável.</span><span class="sxs-lookup"><span data-stu-id="bff2a-117">Match Variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeaders, RequestBody, RequestCookies

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff2a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff2a-118">CommonParameters</span></span>
<span data-ttu-id="bff2a-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bff2a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff2a-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff2a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff2a-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="bff2a-121">INPUTS</span></span>

### <span data-ttu-id="bff2a-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bff2a-122">None</span></span>

## <span data-ttu-id="bff2a-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="bff2a-123">OUTPUTS</span></span>

### <span data-ttu-id="bff2a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="bff2a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="bff2a-125">Notas</span><span class="sxs-lookup"><span data-stu-id="bff2a-125">NOTES</span></span>

## <span data-ttu-id="bff2a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bff2a-126">RELATED LINKS</span></span>
