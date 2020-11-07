---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: e25a41c80c7bc277073f9b00331087203590cd22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773317"
---
# <span data-ttu-id="37b40-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="37b40-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="37b40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37b40-102">SYNOPSIS</span></span>
<span data-ttu-id="37b40-103">Remove uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="37b40-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="37b40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37b40-104">SYNTAX</span></span>

### <span data-ttu-id="37b40-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="37b40-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37b40-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37b40-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37b40-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37b40-107">DESCRIPTION</span></span>
<span data-ttu-id="37b40-108">O cmdlet **Remove-AzPolicyAssignment** remove a atribuição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="37b40-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="37b40-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37b40-109">EXAMPLES</span></span>

### <span data-ttu-id="37b40-110">Exemplo 1: remover a atribuição de política por nome e escopo</span><span class="sxs-lookup"><span data-stu-id="37b40-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="37b40-111">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="37b40-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="37b40-112">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="37b40-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="37b40-113">O segundo comando Remove a atribuição de política chamada PolicyAssignment07 que foi atribuída a um nível de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="37b40-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="37b40-114">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="37b40-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="37b40-115">Exemplo 2: remover a atribuição de política por ID</span><span class="sxs-lookup"><span data-stu-id="37b40-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="37b40-116">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="37b40-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="37b40-117">O segundo comando obtém a atribuição de política em um nível de grupo de recursos e, em seguida, armazena-a na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="37b40-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="37b40-118">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="37b40-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="37b40-119">O comando final remove a atribuição de política que a propriedade **Resource** do $PolicyAssignment identifica.</span><span class="sxs-lookup"><span data-stu-id="37b40-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="37b40-120">OS</span><span class="sxs-lookup"><span data-stu-id="37b40-120">PARAMETERS</span></span>

### <span data-ttu-id="37b40-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="37b40-121">-ApiVersion</span></span>
<span data-ttu-id="37b40-122">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="37b40-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="37b40-123">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="37b40-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="37b40-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b40-124">-DefaultProfile</span></span>
<span data-ttu-id="37b40-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="37b40-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37b40-126">-ID</span><span class="sxs-lookup"><span data-stu-id="37b40-126">-Id</span></span>
<span data-ttu-id="37b40-127">Especifica a ID de recurso totalmente qualificado para a atribuição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="37b40-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="37b40-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="37b40-128">-Name</span></span>
<span data-ttu-id="37b40-129">Especifica o nome da atribuição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="37b40-129">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="37b40-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="37b40-130">-Pre</span></span>
<span data-ttu-id="37b40-131">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="37b40-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="37b40-132">-Escopo</span><span class="sxs-lookup"><span data-stu-id="37b40-132">-Scope</span></span>
<span data-ttu-id="37b40-133">Especifica o escopo no qual a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="37b40-133">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="37b40-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="37b40-134">-Confirm</span></span>
<span data-ttu-id="37b40-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37b40-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37b40-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b40-136">-WhatIf</span></span>
<span data-ttu-id="37b40-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37b40-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37b40-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37b40-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37b40-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b40-139">CommonParameters</span></span>
<span data-ttu-id="37b40-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b40-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b40-141">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37b40-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b40-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37b40-142">INPUTS</span></span>

### <span data-ttu-id="37b40-143">System. String</span><span class="sxs-lookup"><span data-stu-id="37b40-143">System.String</span></span>

## <span data-ttu-id="37b40-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37b40-144">OUTPUTS</span></span>

### <span data-ttu-id="37b40-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37b40-145">System.Boolean</span></span>

## <span data-ttu-id="37b40-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37b40-146">NOTES</span></span>

## <span data-ttu-id="37b40-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37b40-147">RELATED LINKS</span></span>

[<span data-ttu-id="37b40-148">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="37b40-148">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="37b40-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="37b40-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="37b40-150">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="37b40-150">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


