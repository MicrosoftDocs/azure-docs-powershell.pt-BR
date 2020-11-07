---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 1b8a7bd3d0c9f73b551cf6eefcb2564918fde1fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776395"
---
# <span data-ttu-id="13782-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="13782-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="13782-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13782-102">SYNOPSIS</span></span>
<span data-ttu-id="13782-103">Cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="13782-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="13782-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13782-104">SYNTAX</span></span>

### <span data-ttu-id="13782-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="13782-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="13782-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13782-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="13782-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="13782-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="13782-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13782-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="13782-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="13782-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="13782-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13782-110">DESCRIPTION</span></span>
<span data-ttu-id="13782-111">O cmdlet **New-AzPolicyAssignment** cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="13782-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="13782-112">Especifique uma política e um escopo.</span><span class="sxs-lookup"><span data-stu-id="13782-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="13782-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13782-113">EXAMPLES</span></span>

### <span data-ttu-id="13782-114">Exemplo 1: atribuição de política em nível de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="13782-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="13782-115">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="13782-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="13782-116">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e a armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="13782-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="13782-117">O comando final atribui a política em $Policy no nível do grupo de recursos identificado pela propriedade **ResourceId** de $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="13782-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="13782-118">Exemplo 2: atribuição de política em nível de grupo de recursos com objeto de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="13782-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="13782-119">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="13782-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="13782-120">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="13782-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="13782-121">O segundo comando obtém a definição de política interna para locais permitidos usando o cmdlet Get-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="13782-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="13782-122">O comando armazena esse objeto na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="13782-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="13782-123">O terceiro e o quarto comandos criam um objeto que contém todas as regiões do Azure com "East" no nome.</span><span class="sxs-lookup"><span data-stu-id="13782-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="13782-124">Os comandos armazenam esse objeto na variável $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="13782-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="13782-125">O comando final atribui a política em $Policy no nível de um grupo de recursos usando o objeto Parameter da política em $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="13782-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="13782-126">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13782-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="13782-127">Exemplo 3: atribuição de política em nível de grupo de recursos com arquivo de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="13782-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="13782-128">Crie um arquivo chamado _AllowedLocations.jsno_ diretório de trabalho local com o conteúdo a seguir.</span><span class="sxs-lookup"><span data-stu-id="13782-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="13782-129">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="13782-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="13782-130">O segundo comando obtém a definição de política interna para locais permitidos usando o cmdlet Get-AzPolicyDefinition e armazena-o na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="13782-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="13782-131">O comando final atribui a política em $Policy no grupo de recursos identificado pela propriedade **ResourceId** de $ResourceGroup usando o arquivo de parâmetro de política AllowedLocations.jsno diretório de trabalho local.</span><span class="sxs-lookup"><span data-stu-id="13782-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="13782-132">Exemplo 4: atribuição de política com uma identidade gerenciada</span><span class="sxs-lookup"><span data-stu-id="13782-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

<span data-ttu-id="13782-133">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup e o armazena na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="13782-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="13782-134">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzPolicyDefinition e a armazena na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="13782-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="13782-135">O comando final atribui a política em $Policy ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13782-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="13782-136">Uma identidade gerenciada é criada automaticamente e atribuída à atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="13782-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="13782-137">OS</span><span class="sxs-lookup"><span data-stu-id="13782-137">PARAMETERS</span></span>

### <span data-ttu-id="13782-138">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="13782-138">-ApiVersion</span></span>
<span data-ttu-id="13782-139">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="13782-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="13782-140">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="13782-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="13782-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="13782-141">-AssignIdentity</span></span>
<span data-ttu-id="13782-142">Gerar e atribuir uma identidade do Azure Active Directory para esta atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="13782-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="13782-143">A identidade será usada ao executar implantações para políticas de "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="13782-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="13782-144">A localização é necessária ao atribuir uma identidade.</span><span class="sxs-lookup"><span data-stu-id="13782-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="13782-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13782-145">-DefaultProfile</span></span>
<span data-ttu-id="13782-146">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="13782-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13782-147">-Descrição</span><span class="sxs-lookup"><span data-stu-id="13782-147">-Description</span></span>
<span data-ttu-id="13782-148">A descrição da atribuição de política</span><span class="sxs-lookup"><span data-stu-id="13782-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="13782-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="13782-149">-DisplayName</span></span>
<span data-ttu-id="13782-150">Especifica um nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="13782-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="13782-151">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="13782-151">-InformationAction</span></span>
<span data-ttu-id="13782-152">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="13782-152">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="13782-153">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="13782-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="13782-154">Contínuo</span><span class="sxs-lookup"><span data-stu-id="13782-154">Continue</span></span>
- <span data-ttu-id="13782-155">Ignorar</span><span class="sxs-lookup"><span data-stu-id="13782-155">Ignore</span></span>
- <span data-ttu-id="13782-156">Inquire</span><span class="sxs-lookup"><span data-stu-id="13782-156">Inquire</span></span>
- <span data-ttu-id="13782-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="13782-157">SilentlyContinue</span></span>
- <span data-ttu-id="13782-158">Finaliza</span><span class="sxs-lookup"><span data-stu-id="13782-158">Stop</span></span>
- <span data-ttu-id="13782-159">Suspensão</span><span class="sxs-lookup"><span data-stu-id="13782-159">Suspend</span></span>

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

