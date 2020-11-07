---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 6f8943fb4e75c96a97ad2b7f128d671a8be7c906
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775362"
---
# <span data-ttu-id="b7948-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7948-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="b7948-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7948-102">SYNOPSIS</span></span>
<span data-ttu-id="b7948-103">Cria uma regra de filtro de rota para um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="b7948-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="b7948-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7948-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7948-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7948-105">DESCRIPTION</span></span>
<span data-ttu-id="b7948-106">O cmdlet New-AzRouteFilterRuleConfig cria uma regra de filtro de rota para um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="b7948-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="b7948-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7948-107">EXAMPLES</span></span>

### <span data-ttu-id="b7948-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7948-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b7948-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="b7948-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b7948-110">OS</span><span class="sxs-lookup"><span data-stu-id="b7948-110">PARAMETERS</span></span>

### <span data-ttu-id="b7948-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="b7948-111">-Access</span></span>
<span data-ttu-id="b7948-112">Acesso à regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="b7948-112">Access for route filter rule.</span></span>
<span data-ttu-id="b7948-113">Os valores válidos são Allow ou Deny.</span><span class="sxs-lookup"><span data-stu-id="b7948-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="b7948-114">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="b7948-114">-CommunityList</span></span>
<span data-ttu-id="b7948-115">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="b7948-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="b7948-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7948-116">-DefaultProfile</span></span>
<span data-ttu-id="b7948-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7948-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7948-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b7948-118">-Force</span></span>
<span data-ttu-id="b7948-119">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="b7948-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="b7948-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7948-120">-Name</span></span>
<span data-ttu-id="b7948-121">Especifica um nome para a regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="b7948-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="b7948-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="b7948-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="b7948-123">Tipo de regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="b7948-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="b7948-124">Os valores válidos são: Comunidade</span><span class="sxs-lookup"><span data-stu-id="b7948-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="b7948-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b7948-125">-Confirm</span></span>
<span data-ttu-id="b7948-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7948-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7948-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7948-127">-WhatIf</span></span>
<span data-ttu-id="b7948-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7948-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7948-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7948-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7948-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7948-130">CommonParameters</span></span>
<span data-ttu-id="b7948-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7948-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7948-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7948-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7948-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7948-133">INPUTS</span></span>

## <span data-ttu-id="b7948-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7948-134">OUTPUTS</span></span>

### <span data-ttu-id="b7948-135">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="b7948-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="b7948-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7948-136">NOTES</span></span>
<span data-ttu-id="b7948-137">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="b7948-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b7948-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7948-138">RELATED LINKS</span></span>

[<span data-ttu-id="b7948-139">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7948-139">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b7948-140">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7948-140">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b7948-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7948-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b7948-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7948-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

