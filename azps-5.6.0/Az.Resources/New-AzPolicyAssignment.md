---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: d1e6b5b2b2e76c4ec807c27922f9ce577d94a7d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887966"
---
# <span data-ttu-id="957ea-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="957ea-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="957ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="957ea-102">SYNOPSIS</span></span>
<span data-ttu-id="957ea-103">Cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="957ea-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="957ea-104">SYNTAX</span></span>

### <span data-ttu-id="957ea-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="957ea-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="957ea-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="957ea-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="957ea-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="957ea-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="957ea-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="957ea-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="957ea-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="957ea-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="957ea-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="957ea-110">DESCRIPTION</span></span>
<span data-ttu-id="957ea-111">O cmdlet **New-AzPolicyAssignment** cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="957ea-112">Especifique uma política e escopo.</span><span class="sxs-lookup"><span data-stu-id="957ea-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="957ea-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="957ea-113">EXAMPLES</span></span>

### <span data-ttu-id="957ea-114">Exemplo 1: atribuição de política no nível de assinatura</span><span class="sxs-lookup"><span data-stu-id="957ea-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="957ea-115">O primeiro comando obtém uma assinatura chamada Subscription01 usando o cmdlet Get-AzSubscription e o armazena na variável $Subscription.</span><span class="sxs-lookup"><span data-stu-id="957ea-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="957ea-116">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e o armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="957ea-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="957ea-117">O comando final atribui a política em $Policy no nível da assinatura identificada pela cadeia de caracteres de escopo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="957ea-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="957ea-118">Exemplo 2: atribuição de política no nível do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="957ea-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="957ea-119">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="957ea-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="957ea-120">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e o armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="957ea-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="957ea-121">O comando final atribui a política em $Policy no nível do grupo de recursos identificado pela **propriedade ResourceId** de $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="957ea-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="957ea-122">Exemplo 3: atribuição de política no nível do grupo de recursos com o objeto de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="957ea-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="957ea-123">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="957ea-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="957ea-124">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="957ea-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="957ea-125">O segundo comando obtém a definição de política interna para locais permitidos usando o cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="957ea-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="957ea-126">O comando armazena esse objeto na $Policy variável.</span><span class="sxs-lookup"><span data-stu-id="957ea-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="957ea-127">O terceiro e quarto comandos criam um objeto que contém todas as regiões do Azure com "leste" no nome.</span><span class="sxs-lookup"><span data-stu-id="957ea-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="957ea-128">Os comandos armazenam esse objeto na $AllowedLocations variável.</span><span class="sxs-lookup"><span data-stu-id="957ea-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="957ea-129">O comando final atribui a política em $Policy no nível de um grupo de recursos usando o objeto parâmetro policy em $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="957ea-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="957ea-130">A **propriedade ResourceId** do $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="957ea-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="957ea-131">Exemplo 4: atribuição de política no nível do grupo de recursos com o arquivo de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="957ea-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="957ea-132">Crie um arquivo _chamadoAllowedLocations.jsno_ diretório de trabalho local com o seguinte conteúdo.</span><span class="sxs-lookup"><span data-stu-id="957ea-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="957ea-133">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="957ea-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="957ea-134">O segundo comando obtém a definição de política interna para locais permitidos usando o cmdlet Get-AzPolicyDefinition e o armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="957ea-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="957ea-135">O comando final atribui $Policy política no grupo de recursos identificado pela **propriedade ResourceId** do $ResourceGroup usando o arquivo de parâmetro de política AllowedLocations.jsno diretório de trabalho local.</span><span class="sxs-lookup"><span data-stu-id="957ea-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="957ea-136">Exemplo 5: atribuição de política com uma identidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="957ea-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="957ea-137">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="957ea-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="957ea-138">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e o armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="957ea-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="957ea-139">O comando final atribui a política em $Policy ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="957ea-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="957ea-140">Uma identidade gerenciada é criada e atribuída automaticamente à atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="957ea-141">Exemplo 6: atribuição de política com uma propriedade de modo de imposição</span><span class="sxs-lookup"><span data-stu-id="957ea-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="957ea-142">O primeiro comando obtém uma assinatura chamada Subscription01 usando o cmdlet Get-AzSubscription e o armazena na variável $Subscription.</span><span class="sxs-lookup"><span data-stu-id="957ea-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="957ea-143">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e o armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="957ea-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="957ea-144">O comando final atribui a política em $Policy no nível da assinatura identificada pela cadeia de caracteres de escopo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="957ea-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="957ea-145">A atribuição é definida com um valor EnforcementMode _de DoNotEnforce_ ou seja, o efeito da política não é imposto durante a criação ou atualização de recursos.</span><span class="sxs-lookup"><span data-stu-id="957ea-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="957ea-146">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="957ea-146">PARAMETERS</span></span>

