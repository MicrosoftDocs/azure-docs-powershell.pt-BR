---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944772"
---
# <span data-ttu-id="4f819-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f819-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="4f819-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f819-102">SYNOPSIS</span></span>
<span data-ttu-id="4f819-103">Cria uma configuração de URL de regra de regravação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4f819-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="4f819-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f819-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f819-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f819-105">DESCRIPTION</span></span>
<span data-ttu-id="4f819-106">**O cmdlet AzApplicationGatewayRewriteRuleUrlConfiguration** cria uma configuração de URL de regra de regravação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f819-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="4f819-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f819-107">EXAMPLES</span></span>

### <span data-ttu-id="4f819-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4f819-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="4f819-109">Esse comando cria uma configuração de URL de regra de regravação e armazena o resultado na variável chamada $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4f819-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="4f819-110">Se você deseja atualizar qualquer UrlConfiguration existente, é possível fazer isso criando um novo UrlConfiguration e atribuindo o novo UrlConfiguration à propriedade UrlConfiguration do conjunto de ações regra de regravação.</span><span class="sxs-lookup"><span data-stu-id="4f819-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="4f819-111">OS</span><span class="sxs-lookup"><span data-stu-id="4f819-111">PARAMETERS</span></span>

### <span data-ttu-id="4f819-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f819-112">-DefaultProfile</span></span>
<span data-ttu-id="4f819-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f819-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f819-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="4f819-114">-ModifiedPath</span></span>
<span data-ttu-id="4f819-115">Valor de caminho da URL.</span><span class="sxs-lookup"><span data-stu-id="4f819-115">Url path value.</span></span>

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

### <span data-ttu-id="4f819-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="4f819-116">-ModifiedQueryString</span></span>
<span data-ttu-id="4f819-117">Valor da cadeia de consulta de URL.</span><span class="sxs-lookup"><span data-stu-id="4f819-117">Url query string value.</span></span>

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

### <span data-ttu-id="4f819-118">-Redirecionar</span><span class="sxs-lookup"><span data-stu-id="4f819-118">-Reroute</span></span>
<span data-ttu-id="4f819-119">Sinalizador para reavaliar o mapa de caminho de URL fornecido em regras de roteamento de solicitação baseado em caminho usando o caminho modificado.</span><span class="sxs-lookup"><span data-stu-id="4f819-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f819-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f819-120">CommonParameters</span></span>
<span data-ttu-id="4f819-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f819-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f819-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f819-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f819-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f819-123">INPUTS</span></span>

### <span data-ttu-id="4f819-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4f819-124">None</span></span>

## <span data-ttu-id="4f819-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f819-125">OUTPUTS</span></span>

### <span data-ttu-id="4f819-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f819-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="4f819-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f819-127">NOTES</span></span>

## <span data-ttu-id="4f819-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f819-128">RELATED LINKS</span></span>

[<span data-ttu-id="4f819-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f819-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4f819-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f819-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4f819-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f819-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4f819-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f819-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4f819-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f819-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4f819-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4f819-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="4f819-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4f819-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)