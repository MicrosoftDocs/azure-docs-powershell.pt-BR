---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 8efda1a15546a09f0946506f3bc7fd27462b3c03
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117171"
---
# <span data-ttu-id="a7632-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a7632-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="a7632-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7632-102">SYNOPSIS</span></span>
<span data-ttu-id="a7632-103">Modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="a7632-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="a7632-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7632-104">SYNTAX</span></span>

### <span data-ttu-id="a7632-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a7632-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7632-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7632-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7632-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7632-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7632-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7632-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7632-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7632-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7632-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7632-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7632-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7632-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7632-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7632-112">DESCRIPTION</span></span>
<span data-ttu-id="a7632-113">O cmdlet **Set-AzPolicyAssignment** modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="a7632-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="a7632-114">Especifique uma tarefa por ID ou por nome e escopo.</span><span class="sxs-lookup"><span data-stu-id="a7632-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="a7632-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7632-115">EXAMPLES</span></span>

### <span data-ttu-id="a7632-116">Exemplo 1: Atualizar o nome de exibição</span><span class="sxs-lookup"><span data-stu-id="a7632-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="a7632-117">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7632-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="a7632-118">O comando armazena esse objeto na variável $ResourceGroup dados.</span><span class="sxs-lookup"><span data-stu-id="a7632-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a7632-119">O segundo comando obtém a atribuição de política chamada PolicyAssignment usando Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7632-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="a7632-120">O comando armazena esse objeto na variável $PolicyAssignment dados.</span><span class="sxs-lookup"><span data-stu-id="a7632-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="a7632-121">O comando final atualiza o nome de exibição na atribuição de política no grupo de recursos identificado pela propriedade **ResourceId** da $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a7632-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="a7632-122">Exemplo 2: Adicionar uma identidade gerenciada à atribuição de política</span><span class="sxs-lookup"><span data-stu-id="a7632-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="a7632-123">O primeiro comando obtém a atribuição de política chamada PolicyAssignment da assinatura atual usando o cmdlet Get-AzPolicyAssignment dados.</span><span class="sxs-lookup"><span data-stu-id="a7632-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="a7632-124">O comando armazena esse objeto na variável $PolicyAssignment dados.</span><span class="sxs-lookup"><span data-stu-id="a7632-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="a7632-125">O comando final atribui uma identidade gerenciada à atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="a7632-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="a7632-126">Exemplo 3: Atualizar parâmetros de atribuição de política com o novo objeto de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="a7632-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="a7632-127">O primeiro e o segundo comandos criam um objeto que contém todas as regiões do Azure cujos nomes começam com "frança" ou "reino unido".</span><span class="sxs-lookup"><span data-stu-id="a7632-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="a7632-128">O segundo comando armazena esse objeto na variável $AllowedLocations dados.</span><span class="sxs-lookup"><span data-stu-id="a7632-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="a7632-129">O terceiro comando obtém a atribuição de política chamada 'PolicyAssignment' O comando armazena esse objeto na variável $PolicyAssignment política.</span><span class="sxs-lookup"><span data-stu-id="a7632-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="a7632-130">O comando final atualiza os valores de parâmetro na atribuição de política chamada PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="a7632-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="a7632-131">Exemplo 4: Atualizar parâmetros de atribuição de política com o arquivo de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="a7632-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="a7632-132">Crie um arquivo chamado _AllowedLocations.jsno_ diretório de trabalho local com o conteúdo a seguir.</span><span class="sxs-lookup"><span data-stu-id="a7632-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "uksouth",
        "ukwest",
        "francecentral",
        "francesouth"
      ]
    }
}
```

```
PS C:\> Set-AzPolicyAssignment -Name 'PolicyAssignment' -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="a7632-133">O comando atualiza a atribuição de política chamada "PolicyAssignment" usando o arquivo de parâmetro de política AllowedLocations.jsno diretório de trabalho local.</span><span class="sxs-lookup"><span data-stu-id="a7632-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="a7632-134">Exemplo 5: Atualizar um enforcementMode</span><span class="sxs-lookup"><span data-stu-id="a7632-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="a7632-135">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7632-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="a7632-136">O comando armazena esse objeto na variável $ResourceGroup dados.</span><span class="sxs-lookup"><span data-stu-id="a7632-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a7632-137">O segundo comando obtém a atribuição de política chamada PolicyAssignment usando Get-AzPolicyAssignment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7632-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="a7632-138">O comando armazena esse objeto na variável $PolicyAssignment dados.</span><span class="sxs-lookup"><span data-stu-id="a7632-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="a7632-139">O comando final atualiza a propriedade enforcementMode na atribuição de política no grupo de recursos identificado pela propriedade **ResourceId** da $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a7632-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="a7632-140">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7632-140">PARAMETERS</span></span>

