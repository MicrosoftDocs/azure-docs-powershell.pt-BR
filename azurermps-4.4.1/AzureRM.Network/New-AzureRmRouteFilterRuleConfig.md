---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3c3e20762bcf8e48fc3f01d750419493a81ca8aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602435"
---
# <span data-ttu-id="601b5-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="601b5-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="601b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="601b5-102">SYNOPSIS</span></span>
<span data-ttu-id="601b5-103">Cria uma regra de filtro de rota para um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="601b5-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="601b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="601b5-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="601b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="601b5-105">DESCRIPTION</span></span>
<span data-ttu-id="601b5-106">O cmdlet New-AzureRmRouteFilterRuleConfig cria uma regra de filtro de rota para um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="601b5-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="601b5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="601b5-107">EXAMPLES</span></span>

### <span data-ttu-id="601b5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="601b5-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="601b5-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="601b5-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="601b5-110">OS</span><span class="sxs-lookup"><span data-stu-id="601b5-110">PARAMETERS</span></span>

### <span data-ttu-id="601b5-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="601b5-111">-Access</span></span>
<span data-ttu-id="601b5-112">Acesso à regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="601b5-112">Access for route filter rule.</span></span>
<span data-ttu-id="601b5-113">Os valores válidos são Allow ou Deny.</span><span class="sxs-lookup"><span data-stu-id="601b5-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="601b5-114">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="601b5-114">-CommunityList</span></span>
<span data-ttu-id="601b5-115">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="601b5-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="601b5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="601b5-116">-Force</span></span>
<span data-ttu-id="601b5-117">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="601b5-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="601b5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="601b5-118">-Name</span></span>
<span data-ttu-id="601b5-119">Especifica um nome para a regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="601b5-119">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="601b5-120">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="601b5-120">-RouteFilterRuleType</span></span>
<span data-ttu-id="601b5-121">Tipo de regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="601b5-121">Route Filter Rule Type.</span></span>
<span data-ttu-id="601b5-122">Os valores válidos são: Comunidade</span><span class="sxs-lookup"><span data-stu-id="601b5-122">Valid values are: Community</span></span>

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

### <span data-ttu-id="601b5-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="601b5-123">-Confirm</span></span>
<span data-ttu-id="601b5-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="601b5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="601b5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="601b5-125">-WhatIf</span></span>
<span data-ttu-id="601b5-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="601b5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="601b5-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="601b5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="601b5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="601b5-128">-DefaultProfile</span></span>
<span data-ttu-id="601b5-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="601b5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="601b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="601b5-130">CommonParameters</span></span>
<span data-ttu-id="601b5-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="601b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="601b5-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="601b5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="601b5-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="601b5-133">INPUTS</span></span>

## <span data-ttu-id="601b5-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="601b5-134">OUTPUTS</span></span>

### <span data-ttu-id="601b5-135">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="601b5-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="601b5-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="601b5-136">NOTES</span></span>
<span data-ttu-id="601b5-137">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="601b5-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="601b5-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="601b5-138">RELATED LINKS</span></span>

[<span data-ttu-id="601b5-139">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="601b5-139">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="601b5-140">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="601b5-140">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="601b5-141">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="601b5-141">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="601b5-142">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="601b5-142">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

