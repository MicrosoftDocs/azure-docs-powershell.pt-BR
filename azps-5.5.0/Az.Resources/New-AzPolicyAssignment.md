---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 63efc580cf47274363f04750dc6a3f8da93b6665
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118749"
---
# <span data-ttu-id="c31f7-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c31f7-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="c31f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c31f7-102">SYNOPSIS</span></span>
<span data-ttu-id="c31f7-103">Cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="c31f7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c31f7-104">SYNTAX</span></span>

### <span data-ttu-id="c31f7-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c31f7-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31f7-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c31f7-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31f7-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c31f7-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31f7-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c31f7-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31f7-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c31f7-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c31f7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c31f7-110">DESCRIPTION</span></span>
<span data-ttu-id="c31f7-111">O **cmdlet New-AzPolicyAssignment** cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="c31f7-112">Especifique uma política e um escopo.</span><span class="sxs-lookup"><span data-stu-id="c31f7-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="c31f7-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c31f7-113">EXAMPLES</span></span>

### <span data-ttu-id="c31f7-114">Exemplo 1: Atribuição de política no nível da assinatura</span><span class="sxs-lookup"><span data-stu-id="c31f7-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="c31f7-115">O primeiro comando obtém uma assinatura chamada Subscription01 usando o cmdlet Get-AzSubscription e o armazena na variável $Subscription usuário.</span><span class="sxs-lookup"><span data-stu-id="c31f7-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="c31f7-116">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e armazena-o na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="c31f7-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c31f7-117">O comando final atribui a política em $Policy no nível da assinatura identificada pela cadeia de escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="c31f7-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="c31f7-118">Exemplo 2: Atribuição de política no nível de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c31f7-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="c31f7-119">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup dados.</span><span class="sxs-lookup"><span data-stu-id="c31f7-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c31f7-120">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e armazena-o na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="c31f7-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c31f7-121">O comando final atribui a política $Policy no nível do grupo de recursos identificado pela propriedade **ResourceId** do $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c31f7-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="c31f7-122">Exemplo 3: Atribuição de política no nível de grupo de recursos com objeto de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="c31f7-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="c31f7-123">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c31f7-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c31f7-124">O comando armazena esse objeto na variável $ResourceGroup dados.</span><span class="sxs-lookup"><span data-stu-id="c31f7-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c31f7-125">O segundo comando obtém a definição de política interna para locais permitidos usando Get-AzPolicyDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c31f7-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="c31f7-126">O comando armazena esse objeto na variável $Policy dados.</span><span class="sxs-lookup"><span data-stu-id="c31f7-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="c31f7-127">O terceiro e o quarto comandos criam um objeto que contém todas as regiões do Azure com "leste" no nome.</span><span class="sxs-lookup"><span data-stu-id="c31f7-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="c31f7-128">Os comandos armazenam esse objeto na variável $AllowedLocations dados.</span><span class="sxs-lookup"><span data-stu-id="c31f7-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="c31f7-129">O comando final atribui a política em $Policy no nível de um grupo de recursos usando o objeto de parâmetro de política no $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="c31f7-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="c31f7-130">A **propriedade ResourceId** da $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c31f7-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="c31f7-131">Exemplo 4: Atribuição de política no nível de grupo de recursos com arquivo de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="c31f7-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="c31f7-132">Crie um arquivo chamado _AllowedLocations.jsno_ diretório de trabalho local com o conteúdo a seguir.</span><span class="sxs-lookup"><span data-stu-id="c31f7-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="c31f7-133">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup dados.</span><span class="sxs-lookup"><span data-stu-id="c31f7-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c31f7-134">O segundo comando obtém a definição de política interna para locais permitidos usando o cmdlet Get-AzPolicyDefinition e armazena-o na variável $Policy dados.</span><span class="sxs-lookup"><span data-stu-id="c31f7-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c31f7-135">O comando final atribui a política no $Policy no grupo de recursos identificado pela propriedade **ResourceId** do $ResourceGroup usando o arquivo de parâmetro de política AllowedLocations.jsno diretório de trabalho local.</span><span class="sxs-lookup"><span data-stu-id="c31f7-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="c31f7-136">Exemplo 5: Atribuição de política com uma identidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="c31f7-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="c31f7-137">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup dados.</span><span class="sxs-lookup"><span data-stu-id="c31f7-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="c31f7-138">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e armazena-o na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="c31f7-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c31f7-139">O comando final atribui a política em $Policy ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c31f7-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="c31f7-140">Uma identidade gerenciada é criada automaticamente e atribuída à atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="c31f7-141">Exemplo 6: Atribuição de política com uma propriedade de modo de imposição</span><span class="sxs-lookup"><span data-stu-id="c31f7-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="c31f7-142">O primeiro comando obtém uma assinatura chamada Subscription01 usando o cmdlet Get-AzSubscription e o armazena na variável $Subscription usuário.</span><span class="sxs-lookup"><span data-stu-id="c31f7-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="c31f7-143">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e armazena-o na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="c31f7-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="c31f7-144">O comando final atribui a política em $Policy no nível da assinatura identificada pela cadeia de escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="c31f7-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="c31f7-145">A atribuição é definida com um valor EnforcementMode _do DoNotEnforce_ ou seja, o efeito de política não é imposto durante a criação ou atualização de recursos.</span><span class="sxs-lookup"><span data-stu-id="c31f7-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="c31f7-146">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c31f7-146">PARAMETERS</span></span>

