---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: ab0617b4012ca623bf67471a9a5bcc3ccf54d905
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941736"
---
# <span data-ttu-id="8ccf8-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8ccf8-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="8ccf8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ccf8-102">SYNOPSIS</span></span>
<span data-ttu-id="8ccf8-103">Modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="8ccf8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ccf8-104">SYNTAX</span></span>

### <span data-ttu-id="8ccf8-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8ccf8-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ccf8-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ccf8-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ccf8-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ccf8-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ccf8-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ccf8-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ccf8-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ccf8-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ccf8-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ccf8-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ccf8-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ccf8-111">DESCRIPTION</span></span>
<span data-ttu-id="8ccf8-112">O cmdlet **set-AzPolicyAssignment** modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="8ccf8-113">Especifique uma atribuição por ID ou por nome e escopo.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="8ccf8-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ccf8-114">EXAMPLES</span></span>

### <span data-ttu-id="8ccf8-115">Exemplo 1: atualizar o nome para exibição</span><span class="sxs-lookup"><span data-stu-id="8ccf8-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="8ccf8-116">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="8ccf8-117">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="8ccf8-118">O segundo comando obtém a atribuição de política chamada PolicyAssignment usando o cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="8ccf8-119">O comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="8ccf8-120">O comando final atualiza o nome de exibição na atribuição de política no grupo de recursos identificado pela propriedade **ResourceId** de $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="8ccf8-121">Exemplo 2: adicionar uma identidade gerenciada à atribuição de política</span><span class="sxs-lookup"><span data-stu-id="8ccf8-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="8ccf8-122">O primeiro comando obtém a atribuição de política chamada PolicyAssignment da assinatura atual usando o cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="8ccf8-123">O comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="8ccf8-124">O comando final atribui uma identidade gerenciada à atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="8ccf8-125">Exemplo 3: atualizar parâmetros de atribuição de política com o novo objeto de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="8ccf8-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="8ccf8-126">O primeiro e o segundo comandos criam um objeto que contém todas as regiões do Azure cujos nomes começam com "França" ou "Reino Unido".</span><span class="sxs-lookup"><span data-stu-id="8ccf8-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="8ccf8-127">O segundo comando armazena esse objeto na variável $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="8ccf8-128">O terceiro comando obtém a atribuição de política chamada ' PolicyAssignment ', o comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="8ccf8-129">O comando final atualiza os valores de parâmetro na atribuição de política chamada PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="8ccf8-130">Exemplo 4: atualizar parâmetros de atribuição de política com o arquivo de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="8ccf8-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="8ccf8-131">Crie um arquivo chamado _AllowedLocations.jsno_ diretório de trabalho local com o conteúdo a seguir.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="8ccf8-132">O comando atualiza a atribuição de política chamada "PolicyAssignment" usando o arquivo de parâmetro de política AllowedLocations.jsno diretório de trabalho local.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="8ccf8-133">Exemplo 5: atualizar um imposiçãomode</span><span class="sxs-lookup"><span data-stu-id="8ccf8-133">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="8ccf8-134">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-134">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="8ccf8-135">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-135">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="8ccf8-136">O segundo comando obtém a atribuição de política chamada PolicyAssignment usando o cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-136">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="8ccf8-137">O comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-137">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="8ccf8-138">O comando final atualiza a propriedade imposiçãomode na atribuição de política no grupo de recursos identificado pela propriedade **ResourceId** de $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-138">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="8ccf8-139">OS</span><span class="sxs-lookup"><span data-stu-id="8ccf8-139">PARAMETERS</span></span>

