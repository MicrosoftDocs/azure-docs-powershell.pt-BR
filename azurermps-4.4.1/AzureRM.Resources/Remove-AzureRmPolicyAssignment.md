---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: 9a238515b0482b36dcebd3bdcdf6976aebc64448
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610184"
---
# <span data-ttu-id="03a50-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="03a50-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="03a50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03a50-102">SYNOPSIS</span></span>
<span data-ttu-id="03a50-103">Remove uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="03a50-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03a50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03a50-104">SYNTAX</span></span>

### <span data-ttu-id="03a50-105">O conjunto de parâmetros de nome da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="03a50-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="03a50-106">Assume</span><span class="sxs-lookup"><span data-stu-id="03a50-106">(Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03a50-107">O conjunto de parâmetros de ID da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="03a50-107">The policy assignment Id parameter set.</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03a50-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03a50-108">DESCRIPTION</span></span>
<span data-ttu-id="03a50-109">O cmdlet **Remove-AzureRmPolicyAssignment** remove a atribuição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="03a50-109">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="03a50-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03a50-110">EXAMPLES</span></span>

### <span data-ttu-id="03a50-111">Exemplo 1: remover a atribuição de política por nome e escopo</span><span class="sxs-lookup"><span data-stu-id="03a50-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="03a50-112">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="03a50-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="03a50-113">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="03a50-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="03a50-114">O segundo comando Remove a atribuição de política chamada PolicyAssignment07 que foi atribuída a um nível de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="03a50-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="03a50-115">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="03a50-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="03a50-116">Exemplo 2: remover a atribuição de política por ID</span><span class="sxs-lookup"><span data-stu-id="03a50-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="03a50-117">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="03a50-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="03a50-118">O segundo comando obtém a atribuição de política em um nível de grupo de recursos e, em seguida, armazena-a na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="03a50-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="03a50-119">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="03a50-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="03a50-120">O comando final remove a atribuição de política que a propriedade **Resource** do $PolicyAssignment identifica.</span><span class="sxs-lookup"><span data-stu-id="03a50-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="03a50-121">OS</span><span class="sxs-lookup"><span data-stu-id="03a50-121">PARAMETERS</span></span>

### <span data-ttu-id="03a50-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="03a50-122">-ApiVersion</span></span>
<span data-ttu-id="03a50-123">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="03a50-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="03a50-124">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="03a50-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="03a50-125">-ID</span><span class="sxs-lookup"><span data-stu-id="03a50-125">-Id</span></span>
<span data-ttu-id="03a50-126">Especifica a ID de recurso totalmente qualificado para a atribuição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="03a50-126">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a50-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="03a50-127">-InformationAction</span></span>
<span data-ttu-id="03a50-128">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="03a50-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="03a50-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="03a50-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="03a50-130">Contínuo</span><span class="sxs-lookup"><span data-stu-id="03a50-130">Continue</span></span>
- <span data-ttu-id="03a50-131">Ignorar</span><span class="sxs-lookup"><span data-stu-id="03a50-131">Ignore</span></span>
- <span data-ttu-id="03a50-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="03a50-132">Inquire</span></span>
- <span data-ttu-id="03a50-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="03a50-133">SilentlyContinue</span></span>
- <span data-ttu-id="03a50-134">Finaliza</span><span class="sxs-lookup"><span data-stu-id="03a50-134">Stop</span></span>
- <span data-ttu-id="03a50-135">Suspensão</span><span class="sxs-lookup"><span data-stu-id="03a50-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a50-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="03a50-136">-InformationVariable</span></span>
<span data-ttu-id="03a50-137">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="03a50-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a50-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="03a50-138">-Name</span></span>
<span data-ttu-id="03a50-139">Especifica o nome da atribuição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="03a50-139">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a50-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="03a50-140">-Pre</span></span>
<span data-ttu-id="03a50-141">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="03a50-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="03a50-142">-Escopo</span><span class="sxs-lookup"><span data-stu-id="03a50-142">-Scope</span></span>
<span data-ttu-id="03a50-143">Especifica o escopo no qual a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="03a50-143">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a50-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="03a50-144">-Confirm</span></span>
<span data-ttu-id="03a50-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03a50-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03a50-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03a50-146">-WhatIf</span></span>
<span data-ttu-id="03a50-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03a50-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03a50-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03a50-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03a50-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a50-149">-DefaultProfile</span></span>
<span data-ttu-id="03a50-150">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03a50-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a50-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a50-151">CommonParameters</span></span>
<span data-ttu-id="03a50-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03a50-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a50-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03a50-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a50-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03a50-154">INPUTS</span></span>

## <span data-ttu-id="03a50-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03a50-155">OUTPUTS</span></span>

### <span data-ttu-id="03a50-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03a50-156">System.Boolean</span></span>

## <span data-ttu-id="03a50-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03a50-157">NOTES</span></span>

## <span data-ttu-id="03a50-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03a50-158">RELATED LINKS</span></span>

[<span data-ttu-id="03a50-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="03a50-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="03a50-160">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="03a50-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="03a50-161">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="03a50-161">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


