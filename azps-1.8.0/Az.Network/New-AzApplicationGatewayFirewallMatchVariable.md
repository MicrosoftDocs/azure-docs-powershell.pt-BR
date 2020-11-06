---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: 05a1929f79799be8006ae82c4948dc0a81839040
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600414"
---
# <span data-ttu-id="987fb-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="987fb-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="987fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="987fb-102">SYNOPSIS</span></span>
<span data-ttu-id="987fb-103">Cria uma variável de correspondência para a condição do firewall.</span><span class="sxs-lookup"><span data-stu-id="987fb-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="987fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="987fb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="987fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="987fb-105">DESCRIPTION</span></span>
<span data-ttu-id="987fb-106">O **New-AzApplicationGatewayFirewallMatchVariable** cria uma variável match para a condição do firewall.</span><span class="sxs-lookup"><span data-stu-id="987fb-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="987fb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="987fb-107">EXAMPLES</span></span>

### <span data-ttu-id="987fb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="987fb-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzureRmApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="987fb-109">O comando cria uma nova variável de correspondência com nome dos cabeçalhos de solicitação e do seletor é o campo Content-Length.</span><span class="sxs-lookup"><span data-stu-id="987fb-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="987fb-110">A nova variável de correspondência é salva em $variable.</span><span class="sxs-lookup"><span data-stu-id="987fb-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="987fb-111">OS</span><span class="sxs-lookup"><span data-stu-id="987fb-111">PARAMETERS</span></span>

### <span data-ttu-id="987fb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987fb-112">-DefaultProfile</span></span>
<span data-ttu-id="987fb-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="987fb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="987fb-114">-Seletor</span><span class="sxs-lookup"><span data-stu-id="987fb-114">-Selector</span></span>
<span data-ttu-id="987fb-115">Descreve o campo da coleção matchVariable.</span><span class="sxs-lookup"><span data-stu-id="987fb-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="987fb-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="987fb-116">-VariableName</span></span>
<span data-ttu-id="987fb-117">Corresponder variável.</span><span class="sxs-lookup"><span data-stu-id="987fb-117">Match Variable.</span></span>

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

### <span data-ttu-id="987fb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987fb-118">CommonParameters</span></span>
<span data-ttu-id="987fb-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="987fb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987fb-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="987fb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987fb-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="987fb-121">INPUTS</span></span>

### <span data-ttu-id="987fb-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="987fb-122">None</span></span>

## <span data-ttu-id="987fb-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="987fb-123">OUTPUTS</span></span>

### <span data-ttu-id="987fb-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="987fb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="987fb-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="987fb-125">NOTES</span></span>

## <span data-ttu-id="987fb-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="987fb-126">RELATED LINKS</span></span>
