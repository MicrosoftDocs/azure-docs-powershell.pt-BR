---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 285acdcd7e913d4fb502fb656057f1fc81d6dfcd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887354"
---
# <span data-ttu-id="c043b-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="c043b-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="c043b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c043b-102">SYNOPSIS</span></span>
<span data-ttu-id="c043b-103">Remove uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="c043b-103">Removes a managed application definition</span></span>

## <span data-ttu-id="c043b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c043b-104">SYNTAX</span></span>

### <span data-ttu-id="c043b-105">RemoveByNameAndResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c043b-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c043b-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="c043b-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c043b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c043b-107">DESCRIPTION</span></span>
<span data-ttu-id="c043b-108">O cmdlet **Remove-AzManagedApplicationDefinition** remove uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="c043b-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="c043b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c043b-109">EXAMPLES</span></span>

### <span data-ttu-id="c043b-110">Exemplo 1: Remover definição de aplicativo gerenciado por ID de recurso</span><span class="sxs-lookup"><span data-stu-id="c043b-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="c043b-111">O primeiro comando obtém uma definição de aplicativo gerenciado chamada myAppDef usando Get-AzManagedApplicationDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c043b-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="c043b-112">O comando armazena-o na variável $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="c043b-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="c043b-113">O segundo comando remove a definição de aplicativo gerenciado identificada pela **propriedade ResourceId** do $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="c043b-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="c043b-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c043b-114">PARAMETERS</span></span>

### <span data-ttu-id="c043b-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c043b-115">-ApiVersion</span></span>
<span data-ttu-id="c043b-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c043b-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c043b-117">Se não for especificada, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="c043b-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c043b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c043b-118">-DefaultProfile</span></span>
<span data-ttu-id="c043b-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c043b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c043b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c043b-120">-Force</span></span>
<span data-ttu-id="c043b-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c043b-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c043b-122">-Id</span><span class="sxs-lookup"><span data-stu-id="c043b-122">-Id</span></span>
<span data-ttu-id="c043b-123">A ID de definição de aplicativo gerenciado totalmente qualificado, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="c043b-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="c043b-124">por exemplo, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c043b-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c043b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c043b-125">-Name</span></span>
<span data-ttu-id="c043b-126">O nome da definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c043b-126">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c043b-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="c043b-127">-Pre</span></span>
<span data-ttu-id="c043b-128">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="c043b-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c043b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c043b-129">-ResourceGroupName</span></span>
<span data-ttu-id="c043b-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c043b-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c043b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c043b-131">-Confirm</span></span>
<span data-ttu-id="c043b-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c043b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c043b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c043b-133">-WhatIf</span></span>
<span data-ttu-id="c043b-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c043b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c043b-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c043b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c043b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c043b-136">CommonParameters</span></span>
<span data-ttu-id="c043b-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c043b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c043b-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c043b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c043b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c043b-139">INPUTS</span></span>

### <span data-ttu-id="c043b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c043b-140">System.String</span></span>

## <span data-ttu-id="c043b-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c043b-141">OUTPUTS</span></span>

### <span data-ttu-id="c043b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c043b-142">System.Boolean</span></span>

## <span data-ttu-id="c043b-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="c043b-143">NOTES</span></span>

## <span data-ttu-id="c043b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c043b-144">RELATED LINKS</span></span>
