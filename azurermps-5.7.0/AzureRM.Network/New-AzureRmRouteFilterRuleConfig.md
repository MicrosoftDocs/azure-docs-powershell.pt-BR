---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 6e0ff70671ceff4094d7f1a48bbebcc81398d5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427528"
---
# <span data-ttu-id="1dca2-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dca2-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1dca2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1dca2-102">SYNOPSIS</span></span>
<span data-ttu-id="1dca2-103">Cria uma regra de filtro de rota para um filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="1dca2-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dca2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dca2-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dca2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1dca2-105">DESCRIPTION</span></span>
<span data-ttu-id="1dca2-106">O cmdlet New-AzureRmRouteFilterRuleConfig cria uma regra de filtro de rota para um filtro de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="1dca2-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="1dca2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1dca2-107">EXAMPLES</span></span>

### <span data-ttu-id="1dca2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1dca2-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1dca2-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="1dca2-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1dca2-110">OS</span><span class="sxs-lookup"><span data-stu-id="1dca2-110">PARAMETERS</span></span>

### <span data-ttu-id="1dca2-111">-Acesso</span><span class="sxs-lookup"><span data-stu-id="1dca2-111">-Access</span></span>
<span data-ttu-id="1dca2-112">Acesso à regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="1dca2-112">Access for route filter rule.</span></span>
<span data-ttu-id="1dca2-113">Os valores válidos são Allow ou Deny.</span><span class="sxs-lookup"><span data-stu-id="1dca2-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="1dca2-114">-Communitylist</span><span class="sxs-lookup"><span data-stu-id="1dca2-114">-CommunityList</span></span>
<span data-ttu-id="1dca2-115">A lista de valor da Comunidade para a qual o filtro de rota será filtrado</span><span class="sxs-lookup"><span data-stu-id="1dca2-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="1dca2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dca2-116">-DefaultProfile</span></span>
<span data-ttu-id="1dca2-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1dca2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dca2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1dca2-118">-Force</span></span>
<span data-ttu-id="1dca2-119">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="1dca2-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="1dca2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dca2-120">-Name</span></span>
<span data-ttu-id="1dca2-121">Especifica um nome para a regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="1dca2-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="1dca2-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="1dca2-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="1dca2-123">Tipo de regra de filtro de rota.</span><span class="sxs-lookup"><span data-stu-id="1dca2-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="1dca2-124">Os valores válidos são: Comunidade</span><span class="sxs-lookup"><span data-stu-id="1dca2-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="1dca2-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1dca2-125">-Confirm</span></span>
<span data-ttu-id="1dca2-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dca2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dca2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dca2-127">-WhatIf</span></span>
<span data-ttu-id="1dca2-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1dca2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dca2-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1dca2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dca2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dca2-130">CommonParameters</span></span>
<span data-ttu-id="1dca2-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dca2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dca2-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dca2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dca2-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1dca2-133">INPUTS</span></span>

### <span data-ttu-id="1dca2-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1dca2-134">None</span></span>
<span data-ttu-id="1dca2-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1dca2-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1dca2-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1dca2-136">OUTPUTS</span></span>

### <span data-ttu-id="1dca2-137">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="1dca2-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="1dca2-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1dca2-138">NOTES</span></span>
<span data-ttu-id="1dca2-139">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="1dca2-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1dca2-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dca2-140">RELATED LINKS</span></span>

[<span data-ttu-id="1dca2-141">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dca2-141">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="1dca2-142">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dca2-142">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="1dca2-143">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dca2-143">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="1dca2-144">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dca2-144">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)
