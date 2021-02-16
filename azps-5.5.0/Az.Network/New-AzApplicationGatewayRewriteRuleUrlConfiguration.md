---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113494"
---
# <span data-ttu-id="48b3b-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="48b3b-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="48b3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="48b3b-103">Cria uma configuração de url de regra de reescrita para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="48b3b-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="48b3b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48b3b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48b3b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="48b3b-105">DESCRIPTION</span></span>
<span data-ttu-id="48b3b-106">**O cmdlet AzApplicationGatewayRewriteRuleUrlConfiguration** cria uma configuração de url de regra de reescrita para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="48b3b-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="48b3b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48b3b-107">EXAMPLES</span></span>

### <span data-ttu-id="48b3b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="48b3b-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="48b3b-109">Esse comando cria uma configuração de url de regra de reescrita e armazena o resultado na variável chamada $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="48b3b-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="48b3b-110">Se você quiser atualizar qualquer UrlConfiguration existente, poderá fazê-lo criando uma nova UrlConfiguration e atribuindo a nova UrlConfiguration à propriedade UrlConfiguration do Conjunto de Ações de Regra de Reescrita.</span><span class="sxs-lookup"><span data-stu-id="48b3b-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="48b3b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48b3b-111">PARAMETERS</span></span>

### <span data-ttu-id="48b3b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b3b-112">-DefaultProfile</span></span>
<span data-ttu-id="48b3b-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48b3b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48b3b-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="48b3b-114">-ModifiedPath</span></span>
<span data-ttu-id="48b3b-115">Valor do caminho da URL.</span><span class="sxs-lookup"><span data-stu-id="48b3b-115">Url path value.</span></span>

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

### <span data-ttu-id="48b3b-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="48b3b-116">-ModifiedQueryString</span></span>
<span data-ttu-id="48b3b-117">Valor da cadeia de caracteres de consulta de url.</span><span class="sxs-lookup"><span data-stu-id="48b3b-117">Url query string value.</span></span>

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

### <span data-ttu-id="48b3b-118">-Redirecionar</span><span class="sxs-lookup"><span data-stu-id="48b3b-118">-Reroute</span></span>
<span data-ttu-id="48b3b-119">Sinalizar para reavaliação do mapa do caminho da URL fornecido nas regras de roteamento de solicitação baseadas em caminho usando o caminho modificado.</span><span class="sxs-lookup"><span data-stu-id="48b3b-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="48b3b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b3b-120">CommonParameters</span></span>
<span data-ttu-id="48b3b-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b3b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b3b-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48b3b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b3b-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="48b3b-123">INPUTS</span></span>

### <span data-ttu-id="48b3b-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="48b3b-124">None</span></span>

## <span data-ttu-id="48b3b-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="48b3b-125">OUTPUTS</span></span>

### <span data-ttu-id="48b3b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="48b3b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="48b3b-127">Notas</span><span class="sxs-lookup"><span data-stu-id="48b3b-127">NOTES</span></span>

## <span data-ttu-id="48b3b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48b3b-128">RELATED LINKS</span></span>

[<span data-ttu-id="48b3b-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="48b3b-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="48b3b-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="48b3b-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="48b3b-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="48b3b-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="48b3b-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="48b3b-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="48b3b-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="48b3b-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="48b3b-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="48b3b-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="48b3b-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="48b3b-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)