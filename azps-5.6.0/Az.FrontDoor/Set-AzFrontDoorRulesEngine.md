---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 7f24d7a7fc027e8d4411b12a3f04d24121af5354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887528"
---
# <span data-ttu-id="4c6d1-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="4c6d1-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="4c6d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c6d1-102">SYNOPSIS</span></span>
<span data-ttu-id="4c6d1-103">Atualizar um Mecanismo de Regras.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="4c6d1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4c6d1-104">SYNTAX</span></span>

### <span data-ttu-id="4c6d1-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4c6d1-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c6d1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c6d1-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c6d1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c6d1-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c6d1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4c6d1-108">DESCRIPTION</span></span>
<span data-ttu-id="4c6d1-109">Atualizar um Mecanismo de Regras.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="4c6d1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c6d1-110">EXAMPLES</span></span>

### <span data-ttu-id="4c6d1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4c6d1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}

PS C:\> $rulesEngineRule2 = New-AzFrontDoorRulesEngineRuleObject -Name rules2 -Priority 3 -Action $rulesEngineAction
PS C:\AFD\azure-powershell\artifacts\Debug\Az.FrontDoor> Set-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1, $rulesEngineRule2

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1, rules2}
```

<span data-ttu-id="4c6d1-112">Obter uma configuração do mecanismo de regras existente e adicionar outra regra de mecanismo de regras a ela.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="4c6d1-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4c6d1-113">PARAMETERS</span></span>

### <span data-ttu-id="4c6d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c6d1-114">-DefaultProfile</span></span>
<span data-ttu-id="4c6d1-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c6d1-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="4c6d1-116">-FrontDoorName</span></span>
<span data-ttu-id="4c6d1-117">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-117">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6d1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c6d1-118">-InputObject</span></span>
<span data-ttu-id="4c6d1-119">O objeto Mecanismo de Regras a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-119">The Rules Engine object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6d1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4c6d1-120">-Name</span></span>
<span data-ttu-id="4c6d1-121">Nome do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-121">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c6d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="4c6d1-123">O nome do grupo de recursos em que a Porta da Frente será criada.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-123">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6d1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c6d1-124">-ResourceId</span></span>
<span data-ttu-id="4c6d1-125">ID de recurso do RulesEngine a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="4c6d1-125">Resource Id of the RulesEngine to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6d1-126">-Rule</span><span class="sxs-lookup"><span data-stu-id="4c6d1-126">-Rule</span></span>
<span data-ttu-id="4c6d1-127">Uma lista de regras que definem uma configuração específica do Mecanismo de Regras.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6d1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c6d1-128">-Confirm</span></span>
<span data-ttu-id="4c6d1-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c6d1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c6d1-130">-WhatIf</span></span>
<span data-ttu-id="4c6d1-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c6d1-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c6d1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c6d1-133">CommonParameters</span></span>
<span data-ttu-id="4c6d1-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c6d1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c6d1-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c6d1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c6d1-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c6d1-136">INPUTS</span></span>

### <span data-ttu-id="4c6d1-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="4c6d1-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="4c6d1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4c6d1-138">System.String</span></span>

## <span data-ttu-id="4c6d1-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4c6d1-139">OUTPUTS</span></span>

### <span data-ttu-id="4c6d1-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="4c6d1-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="4c6d1-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="4c6d1-141">NOTES</span></span>

## <span data-ttu-id="4c6d1-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c6d1-142">RELATED LINKS</span></span>
