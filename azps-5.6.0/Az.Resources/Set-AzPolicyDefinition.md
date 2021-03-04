---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: ee3f1ffdb7e95e3c00b30238bf6d35833d99cea6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893120"
---
# <span data-ttu-id="cc34d-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cc34d-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="cc34d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc34d-102">SYNOPSIS</span></span>
<span data-ttu-id="cc34d-103">Modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc34d-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="cc34d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cc34d-104">SYNTAX</span></span>

### <span data-ttu-id="cc34d-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cc34d-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc34d-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc34d-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc34d-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc34d-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc34d-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc34d-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc34d-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc34d-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc34d-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cc34d-110">DESCRIPTION</span></span>
<span data-ttu-id="cc34d-111">O cmdlet **Set-AzPolicyDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc34d-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="cc34d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc34d-112">EXAMPLES</span></span>

### <span data-ttu-id="cc34d-113">Exemplo 1: atualizar a descrição de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="cc34d-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="cc34d-114">O primeiro comando obtém uma definição de política chamada VMPolicyDefinition usando o cmdlet Get-AzPolicyDefinition de segurança.</span><span class="sxs-lookup"><span data-stu-id="cc34d-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="cc34d-115">O comando armazena esse objeto na $PolicyDefinition variável.</span><span class="sxs-lookup"><span data-stu-id="cc34d-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="cc34d-116">O segundo comando atualiza a descrição da definição de política identificada pela **propriedade ResourceId** do $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="cc34d-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="cc34d-117">Exemplo 2: atualizar o modo de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="cc34d-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="cc34d-118">Este comando atualiza a definição de política chamada VMPolicyDefinition usando o cmdlet Set-AzPolicyDefinition para definir sua propriedade mode como 'All'.</span><span class="sxs-lookup"><span data-stu-id="cc34d-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="cc34d-119">Exemplo 3: Atualizar os metadados de uma definição de política</span><span class="sxs-lookup"><span data-stu-id="cc34d-119">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="cc34d-120">Este comando atualiza os metadados de uma definição de política chamada VMPolicyDefinition para indicar que sua categoria é "Máquina Virtual".</span><span class="sxs-lookup"><span data-stu-id="cc34d-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="cc34d-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cc34d-121">PARAMETERS</span></span>

### <span data-ttu-id="cc34d-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cc34d-122">-ApiVersion</span></span>
<span data-ttu-id="cc34d-123">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="cc34d-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="cc34d-124">Se você não especificar uma versão, este cmdlet usará a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="cc34d-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="cc34d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc34d-125">-DefaultProfile</span></span>
<span data-ttu-id="cc34d-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="cc34d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc34d-127">-Description</span><span class="sxs-lookup"><span data-stu-id="cc34d-127">-Description</span></span>
<span data-ttu-id="cc34d-128">Especifica uma nova descrição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc34d-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="cc34d-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cc34d-129">-DisplayName</span></span>
<span data-ttu-id="cc34d-130">Especifica um novo nome de exibição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc34d-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="cc34d-131">-Id</span><span class="sxs-lookup"><span data-stu-id="cc34d-131">-Id</span></span>
<span data-ttu-id="cc34d-132">Especifica a ID de recurso totalmente qualificada para a definição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="cc34d-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cc34d-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc34d-133">-InputObject</span></span>
<span data-ttu-id="cc34d-134">O objeto de definição de política para atualizar que foi saída de outro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc34d-134">The policy definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="cc34d-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="cc34d-135">-ManagementGroupName</span></span>
<span data-ttu-id="cc34d-136">O nome do grupo de gerenciamento da definição de política a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="cc34d-136">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="cc34d-137">-Metadados</span><span class="sxs-lookup"><span data-stu-id="cc34d-137">-Metadata</span></span>
<span data-ttu-id="cc34d-138">Os metadados para definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc34d-138">The metadata for policy definition.</span></span> <span data-ttu-id="cc34d-139">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cc34d-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="cc34d-140">-Mode</span><span class="sxs-lookup"><span data-stu-id="cc34d-140">-Mode</span></span>
<span data-ttu-id="cc34d-141">O modo da nova definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc34d-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="cc34d-142">-Name</span><span class="sxs-lookup"><span data-stu-id="cc34d-142">-Name</span></span>
<span data-ttu-id="cc34d-143">Especifica o nome da definição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="cc34d-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cc34d-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="cc34d-144">-Parameter</span></span>
<span data-ttu-id="cc34d-145">A declaração de parâmetros para definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc34d-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="cc34d-146">Isso pode ser um caminho para um nome de arquivo ou uri contendo a declaração de parâmetros ou a declaração de parâmetros como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cc34d-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="cc34d-147">-Policy</span><span class="sxs-lookup"><span data-stu-id="cc34d-147">-Policy</span></span>
<span data-ttu-id="cc34d-148">Especifica a nova regra de política para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="cc34d-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="cc34d-149">Você pode especificar o caminho de um arquivo .json ou uma cadeia de caracteres que contém a política no formato JSON (Notação de Objeto JavaScript).</span><span class="sxs-lookup"><span data-stu-id="cc34d-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="cc34d-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="cc34d-150">-Pre</span></span>
<span data-ttu-id="cc34d-151">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="cc34d-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cc34d-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc34d-152">-SubscriptionId</span></span>
<span data-ttu-id="cc34d-153">A ID da assinatura da definição de política a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="cc34d-153">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="cc34d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc34d-154">CommonParameters</span></span>
<span data-ttu-id="cc34d-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc34d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc34d-156">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc34d-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc34d-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc34d-157">INPUTS</span></span>

### <span data-ttu-id="cc34d-158">System.String</span><span class="sxs-lookup"><span data-stu-id="cc34d-158">System.String</span></span>

### <span data-ttu-id="cc34d-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cc34d-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cc34d-160">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cc34d-160">OUTPUTS</span></span>

### <span data-ttu-id="cc34d-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="cc34d-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cc34d-162">NOTES</span><span class="sxs-lookup"><span data-stu-id="cc34d-162">NOTES</span></span>

## <span data-ttu-id="cc34d-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc34d-163">RELATED LINKS</span></span>

[<span data-ttu-id="cc34d-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cc34d-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="cc34d-165">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cc34d-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="cc34d-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cc34d-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


