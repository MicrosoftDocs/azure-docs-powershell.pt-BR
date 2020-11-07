---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusIPRule.md
ms.openlocfilehash: f159e3d82aa93f4b3bf663f6bff6e8ede599e860
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773226"
---
# <span data-ttu-id="7d4db-101">Remove-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="7d4db-101">Remove-AzServiceBusIPRule</span></span>

## <span data-ttu-id="7d4db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d4db-102">SYNOPSIS</span></span>
<span data-ttu-id="7d4db-103">Remover uma única regra de IP para o NetworkRuleSet do namespace especificado</span><span class="sxs-lookup"><span data-stu-id="7d4db-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="7d4db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d4db-104">SYNTAX</span></span>

### <span data-ttu-id="7d4db-105">IPRulePropertiesParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7d4db-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d4db-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d4db-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d4db-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d4db-107">DESCRIPTION</span></span>
<span data-ttu-id="7d4db-108">Remover uma única regra de IP para o NetworkRuleSet do namespace especificado</span><span class="sxs-lookup"><span data-stu-id="7d4db-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="7d4db-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d4db-109">EXAMPLES</span></span>

### <span data-ttu-id="7d4db-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d4db-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="7d4db-111">Remove IpMask do NetworkRuleSet do namespace especificado</span><span class="sxs-lookup"><span data-stu-id="7d4db-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="7d4db-112">OS</span><span class="sxs-lookup"><span data-stu-id="7d4db-112">PARAMETERS</span></span>

### <span data-ttu-id="7d4db-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d4db-113">-AsJob</span></span>
<span data-ttu-id="7d4db-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7d4db-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d4db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d4db-115">-DefaultProfile</span></span>
<span data-ttu-id="7d4db-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d4db-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="7d4db-117">-IpMask</span></span>
<span data-ttu-id="7d4db-118">ID do recurso de sub-rede</span><span class="sxs-lookup"><span data-stu-id="7d4db-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="7d4db-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="7d4db-119">-IpRuleObject</span></span>
<span data-ttu-id="7d4db-120">Objeto de configuração IPRule</span><span class="sxs-lookup"><span data-stu-id="7d4db-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="7d4db-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d4db-121">-Name</span></span>
<span data-ttu-id="7d4db-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="7d4db-122">Namespace Name</span></span>

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

### <span data-ttu-id="7d4db-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d4db-123">-PassThru</span></span>
<span data-ttu-id="7d4db-124">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="7d4db-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7d4db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d4db-125">-ResourceGroupName</span></span>
<span data-ttu-id="7d4db-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7d4db-126">Resource Group Name</span></span>

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

### <span data-ttu-id="7d4db-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7d4db-127">-Confirm</span></span>
<span data-ttu-id="7d4db-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d4db-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d4db-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d4db-129">-WhatIf</span></span>
<span data-ttu-id="7d4db-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d4db-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d4db-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d4db-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d4db-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d4db-132">CommonParameters</span></span>
<span data-ttu-id="7d4db-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d4db-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7d4db-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d4db-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d4db-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d4db-135">INPUTS</span></span>

### <span data-ttu-id="7d4db-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7d4db-136">System.String</span></span>

### <span data-ttu-id="7d4db-137">Microsoft. Azure. Commands. ServiceBus. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="7d4db-137">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="7d4db-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d4db-138">OUTPUTS</span></span>

### <span data-ttu-id="7d4db-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="7d4db-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="7d4db-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d4db-140">NOTES</span></span>

## <span data-ttu-id="7d4db-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d4db-141">RELATED LINKS</span></span>
