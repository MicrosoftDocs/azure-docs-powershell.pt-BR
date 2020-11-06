---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3cd01d2e9bb3673e2c0e42ea43418c9601796a08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433077"
---
# <span data-ttu-id="1a710-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1a710-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1a710-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a710-102">SYNOPSIS</span></span>
<span data-ttu-id="1a710-103">Adiciona uma regra de filtro de rota a um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="1a710-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a710-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a710-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a710-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a710-105">DESCRIPTION</span></span>
<span data-ttu-id="1a710-106">O cmdlet Add-AzureRmRouteFilterRuleConfig adiciona uma regra de filtro de rota a um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a710-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="1a710-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a710-107">EXAMPLES</span></span>

### <span data-ttu-id="1a710-108">--------------------------Exemplo 1: adicionar uma regra de filtro de rota a um filtro de rota--------------------------</span><span class="sxs-lookup"><span data-stu-id="1a710-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
<span data-ttu-id="1a710-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="1a710-109">@{paragraph=PS C:\\\>}</span></span>















```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="1a710-110">O primeiro comando obtém um filtro de rota chamado routefilter01 usando o cmdlet Get-AzureRmRouteFilter.</span><span class="sxs-lookup"><span data-stu-id="1a710-110">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="1a710-111">O comando armazena o filtro na variável $RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="1a710-111">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="1a710-112">OS</span><span class="sxs-lookup"><span data-stu-id="1a710-112">PARAMETERS</span></span>

### <span data-ttu-id="1a710-113">-Acesso</span><span class="sxs-lookup"><span data-stu-id="1a710-113">-Access</span></span>
<span data-ttu-id="1a710-114">Especifica o acesso da regra de filtro de rota, os valores válidos são Deny ou Allow.</span><span class="sxs-lookup"><span data-stu-id="1a710-114">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a710-115">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="1a710-115">-CommunityList</span></span>
<span data-ttu-id="1a710-116">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="1a710-116">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="1a710-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1a710-117">-Force</span></span>
<span data-ttu-id="1a710-118">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="1a710-118">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="1a710-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a710-119">-Name</span></span>
<span data-ttu-id="1a710-120">Especifica um nome da regra de filtro de rota a ser adicionada ao filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="1a710-120">Specifies a name of the route filter rule to add to the route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a710-121">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1a710-121">-RouteFilter</span></span>
<span data-ttu-id="1a710-122">Especifica o filtro de rota para o qual esse cmdlet adiciona uma regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="1a710-122">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a710-123">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="1a710-123">-RouteFilterRuleType</span></span>
<span data-ttu-id="1a710-124">Especifica o tipo de regra do filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="1a710-124">Specifies the route filter rule type.</span></span>
<span data-ttu-id="1a710-125">Os valores válidos são: Comunidade</span><span class="sxs-lookup"><span data-stu-id="1a710-125">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a710-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a710-126">-Confirm</span></span>
<span data-ttu-id="1a710-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a710-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a710-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a710-128">-WhatIf</span></span>
<span data-ttu-id="1a710-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a710-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a710-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a710-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a710-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a710-131">-DefaultProfile</span></span>
<span data-ttu-id="1a710-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a710-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a710-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a710-133">CommonParameters</span></span>
<span data-ttu-id="1a710-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a710-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a710-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a710-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a710-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a710-136">INPUTS</span></span>

### <span data-ttu-id="1a710-137">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1a710-137">PSRouteFilter</span></span>
<span data-ttu-id="1a710-138">O parâmetro ' RouteFilter ' aceita o valor do tipo ' PSRouteFilter ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="1a710-138">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="1a710-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a710-139">OUTPUTS</span></span>

### <span data-ttu-id="1a710-140">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1a710-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1a710-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a710-141">NOTES</span></span>
<span data-ttu-id="1a710-142">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="1a710-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1a710-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a710-143">RELATED LINKS</span></span>

[<span data-ttu-id="1a710-144">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1a710-144">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="1a710-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1a710-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="1a710-146">New-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="1a710-146">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="1a710-147">Remove-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="1a710-147">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="1a710-148">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="1a710-148">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="1a710-149">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1a710-149">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

