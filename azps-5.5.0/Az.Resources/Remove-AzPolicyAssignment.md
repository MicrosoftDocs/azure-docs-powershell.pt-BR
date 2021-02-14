---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117179"
---
# <span data-ttu-id="bdf09-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bdf09-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="bdf09-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdf09-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf09-103">Remove uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="bdf09-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="bdf09-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdf09-104">SYNTAX</span></span>

### <span data-ttu-id="bdf09-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bdf09-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdf09-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdf09-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdf09-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdf09-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdf09-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bdf09-108">DESCRIPTION</span></span>
<span data-ttu-id="bdf09-109">O cmdlet **Remove-AzPolicyAssignment** remove a atribuição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="bdf09-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="bdf09-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bdf09-110">EXAMPLES</span></span>

### <span data-ttu-id="bdf09-111">Exemplo 1: Remover atribuição de política por nome e escopo</span><span class="sxs-lookup"><span data-stu-id="bdf09-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="bdf09-112">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdf09-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="bdf09-113">O comando armazena esse objeto na variável $ResourceGroup dados.</span><span class="sxs-lookup"><span data-stu-id="bdf09-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="bdf09-114">O segundo comando remove a atribuição de política chamada PolicyAssignment07 que foi atribuída a um nível de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bdf09-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="bdf09-115">A **propriedade ResourceId** da $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bdf09-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="bdf09-116">Exemplo 2: Remover atribuição de política por ID</span><span class="sxs-lookup"><span data-stu-id="bdf09-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="bdf09-117">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $ResourceGroup dados.</span><span class="sxs-lookup"><span data-stu-id="bdf09-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="bdf09-118">O segundo comando obtém a atribuição de política em um nível de grupo de recursos e a armazena na variável $PolicyAssignment dados.</span><span class="sxs-lookup"><span data-stu-id="bdf09-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="bdf09-119">A **propriedade ResourceId** da $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bdf09-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="bdf09-120">O comando final remove a atribuição de política que a propriedade **ResourceId** da $PolicyAssignment identifica.</span><span class="sxs-lookup"><span data-stu-id="bdf09-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="bdf09-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdf09-121">PARAMETERS</span></span>

### <span data-ttu-id="bdf09-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bdf09-122">-ApiVersion</span></span>
<span data-ttu-id="bdf09-123">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="bdf09-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bdf09-124">Se você não especificar uma versão, este cmdlet usará a versão disponível mais recente.</span><span class="sxs-lookup"><span data-stu-id="bdf09-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bdf09-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf09-125">-DefaultProfile</span></span>
<span data-ttu-id="bdf09-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="bdf09-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdf09-127">-ID</span><span class="sxs-lookup"><span data-stu-id="bdf09-127">-Id</span></span>
<span data-ttu-id="bdf09-128">Especifica a ID de recurso totalmente qualificada para a atribuição de política que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="bdf09-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf09-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdf09-129">-InputObject</span></span>
<span data-ttu-id="bdf09-130">O objeto de atribuição de política para remover que foi saída de outro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdf09-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf09-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdf09-131">-Name</span></span>
<span data-ttu-id="bdf09-132">Especifica o nome da atribuição de política que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="bdf09-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf09-133">-Pré-</span><span class="sxs-lookup"><span data-stu-id="bdf09-133">-Pre</span></span>
<span data-ttu-id="bdf09-134">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="bdf09-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bdf09-135">-Escopo</span><span class="sxs-lookup"><span data-stu-id="bdf09-135">-Scope</span></span>
<span data-ttu-id="bdf09-136">Especifica o escopo no qual a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="bdf09-136">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf09-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bdf09-137">-Confirm</span></span>
<span data-ttu-id="bdf09-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdf09-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf09-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdf09-139">-WhatIf</span></span>
<span data-ttu-id="bdf09-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bdf09-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdf09-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdf09-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdf09-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf09-142">CommonParameters</span></span>
<span data-ttu-id="bdf09-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf09-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf09-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdf09-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf09-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="bdf09-145">INPUTS</span></span>

### <span data-ttu-id="bdf09-146">System.String</span><span class="sxs-lookup"><span data-stu-id="bdf09-146">System.String</span></span>

## <span data-ttu-id="bdf09-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="bdf09-147">OUTPUTS</span></span>

### <span data-ttu-id="bdf09-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bdf09-148">System.Boolean</span></span>

## <span data-ttu-id="bdf09-149">Notas</span><span class="sxs-lookup"><span data-stu-id="bdf09-149">NOTES</span></span>

## <span data-ttu-id="bdf09-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdf09-150">RELATED LINKS</span></span>

[<span data-ttu-id="bdf09-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bdf09-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="bdf09-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bdf09-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="bdf09-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bdf09-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


