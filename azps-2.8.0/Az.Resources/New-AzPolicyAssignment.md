---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: bec39b242de14da944496a4371fa661d95ce9c59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773344"
---
# <span data-ttu-id="7227d-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7227d-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="7227d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7227d-102">SYNOPSIS</span></span>
<span data-ttu-id="7227d-103">Cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7227d-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="7227d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7227d-104">SYNTAX</span></span>

### <span data-ttu-id="7227d-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7227d-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7227d-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7227d-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7227d-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7227d-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7227d-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7227d-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7227d-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7227d-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7227d-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7227d-110">DESCRIPTION</span></span>
<span data-ttu-id="7227d-111">O cmdlet **New-AzPolicyAssignment** cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7227d-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="7227d-112">Especifique uma política e um escopo.</span><span class="sxs-lookup"><span data-stu-id="7227d-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="7227d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7227d-113">EXAMPLES</span></span>

### <span data-ttu-id="7227d-114">Exemplo 1: atribuição de política no nível de assinatura</span><span class="sxs-lookup"><span data-stu-id="7227d-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="7227d-115">O primeiro comando obtém uma assinatura chamada Subscription01 usando o cmdlet Get-AzSubscription e a armazena na variável $Subscription.</span><span class="sxs-lookup"><span data-stu-id="7227d-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="7227d-116">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e a armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="7227d-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7227d-117">O comando final atribui a política em $Policy no nível da assinatura identificada pela cadeia de caracteres de escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7227d-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="7227d-118">Exemplo 2: atribuição de política em nível de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7227d-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="7227d-119">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7227d-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7227d-120">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e a armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="7227d-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7227d-121">O comando final atribui a política em $Policy no nível do grupo de recursos identificado pela propriedade **ResourceId** de $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7227d-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="7227d-122">Exemplo 3: atribuição de política no nível de grupo de recursos com objeto de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="7227d-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="7227d-123">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7227d-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="7227d-124">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7227d-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7227d-125">O segundo comando obtém a definição de política interna para locais permitidos usando o cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7227d-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="7227d-126">O comando armazena esse objeto na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="7227d-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="7227d-127">O terceiro e o quarto comandos criam um objeto que contém todas as regiões do Azure com "East" no nome.</span><span class="sxs-lookup"><span data-stu-id="7227d-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="7227d-128">Os comandos armazenam esse objeto na variável $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="7227d-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="7227d-129">O comando final atribui a política em $Policy no nível de um grupo de recursos usando o objeto Parameter da política em $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="7227d-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="7227d-130">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7227d-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="7227d-131">Exemplo 4: atribuição de política em nível de grupo de recursos com arquivo de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="7227d-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="7227d-132">Crie um arquivo chamado _AllowedLocations.jsno_ diretório de trabalho local com o conteúdo a seguir.</span><span class="sxs-lookup"><span data-stu-id="7227d-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="7227d-133">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7227d-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7227d-134">O segundo comando obtém a definição de política interna para locais permitidos usando o cmdlet Get-AzPolicyDefinition e armazena-o na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="7227d-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7227d-135">O comando final atribui a política em $Policy no grupo de recursos identificado pela propriedade **ResourceId** de $ResourceGroup usando o arquivo de parâmetro de política AllowedLocations.jsno diretório de trabalho local.</span><span class="sxs-lookup"><span data-stu-id="7227d-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="7227d-136">Exemplo 5: atribuição de política com uma identidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="7227d-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="7227d-137">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7227d-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7227d-138">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e a armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="7227d-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="7227d-139">O comando final atribui a política em $Policy ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7227d-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="7227d-140">Uma identidade gerenciada é criada automaticamente e atribuída à atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7227d-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="7227d-141">OS</span><span class="sxs-lookup"><span data-stu-id="7227d-141">PARAMETERS</span></span>

### <span data-ttu-id="7227d-142">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7227d-142">-ApiVersion</span></span>
<span data-ttu-id="7227d-143">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="7227d-143">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7227d-144">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="7227d-144">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7227d-145">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7227d-145">-AssignIdentity</span></span>
<span data-ttu-id="7227d-146">Gerar e atribuir uma identidade do Azure Active Directory para esta atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7227d-146">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="7227d-147">A identidade será usada ao executar implantações para políticas de "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="7227d-147">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="7227d-148">A localização é necessária ao atribuir uma identidade.</span><span class="sxs-lookup"><span data-stu-id="7227d-148">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="7227d-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7227d-149">-DefaultProfile</span></span>
<span data-ttu-id="7227d-150">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7227d-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7227d-151">-Descrição</span><span class="sxs-lookup"><span data-stu-id="7227d-151">-Description</span></span>
<span data-ttu-id="7227d-152">A descrição da atribuição de política</span><span class="sxs-lookup"><span data-stu-id="7227d-152">The description for policy assignment</span></span>

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