### <span data-ttu-id="c31f7-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c31f7-147">-ApiVersion</span></span>
<span data-ttu-id="c31f7-148">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c31f7-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c31f7-149">Se você não especificar uma versão, este cmdlet usará a versão disponível mais recente.</span><span class="sxs-lookup"><span data-stu-id="c31f7-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c31f7-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c31f7-150">-AssignIdentity</span></span>
<span data-ttu-id="c31f7-151">Gere e atribua uma Identidade do Azure Active Directory para essa atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="c31f7-152">A identidade será usada durante a execução de implantações para políticas "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="c31f7-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="c31f7-153">O local é necessário ao atribuir uma identidade.</span><span class="sxs-lookup"><span data-stu-id="c31f7-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="c31f7-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c31f7-154">-DefaultProfile</span></span>
<span data-ttu-id="c31f7-155">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c31f7-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c31f7-156">-Descrição</span><span class="sxs-lookup"><span data-stu-id="c31f7-156">-Description</span></span>
<span data-ttu-id="c31f7-157">A descrição da atribuição de política</span><span class="sxs-lookup"><span data-stu-id="c31f7-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="c31f7-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c31f7-158">-DisplayName</span></span>
<span data-ttu-id="c31f7-159">Especifica um nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="c31f7-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="c31f7-160">-EnforcementMode</span></span>
<span data-ttu-id="c31f7-161">O modo de imposição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="c31f7-162">Atualmente, os valores válidos são Padrão, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="c31f7-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="c31f7-163">-Local</span><span class="sxs-lookup"><span data-stu-id="c31f7-163">-Location</span></span>
<span data-ttu-id="c31f7-164">O local da identidade de recurso da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="c31f7-165">Isso é necessário quando a opção -AssignIdentity é usada.</span><span class="sxs-lookup"><span data-stu-id="c31f7-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="c31f7-166">-Metadados</span><span class="sxs-lookup"><span data-stu-id="c31f7-166">-Metadata</span></span>
<span data-ttu-id="c31f7-167">Os metadados da nova atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="c31f7-168">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c31f7-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="c31f7-169">-Nome</span><span class="sxs-lookup"><span data-stu-id="c31f7-169">-Name</span></span>
<span data-ttu-id="c31f7-170">Especifica um nome para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="c31f7-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="c31f7-171">-NotScope</span></span>
<span data-ttu-id="c31f7-172">Os escopos não para atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="c31f7-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c31f7-173">-PolicyDefinition</span></span>
<span data-ttu-id="c31f7-174">Especifica uma política, como um **objeto PsPolicyDefinition** que contém a regra de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="c31f7-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="c31f7-175">-PolicyParameter</span></span>
<span data-ttu-id="c31f7-176">O caminho do arquivo de parâmetro de política ou a cadeia de parâmetros de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="c31f7-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="c31f7-177">-PolicyParameterObject</span></span>
<span data-ttu-id="c31f7-178">O objeto de parâmetro de política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="c31f7-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c31f7-179">-PolicySetDefinition</span></span>
<span data-ttu-id="c31f7-180">O objeto de definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="c31f7-180">The policy set definition object.</span></span>

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

### <span data-ttu-id="c31f7-181">-Pré-</span><span class="sxs-lookup"><span data-stu-id="c31f7-181">-Pre</span></span>
<span data-ttu-id="c31f7-182">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="c31f7-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c31f7-183">-Escopo</span><span class="sxs-lookup"><span data-stu-id="c31f7-183">-Scope</span></span>
<span data-ttu-id="c31f7-184">Especifica o escopo ao qual atribuir a política.</span><span class="sxs-lookup"><span data-stu-id="c31f7-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="c31f7-185">Por exemplo, para atribuir uma política a um grupo de recursos, especifique o seguinte: nome do grupo de recursos `/subscriptions/` de ID `/resourcegroups/` de assinatura</span><span class="sxs-lookup"><span data-stu-id="c31f7-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="c31f7-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c31f7-186">CommonParameters</span></span>
<span data-ttu-id="c31f7-187">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c31f7-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c31f7-188">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c31f7-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c31f7-189">Entradas</span><span class="sxs-lookup"><span data-stu-id="c31f7-189">INPUTS</span></span>

### <span data-ttu-id="c31f7-190">System.String</span><span class="sxs-lookup"><span data-stu-id="c31f7-190">System.String</span></span>

### <span data-ttu-id="c31f7-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c31f7-191">System.String[]</span></span>

### <span data-ttu-id="c31f7-192">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c31f7-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c31f7-193">Saídas</span><span class="sxs-lookup"><span data-stu-id="c31f7-193">OUTPUTS</span></span>

### <span data-ttu-id="c31f7-194">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c31f7-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c31f7-195">Notas</span><span class="sxs-lookup"><span data-stu-id="c31f7-195">NOTES</span></span>

## <span data-ttu-id="c31f7-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c31f7-196">RELATED LINKS</span></span>

[<span data-ttu-id="c31f7-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c31f7-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="c31f7-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c31f7-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="c31f7-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c31f7-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="c31f7-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c31f7-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


