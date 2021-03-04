---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: e9b0b8cdbee1e4d5c488e51f537d18cca2ef681a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885409"
---
# <span data-ttu-id="37623-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="37623-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="37623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37623-102">SYNOPSIS</span></span>
<span data-ttu-id="37623-103">Cria uma configuração de url de regra de regra de reescrita para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="37623-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="37623-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="37623-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37623-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="37623-105">DESCRIPTION</span></span>
<span data-ttu-id="37623-106">O cmdlet **AzApplicationGatewayRewriteRuleUrlConfiguration** cria uma configuração de url de regra de regra de reescrita para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="37623-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="37623-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37623-107">EXAMPLES</span></span>

### <span data-ttu-id="37623-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37623-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="37623-109">Este comando cria uma configuração de url de regra de regra de reescrita e armazena o resultado na variável chamada $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="37623-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="37623-110">Se você quiser atualizar qualquer UrlConfiguration existente, você pode fazê-lo criando uma nova UrlConfiguration e atribuindo a nova UrlConfiguration à propriedade UrlConfiguration do Conjunto de Ações de Regra de Regra de Reescrita.</span><span class="sxs-lookup"><span data-stu-id="37623-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="37623-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="37623-111">PARAMETERS</span></span>

### <span data-ttu-id="37623-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37623-112">-DefaultProfile</span></span>
<span data-ttu-id="37623-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37623-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37623-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="37623-114">-ModifiedPath</span></span>
<span data-ttu-id="37623-115">Valor do caminho da URL.</span><span class="sxs-lookup"><span data-stu-id="37623-115">Url path value.</span></span>

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

### <span data-ttu-id="37623-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="37623-116">-ModifiedQueryString</span></span>
<span data-ttu-id="37623-117">Valor da cadeia de caracteres de consulta de url.</span><span class="sxs-lookup"><span data-stu-id="37623-117">Url query string value.</span></span>

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

### <span data-ttu-id="37623-118">-Redirecionar</span><span class="sxs-lookup"><span data-stu-id="37623-118">-Reroute</span></span>
<span data-ttu-id="37623-119">Sinalizador para reavaliação do mapa de caminho da url fornecido em regras de roteamento de solicitações baseadas no caminho usando caminho modificado.</span><span class="sxs-lookup"><span data-stu-id="37623-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="37623-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37623-120">CommonParameters</span></span>
<span data-ttu-id="37623-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37623-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37623-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37623-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37623-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37623-123">INPUTS</span></span>

### <span data-ttu-id="37623-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="37623-124">None</span></span>

## <span data-ttu-id="37623-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="37623-125">OUTPUTS</span></span>

### <span data-ttu-id="37623-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="37623-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="37623-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="37623-127">NOTES</span></span>

## <span data-ttu-id="37623-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37623-128">RELATED LINKS</span></span>

[<span data-ttu-id="37623-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37623-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37623-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37623-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37623-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37623-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37623-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37623-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37623-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="37623-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="37623-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="37623-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="37623-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="37623-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)