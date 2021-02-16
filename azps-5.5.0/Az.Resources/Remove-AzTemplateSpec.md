---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114021"
---
# <span data-ttu-id="6a77f-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="6a77f-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="6a77f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a77f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a77f-103">Remove uma Especificação de Modelo</span><span class="sxs-lookup"><span data-stu-id="6a77f-103">Removes a Template Spec</span></span>

## <span data-ttu-id="6a77f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a77f-104">SYNTAX</span></span>

### <span data-ttu-id="6a77f-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6a77f-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a77f-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a77f-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a77f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a77f-107">DESCRIPTION</span></span>
<span data-ttu-id="6a77f-108">Remove uma Especificação de Modelo especificada. Se o parâmetro **versão -Versão** for fornecido, somente a versão especificada será removida.</span><span class="sxs-lookup"><span data-stu-id="6a77f-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="6a77f-109">Se nenhuma versão específica for fornecida, a Especificação de Modelo e todas as suas versões serão removidas.</span><span class="sxs-lookup"><span data-stu-id="6a77f-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="6a77f-110">Se o **sinalizador -Force** estiver presente, não haverá nenhuma solicitação de confirmação para remoção.</span><span class="sxs-lookup"><span data-stu-id="6a77f-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="6a77f-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6a77f-111">EXAMPLES</span></span>

### <span data-ttu-id="6a77f-112">Exemplo 1: Removendo uma versão específica por nome</span><span class="sxs-lookup"><span data-stu-id="6a77f-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="6a77f-113">Remove a versão 'v1.0' da Especificação de Modelo chamada 'MyTemplateSpec' dentro do grupo de recursos 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="6a77f-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="6a77f-114">Exemplo 2: Removendo uma versão específica por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="6a77f-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="6a77f-115">Remove a versão 'v1.0' da Especificação de Modelo chamada 'MyTemplateSpec' no grupo de recursos "myRG" da subId de \{ \} assinatura.</span><span class="sxs-lookup"><span data-stu-id="6a77f-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="6a77f-116">Exemplo 3: Removendo uma Especificação de Modelo e todas as versões por nome</span><span class="sxs-lookup"><span data-stu-id="6a77f-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="6a77f-117">Remove a Especificação de Modelo chamada 'MyTemplateSpec' e todas as suas versões dentro do grupo de recursos "meuRG".</span><span class="sxs-lookup"><span data-stu-id="6a77f-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="6a77f-118">Exemplo 3: Removendo uma Especificação de Modelo e todas as versões por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="6a77f-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="6a77f-119">Remove a Especificação de Modelo chamada 'MyTemplateSpec' e todas as suas versões dentro do grupo de recursos "myRG" da subId de \{ \} assinatura.</span><span class="sxs-lookup"><span data-stu-id="6a77f-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="6a77f-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a77f-120">PARAMETERS</span></span>

### <span data-ttu-id="6a77f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a77f-121">-DefaultProfile</span></span>
<span data-ttu-id="6a77f-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a77f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a77f-123">-Forçar</span><span class="sxs-lookup"><span data-stu-id="6a77f-123">-Force</span></span>
<span data-ttu-id="6a77f-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="6a77f-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6a77f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a77f-125">-Name</span></span>
<span data-ttu-id="6a77f-126">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="6a77f-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a77f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a77f-127">-ResourceGroupName</span></span>
<span data-ttu-id="6a77f-128">O nome do grupo de recursos da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="6a77f-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a77f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a77f-129">-ResourceId</span></span>
<span data-ttu-id="6a77f-130">A ID de recurso totalmente qualificada da especificação do modelo. Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="6a77f-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a77f-131">-Versão</span><span class="sxs-lookup"><span data-stu-id="6a77f-131">-Version</span></span>
<span data-ttu-id="6a77f-132">A versão da especificação do modelo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6a77f-132">The version of the template spec to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a77f-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6a77f-133">-Confirm</span></span>
<span data-ttu-id="6a77f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a77f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a77f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a77f-135">-WhatIf</span></span>
<span data-ttu-id="6a77f-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6a77f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a77f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6a77f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a77f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a77f-138">CommonParameters</span></span>
<span data-ttu-id="6a77f-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a77f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a77f-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a77f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a77f-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="6a77f-141">INPUTS</span></span>

### <span data-ttu-id="6a77f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6a77f-142">System.String</span></span>

## <span data-ttu-id="6a77f-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="6a77f-143">OUTPUTS</span></span>

### <span data-ttu-id="6a77f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a77f-144">System.Boolean</span></span>

## <span data-ttu-id="6a77f-145">Notas</span><span class="sxs-lookup"><span data-stu-id="6a77f-145">NOTES</span></span>

## <span data-ttu-id="6a77f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a77f-146">RELATED LINKS</span></span>
