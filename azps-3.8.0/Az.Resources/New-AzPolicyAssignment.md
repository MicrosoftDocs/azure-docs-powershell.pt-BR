---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 2ae25ea7679655c4bc10f8eea714cba851bc8c9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778048"
---
# <span data-ttu-id="7301e-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7301e-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="7301e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7301e-102">SYNOPSIS</span></span>
<span data-ttu-id="7301e-103">Cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7301e-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="7301e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7301e-104">SYNTAX</span></span>

### <span data-ttu-id="7301e-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7301e-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7301e-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7301e-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7301e-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7301e-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7301e-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7301e-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7301e-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7301e-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7301e-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7301e-110">DESCRIPTION</span></span>
<span data-ttu-id="7301e-111">O cmdlet **New-AzPolicyAssignment** cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7301e-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="7301e-112">Especifique uma política e um escopo.</span><span class="sxs-lookup"><span data-stu-id="7301e-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="7301e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7301e-113">EXAMPLES</span></span>

### <span data-ttu-id="7301e-114">Exemplo 1: atribuição de política no nível de assinatura</span><span class="sxs-lookup"><span data-stu-id="7301e-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="7301e-115">O primeiro comando obtém uma assinatura chamada Subscription01 usando o cmdlet Get-AzSubscription e a armazena na variável $Subscription.</span><span class="sxs-lookup"><span data-stu-id="7301e-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="7301e-116">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e a armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="7301e-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7301e-117">O comando final atribui a política em $Policy no nível da assinatura identificada pela cadeia de caracteres de escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7301e-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="7301e-118">Exemplo 2: atribuição de política em nível de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7301e-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="7301e-119">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7301e-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7301e-120">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e a armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="7301e-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7301e-121">O comando final atribui a política em $Policy no nível do grupo de recursos identificado pela propriedade **ResourceId** de $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7301e-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="7301e-122">Exemplo 3: atribuição de política no nível de grupo de recursos com objeto de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="7301e-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="7301e-123">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7301e-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="7301e-124">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7301e-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7301e-125">O segundo comando obtém a definição de política interna para locais permitidos usando o cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7301e-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="7301e-126">O comando armazena esse objeto na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="7301e-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="7301e-127">O terceiro e o quarto comandos criam um objeto que contém todas as regiões do Azure com "East" no nome.</span><span class="sxs-lookup"><span data-stu-id="7301e-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="7301e-128">Os comandos armazenam esse objeto na variável $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="7301e-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="7301e-129">O comando final atribui a política em $Policy no nível de um grupo de recursos usando o objeto Parameter da política em $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="7301e-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="7301e-130">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7301e-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="7301e-131">Exemplo 4: atribuição de política em nível de grupo de recursos com arquivo de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="7301e-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="7301e-132">Crie um arquivo chamado _AllowedLocations.jsno_ diretório de trabalho local com o conteúdo a seguir.</span><span class="sxs-lookup"><span data-stu-id="7301e-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="7301e-133">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7301e-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7301e-134">O segundo comando obtém a definição de política interna para locais permitidos usando o cmdlet Get-AzPolicyDefinition e armazena-o na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="7301e-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7301e-135">O comando final atribui a política em $Policy no grupo de recursos identificado pela propriedade **ResourceId** de $ResourceGroup usando o arquivo de parâmetro de política AllowedLocations.jsno diretório de trabalho local.</span><span class="sxs-lookup"><span data-stu-id="7301e-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="7301e-136">Exemplo 5: atribuição de política com uma identidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="7301e-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="7301e-137">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7301e-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7301e-138">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e a armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="7301e-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7301e-139">O comando final atribui a política em $Policy ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7301e-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="7301e-140">Uma identidade gerenciada é criada automaticamente e atribuída à atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7301e-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="7301e-141">Exemplo 6: atribuição de política com uma propriedade do modo de imposição</span><span class="sxs-lookup"><span data-stu-id="7301e-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="7301e-142">O primeiro comando obtém uma assinatura chamada Subscription01 usando o cmdlet Get-AzSubscription e a armazena na variável $Subscription.</span><span class="sxs-lookup"><span data-stu-id="7301e-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="7301e-143">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e a armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="7301e-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7301e-144">O comando final atribui a política em $Policy no nível da assinatura identificada pela cadeia de caracteres de escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7301e-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="7301e-145">A atribuição é definida com um valor de imposiçãomode de _DoNotEnforce_ , ou seja, o efeito de política não é imposto durante a criação ou atualização de recursos.</span><span class="sxs-lookup"><span data-stu-id="7301e-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="7301e-146">OS</span><span class="sxs-lookup"><span data-stu-id="7301e-146">PARAMETERS</span></span>

