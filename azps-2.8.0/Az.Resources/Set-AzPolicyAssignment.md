---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 5d83266e341643adc45a2fc7af8eff1f9a5e0b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773306"
---
# <span data-ttu-id="5bcc4-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5bcc4-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="5bcc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bcc4-102">SYNOPSIS</span></span>
<span data-ttu-id="5bcc4-103">Modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="5bcc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5bcc4-104">SYNTAX</span></span>

### <span data-ttu-id="5bcc4-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5bcc4-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bcc4-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bcc4-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5bcc4-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bcc4-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bcc4-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bcc4-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bcc4-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bcc4-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bcc4-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bcc4-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bcc4-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5bcc4-111">DESCRIPTION</span></span>
<span data-ttu-id="5bcc4-112">O cmdlet **set-AzPolicyAssignment** modifica uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="5bcc4-113">Especifique uma atribuição por ID ou por nome e escopo.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="5bcc4-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5bcc4-114">EXAMPLES</span></span>

### <span data-ttu-id="5bcc4-115">Exemplo 1: atualizar o nome para exibição</span><span class="sxs-lookup"><span data-stu-id="5bcc4-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="5bcc4-116">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="5bcc4-117">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="5bcc4-118">O segundo comando obtém a atribuição de política chamada PolicyAssignment usando o cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="5bcc4-119">O comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="5bcc4-120">O comando final atualiza o nome de exibição na atribuição de política no grupo de recursos identificado pela propriedade **ResourceId** de $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="5bcc4-121">Exemplo 2: adicionar uma identidade gerenciada à atribuição de política</span><span class="sxs-lookup"><span data-stu-id="5bcc4-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="5bcc4-122">O primeiro comando obtém a atribuição de política chamada PolicyAssignment da assinatura atual usando o cmdlet Get-AzPolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="5bcc4-123">O comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="5bcc4-124">O comando final atribui uma identidade gerenciada à atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="5bcc4-125">Exemplo 3: atualizar parâmetros de atribuição de política com o novo objeto de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="5bcc4-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="5bcc4-126">O primeiro e o segundo comandos criam um objeto que contém todas as regiões do Azure cujos nomes começam com "França" ou "Reino Unido".</span><span class="sxs-lookup"><span data-stu-id="5bcc4-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="5bcc4-127">O segundo comando armazena esse objeto na variável $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="5bcc4-128">O terceiro comando obtém a atribuição de política chamada ' PolicyAssignment ', o comando armazena esse objeto na variável $PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="5bcc4-129">O comando final atualiza os valores de parâmetro na atribuição de política chamada PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="5bcc4-130">Exemplo 4: atualizar parâmetros de atribuição de política com o arquivo de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="5bcc4-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="5bcc4-131">Crie um arquivo chamado _AllowedLocations.jsno_ diretório de trabalho local com o conteúdo a seguir.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="5bcc4-132">O comando atualiza a atribuição de política chamada "PolicyAssignment" usando o arquivo de parâmetro de política AllowedLocations.jsno diretório de trabalho local.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

## <span data-ttu-id="5bcc4-133">OS</span><span class="sxs-lookup"><span data-stu-id="5bcc4-133">PARAMETERS</span></span>

### <span data-ttu-id="5bcc4-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5bcc4-134">-ApiVersion</span></span>
<span data-ttu-id="5bcc4-135">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-135">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5bcc4-136">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-136">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5bcc4-137">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5bcc4-137">-AssignIdentity</span></span>
<span data-ttu-id="5bcc4-138">Gerar e atribuir uma identidade do Azure Active Directory para esta atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-138">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="5bcc4-139">A identidade será usada ao executar implantações para políticas de "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="5bcc4-139">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="5bcc4-140">A localização é necessária ao atribuir uma identidade.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-140">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="5bcc4-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bcc4-141">-DefaultProfile</span></span>
<span data-ttu-id="5bcc4-142">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5bcc4-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bcc4-143">-Descrição</span><span class="sxs-lookup"><span data-stu-id="5bcc4-143">-Description</span></span>
<span data-ttu-id="5bcc4-144">A descrição da atribuição de política</span><span class="sxs-lookup"><span data-stu-id="5bcc4-144">The description for policy assignment</span></span>

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

### <span data-ttu-id="5bcc4-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5bcc4-145">-DisplayName</span></span>
<span data-ttu-id="5bcc4-146">Especifica um novo nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-146">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="5bcc4-147">-ID</span><span class="sxs-lookup"><span data-stu-id="5bcc4-147">-Id</span></span>
<span data-ttu-id="5bcc4-148">Especifica a ID de recurso totalmente qualificado para a atribuição de política que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-148">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5bcc4-149">-Local</span><span class="sxs-lookup"><span data-stu-id="5bcc4-149">-Location</span></span>
<span data-ttu-id="5bcc4-150">O local da identidade do recurso da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-150">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="5bcc4-151">Isso é necessário quando a opção-AssignIdentity é usada.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-151">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="5bcc4-152">-Metadados</span><span class="sxs-lookup"><span data-stu-id="5bcc4-152">-Metadata</span></span>
<span data-ttu-id="5bcc4-153">Os metadados atualizados para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-153">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="5bcc4-154">Isso pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-154">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="5bcc4-155">-Nome</span><span class="sxs-lookup"><span data-stu-id="5bcc4-155">-Name</span></span>
<span data-ttu-id="5bcc4-156">Especifica o nome da atribuição de política que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-156">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5bcc4-157">-Não-escopo</span><span class="sxs-lookup"><span data-stu-id="5bcc4-157">-NotScope</span></span>
<span data-ttu-id="5bcc4-158">A atribuição de política não é de escopos.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-158">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="5bcc4-159">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="5bcc4-159">-PolicyParameter</span></span>
<span data-ttu-id="5bcc4-160">O novo caminho de arquivo de parâmetros de política ou a cadeia de caracteres da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-160">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="5bcc4-161">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="5bcc4-161">-PolicyParameterObject</span></span>
<span data-ttu-id="5bcc4-162">O novo objeto de parâmetros de política para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-162">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="5bcc4-163">-Pre</span><span class="sxs-lookup"><span data-stu-id="5bcc4-163">-Pre</span></span>
<span data-ttu-id="5bcc4-164">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-164">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5bcc4-165">-Escopo</span><span class="sxs-lookup"><span data-stu-id="5bcc4-165">-Scope</span></span>
<span data-ttu-id="5bcc4-166">Especifica o escopo no qual a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-166">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="5bcc4-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bcc4-167">CommonParameters</span></span>
<span data-ttu-id="5bcc4-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bcc4-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bcc4-169">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bcc4-169">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bcc4-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5bcc4-170">INPUTS</span></span>

### <span data-ttu-id="5bcc4-171">System. String</span><span class="sxs-lookup"><span data-stu-id="5bcc4-171">System.String</span></span>

### <span data-ttu-id="5bcc4-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="5bcc4-172">System.String[]</span></span>

## <span data-ttu-id="5bcc4-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5bcc4-173">OUTPUTS</span></span>

### <span data-ttu-id="5bcc4-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5bcc4-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5bcc4-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5bcc4-175">NOTES</span></span>

## <span data-ttu-id="5bcc4-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bcc4-176">RELATED LINKS</span></span>

[<span data-ttu-id="5bcc4-177">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5bcc4-177">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="5bcc4-178">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5bcc4-178">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="5bcc4-179">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="5bcc4-179">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


