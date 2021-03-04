---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: a65892efce36490d256c99935f6cbe8a96f5ff98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890082"
---
# <span data-ttu-id="6f236-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f236-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="6f236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f236-102">SYNOPSIS</span></span>
<span data-ttu-id="6f236-103">Remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="6f236-103">Removes a policy definition.</span></span>

## <span data-ttu-id="6f236-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6f236-104">SYNTAX</span></span>

### <span data-ttu-id="6f236-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6f236-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f236-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f236-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f236-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f236-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f236-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f236-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f236-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f236-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f236-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6f236-110">DESCRIPTION</span></span>
<span data-ttu-id="6f236-111">O cmdlet **Remove-AzPolicyDefinition** remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="6f236-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="6f236-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f236-112">EXAMPLES</span></span>

### <span data-ttu-id="6f236-113">Exemplo 1: Remover a definição de política pelo nome</span><span class="sxs-lookup"><span data-stu-id="6f236-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="6f236-114">Este comando remove a definição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="6f236-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="6f236-115">Exemplo 2: Remover definição de política por ID de recurso</span><span class="sxs-lookup"><span data-stu-id="6f236-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="6f236-116">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzPolicyDefinition de segurança.</span><span class="sxs-lookup"><span data-stu-id="6f236-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="6f236-117">O comando armazena-o na variável $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="6f236-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="6f236-118">O segundo comando remove a definição de política identificada pela **propriedade ResourceId** do $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="6f236-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="6f236-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6f236-119">PARAMETERS</span></span>

### <span data-ttu-id="6f236-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6f236-120">-ApiVersion</span></span>
<span data-ttu-id="6f236-121">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="6f236-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6f236-122">Se você não especificar uma versão, este cmdlet usará a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="6f236-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6f236-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f236-123">-DefaultProfile</span></span>
<span data-ttu-id="6f236-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6f236-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f236-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6f236-125">-Force</span></span>
<span data-ttu-id="6f236-126">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6f236-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f236-127">-Id</span><span class="sxs-lookup"><span data-stu-id="6f236-127">-Id</span></span>
<span data-ttu-id="6f236-128">Especifica a ID de recurso totalmente qualificada para a definição de política que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="6f236-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6f236-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f236-129">-InputObject</span></span>
<span data-ttu-id="6f236-130">O objeto de definição de política a ser removido que foi saída de outro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f236-130">The policy definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f236-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6f236-131">-ManagementGroupName</span></span>
<span data-ttu-id="6f236-132">O nome do grupo de gerenciamento da definição de política a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6f236-132">The name of the management group of the policy definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f236-133">-Name</span><span class="sxs-lookup"><span data-stu-id="6f236-133">-Name</span></span>
<span data-ttu-id="6f236-134">Especifica o nome da definição de política que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="6f236-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f236-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="6f236-135">-Pre</span></span>
<span data-ttu-id="6f236-136">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="6f236-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6f236-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f236-137">-SubscriptionId</span></span>
<span data-ttu-id="6f236-138">A ID da assinatura da definição de política a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6f236-138">The subscription ID of the policy definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f236-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f236-139">-Confirm</span></span>
<span data-ttu-id="6f236-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f236-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f236-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f236-141">-WhatIf</span></span>
<span data-ttu-id="6f236-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6f236-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f236-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6f236-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f236-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f236-144">CommonParameters</span></span>
<span data-ttu-id="6f236-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f236-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f236-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f236-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f236-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f236-147">INPUTS</span></span>

### <span data-ttu-id="6f236-148">System.String</span><span class="sxs-lookup"><span data-stu-id="6f236-148">System.String</span></span>

### <span data-ttu-id="6f236-149">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6f236-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6f236-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6f236-150">OUTPUTS</span></span>

### <span data-ttu-id="6f236-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f236-151">System.Boolean</span></span>

## <span data-ttu-id="6f236-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="6f236-152">NOTES</span></span>

## <span data-ttu-id="6f236-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f236-153">RELATED LINKS</span></span>

[<span data-ttu-id="6f236-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f236-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="6f236-155">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f236-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="6f236-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f236-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