### <span data-ttu-id="7301e-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7301e-147">-ApiVersion</span></span>
<span data-ttu-id="7301e-148">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="7301e-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7301e-149">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="7301e-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7301e-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7301e-150">-AssignIdentity</span></span>
<span data-ttu-id="7301e-151">Gerar e atribuir uma identidade do Azure Active Directory para esta atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7301e-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="7301e-152">A identidade será usada ao executar implantações para políticas de "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="7301e-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="7301e-153">A localização é necessária ao atribuir uma identidade.</span><span class="sxs-lookup"><span data-stu-id="7301e-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="7301e-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7301e-154">-DefaultProfile</span></span>
<span data-ttu-id="7301e-155">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7301e-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7301e-156">-Descrição</span><span class="sxs-lookup"><span data-stu-id="7301e-156">-Description</span></span>
<span data-ttu-id="7301e-157">A descrição da atribuição de política</span><span class="sxs-lookup"><span data-stu-id="7301e-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="7301e-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7301e-158">-DisplayName</span></span>
<span data-ttu-id="7301e-159">Especifica um nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7301e-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="7301e-160">-Imposiçãomode</span><span class="sxs-lookup"><span data-stu-id="7301e-160">-EnforcementMode</span></span>
<span data-ttu-id="7301e-161">O modo de imposição para atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7301e-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="7301e-162">Atualmente, os valores válidos são padrão, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="7301e-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="7301e-163">-Local</span><span class="sxs-lookup"><span data-stu-id="7301e-163">-Location</span></span>
<span data-ttu-id="7301e-164">O local da identidade do recurso da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7301e-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="7301e-165">Isso é necessário quando a opção-AssignIdentity é usada.</span><span class="sxs-lookup"><span data-stu-id="7301e-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="7301e-166">-Metadados</span><span class="sxs-lookup"><span data-stu-id="7301e-166">-Metadata</span></span>
<span data-ttu-id="7301e-167">Os metadados da nova atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7301e-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="7301e-168">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7301e-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="7301e-169">-Nome</span><span class="sxs-lookup"><span data-stu-id="7301e-169">-Name</span></span>
<span data-ttu-id="7301e-170">Especifica um nome para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7301e-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="7301e-171">-Não-escopo</span><span class="sxs-lookup"><span data-stu-id="7301e-171">-NotScope</span></span>
<span data-ttu-id="7301e-172">Os não escopos para atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7301e-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="7301e-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7301e-173">-PolicyDefinition</span></span>
<span data-ttu-id="7301e-174">Especifica uma política, como um objeto **PsPolicyDefinition** que contém a regra de política.</span><span class="sxs-lookup"><span data-stu-id="7301e-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7301e-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="7301e-175">-PolicyParameter</span></span>
<span data-ttu-id="7301e-176">O caminho do arquivo de parâmetro da política ou a cadeia de caracteres de parâmetro da política.</span><span class="sxs-lookup"><span data-stu-id="7301e-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="7301e-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="7301e-177">-PolicyParameterObject</span></span>
<span data-ttu-id="7301e-178">O objeto de parâmetro de política.</span><span class="sxs-lookup"><span data-stu-id="7301e-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="7301e-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="7301e-179">-PolicySetDefinition</span></span>
<span data-ttu-id="7301e-180">O objeto de definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="7301e-180">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7301e-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="7301e-181">-Pre</span></span>
<span data-ttu-id="7301e-182">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="7301e-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7301e-183">-Escopo</span><span class="sxs-lookup"><span data-stu-id="7301e-183">-Scope</span></span>
<span data-ttu-id="7301e-184">Especifica o escopo no qual atribuir a política.</span><span class="sxs-lookup"><span data-stu-id="7301e-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="7301e-185">Por exemplo, para atribuir uma política a um grupo de recursos, especifique o seguinte: `/subscriptions/` nome do grupo de recursos de ID de assinatura `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="7301e-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="7301e-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7301e-186">CommonParameters</span></span>
<span data-ttu-id="7301e-187">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7301e-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7301e-188">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7301e-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7301e-189">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7301e-189">INPUTS</span></span>

### <span data-ttu-id="7301e-190">System. String</span><span class="sxs-lookup"><span data-stu-id="7301e-190">System.String</span></span>

### <span data-ttu-id="7301e-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="7301e-191">System.String[]</span></span>

### <span data-ttu-id="7301e-192">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7301e-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7301e-193">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7301e-193">OUTPUTS</span></span>

### <span data-ttu-id="7301e-194">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7301e-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7301e-195">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7301e-195">NOTES</span></span>

## <span data-ttu-id="7301e-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7301e-196">RELATED LINKS</span></span>

[<span data-ttu-id="7301e-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7301e-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="7301e-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7301e-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="7301e-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7301e-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="7301e-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7301e-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


