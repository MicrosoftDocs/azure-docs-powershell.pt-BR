---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: ded23a30c078cd1d474310d73d94717d050f6824
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399270"
---
# <span data-ttu-id="b8c9a-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8c9a-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="b8c9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c9a-103">Adiciona uma regra de filtro de rota a um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="b8c9a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8c9a-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8c9a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8c9a-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c9a-106">O Add-AzRouteFilterRuleConfig cmdlet adiciona uma regra de filtro de rota a um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="b8c9a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b8c9a-107">EXAMPLES</span></span>

### <span data-ttu-id="b8c9a-108">-------------------------- Exemplo 1: Adicionar uma regra de filtro de rota a um filtro de rota --------------------------</span><span class="sxs-lookup"><span data-stu-id="b8c9a-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="b8c9a-109">O primeiro comando obtém um filtro de rota chamado routefilter01 usando o cmdlet Get-AzRouteFilter rota.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="b8c9a-110">O comando armazena o filtro na variável $RouteFilter dados.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="b8c9a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8c9a-111">PARAMETERS</span></span>

### <span data-ttu-id="b8c9a-112">-Access</span><span class="sxs-lookup"><span data-stu-id="b8c9a-112">-Access</span></span>
<span data-ttu-id="b8c9a-113">Especifica o acesso da regra de filtro de rota, os valores válidos são Negar ou Permitir.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c9a-114">-Lista de Comunidade</span><span class="sxs-lookup"><span data-stu-id="b8c9a-114">-CommunityList</span></span>
<span data-ttu-id="b8c9a-115">A lista de valor da comunidade em que o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="b8c9a-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c9a-116">-DefaultProfile</span></span>
<span data-ttu-id="b8c9a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c9a-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b8c9a-118">-Force</span></span>
<span data-ttu-id="b8c9a-119">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="b8c9a-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="b8c9a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8c9a-120">-Name</span></span>
<span data-ttu-id="b8c9a-121">Especifica um nome da regra de filtro de rota para adicionar ao filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c9a-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b8c9a-122">-RouteFilter</span></span>
<span data-ttu-id="b8c9a-123">Especifica o filtro de rota ao qual este cmdlet adiciona uma regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c9a-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="b8c9a-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="b8c9a-125">Especifica o tipo de regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="b8c9a-126">Os valores válidos são: Comunidade</span><span class="sxs-lookup"><span data-stu-id="b8c9a-126">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c9a-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b8c9a-127">-Confirm</span></span>
<span data-ttu-id="b8c9a-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c9a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c9a-129">-WhatIf</span></span>
<span data-ttu-id="b8c9a-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8c9a-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c9a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c9a-132">CommonParameters</span></span>
<span data-ttu-id="b8c9a-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c9a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c9a-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c9a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c9a-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="b8c9a-135">INPUTS</span></span>

### <span data-ttu-id="b8c9a-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b8c9a-136">PSRouteFilter</span></span>
<span data-ttu-id="b8c9a-137">Parâmetro 'RouteFilter' aceita o valor do tipo 'PSRouteFilter' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b8c9a-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="b8c9a-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="b8c9a-138">OUTPUTS</span></span>

### <span data-ttu-id="b8c9a-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b8c9a-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b8c9a-140">Notas</span><span class="sxs-lookup"><span data-stu-id="b8c9a-140">NOTES</span></span>
<span data-ttu-id="b8c9a-141">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="b8c9a-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b8c9a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8c9a-142">RELATED LINKS</span></span>

[<span data-ttu-id="b8c9a-143">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8c9a-143">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b8c9a-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b8c9a-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)




[<span data-ttu-id="b8c9a-145">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b8c9a-145">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

