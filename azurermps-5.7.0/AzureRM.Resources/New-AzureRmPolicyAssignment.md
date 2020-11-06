---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 364411d6b69c04d8b29c1c32e2809ec3c4789b09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432406"
---
# <span data-ttu-id="c910a-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c910a-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="c910a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c910a-102">SYNOPSIS</span></span>
<span data-ttu-id="c910a-103">Cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c910a-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c910a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c910a-104">SYNTAX</span></span>

### <span data-ttu-id="c910a-105">Createwithparameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="c910a-105">CreateWithoutParameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c910a-106">CreateWithPolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="c910a-106">CreateWithPolicyParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c910a-107">CreateWithPolicyParameterString</span><span class="sxs-lookup"><span data-stu-id="c910a-107">CreateWithPolicyParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c910a-108">CreateWithPolicySetParameterObject</span><span class="sxs-lookup"><span data-stu-id="c910a-108">CreateWithPolicySetParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c910a-109">CreateWithPolicySetParameterString</span><span class="sxs-lookup"><span data-stu-id="c910a-109">CreateWithPolicySetParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c910a-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c910a-110">DESCRIPTION</span></span>
<span data-ttu-id="c910a-111">O cmdlet **New-AzureRmPolicyAssignment** cria uma atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c910a-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="c910a-112">Especifique uma política e um escopo.</span><span class="sxs-lookup"><span data-stu-id="c910a-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="c910a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c910a-113">EXAMPLES</span></span>

