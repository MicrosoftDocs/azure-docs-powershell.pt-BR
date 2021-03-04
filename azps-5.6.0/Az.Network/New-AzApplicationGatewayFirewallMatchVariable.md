---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: 824c1c4e98fca6b6f7d2ff3df9217cb000eeaf21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901459"
---
# <span data-ttu-id="bf890-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="bf890-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="bf890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf890-102">SYNOPSIS</span></span>
<span data-ttu-id="bf890-103">Cria uma variável de match para a condição de firewall.</span><span class="sxs-lookup"><span data-stu-id="bf890-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="bf890-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bf890-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf890-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bf890-105">DESCRIPTION</span></span>
<span data-ttu-id="bf890-106">O **New-AzApplicationGatewayFirewallMatchVariable** cria uma variável de match para a condição de firewall.</span><span class="sxs-lookup"><span data-stu-id="bf890-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="bf890-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf890-107">EXAMPLES</span></span>

### <span data-ttu-id="bf890-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf890-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="bf890-109">O comando cria uma nova variável de match com o nome dos headers de solicitação e o seletor é o campo Content-Length.</span><span class="sxs-lookup"><span data-stu-id="bf890-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="bf890-110">A nova variável de match é salva $variable.</span><span class="sxs-lookup"><span data-stu-id="bf890-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="bf890-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bf890-111">PARAMETERS</span></span>

### <span data-ttu-id="bf890-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf890-112">-DefaultProfile</span></span>
<span data-ttu-id="bf890-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf890-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf890-114">-Seletor</span><span class="sxs-lookup"><span data-stu-id="bf890-114">-Selector</span></span>
<span data-ttu-id="bf890-115">Descreve o campo da coleção matchVariable.</span><span class="sxs-lookup"><span data-stu-id="bf890-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="bf890-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="bf890-116">-VariableName</span></span>
<span data-ttu-id="bf890-117">Match Variable.</span><span class="sxs-lookup"><span data-stu-id="bf890-117">Match Variable.</span></span>

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

### <span data-ttu-id="bf890-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf890-118">CommonParameters</span></span>
<span data-ttu-id="bf890-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf890-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf890-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf890-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf890-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf890-121">INPUTS</span></span>

### <span data-ttu-id="bf890-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bf890-122">None</span></span>

## <span data-ttu-id="bf890-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bf890-123">OUTPUTS</span></span>

### <span data-ttu-id="bf890-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="bf890-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="bf890-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="bf890-125">NOTES</span></span>

## <span data-ttu-id="bf890-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf890-126">RELATED LINKS</span></span>