### <span data-ttu-id="8ccf8-140">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8ccf8-140">-ApiVersion</span></span>
<span data-ttu-id="8ccf8-141">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-141">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8ccf8-142">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-142">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8ccf8-143">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8ccf8-143">-AssignIdentity</span></span>
<span data-ttu-id="8ccf8-144">Gerar e atribuir uma identidade do Azure Active Directory para esta atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-144">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="8ccf8-145">A identidade será usada ao executar implantações para políticas de "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="8ccf8-145">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="8ccf8-146">A localização é necessária ao atribuir uma identidade.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-146">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="8ccf8-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ccf8-147">-DefaultProfile</span></span>
<span data-ttu-id="8ccf8-148">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8ccf8-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ccf8-149">-Descrição</span><span class="sxs-lookup"><span data-stu-id="8ccf8-149">-Description</span></span>
<span data-ttu-id="8ccf8-150">A descrição da atribuição de política</span><span class="sxs-lookup"><span data-stu-id="8ccf8-150">The description for policy assignment</span></span>

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

### <span data-ttu-id="8ccf8-151">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8ccf8-151">-DisplayName</span></span>
<span data-ttu-id="8ccf8-152">Especifica um novo nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-152">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="8ccf8-153">-Imposiçãomode</span><span class="sxs-lookup"><span data-stu-id="8ccf8-153">-EnforcementMode</span></span>
<span data-ttu-id="8ccf8-154">O modo de imposição para atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-154">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="8ccf8-155">Atualmente, os valores válidos são padrão, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-155">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="8ccf8-156">-ID</span><span class="sxs-lookup"><span data-stu-id="8ccf8-156">-Id</span></span>
<span data-ttu-id="8ccf8-157">Especifica a ID de recurso totalmente qualificado para a atribuição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-157">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8ccf8-158">-Local</span><span class="sxs-lookup"><span data-stu-id="8ccf8-158">-Location</span></span>
<span data-ttu-id="8ccf8-159">O local da identidade do recurso da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-159">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="8ccf8-160">Isso é necessário quando a opção-AssignIdentity é usada.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-160">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="8ccf8-161">-Metadados</span><span class="sxs-lookup"><span data-stu-id="8ccf8-161">-Metadata</span></span>
<span data-ttu-id="8ccf8-162">Os metadados atualizados para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-162">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="8ccf8-163">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-163">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="8ccf8-164">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ccf8-164">-Name</span></span>
<span data-ttu-id="8ccf8-165">Especifica o nome da atribuição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-165">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8ccf8-166">-Não-escopo</span><span class="sxs-lookup"><span data-stu-id="8ccf8-166">-NotScope</span></span>
<span data-ttu-id="8ccf8-167">A atribuição de política não é de escopos.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-167">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="8ccf8-168">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="8ccf8-168">-PolicyParameter</span></span>
<span data-ttu-id="8ccf8-169">O novo caminho de arquivo de parâmetros de política ou a cadeia de caracteres da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-169">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="8ccf8-170">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="8ccf8-170">-PolicyParameterObject</span></span>
<span data-ttu-id="8ccf8-171">O novo objeto de parâmetros de política para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-171">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="8ccf8-172">-Pre</span><span class="sxs-lookup"><span data-stu-id="8ccf8-172">-Pre</span></span>
<span data-ttu-id="8ccf8-173">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-173">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8ccf8-174">-Escopo</span><span class="sxs-lookup"><span data-stu-id="8ccf8-174">-Scope</span></span>
<span data-ttu-id="8ccf8-175">Especifica o escopo no qual a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-175">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="8ccf8-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ccf8-176">CommonParameters</span></span>
<span data-ttu-id="8ccf8-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ccf8-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ccf8-178">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ccf8-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ccf8-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ccf8-179">INPUTS</span></span>

### <span data-ttu-id="8ccf8-180">System. String</span><span class="sxs-lookup"><span data-stu-id="8ccf8-180">System.String</span></span>

### <span data-ttu-id="8ccf8-181">System. String []</span><span class="sxs-lookup"><span data-stu-id="8ccf8-181">System.String[]</span></span>

## <span data-ttu-id="8ccf8-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ccf8-182">OUTPUTS</span></span>

### <span data-ttu-id="8ccf8-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8ccf8-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8ccf8-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ccf8-184">NOTES</span></span>

## <span data-ttu-id="8ccf8-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ccf8-185">RELATED LINKS</span></span>

[<span data-ttu-id="8ccf8-186">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8ccf8-186">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="8ccf8-187">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8ccf8-187">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="8ccf8-188">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8ccf8-188">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


