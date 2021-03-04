---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: e14d82fbf503487ddb4e4ebac1385400305e9209
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892037"
---
# <span data-ttu-id="606cb-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="606cb-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="606cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="606cb-102">SYNOPSIS</span></span>
<span data-ttu-id="606cb-103">Remover uma única regra IP para o NetworkRuleSet do namespace determinado</span><span class="sxs-lookup"><span data-stu-id="606cb-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="606cb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="606cb-104">SYNTAX</span></span>

### <span data-ttu-id="606cb-105">IPRulePropertiesParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="606cb-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="606cb-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="606cb-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="606cb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="606cb-107">DESCRIPTION</span></span>
<span data-ttu-id="606cb-108">Remover uma única regra IP para o NetworkRuleSet do namespace determinado</span><span class="sxs-lookup"><span data-stu-id="606cb-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="606cb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="606cb-109">EXAMPLES</span></span>

### <span data-ttu-id="606cb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="606cb-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="606cb-111">Remove IpMask do NetworkRuleSet do namespace determinado</span><span class="sxs-lookup"><span data-stu-id="606cb-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="606cb-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="606cb-112">PARAMETERS</span></span>

### <span data-ttu-id="606cb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="606cb-113">-AsJob</span></span>
<span data-ttu-id="606cb-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="606cb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="606cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="606cb-115">-DefaultProfile</span></span>
<span data-ttu-id="606cb-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="606cb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="606cb-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="606cb-117">-IpMask</span></span>
<span data-ttu-id="606cb-118">ID do Recurso de Sub-rede</span><span class="sxs-lookup"><span data-stu-id="606cb-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="606cb-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="606cb-119">-IpRuleObject</span></span>
<span data-ttu-id="606cb-120">Objeto de configuração IPRule</span><span class="sxs-lookup"><span data-stu-id="606cb-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="606cb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="606cb-121">-Name</span></span>
<span data-ttu-id="606cb-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="606cb-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="606cb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="606cb-123">-PassThru</span></span>
<span data-ttu-id="606cb-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="606cb-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="606cb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="606cb-125">-ResourceGroupName</span></span>
<span data-ttu-id="606cb-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="606cb-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="606cb-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="606cb-127">-Confirm</span></span>
<span data-ttu-id="606cb-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="606cb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="606cb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="606cb-129">-WhatIf</span></span>
<span data-ttu-id="606cb-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="606cb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="606cb-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="606cb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="606cb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="606cb-132">CommonParameters</span></span>
<span data-ttu-id="606cb-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="606cb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="606cb-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="606cb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="606cb-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="606cb-135">INPUTS</span></span>

### <span data-ttu-id="606cb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="606cb-136">System.String</span></span>

### <span data-ttu-id="606cb-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="606cb-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="606cb-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="606cb-138">OUTPUTS</span></span>

### <span data-ttu-id="606cb-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="606cb-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="606cb-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="606cb-140">NOTES</span></span>

## <span data-ttu-id="606cb-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="606cb-141">RELATED LINKS</span></span>
