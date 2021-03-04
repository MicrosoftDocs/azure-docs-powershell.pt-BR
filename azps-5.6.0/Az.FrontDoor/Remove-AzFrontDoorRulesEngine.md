---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 84bcc64127636adc318935d1a7fd97f7ce79d760
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901480"
---
# <span data-ttu-id="fb295-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="fb295-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="fb295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb295-102">SYNOPSIS</span></span>
<span data-ttu-id="fb295-103">Remover Mecanismo de Regras da Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="fb295-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="fb295-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fb295-104">SYNTAX</span></span>

### <span data-ttu-id="fb295-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fb295-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb295-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb295-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb295-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb295-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb295-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fb295-108">DESCRIPTION</span></span>
<span data-ttu-id="fb295-109">Remover Mecanismo de Regras da Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="fb295-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="fb295-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb295-110">EXAMPLES</span></span>

### <span data-ttu-id="fb295-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb295-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="fb295-112">Remover configuração do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="fb295-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="fb295-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fb295-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="fb295-114">Resultado esperado ao remover uma configuração do mecanismo de regras inexistente.</span><span class="sxs-lookup"><span data-stu-id="fb295-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="fb295-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fb295-115">PARAMETERS</span></span>

### <span data-ttu-id="fb295-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb295-116">-DefaultProfile</span></span>
<span data-ttu-id="fb295-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb295-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb295-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="fb295-118">-FrontDoorName</span></span>
<span data-ttu-id="fb295-119">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="fb295-119">Front Door name.</span></span>

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

### <span data-ttu-id="fb295-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb295-120">-InputObject</span></span>
<span data-ttu-id="fb295-121">O objeto Mecanismo de Regras a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="fb295-121">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="fb295-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fb295-122">-Name</span></span>
<span data-ttu-id="fb295-123">Nome do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="fb295-123">Rules engine name.</span></span>

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

### <span data-ttu-id="fb295-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb295-124">-PassThru</span></span>
<span data-ttu-id="fb295-125">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="fb295-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="fb295-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb295-126">-ResourceGroupName</span></span>
<span data-ttu-id="fb295-127">O nome do grupo de recursos em que a Porta da Frente será criada.</span><span class="sxs-lookup"><span data-stu-id="fb295-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="fb295-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb295-128">-ResourceId</span></span>
<span data-ttu-id="fb295-129">ID de recurso do RulesEngine a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="fb295-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="fb295-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb295-130">-Confirm</span></span>
<span data-ttu-id="fb295-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb295-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb295-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb295-132">-WhatIf</span></span>
<span data-ttu-id="fb295-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb295-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb295-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb295-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb295-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb295-135">CommonParameters</span></span>
<span data-ttu-id="fb295-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb295-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb295-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb295-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb295-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb295-138">INPUTS</span></span>

### <span data-ttu-id="fb295-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="fb295-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="fb295-140">System.String</span><span class="sxs-lookup"><span data-stu-id="fb295-140">System.String</span></span>

## <span data-ttu-id="fb295-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fb295-141">OUTPUTS</span></span>

### <span data-ttu-id="fb295-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb295-142">System.Boolean</span></span>

## <span data-ttu-id="fb295-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="fb295-143">NOTES</span></span>

## <span data-ttu-id="fb295-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb295-144">RELATED LINKS</span></span>
