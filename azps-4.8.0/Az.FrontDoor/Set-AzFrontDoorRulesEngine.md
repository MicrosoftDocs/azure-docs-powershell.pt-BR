---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: cf98121f535f60c7d1ddc3b29e33f10fd8f29842
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114941"
---
# <span data-ttu-id="48742-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="48742-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="48742-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48742-102">SYNOPSIS</span></span>
<span data-ttu-id="48742-103">Atualizar um mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="48742-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="48742-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48742-104">SYNTAX</span></span>

### <span data-ttu-id="48742-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="48742-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48742-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48742-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48742-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48742-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48742-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48742-108">DESCRIPTION</span></span>
<span data-ttu-id="48742-109">Atualizar um mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="48742-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="48742-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48742-110">EXAMPLES</span></span>

### <span data-ttu-id="48742-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="48742-111">Example 1</span></span>
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

<span data-ttu-id="48742-112">Obtenha uma configuração de mecanismo de regras existente e adicione outra regra de mecanismo de regras a ele.</span><span class="sxs-lookup"><span data-stu-id="48742-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="48742-113">OS</span><span class="sxs-lookup"><span data-stu-id="48742-113">PARAMETERS</span></span>

### <span data-ttu-id="48742-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48742-114">-DefaultProfile</span></span>
<span data-ttu-id="48742-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48742-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48742-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="48742-116">-FrontDoorName</span></span>
<span data-ttu-id="48742-117">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="48742-117">Front Door name.</span></span>

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

### <span data-ttu-id="48742-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48742-118">-InputObject</span></span>
<span data-ttu-id="48742-119">O objeto de mecanismo de regras para atualizar.</span><span class="sxs-lookup"><span data-stu-id="48742-119">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="48742-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="48742-120">-Name</span></span>
<span data-ttu-id="48742-121">Nome do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="48742-121">Rules engine name.</span></span>

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

### <span data-ttu-id="48742-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48742-122">-ResourceGroupName</span></span>
<span data-ttu-id="48742-123">O nome do grupo de recursos no qual a porta frontal será criada.</span><span class="sxs-lookup"><span data-stu-id="48742-123">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="48742-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48742-124">-ResourceId</span></span>
<span data-ttu-id="48742-125">ID do recurso do RulesEngine para atualizar</span><span class="sxs-lookup"><span data-stu-id="48742-125">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="48742-126">-Regra</span><span class="sxs-lookup"><span data-stu-id="48742-126">-Rule</span></span>
<span data-ttu-id="48742-127">Uma lista de regras que definem uma configuração de mecanismo de regras específica.</span><span class="sxs-lookup"><span data-stu-id="48742-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="48742-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="48742-128">-Confirm</span></span>
<span data-ttu-id="48742-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48742-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48742-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48742-130">-WhatIf</span></span>
<span data-ttu-id="48742-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48742-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48742-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48742-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48742-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48742-133">CommonParameters</span></span>
<span data-ttu-id="48742-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48742-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48742-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48742-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48742-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48742-136">INPUTS</span></span>

### <span data-ttu-id="48742-137">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="48742-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="48742-138">System. String</span><span class="sxs-lookup"><span data-stu-id="48742-138">System.String</span></span>

## <span data-ttu-id="48742-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48742-139">OUTPUTS</span></span>

### <span data-ttu-id="48742-140">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="48742-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="48742-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48742-141">NOTES</span></span>

## <span data-ttu-id="48742-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48742-142">RELATED LINKS</span></span>
