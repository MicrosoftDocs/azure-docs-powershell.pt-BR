---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: da4a08e46abce04b4a30726a419582a22b6e0b41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599312"
---
# <span data-ttu-id="60502-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="60502-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="60502-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60502-102">SYNOPSIS</span></span>
<span data-ttu-id="60502-103">Modifica uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="60502-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="60502-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60502-104">SYNTAX</span></span>

### <span data-ttu-id="60502-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="60502-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60502-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="60502-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60502-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60502-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60502-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60502-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60502-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60502-109">DESCRIPTION</span></span>
<span data-ttu-id="60502-110">O cmdlet **set-AzPolicySetDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="60502-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="60502-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60502-111">EXAMPLES</span></span>

### <span data-ttu-id="60502-112">Exemplo 1: atualizar a descrição de uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="60502-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="60502-113">O primeiro comando obtém uma definição de conjunto de políticas usando o cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="60502-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="60502-114">O comando armazena esse objeto na variável $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="60502-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="60502-115">O segundo comando atualiza a descrição da definição do conjunto de políticas identificada pela propriedade **ResourceId** de $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="60502-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="60502-116">OS</span><span class="sxs-lookup"><span data-stu-id="60502-116">PARAMETERS</span></span>

### <span data-ttu-id="60502-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="60502-117">-ApiVersion</span></span>
<span data-ttu-id="60502-118">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="60502-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="60502-119">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="60502-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="60502-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60502-120">-DefaultProfile</span></span>
<span data-ttu-id="60502-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="60502-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60502-122">-Descrição</span><span class="sxs-lookup"><span data-stu-id="60502-122">-Description</span></span>
<span data-ttu-id="60502-123">A descrição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="60502-123">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60502-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="60502-124">-DisplayName</span></span>
<span data-ttu-id="60502-125">O nome de exibição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="60502-125">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60502-126">-ID</span><span class="sxs-lookup"><span data-stu-id="60502-126">-Id</span></span>
<span data-ttu-id="60502-127">A ID da definição da política totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="60502-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="60502-128">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="60502-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="60502-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="60502-129">-ManagementGroupName</span></span>
<span data-ttu-id="60502-130">O nome do grupo de gerenciamento da definição do conjunto de políticas a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="60502-130">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="60502-131">-Metadados</span><span class="sxs-lookup"><span data-stu-id="60502-131">-Metadata</span></span>
<span data-ttu-id="60502-132">Os metadados da definição do conjunto de políticas atualizado.</span><span class="sxs-lookup"><span data-stu-id="60502-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="60502-133">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="60502-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60502-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="60502-134">-Name</span></span>
<span data-ttu-id="60502-135">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="60502-135">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60502-136">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="60502-136">-Parameter</span></span>
<span data-ttu-id="60502-137">A declaração Parameters da definição de conjunto de políticas atualizada.</span><span class="sxs-lookup"><span data-stu-id="60502-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="60502-138">Isso pode ser um caminho para um nome de arquivo ou URI que contém a declaração Parameters ou a declaração Parameters como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="60502-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60502-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="60502-139">-PolicyDefinition</span></span>
<span data-ttu-id="60502-140">Definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="60502-140">The policy set definition.</span></span> <span data-ttu-id="60502-141">Pode ser um caminho para um nome de arquivo que contenha as definições da política ou a definição do conjunto de políticas como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="60502-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60502-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="60502-142">-Pre</span></span>
<span data-ttu-id="60502-143">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="60502-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="60502-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60502-144">-SubscriptionId</span></span>
<span data-ttu-id="60502-145">A ID da assinatura da definição do conjunto de políticas a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="60502-145">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="60502-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60502-146">-Confirm</span></span>
<span data-ttu-id="60502-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60502-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60502-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60502-148">-WhatIf</span></span>
<span data-ttu-id="60502-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60502-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60502-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60502-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60502-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60502-151">CommonParameters</span></span>
<span data-ttu-id="60502-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60502-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60502-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60502-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60502-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60502-154">INPUTS</span></span>

### <span data-ttu-id="60502-155">System. String</span><span class="sxs-lookup"><span data-stu-id="60502-155">System.String</span></span>

### <span data-ttu-id="60502-156">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="60502-156">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="60502-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60502-157">OUTPUTS</span></span>

### <span data-ttu-id="60502-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="60502-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="60502-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60502-159">NOTES</span></span>

## <span data-ttu-id="60502-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60502-160">RELATED LINKS</span></span>
