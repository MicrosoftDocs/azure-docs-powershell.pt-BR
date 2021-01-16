---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261846"
---
# <span data-ttu-id="2e3f7-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="2e3f7-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="2e3f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e3f7-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3f7-103">Remove uma especificação de modelo</span><span class="sxs-lookup"><span data-stu-id="2e3f7-103">Removes a Template Spec</span></span>

## <span data-ttu-id="2e3f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e3f7-104">SYNTAX</span></span>

### <span data-ttu-id="2e3f7-105">RemoveByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2e3f7-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e3f7-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e3f7-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e3f7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e3f7-107">DESCRIPTION</span></span>
<span data-ttu-id="2e3f7-108">Remove uma especificação de modelo especificada. Se o parâmetro version **-version** for fornecido, somente a versão especificada será removida.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="2e3f7-109">Se nenhuma versão específica for fornecida, a especificação do modelo e todas as suas versões serão removidas.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="2e3f7-110">Se o sinalizador **-Force** estiver presente, não haverá prompt de confirmação para remoção.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="2e3f7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e3f7-111">EXAMPLES</span></span>

### <span data-ttu-id="2e3f7-112">Exemplo 1: removendo uma versão específica por nome</span><span class="sxs-lookup"><span data-stu-id="2e3f7-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="2e3f7-113">Remove a versão "v 1.0" da especificação de modelo chamada "MyTemplateSpec" no grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="2e3f7-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="2e3f7-114">Exemplo 2: removendo uma versão específica por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="2e3f7-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="2e3f7-115">Remove a versão "v 1.0" da especificação de modelo chamada "MyTemplateSpec" no grupo de recursos "myRG" da \{ subId de assinatura \} .</span><span class="sxs-lookup"><span data-stu-id="2e3f7-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="2e3f7-116">Exemplo 3: removendo uma especificação de modelo e todas as versões por nome</span><span class="sxs-lookup"><span data-stu-id="2e3f7-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="2e3f7-117">Remove a especificação de modelo chamada ' MyTemplateSpec ' e todas as suas versões dentro do grupo de recursos ' myRG '.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="2e3f7-118">Exemplo 3: removendo uma especificação de modelo e todas as versões por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="2e3f7-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="2e3f7-119">Remove a especificação de modelo chamada ' MyTemplateSpec ' e todas as suas versões dentro do grupo de recursos ' myRG ' da assinatura \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="2e3f7-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="2e3f7-120">OS</span><span class="sxs-lookup"><span data-stu-id="2e3f7-120">PARAMETERS</span></span>

### <span data-ttu-id="2e3f7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3f7-121">-DefaultProfile</span></span>
<span data-ttu-id="2e3f7-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e3f7-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2e3f7-123">-Force</span></span>
<span data-ttu-id="2e3f7-124">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2e3f7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e3f7-125">-Name</span></span>
<span data-ttu-id="2e3f7-126">O nome da especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-126">The name of the template spec.</span></span>

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

### <span data-ttu-id="2e3f7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e3f7-127">-ResourceGroupName</span></span>
<span data-ttu-id="2e3f7-128">O nome do grupo de recursos de especificação do modelo.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-128">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="2e3f7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e3f7-129">-ResourceId</span></span>
<span data-ttu-id="2e3f7-130">A ID de recurso totalmente qualificado da especificação do modelo. exemplo:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="2e3f7-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="2e3f7-131">-Versão</span><span class="sxs-lookup"><span data-stu-id="2e3f7-131">-Version</span></span>
<span data-ttu-id="2e3f7-132">A versão da especificação do modelo a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-132">The version of the template spec to delete.</span></span>

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

### <span data-ttu-id="2e3f7-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2e3f7-133">-Confirm</span></span>
<span data-ttu-id="2e3f7-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e3f7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e3f7-135">-WhatIf</span></span>
<span data-ttu-id="2e3f7-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e3f7-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e3f7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e3f7-138">CommonParameters</span></span>
<span data-ttu-id="2e3f7-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e3f7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e3f7-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e3f7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e3f7-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e3f7-141">INPUTS</span></span>

### <span data-ttu-id="2e3f7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2e3f7-142">System.String</span></span>

## <span data-ttu-id="2e3f7-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e3f7-143">OUTPUTS</span></span>

### <span data-ttu-id="2e3f7-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2e3f7-144">System.Boolean</span></span>

## <span data-ttu-id="2e3f7-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e3f7-145">NOTES</span></span>

## <span data-ttu-id="2e3f7-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e3f7-146">RELATED LINKS</span></span>
