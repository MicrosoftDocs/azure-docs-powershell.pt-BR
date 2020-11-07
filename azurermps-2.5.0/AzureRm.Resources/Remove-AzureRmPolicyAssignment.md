---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: 6972d4df51222804843aa965577f7044ed4bf987
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786383"
---
# <span data-ttu-id="dd662-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dd662-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="dd662-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd662-102">SYNOPSIS</span></span>
<span data-ttu-id="dd662-103">Remove uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="dd662-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd662-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd662-104">SYNTAX</span></span>

### <span data-ttu-id="dd662-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dd662-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd662-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd662-106">IdParameterSet</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd662-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd662-107">DESCRIPTION</span></span>
<span data-ttu-id="dd662-108">O cmdlet **Remove-AzureRmPolicyAssignment** remove a atribuição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="dd662-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="dd662-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd662-109">EXAMPLES</span></span>

### <span data-ttu-id="dd662-110">Exemplo 1: remover a atribuição de política por nome e escopo</span><span class="sxs-lookup"><span data-stu-id="dd662-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="dd662-111">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dd662-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="dd662-112">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dd662-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="dd662-113">O segundo comando Remove a atribuição de política chamada PolicyAssignment07 que foi atribuída a um nível de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd662-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="dd662-114">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd662-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="dd662-115">Exemplo 2: remover a atribuição de política por ID</span><span class="sxs-lookup"><span data-stu-id="dd662-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="dd662-116">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dd662-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="dd662-117">O segundo comando obtém a atribuição de política em um nível de grupo de recursos e, em seguida, armazena-a na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="dd662-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="dd662-118">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd662-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="dd662-119">O comando final remove a atribuição de política que a propriedade **Resource** do $PolicyAssignment identifica.</span><span class="sxs-lookup"><span data-stu-id="dd662-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="dd662-120">OS</span><span class="sxs-lookup"><span data-stu-id="dd662-120">PARAMETERS</span></span>

### <span data-ttu-id="dd662-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dd662-121">-ApiVersion</span></span>
<span data-ttu-id="dd662-122">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="dd662-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="dd662-123">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="dd662-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="dd662-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd662-124">-DefaultProfile</span></span>
<span data-ttu-id="dd662-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dd662-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd662-126">-ID</span><span class="sxs-lookup"><span data-stu-id="dd662-126">-Id</span></span>
<span data-ttu-id="dd662-127">Especifica a ID de recurso totalmente qualificado para a atribuição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="dd662-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dd662-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="dd662-128">-InformationAction</span></span>
<span data-ttu-id="dd662-129">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="dd662-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="dd662-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="dd662-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dd662-131">Contínuo</span><span class="sxs-lookup"><span data-stu-id="dd662-131">Continue</span></span>
- <span data-ttu-id="dd662-132">Ignorar</span><span class="sxs-lookup"><span data-stu-id="dd662-132">Ignore</span></span>
- <span data-ttu-id="dd662-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="dd662-133">Inquire</span></span>
- <span data-ttu-id="dd662-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dd662-134">SilentlyContinue</span></span>
- <span data-ttu-id="dd662-135">Finaliza</span><span class="sxs-lookup"><span data-stu-id="dd662-135">Stop</span></span>
- <span data-ttu-id="dd662-136">Suspensão</span><span class="sxs-lookup"><span data-stu-id="dd662-136">Suspend</span></span>

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

### <span data-ttu-id="dd662-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dd662-137">-InformationVariable</span></span>
<span data-ttu-id="dd662-138">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="dd662-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dd662-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd662-139">-Name</span></span>
<span data-ttu-id="dd662-140">Especifica o nome da atribuição de política que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="dd662-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dd662-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="dd662-141">-Pre</span></span>
<span data-ttu-id="dd662-142">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="dd662-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dd662-143">-Escopo</span><span class="sxs-lookup"><span data-stu-id="dd662-143">-Scope</span></span>
<span data-ttu-id="dd662-144">Especifica o escopo no qual a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="dd662-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="dd662-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dd662-145">-Confirm</span></span>
<span data-ttu-id="dd662-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd662-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd662-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd662-147">-WhatIf</span></span>
<span data-ttu-id="dd662-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd662-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd662-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd662-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd662-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd662-150">CommonParameters</span></span>
<span data-ttu-id="dd662-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd662-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd662-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd662-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd662-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd662-153">INPUTS</span></span>

## <span data-ttu-id="dd662-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd662-154">OUTPUTS</span></span>

## <span data-ttu-id="dd662-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd662-155">NOTES</span></span>

## <span data-ttu-id="dd662-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd662-156">RELATED LINKS</span></span>

[<span data-ttu-id="dd662-157">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dd662-157">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="dd662-158">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dd662-158">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="dd662-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dd662-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


