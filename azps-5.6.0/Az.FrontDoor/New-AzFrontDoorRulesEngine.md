---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 05248a299b907c74f43edddb7caf18697794dc08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887758"
---
# <span data-ttu-id="aa46e-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="aa46e-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="aa46e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa46e-102">SYNOPSIS</span></span>
<span data-ttu-id="aa46e-103">Crie uma nova configuração do mecanismo de regras para uma porta frontal especificada.</span><span class="sxs-lookup"><span data-stu-id="aa46e-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="aa46e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aa46e-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa46e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aa46e-105">DESCRIPTION</span></span>
<span data-ttu-id="aa46e-106">Crie uma nova configuração do mecanismo de regras para uma porta frontal especificada.</span><span class="sxs-lookup"><span data-stu-id="aa46e-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="aa46e-107">Use o cmdlet "New-AzFrontDoorRulesEngineRule" para construir regras de mecanismo de regras para passar para o parâmetro "-Rules" deste cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa46e-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="aa46e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa46e-108">EXAMPLES</span></span>

### <span data-ttu-id="aa46e-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aa46e-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="aa46e-110">Crie uma nova configuração do mecanismo de regras para a porta frontal especificada.</span><span class="sxs-lookup"><span data-stu-id="aa46e-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="aa46e-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aa46e-111">PARAMETERS</span></span>

### <span data-ttu-id="aa46e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa46e-112">-DefaultProfile</span></span>
<span data-ttu-id="aa46e-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa46e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa46e-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="aa46e-114">-FrontDoorName</span></span>
<span data-ttu-id="aa46e-115">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="aa46e-115">Front Door name.</span></span>

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

### <span data-ttu-id="aa46e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="aa46e-116">-Name</span></span>
<span data-ttu-id="aa46e-117">Nome do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="aa46e-117">Rules engine name.</span></span>

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

### <span data-ttu-id="aa46e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa46e-118">-ResourceGroupName</span></span>
<span data-ttu-id="aa46e-119">O nome do grupo de recursos em que a Porta da Frente será criada.</span><span class="sxs-lookup"><span data-stu-id="aa46e-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="aa46e-120">-Rule</span><span class="sxs-lookup"><span data-stu-id="aa46e-120">-Rule</span></span>
<span data-ttu-id="aa46e-121">Uma lista de regras que definem uma configuração específica do Mecanismo de Regras.</span><span class="sxs-lookup"><span data-stu-id="aa46e-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="aa46e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa46e-122">-Confirm</span></span>
<span data-ttu-id="aa46e-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa46e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa46e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa46e-124">-WhatIf</span></span>
<span data-ttu-id="aa46e-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa46e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa46e-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa46e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa46e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa46e-127">CommonParameters</span></span>
<span data-ttu-id="aa46e-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa46e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa46e-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa46e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa46e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa46e-130">INPUTS</span></span>

### <span data-ttu-id="aa46e-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="aa46e-131">None</span></span>

## <span data-ttu-id="aa46e-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aa46e-132">OUTPUTS</span></span>

### <span data-ttu-id="aa46e-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="aa46e-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="aa46e-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="aa46e-134">NOTES</span></span>

## <span data-ttu-id="aa46e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa46e-135">RELATED LINKS</span></span>
