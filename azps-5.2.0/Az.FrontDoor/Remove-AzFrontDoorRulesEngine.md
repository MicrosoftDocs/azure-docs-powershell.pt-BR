---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264249"
---
# <span data-ttu-id="f3db0-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="f3db0-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="f3db0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3db0-102">SYNOPSIS</span></span>
<span data-ttu-id="f3db0-103">Remover o mecanismo regras da porta frontal</span><span class="sxs-lookup"><span data-stu-id="f3db0-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="f3db0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3db0-104">SYNTAX</span></span>

### <span data-ttu-id="f3db0-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f3db0-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3db0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3db0-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3db0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3db0-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3db0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3db0-108">DESCRIPTION</span></span>
<span data-ttu-id="f3db0-109">Remover o mecanismo regras da porta frontal</span><span class="sxs-lookup"><span data-stu-id="f3db0-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="f3db0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3db0-110">EXAMPLES</span></span>

### <span data-ttu-id="f3db0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f3db0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="f3db0-112">Remover a configuração do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="f3db0-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="f3db0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f3db0-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="f3db0-114">Resultado esperado ao remover uma configuração de mecanismo de regras não existentes.</span><span class="sxs-lookup"><span data-stu-id="f3db0-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="f3db0-115">OS</span><span class="sxs-lookup"><span data-stu-id="f3db0-115">PARAMETERS</span></span>

### <span data-ttu-id="f3db0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3db0-116">-DefaultProfile</span></span>
<span data-ttu-id="f3db0-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3db0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3db0-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="f3db0-118">-FrontDoorName</span></span>
<span data-ttu-id="f3db0-119">Nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="f3db0-119">Front Door name.</span></span>

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

### <span data-ttu-id="f3db0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3db0-120">-InputObject</span></span>
<span data-ttu-id="f3db0-121">O objeto de mecanismo de regras para atualizar.</span><span class="sxs-lookup"><span data-stu-id="f3db0-121">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="f3db0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3db0-122">-Name</span></span>
<span data-ttu-id="f3db0-123">Nome do mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="f3db0-123">Rules engine name.</span></span>

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

### <span data-ttu-id="f3db0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3db0-124">-PassThru</span></span>
<span data-ttu-id="f3db0-125">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="f3db0-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="f3db0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3db0-126">-ResourceGroupName</span></span>
<span data-ttu-id="f3db0-127">O nome do grupo de recursos no qual a porta frontal será criada.</span><span class="sxs-lookup"><span data-stu-id="f3db0-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="f3db0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3db0-128">-ResourceId</span></span>
<span data-ttu-id="f3db0-129">ID do recurso do RulesEngine para atualizar</span><span class="sxs-lookup"><span data-stu-id="f3db0-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="f3db0-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f3db0-130">-Confirm</span></span>
<span data-ttu-id="f3db0-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3db0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3db0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3db0-132">-WhatIf</span></span>
<span data-ttu-id="f3db0-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f3db0-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3db0-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3db0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3db0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3db0-135">CommonParameters</span></span>
<span data-ttu-id="f3db0-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3db0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3db0-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3db0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3db0-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3db0-138">INPUTS</span></span>

### <span data-ttu-id="f3db0-139">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="f3db0-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="f3db0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f3db0-140">System.String</span></span>

## <span data-ttu-id="f3db0-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3db0-141">OUTPUTS</span></span>

### <span data-ttu-id="f3db0-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3db0-142">System.Boolean</span></span>

## <span data-ttu-id="f3db0-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3db0-143">NOTES</span></span>

## <span data-ttu-id="f3db0-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3db0-144">RELATED LINKS</span></span>