### <span data-ttu-id="7227d-153">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7227d-153">-DisplayName</span></span>
<span data-ttu-id="7227d-154">Especifica um nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7227d-154">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="7227d-155">-Local</span><span class="sxs-lookup"><span data-stu-id="7227d-155">-Location</span></span>
<span data-ttu-id="7227d-156">O local da identidade do recurso da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7227d-156">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="7227d-157">Isso é necessário quando a opção-AssignIdentity é usada.</span><span class="sxs-lookup"><span data-stu-id="7227d-157">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="7227d-158">-Metadados</span><span class="sxs-lookup"><span data-stu-id="7227d-158">-Metadata</span></span>
<span data-ttu-id="7227d-159">Os metadados da nova atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7227d-159">The metadata for the new policy assignment.</span></span> <span data-ttu-id="7227d-160">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7227d-160">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="7227d-161">-Nome</span><span class="sxs-lookup"><span data-stu-id="7227d-161">-Name</span></span>
<span data-ttu-id="7227d-162">Especifica um nome para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7227d-162">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="7227d-163">-Não-escopo</span><span class="sxs-lookup"><span data-stu-id="7227d-163">-NotScope</span></span>
<span data-ttu-id="7227d-164">Os não escopos para atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7227d-164">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="7227d-165">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7227d-165">-PolicyDefinition</span></span>
<span data-ttu-id="7227d-166">Especifica uma política, como um objeto **PsPolicyDefinition** que contém a regra de política.</span><span class="sxs-lookup"><span data-stu-id="7227d-166">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="7227d-167">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="7227d-167">-PolicyParameter</span></span>
<span data-ttu-id="7227d-168">O caminho do arquivo de parâmetro da política ou a cadeia de caracteres de parâmetro da política.</span><span class="sxs-lookup"><span data-stu-id="7227d-168">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="7227d-169">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="7227d-169">-PolicyParameterObject</span></span>
<span data-ttu-id="7227d-170">O objeto de parâmetro de política.</span><span class="sxs-lookup"><span data-stu-id="7227d-170">The policy parameter object.</span></span>

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

### <span data-ttu-id="7227d-171">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="7227d-171">-PolicySetDefinition</span></span>
<span data-ttu-id="7227d-172">O objeto de definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="7227d-172">The policy set definition object.</span></span>

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

### <span data-ttu-id="7227d-173">-Pre</span><span class="sxs-lookup"><span data-stu-id="7227d-173">-Pre</span></span>
<span data-ttu-id="7227d-174">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="7227d-174">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7227d-175">-Escopo</span><span class="sxs-lookup"><span data-stu-id="7227d-175">-Scope</span></span>
<span data-ttu-id="7227d-176">Especifica o escopo no qual atribuir a política.</span><span class="sxs-lookup"><span data-stu-id="7227d-176">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="7227d-177">Por exemplo, para atribuir uma política a um grupo de recursos, especifique o seguinte: `/subscriptions/` nome do grupo de recursos de ID de assinatura `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="7227d-177">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="7227d-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7227d-178">CommonParameters</span></span>
<span data-ttu-id="7227d-179">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7227d-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7227d-180">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7227d-180">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7227d-181">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7227d-181">INPUTS</span></span>

### <span data-ttu-id="7227d-182">System. String</span><span class="sxs-lookup"><span data-stu-id="7227d-182">System.String</span></span>

### <span data-ttu-id="7227d-183">System. String []</span><span class="sxs-lookup"><span data-stu-id="7227d-183">System.String[]</span></span>

### <span data-ttu-id="7227d-184">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7227d-184">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7227d-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7227d-185">OUTPUTS</span></span>

### <span data-ttu-id="7227d-186">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7227d-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7227d-187">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7227d-187">NOTES</span></span>

## <span data-ttu-id="7227d-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7227d-188">RELATED LINKS</span></span>

[<span data-ttu-id="7227d-189">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7227d-189">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="7227d-190">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7227d-190">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="7227d-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7227d-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="7227d-192">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7227d-192">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