### <span data-ttu-id="c910a-114">Exemplo 1: atribuição de política em nível de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c910a-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="c910a-115">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c910a-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="c910a-116">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c910a-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="c910a-117">O segundo comando obtém a definição de política chamada VirtualMachinePolicy usando o cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="c910a-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="c910a-118">O comando armazena esse objeto na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="c910a-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="c910a-119">O comando final atribui a política em $Policy no nível de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c910a-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="c910a-120">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c910a-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="c910a-121">Exemplo 2: atribuição de política em nível de grupo de recursos com objeto de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="c910a-121">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like "*east*"
PS C:\> $AllowedLocations = @{"listOfAllowedLocations"=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="c910a-122">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c910a-122">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="c910a-123">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c910a-123">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="c910a-124">O segundo comando obtém a definição de política interna para locais permitidos usando o cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="c910a-124">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="c910a-125">O comando armazena esse objeto na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="c910a-125">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="c910a-126">O terceiro e o quarto comandos criam um objeto que contém todas as regiões do Azure com "East" no nome.</span><span class="sxs-lookup"><span data-stu-id="c910a-126">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="c910a-127">Os comandos armazenam esse objeto na variável $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="c910a-127">The commands store that object in the $AllowedLocations variable.</span></span>

<span data-ttu-id="c910a-128">O comando final atribui a política em $Policy no nível de um grupo de recursos usando o objeto Parameter da política em $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="c910a-128">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="c910a-129">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c910a-129">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="c910a-130">Exemplo 3: atribuição de política em nível de grupo de recursos com arquivo de parâmetro de política</span><span class="sxs-lookup"><span data-stu-id="c910a-130">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="c910a-131">Crie um arquivo chamado _AllowedLocations.jsno_ diretório de trabalho local com o conteúdo a seguir.</span><span class="sxs-lookup"><span data-stu-id="c910a-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>
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
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="c910a-132">O primeiro comando obtém um grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c910a-132">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="c910a-133">O comando armazena esse objeto na variável $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c910a-133">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="c910a-134">O segundo comando obtém a definição de política interna para locais permitidos usando o cmdlet Get-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="c910a-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="c910a-135">O comando armazena esse objeto na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="c910a-135">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="c910a-136">O comando final atribui a política em $Policy no nível de um grupo de recursos usando o arquivo de parâmetro de política AllowedLocations.jsno diretório de trabalho local.</span><span class="sxs-lookup"><span data-stu-id="c910a-136">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter file AllowedLocations.json from the local working directory.</span></span>
<span data-ttu-id="c910a-137">A propriedade **ResourceId** de $ResourceGroup identifica o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c910a-137">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>


## <span data-ttu-id="c910a-138">OS</span><span class="sxs-lookup"><span data-stu-id="c910a-138">PARAMETERS</span></span>

### <span data-ttu-id="c910a-139">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c910a-139">-ApiVersion</span></span>
<span data-ttu-id="c910a-140">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c910a-140">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c910a-141">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="c910a-141">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c910a-142">-DefaultProfile</span></span>
<span data-ttu-id="c910a-143">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c910a-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-144">-Descrição</span><span class="sxs-lookup"><span data-stu-id="c910a-144">-Description</span></span>
<span data-ttu-id="c910a-145">A descrição da atribuição de política</span><span class="sxs-lookup"><span data-stu-id="c910a-145">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-146">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c910a-146">-DisplayName</span></span>
<span data-ttu-id="c910a-147">Especifica um nome de exibição para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c910a-147">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-148">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="c910a-148">-InformationAction</span></span>
<span data-ttu-id="c910a-149">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="c910a-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c910a-150">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c910a-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c910a-151">Contínuo</span><span class="sxs-lookup"><span data-stu-id="c910a-151">Continue</span></span>
- <span data-ttu-id="c910a-152">Ignorar</span><span class="sxs-lookup"><span data-stu-id="c910a-152">Ignore</span></span>
- <span data-ttu-id="c910a-153">Inquire</span><span class="sxs-lookup"><span data-stu-id="c910a-153">Inquire</span></span>
- <span data-ttu-id="c910a-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c910a-154">SilentlyContinue</span></span>
- <span data-ttu-id="c910a-155">Finaliza</span><span class="sxs-lookup"><span data-stu-id="c910a-155">Stop</span></span>
- <span data-ttu-id="c910a-156">Suspensão</span><span class="sxs-lookup"><span data-stu-id="c910a-156">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c910a-157">-InformationVariable</span></span>
<span data-ttu-id="c910a-158">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="c910a-158">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="c910a-159">-Name</span></span>
<span data-ttu-id="c910a-160">Especifica um nome para a atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c910a-160">Specifies a name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-161">-Não-escopo</span><span class="sxs-lookup"><span data-stu-id="c910a-161">-NotScope</span></span>
<span data-ttu-id="c910a-162">Os não escopos para atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="c910a-162">The not scopes for policy assignment.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-163">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c910a-163">-PolicyDefinition</span></span>
<span data-ttu-id="c910a-164">Especifica uma política, como um objeto **PSObject** que contém a regra de política.</span><span class="sxs-lookup"><span data-stu-id="c910a-164">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-165">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="c910a-165">-PolicyParameter</span></span>
<span data-ttu-id="c910a-166">O caminho do arquivo de parâmetro da política ou a cadeia de caracteres de parâmetro da política.</span><span class="sxs-lookup"><span data-stu-id="c910a-166">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithPolicyParameterString, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-167">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="c910a-167">-PolicyParameterObject</span></span>
<span data-ttu-id="c910a-168">O objeto de parâmetro de política.</span><span class="sxs-lookup"><span data-stu-id="c910a-168">The policy parameter object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicySetParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-169">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c910a-169">-PolicySetDefinition</span></span>
<span data-ttu-id="c910a-170">O objeto de definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="c910a-170">The policy set definition object.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-171">-Pre</span><span class="sxs-lookup"><span data-stu-id="c910a-171">-Pre</span></span>
<span data-ttu-id="c910a-172">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="c910a-172">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-173">-Escopo</span><span class="sxs-lookup"><span data-stu-id="c910a-173">-Scope</span></span>
<span data-ttu-id="c910a-174">Especifica o escopo no qual atribuir a política.</span><span class="sxs-lookup"><span data-stu-id="c910a-174">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="c910a-175">Por exemplo, para atribuir uma política a um grupo de recursos, especifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c910a-175">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="c910a-176">`/subscriptions/`ID da assinatura `/resourcegroups/` nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c910a-176">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-177">-SKU</span><span class="sxs-lookup"><span data-stu-id="c910a-177">-Sku</span></span>
<span data-ttu-id="c910a-178">Uma tabela de hash que representa as propriedades de SKU.</span><span class="sxs-lookup"><span data-stu-id="c910a-178">A hash table which represents sku properties.</span></span> <span data-ttu-id="c910a-179">Padrões para SKU grátis: Name = a0, Tier = fre</span><span class="sxs-lookup"><span data-stu-id="c910a-179">Defaults to Free Sku: Name = A0, Tier = Fre</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c910a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c910a-180">CommonParameters</span></span>
<span data-ttu-id="c910a-181">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c910a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c910a-182">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c910a-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c910a-183">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c910a-183">INPUTS</span></span>

### <span data-ttu-id="c910a-184">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c910a-184">None</span></span>
<span data-ttu-id="c910a-185">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c910a-185">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c910a-186">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c910a-186">OUTPUTS</span></span>

### <span data-ttu-id="c910a-187">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c910a-187">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c910a-188">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c910a-188">NOTES</span></span>

## <span data-ttu-id="c910a-189">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c910a-189">RELATED LINKS</span></span>

[<span data-ttu-id="c910a-190">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c910a-190">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="c910a-191">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c910a-191">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="c910a-192">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c910a-192">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="c910a-193">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="c910a-193">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


