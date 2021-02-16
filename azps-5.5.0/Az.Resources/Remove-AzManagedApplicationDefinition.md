---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 88d89e819d97a42a797be81e5cb0b4b401401108
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113305"
---
# <span data-ttu-id="007d4-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="007d4-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="007d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="007d4-102">SYNOPSIS</span></span>
<span data-ttu-id="007d4-103">Remove uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="007d4-103">Removes a managed application definition</span></span>

## <span data-ttu-id="007d4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="007d4-104">SYNTAX</span></span>

### <span data-ttu-id="007d4-105">RemoveByNameAndResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="007d4-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="007d4-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="007d4-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="007d4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="007d4-107">DESCRIPTION</span></span>
<span data-ttu-id="007d4-108">O cmdlet **Remove-AzManagedApplicationDefinition** remove uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="007d4-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="007d4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="007d4-109">EXAMPLES</span></span>

### <span data-ttu-id="007d4-110">Exemplo 1: Remover definição de aplicativo gerenciado por ID de recurso</span><span class="sxs-lookup"><span data-stu-id="007d4-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="007d4-111">O primeiro comando obtém uma definição de aplicativo gerenciado chamada myAppDef usando o cmdlet Get-AzManagedApplicationDefinition usuário.</span><span class="sxs-lookup"><span data-stu-id="007d4-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="007d4-112">O comando o armazena na variável $ApplicationDefinition dados.</span><span class="sxs-lookup"><span data-stu-id="007d4-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="007d4-113">O segundo comando remove a definição de aplicativo gerenciado identificada pela propriedade **ResourceId** do $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="007d4-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="007d4-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="007d4-114">PARAMETERS</span></span>

### <span data-ttu-id="007d4-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="007d4-115">-ApiVersion</span></span>
<span data-ttu-id="007d4-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="007d4-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="007d4-117">Se não especificado, a versão da API será determinada automaticamente como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="007d4-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="007d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="007d4-118">-DefaultProfile</span></span>
<span data-ttu-id="007d4-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="007d4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="007d4-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="007d4-120">-Force</span></span>
<span data-ttu-id="007d4-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="007d4-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="007d4-122">-ID</span><span class="sxs-lookup"><span data-stu-id="007d4-122">-Id</span></span>
<span data-ttu-id="007d4-123">A ID de definição de aplicativo gerenciado totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="007d4-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="007d4-124">por exemplo, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="007d4-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="007d4-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="007d4-125">-Name</span></span>
<span data-ttu-id="007d4-126">O nome de definição de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="007d4-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="007d4-127">-Pré-</span><span class="sxs-lookup"><span data-stu-id="007d4-127">-Pre</span></span>
<span data-ttu-id="007d4-128">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="007d4-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="007d4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="007d4-129">-ResourceGroupName</span></span>
<span data-ttu-id="007d4-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="007d4-130">The resource group name.</span></span>

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

### <span data-ttu-id="007d4-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="007d4-131">-Confirm</span></span>
<span data-ttu-id="007d4-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="007d4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="007d4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="007d4-133">-WhatIf</span></span>
<span data-ttu-id="007d4-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="007d4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="007d4-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="007d4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="007d4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007d4-136">CommonParameters</span></span>
<span data-ttu-id="007d4-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="007d4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007d4-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="007d4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007d4-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="007d4-139">INPUTS</span></span>

### <span data-ttu-id="007d4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="007d4-140">System.String</span></span>

## <span data-ttu-id="007d4-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="007d4-141">OUTPUTS</span></span>

### <span data-ttu-id="007d4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="007d4-142">System.Boolean</span></span>

## <span data-ttu-id="007d4-143">Notas</span><span class="sxs-lookup"><span data-stu-id="007d4-143">NOTES</span></span>

## <span data-ttu-id="007d4-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="007d4-144">RELATED LINKS</span></span>
