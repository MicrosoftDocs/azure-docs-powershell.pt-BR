---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: d78cf9d28c453626c26656b9f9280f5c52695434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429682"
---
# <span data-ttu-id="eeb37-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="eeb37-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="eeb37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eeb37-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb37-103">Remove uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="eeb37-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeb37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eeb37-104">SYNTAX</span></span>

### <span data-ttu-id="eeb37-105">RemoveByPolicyAssignmentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="eeb37-105">RemoveByPolicyAssignmentName (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb37-106">RemoveByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="eeb37-106">RemoveByPolicyAssignmentId</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeb37-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eeb37-107">DESCRIPTION</span></span>
<span data-ttu-id="eeb37-108">O cmdlet **Remove-AzureRmPolicyAssignment** remove a atribuição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="eeb37-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="eeb37-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eeb37-109">EXAMPLES</span></span>

### <span data-ttu-id="eeb37-110">Exemplo 1: remover a atribuição de política por nome e escopo</span><span class="sxs-lookup"><span data-stu-id="eeb37-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="eeb37-111">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eeb37-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="eeb37-112">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eeb37-112">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="eeb37-113">O segundo comando Remove a atribuição de política chamada PolicyAssignment07 que foi atribuída a um nível de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eeb37-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="eeb37-114">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eeb37-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="eeb37-115">Exemplo 2: remover a atribuição de política por ID</span><span class="sxs-lookup"><span data-stu-id="eeb37-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="eeb37-116">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eeb37-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="eeb37-117">O segundo comando obtém a atribuição de política em um nível de grupo de recursos e, em seguida, armazena-a na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="eeb37-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="eeb37-118">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eeb37-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="eeb37-119">O comando final remove a atribuição de política que a propriedade **Resource** do $PolicyAssignment identifica.</span><span class="sxs-lookup"><span data-stu-id="eeb37-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="eeb37-120">OS</span><span class="sxs-lookup"><span data-stu-id="eeb37-120">PARAMETERS</span></span>

### <span data-ttu-id="eeb37-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="eeb37-121">-ApiVersion</span></span>
<span data-ttu-id="eeb37-122">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="eeb37-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="eeb37-123">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="eeb37-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb37-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb37-124">-DefaultProfile</span></span>
<span data-ttu-id="eeb37-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="eeb37-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb37-126">-ID</span><span class="sxs-lookup"><span data-stu-id="eeb37-126">-Id</span></span>
<span data-ttu-id="eeb37-127">Especifica a ID de recurso totalmente qualificado para a atribuição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="eeb37-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb37-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="eeb37-128">-InformationAction</span></span>
<span data-ttu-id="eeb37-129">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="eeb37-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eeb37-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="eeb37-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eeb37-131">Contínuo</span><span class="sxs-lookup"><span data-stu-id="eeb37-131">Continue</span></span>
- <span data-ttu-id="eeb37-132">Ignorar</span><span class="sxs-lookup"><span data-stu-id="eeb37-132">Ignore</span></span>
- <span data-ttu-id="eeb37-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="eeb37-133">Inquire</span></span>
- <span data-ttu-id="eeb37-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eeb37-134">SilentlyContinue</span></span>
- <span data-ttu-id="eeb37-135">Finaliza</span><span class="sxs-lookup"><span data-stu-id="eeb37-135">Stop</span></span>
- <span data-ttu-id="eeb37-136">Suspensão</span><span class="sxs-lookup"><span data-stu-id="eeb37-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb37-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eeb37-137">-InformationVariable</span></span>
<span data-ttu-id="eeb37-138">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="eeb37-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb37-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="eeb37-139">-Name</span></span>
<span data-ttu-id="eeb37-140">Especifica o nome da atribuição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="eeb37-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb37-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="eeb37-141">-Pre</span></span>
<span data-ttu-id="eeb37-142">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="eeb37-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb37-143">-Escopo</span><span class="sxs-lookup"><span data-stu-id="eeb37-143">-Scope</span></span>
<span data-ttu-id="eeb37-144">Especifica o escopo no qual a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="eeb37-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb37-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eeb37-145">-Confirm</span></span>
<span data-ttu-id="eeb37-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeb37-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb37-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb37-147">-WhatIf</span></span>
<span data-ttu-id="eeb37-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eeb37-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb37-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eeb37-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb37-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb37-150">CommonParameters</span></span>
<span data-ttu-id="eeb37-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb37-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb37-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeb37-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb37-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eeb37-153">INPUTS</span></span>

### <span data-ttu-id="eeb37-154">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="eeb37-154">None</span></span>
<span data-ttu-id="eeb37-155">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="eeb37-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eeb37-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eeb37-156">OUTPUTS</span></span>

### <span data-ttu-id="eeb37-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eeb37-157">System.Boolean</span></span>

## <span data-ttu-id="eeb37-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eeb37-158">NOTES</span></span>

## <span data-ttu-id="eeb37-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eeb37-159">RELATED LINKS</span></span>

[<span data-ttu-id="eeb37-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="eeb37-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="eeb37-161">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="eeb37-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="eeb37-162">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="eeb37-162">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


