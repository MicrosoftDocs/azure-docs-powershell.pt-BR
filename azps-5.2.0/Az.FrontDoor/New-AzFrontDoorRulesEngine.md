---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260856"
---
# <span data-ttu-id="8e2ed-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8e2ed-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="8e2ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e2ed-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2ed-103">Criar uma nova configuração de mecanismo de regras para uma porta frontal especificada.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="8e2ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e2ed-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e2ed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e2ed-105">DESCRIPTION</span></span>
<span data-ttu-id="8e2ed-106">Criar uma nova configuração de mecanismo de regras para uma porta frontal especificada.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="8e2ed-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" para construir regras de mecanismo de regras para passar para o parâmetro "-Rules" deste cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="8e2ed-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e2ed-108">EXAMPLES</span></span>

### <span data-ttu-id="8e2ed-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e2ed-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="8e2ed-110">Criar uma nova configuração de mecanismo de regras para a porta frontal especificada.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="8e2ed-111">OS</span><span class="sxs-lookup"><span data-stu-id="8e2ed-111">PARAMETERS</span></span>

### <span data-ttu-id="8e2ed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2ed-112">-DefaultProfile</span></span>
<span data-ttu-id="8e2ed-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e2ed-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8e2ed-114">-FrontDoorName</span></span>
<span data-ttu-id="8e2ed-115">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-115">Front Door name.</span></span>

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

### <span data-ttu-id="8e2ed-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e2ed-116">-Name</span></span>
<span data-ttu-id="8e2ed-117">Nome do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-117">Rules engine name.</span></span>

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

### <span data-ttu-id="8e2ed-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2ed-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e2ed-119">O nome do grupo de recursos no qual a porta frontal será criada.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="8e2ed-120">-Regra</span><span class="sxs-lookup"><span data-stu-id="8e2ed-120">-Rule</span></span>
<span data-ttu-id="8e2ed-121">Uma lista de regras que definem uma configuração de mecanismo de regras específica.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="8e2ed-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8e2ed-122">-Confirm</span></span>
<span data-ttu-id="8e2ed-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e2ed-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e2ed-124">-WhatIf</span></span>
<span data-ttu-id="8e2ed-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e2ed-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e2ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2ed-127">CommonParameters</span></span>
<span data-ttu-id="8e2ed-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2ed-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e2ed-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2ed-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e2ed-130">INPUTS</span></span>

### <span data-ttu-id="8e2ed-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8e2ed-131">None</span></span>

## <span data-ttu-id="8e2ed-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e2ed-132">OUTPUTS</span></span>

### <span data-ttu-id="8e2ed-133">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="8e2ed-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="8e2ed-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e2ed-134">NOTES</span></span>

## <span data-ttu-id="8e2ed-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e2ed-135">RELATED LINKS</span></span>