### <span data-ttu-id="a7632-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a7632-141">-ApiVersion</span></span>
<span data-ttu-id="a7632-142">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a7632-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a7632-143">Se você não especificar uma versão, este cmdlet usará a versão disponível mais recente.</span><span class="sxs-lookup"><span data-stu-id="a7632-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a7632-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a7632-144">-AssignIdentity</span></span>
<span data-ttu-id="a7632-145">Gere e atribua uma Identidade do Azure Active Directory para essa atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="a7632-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="a7632-146">A identidade será usada durante a execução de implantações para políticas de "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="a7632-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="a7632-147">O local é necessário ao atribuir uma identidade.</span><span class="sxs-lookup"><span data-stu-id="a7632-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="a7632-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7632-148">-DefaultProfile</span></span>
<span data-ttu-id="a7632-149">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a7632-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7632-150">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a7632-150">-Description</span></span>
<span data-ttu-id="a7632-151">A descrição da atribuição de política</span><span class="sxs-lookup"><span data-stu-id="a7632-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="a7632-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a7632-152">-DisplayName</span></span>
<span data-ttu-id="a7632-153">Especifica um novo nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="a7632-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="a7632-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="a7632-154">-EnforcementMode</span></span>
<span data-ttu-id="a7632-155">O modo de imposição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="a7632-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="a7632-156">Atualmente, os valores válidos são Padrão, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="a7632-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="a7632-157">-ID</span><span class="sxs-lookup"><span data-stu-id="a7632-157">-Id</span></span>
<span data-ttu-id="a7632-158">Especifica a ID de recurso totalmente qualificada para a atribuição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a7632-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet, PolicyParameterIdObjectParameterSet, PolicyParameterIdStringParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7632-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7632-159">-InputObject</span></span>
<span data-ttu-id="a7632-160">O objeto de atribuição de política para atualizar que foi saída de outro cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7632-160">The policy assignment object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7632-161">-Local</span><span class="sxs-lookup"><span data-stu-id="a7632-161">-Location</span></span>
<span data-ttu-id="a7632-162">O local da identidade de recurso da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="a7632-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="a7632-163">Isso é necessário quando a opção -AssignIdentity é usada.</span><span class="sxs-lookup"><span data-stu-id="a7632-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="a7632-164">-Metadados</span><span class="sxs-lookup"><span data-stu-id="a7632-164">-Metadata</span></span>
<span data-ttu-id="a7632-165">Os metadados atualizados para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="a7632-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="a7632-166">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a7632-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="a7632-167">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7632-167">-Name</span></span>
<span data-ttu-id="a7632-168">Especifica o nome da atribuição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a7632-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7632-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="a7632-169">-NotScope</span></span>
<span data-ttu-id="a7632-170">A atribuição de política não escopos.</span><span class="sxs-lookup"><span data-stu-id="a7632-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="a7632-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="a7632-171">-PolicyParameter</span></span>
<span data-ttu-id="a7632-172">O novo caminho ou cadeia de caracteres de parâmetros de política para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="a7632-172">The new policy parameters file path or string for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterNameStringParameterSet, PolicyParameterIdStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7632-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="a7632-173">-PolicyParameterObject</span></span>
<span data-ttu-id="a7632-174">O novo objeto de parâmetros de política para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="a7632-174">The new policy parameters object for the policy assignment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterNameObjectParameterSet, PolicyParameterIdObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7632-175">-Pré-</span><span class="sxs-lookup"><span data-stu-id="a7632-175">-Pre</span></span>
<span data-ttu-id="a7632-176">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="a7632-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a7632-177">-Escopo</span><span class="sxs-lookup"><span data-stu-id="a7632-177">-Scope</span></span>
<span data-ttu-id="a7632-178">Especifica o escopo no qual a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="a7632-178">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7632-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7632-179">CommonParameters</span></span>
<span data-ttu-id="a7632-180">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7632-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7632-181">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7632-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7632-182">Entradas</span><span class="sxs-lookup"><span data-stu-id="a7632-182">INPUTS</span></span>

### <span data-ttu-id="a7632-183">System.String</span><span class="sxs-lookup"><span data-stu-id="a7632-183">System.String</span></span>

### <span data-ttu-id="a7632-184">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a7632-184">System.String[]</span></span>

## <span data-ttu-id="a7632-185">Saídas</span><span class="sxs-lookup"><span data-stu-id="a7632-185">OUTPUTS</span></span>

### <span data-ttu-id="a7632-186">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="a7632-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a7632-187">Notas</span><span class="sxs-lookup"><span data-stu-id="a7632-187">NOTES</span></span>

## <span data-ttu-id="a7632-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7632-188">RELATED LINKS</span></span>

[<span data-ttu-id="a7632-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a7632-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="a7632-190">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a7632-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="a7632-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a7632-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