### <span data-ttu-id="13782-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="13782-160">-InformationVariable</span></span>
<span data-ttu-id="13782-161">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="13782-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="13782-162">-Local</span><span class="sxs-lookup"><span data-stu-id="13782-162">-Location</span></span>
<span data-ttu-id="13782-163">O local da identidade do recurso da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="13782-163">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="13782-164">Isso é necessário quando a opção-AssignIdentity é usada.</span><span class="sxs-lookup"><span data-stu-id="13782-164">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="13782-165">-Metadados</span><span class="sxs-lookup"><span data-stu-id="13782-165">-Metadata</span></span>
<span data-ttu-id="13782-166">Os metadados da nova atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="13782-166">The metadata for the new policy assignment.</span></span> <span data-ttu-id="13782-167">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="13782-167">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="13782-168">-Nome</span><span class="sxs-lookup"><span data-stu-id="13782-168">-Name</span></span>
<span data-ttu-id="13782-169">Especifica um nome para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="13782-169">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="13782-170">-Não-escopo</span><span class="sxs-lookup"><span data-stu-id="13782-170">-NotScope</span></span>
<span data-ttu-id="13782-171">Os não escopos para atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="13782-171">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="13782-172">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="13782-172">-PolicyDefinition</span></span>
<span data-ttu-id="13782-173">Especifica uma política, como um objeto **PsPolicyDefinition** que contém a regra de política.</span><span class="sxs-lookup"><span data-stu-id="13782-173">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="13782-174">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="13782-174">-PolicyParameter</span></span>
<span data-ttu-id="13782-175">O caminho do arquivo de parâmetro da política ou a cadeia de caracteres de parâmetro da política.</span><span class="sxs-lookup"><span data-stu-id="13782-175">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="13782-176">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="13782-176">-PolicyParameterObject</span></span>
<span data-ttu-id="13782-177">O objeto de parâmetro de política.</span><span class="sxs-lookup"><span data-stu-id="13782-177">The policy parameter object.</span></span>

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

### <span data-ttu-id="13782-178">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="13782-178">-PolicySetDefinition</span></span>
<span data-ttu-id="13782-179">O objeto de definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="13782-179">The policy set definition object.</span></span>

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

### <span data-ttu-id="13782-180">-Pre</span><span class="sxs-lookup"><span data-stu-id="13782-180">-Pre</span></span>
<span data-ttu-id="13782-181">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="13782-181">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="13782-182">-Escopo</span><span class="sxs-lookup"><span data-stu-id="13782-182">-Scope</span></span>
<span data-ttu-id="13782-183">Especifica o escopo no qual atribuir a política.</span><span class="sxs-lookup"><span data-stu-id="13782-183">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="13782-184">Por exemplo, para atribuir uma política a um grupo de recursos, especifique o seguinte: `/subscriptions/` nome do grupo de recursos de ID de assinatura `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="13782-184">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="13782-185">-SKU</span><span class="sxs-lookup"><span data-stu-id="13782-185">-Sku</span></span>
<span data-ttu-id="13782-186">Uma tabela de hash que representa as propriedades de SKU.</span><span class="sxs-lookup"><span data-stu-id="13782-186">A hash table which represents SKU properties.</span></span> <span data-ttu-id="13782-187">Padrão para a SKU grátis com os valores: `@{Name = 'A0'; Tier = 'Free'}` .</span><span class="sxs-lookup"><span data-stu-id="13782-187">Defaults to the Free SKU with the values: `@{Name = 'A0'; Tier = 'Free'}`.</span></span> <span data-ttu-id="13782-188">Para usar o SKU padrão, use os valores: `@{Name = 'A1'; Tier = 'Standard'}` .</span><span class="sxs-lookup"><span data-stu-id="13782-188">To use the Standard SKU, use the values: `@{Name = 'A1'; Tier = 'Standard'}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13782-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13782-189">CommonParameters</span></span>
<span data-ttu-id="13782-190">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13782-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13782-191">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13782-191">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13782-192">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13782-192">INPUTS</span></span>

## <span data-ttu-id="13782-193">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13782-193">OUTPUTS</span></span>

## <span data-ttu-id="13782-194">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13782-194">NOTES</span></span>

## <span data-ttu-id="13782-195">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13782-195">RELATED LINKS</span></span>

[<span data-ttu-id="13782-196">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="13782-196">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="13782-197">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="13782-197">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="13782-198">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="13782-198">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="13782-199">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="13782-199">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