### <span data-ttu-id="957ea-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="957ea-147">-ApiVersion</span></span>
<span data-ttu-id="957ea-148">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="957ea-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="957ea-149">Se você não especificar uma versão, este cmdlet usará a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="957ea-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="957ea-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="957ea-150">-AssignIdentity</span></span>
<span data-ttu-id="957ea-151">Gere e atribua uma Identidade do Azure Active Directory para essa atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="957ea-152">A identidade será usada ao executar implantações para políticas 'deployIfNotExists'.</span><span class="sxs-lookup"><span data-stu-id="957ea-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="957ea-153">O local é necessário ao atribuir uma identidade.</span><span class="sxs-lookup"><span data-stu-id="957ea-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="957ea-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957ea-154">-DefaultProfile</span></span>
<span data-ttu-id="957ea-155">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="957ea-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="957ea-156">-Description</span><span class="sxs-lookup"><span data-stu-id="957ea-156">-Description</span></span>
<span data-ttu-id="957ea-157">A descrição da atribuição de política</span><span class="sxs-lookup"><span data-stu-id="957ea-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="957ea-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="957ea-158">-DisplayName</span></span>
<span data-ttu-id="957ea-159">Especifica um nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="957ea-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="957ea-160">-EnforcementMode</span></span>
<span data-ttu-id="957ea-161">O modo de imposição para atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="957ea-162">Atualmente, os valores válidos são Default, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="957ea-162">Currently, valid values are Default, DoNotEnforce.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyAssignmentEnforcementMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, DoNotEnforce

Required: False
Position: Named
Default value: Default
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957ea-163">-Location</span><span class="sxs-lookup"><span data-stu-id="957ea-163">-Location</span></span>
<span data-ttu-id="957ea-164">O local da identidade de recurso da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="957ea-165">Isso é necessário quando a opção -AssignIdentity é usada.</span><span class="sxs-lookup"><span data-stu-id="957ea-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="957ea-166">-Metadados</span><span class="sxs-lookup"><span data-stu-id="957ea-166">-Metadata</span></span>
<span data-ttu-id="957ea-167">Os metadados da nova atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="957ea-168">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="957ea-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="957ea-169">-Name</span><span class="sxs-lookup"><span data-stu-id="957ea-169">-Name</span></span>
<span data-ttu-id="957ea-170">Especifica um nome para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-170">Specifies a name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957ea-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="957ea-171">-NotScope</span></span>
<span data-ttu-id="957ea-172">Os escopos não para atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-172">The not scopes for policy assignment.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957ea-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="957ea-173">-PolicyDefinition</span></span>
<span data-ttu-id="957ea-174">Especifica uma política, como um **objeto PsPolicyDefinition** que contém a regra de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957ea-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="957ea-175">-PolicyParameter</span></span>
<span data-ttu-id="957ea-176">O caminho do arquivo de parâmetro de política ou a cadeia de caracteres de parâmetro de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-176">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957ea-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="957ea-177">-PolicyParameterObject</span></span>
<span data-ttu-id="957ea-178">O objeto de parâmetro de política.</span><span class="sxs-lookup"><span data-stu-id="957ea-178">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="957ea-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="957ea-179">-PolicySetDefinition</span></span>
<span data-ttu-id="957ea-180">O objeto de definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="957ea-180">The policy set definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="957ea-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="957ea-181">-Pre</span></span>
<span data-ttu-id="957ea-182">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="957ea-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="957ea-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="957ea-183">-Scope</span></span>
<span data-ttu-id="957ea-184">Especifica o escopo no qual atribuir a política.</span><span class="sxs-lookup"><span data-stu-id="957ea-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="957ea-185">Por exemplo, para atribuir uma política a um grupo de recursos, especifique o seguinte: nome do grupo de recursos `/subscriptions/` de ID `/resourcegroups/` da assinatura</span><span class="sxs-lookup"><span data-stu-id="957ea-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="957ea-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957ea-186">CommonParameters</span></span>
<span data-ttu-id="957ea-187">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="957ea-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957ea-188">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="957ea-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957ea-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="957ea-189">INPUTS</span></span>

### <span data-ttu-id="957ea-190">System.String</span><span class="sxs-lookup"><span data-stu-id="957ea-190">System.String</span></span>

### <span data-ttu-id="957ea-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="957ea-191">System.String[]</span></span>

### <span data-ttu-id="957ea-192">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="957ea-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="957ea-193">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="957ea-193">OUTPUTS</span></span>

### <span data-ttu-id="957ea-194">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="957ea-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="957ea-195">NOTES</span><span class="sxs-lookup"><span data-stu-id="957ea-195">NOTES</span></span>

## <span data-ttu-id="957ea-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="957ea-196">RELATED LINKS</span></span>

[<span data-ttu-id="957ea-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="957ea-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="957ea-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="957ea-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="957ea-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="957ea-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="957ea-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="957ea-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


