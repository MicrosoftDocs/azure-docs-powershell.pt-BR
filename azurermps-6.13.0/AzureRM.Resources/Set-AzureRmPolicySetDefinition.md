---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d558e7104027e4c3fcef3b6e8d8427d5fd3802fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610240"
---
# <span data-ttu-id="4fc75-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="4fc75-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="4fc75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fc75-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc75-103">Modifica uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="4fc75-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fc75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fc75-104">SYNTAX</span></span>

### <span data-ttu-id="4fc75-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4fc75-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fc75-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc75-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fc75-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc75-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fc75-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fc75-108">IdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fc75-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4fc75-109">DESCRIPTION</span></span>
<span data-ttu-id="4fc75-110">O cmdlet **set-AzureRmPolicySetDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="4fc75-110">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="4fc75-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fc75-111">EXAMPLES</span></span>

### <span data-ttu-id="4fc75-112">Exemplo 1: atualizar a descrição de uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="4fc75-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="4fc75-113">O primeiro comando obtém uma definição de conjunto de políticas usando o cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="4fc75-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="4fc75-114">O comando armazena esse objeto na variável $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="4fc75-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="4fc75-115">O segundo comando atualiza a descrição da definição do conjunto de políticas identificada pela propriedade **ResourceId** de $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="4fc75-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="4fc75-116">OS</span><span class="sxs-lookup"><span data-stu-id="4fc75-116">PARAMETERS</span></span>

### <span data-ttu-id="4fc75-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4fc75-117">-ApiVersion</span></span>
<span data-ttu-id="4fc75-118">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4fc75-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4fc75-119">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="4fc75-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4fc75-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc75-120">-DefaultProfile</span></span>
<span data-ttu-id="4fc75-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4fc75-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fc75-122">-Descrição</span><span class="sxs-lookup"><span data-stu-id="4fc75-122">-Description</span></span>
<span data-ttu-id="4fc75-123">A descrição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="4fc75-123">The description for policy set definition.</span></span>

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

### <span data-ttu-id="4fc75-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4fc75-124">-DisplayName</span></span>
<span data-ttu-id="4fc75-125">O nome de exibição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="4fc75-125">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="4fc75-126">-ID</span><span class="sxs-lookup"><span data-stu-id="4fc75-126">-Id</span></span>
<span data-ttu-id="4fc75-127">A ID da definição da política totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="4fc75-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="4fc75-128">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="4fc75-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="4fc75-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4fc75-129">-ManagementGroupName</span></span>
<span data-ttu-id="4fc75-130">O nome do grupo de gerenciamento da definição do conjunto de políticas a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="4fc75-130">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="4fc75-131">-Metadados</span><span class="sxs-lookup"><span data-stu-id="4fc75-131">-Metadata</span></span>
<span data-ttu-id="4fc75-132">Os metadados da definição do conjunto de políticas atualizado.</span><span class="sxs-lookup"><span data-stu-id="4fc75-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="4fc75-133">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4fc75-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="4fc75-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fc75-134">-Name</span></span>
<span data-ttu-id="4fc75-135">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="4fc75-135">The policy set definition name.</span></span>

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

### <span data-ttu-id="4fc75-136">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="4fc75-136">-Parameter</span></span>
<span data-ttu-id="4fc75-137">A declaração Parameters da definição de conjunto de políticas atualizada.</span><span class="sxs-lookup"><span data-stu-id="4fc75-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="4fc75-138">Isso pode ser um caminho para um nome de arquivo ou URI que contém a declaração Parameters ou a declaração Parameters como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4fc75-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="4fc75-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4fc75-139">-PolicyDefinition</span></span>
<span data-ttu-id="4fc75-140">Definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="4fc75-140">The policy set definition.</span></span> <span data-ttu-id="4fc75-141">Pode ser um caminho para um nome de arquivo que contenha as definições da política ou a definição do conjunto de políticas como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4fc75-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="4fc75-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="4fc75-142">-Pre</span></span>
<span data-ttu-id="4fc75-143">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4fc75-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4fc75-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4fc75-144">-SubscriptionId</span></span>
<span data-ttu-id="4fc75-145">A ID da assinatura da definição do conjunto de políticas a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="4fc75-145">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="4fc75-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4fc75-146">-Confirm</span></span>
<span data-ttu-id="4fc75-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fc75-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fc75-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc75-148">-WhatIf</span></span>
<span data-ttu-id="4fc75-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4fc75-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fc75-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4fc75-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fc75-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc75-151">CommonParameters</span></span>
<span data-ttu-id="4fc75-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc75-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc75-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc75-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc75-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4fc75-154">INPUTS</span></span>

### <span data-ttu-id="4fc75-155">System. String</span><span class="sxs-lookup"><span data-stu-id="4fc75-155">System.String</span></span>

### <span data-ttu-id="4fc75-156">System. Nullable ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4fc75-156">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4fc75-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4fc75-157">OUTPUTS</span></span>

### <span data-ttu-id="4fc75-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4fc75-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4fc75-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4fc75-159">NOTES</span></span>

## <span data-ttu-id="4fc75-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fc75-160">RELATED LINKS</span></span>
