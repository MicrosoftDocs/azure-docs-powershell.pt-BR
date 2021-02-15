---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: c7d292a983090d8be22e159fbca6e423778b21f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111408"
---
# <span data-ttu-id="4b5dd-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4b5dd-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="4b5dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b5dd-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5dd-103">Remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-103">Removes a policy definition.</span></span>

## <span data-ttu-id="4b5dd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b5dd-104">SYNTAX</span></span>

### <span data-ttu-id="4b5dd-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4b5dd-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b5dd-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b5dd-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b5dd-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b5dd-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b5dd-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b5dd-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b5dd-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b5dd-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b5dd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b5dd-110">DESCRIPTION</span></span>
<span data-ttu-id="4b5dd-111">O cmdlet **Remove-AzPolicyDefinition** remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="4b5dd-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b5dd-112">EXAMPLES</span></span>

### <span data-ttu-id="4b5dd-113">Exemplo 1: Remover a definição da política por nome</span><span class="sxs-lookup"><span data-stu-id="4b5dd-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="4b5dd-114">Esse comando remove a definição de política especificada.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="4b5dd-115">Exemplo 2: Remover definição de política por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="4b5dd-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="4b5dd-116">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzPolicyDefinition dados.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="4b5dd-117">O comando o armazena na variável $PolicyDefinition dados.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="4b5dd-118">O segundo comando remove a definição de política identificada pela propriedade **ResourceId** da $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="4b5dd-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b5dd-119">PARAMETERS</span></span>

### <span data-ttu-id="4b5dd-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4b5dd-120">-ApiVersion</span></span>
<span data-ttu-id="4b5dd-121">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4b5dd-122">Se você não especificar uma versão, este cmdlet usará a versão disponível mais recente.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4b5dd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5dd-123">-DefaultProfile</span></span>
<span data-ttu-id="4b5dd-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4b5dd-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b5dd-125">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4b5dd-125">-Force</span></span>
<span data-ttu-id="4b5dd-126">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4b5dd-127">-ID</span><span class="sxs-lookup"><span data-stu-id="4b5dd-127">-Id</span></span>
<span data-ttu-id="4b5dd-128">Especifica a ID de recurso totalmente qualificada para a definição de política que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4b5dd-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b5dd-129">-InputObject</span></span>
<span data-ttu-id="4b5dd-130">O objeto de definição de política para remover a saída de outro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-130">The policy definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="4b5dd-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4b5dd-131">-ManagementGroupName</span></span>
<span data-ttu-id="4b5dd-132">O nome do grupo de gerenciamento da definição de política a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="4b5dd-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b5dd-133">-Name</span></span>
<span data-ttu-id="4b5dd-134">Especifica o nome da definição de política que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4b5dd-135">-Pré-</span><span class="sxs-lookup"><span data-stu-id="4b5dd-135">-Pre</span></span>
<span data-ttu-id="4b5dd-136">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4b5dd-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b5dd-137">-SubscriptionId</span></span>
<span data-ttu-id="4b5dd-138">A ID da assinatura da definição de política a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="4b5dd-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4b5dd-139">-Confirm</span></span>
<span data-ttu-id="4b5dd-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b5dd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b5dd-141">-WhatIf</span></span>
<span data-ttu-id="4b5dd-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b5dd-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b5dd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5dd-144">CommonParameters</span></span>
<span data-ttu-id="4b5dd-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b5dd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5dd-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b5dd-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5dd-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="4b5dd-147">INPUTS</span></span>

### <span data-ttu-id="4b5dd-148">System.String</span><span class="sxs-lookup"><span data-stu-id="4b5dd-148">System.String</span></span>

### <span data-ttu-id="4b5dd-149">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4b5dd-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4b5dd-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="4b5dd-150">OUTPUTS</span></span>

### <span data-ttu-id="4b5dd-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b5dd-151">System.Boolean</span></span>

## <span data-ttu-id="4b5dd-152">Notas</span><span class="sxs-lookup"><span data-stu-id="4b5dd-152">NOTES</span></span>

## <span data-ttu-id="4b5dd-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b5dd-153">RELATED LINKS</span></span>

[<span data-ttu-id="4b5dd-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4b5dd-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="4b5dd-155">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4b5dd-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="4b5dd-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4b5dd-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


