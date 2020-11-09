---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282210"
---
# <span data-ttu-id="9f410-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="9f410-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="9f410-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f410-102">SYNOPSIS</span></span>
<span data-ttu-id="9f410-103">Cria uma variável de correspondência para a condição do firewall.</span><span class="sxs-lookup"><span data-stu-id="9f410-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="9f410-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f410-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f410-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f410-105">DESCRIPTION</span></span>
<span data-ttu-id="9f410-106">O **New-AzApplicationGatewayFirewallMatchVariable** cria uma variável match para a condição do firewall.</span><span class="sxs-lookup"><span data-stu-id="9f410-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="9f410-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f410-107">EXAMPLES</span></span>

### <span data-ttu-id="9f410-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f410-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="9f410-109">O comando cria uma nova variável de correspondência com nome dos cabeçalhos de solicitação e do seletor é o campo Content-Length.</span><span class="sxs-lookup"><span data-stu-id="9f410-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="9f410-110">A nova variável de correspondência é salva em $variable.</span><span class="sxs-lookup"><span data-stu-id="9f410-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="9f410-111">OS</span><span class="sxs-lookup"><span data-stu-id="9f410-111">PARAMETERS</span></span>

### <span data-ttu-id="9f410-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f410-112">-DefaultProfile</span></span>
<span data-ttu-id="9f410-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f410-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f410-114">-Seletor</span><span class="sxs-lookup"><span data-stu-id="9f410-114">-Selector</span></span>
<span data-ttu-id="9f410-115">Descreve o campo da coleção matchVariable.</span><span class="sxs-lookup"><span data-stu-id="9f410-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="9f410-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="9f410-116">-VariableName</span></span>
<span data-ttu-id="9f410-117">Corresponder variável.</span><span class="sxs-lookup"><span data-stu-id="9f410-117">Match Variable.</span></span>

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

### <span data-ttu-id="9f410-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f410-118">CommonParameters</span></span>
<span data-ttu-id="9f410-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f410-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f410-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f410-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f410-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f410-121">INPUTS</span></span>

### <span data-ttu-id="9f410-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9f410-122">None</span></span>

## <span data-ttu-id="9f410-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f410-123">OUTPUTS</span></span>

### <span data-ttu-id="9f410-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="9f410-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="9f410-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f410-125">NOTES</span></span>

## <span data-ttu-id="9f410-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f410-126">RELATED LINKS</span></span>
