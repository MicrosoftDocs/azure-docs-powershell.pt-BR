---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 1c3b18d5e098e19a8259f3b8faf06adcc25f7333
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772566"
---
# <span data-ttu-id="a0be3-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a0be3-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="a0be3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0be3-102">SYNOPSIS</span></span>
<span data-ttu-id="a0be3-103">Cria uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="a0be3-103">Creates a policy definition.</span></span>

## <span data-ttu-id="a0be3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0be3-104">SYNTAX</span></span>

### <span data-ttu-id="a0be3-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0be3-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0be3-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0be3-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0be3-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0be3-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0be3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0be3-108">DESCRIPTION</span></span>
<span data-ttu-id="a0be3-109">O cmdlet **New-AzPolicyDefinition** cria uma definição de política que inclui uma regra de política no formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="a0be3-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="a0be3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0be3-110">EXAMPLES</span></span>

### <span data-ttu-id="a0be3-111">Exemplo 1: criar uma definição de política usando um arquivo de política</span><span class="sxs-lookup"><span data-stu-id="a0be3-111">Example 1: Create a policy definition by using a policy file</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": ["eastus", "westus", "centralus"]
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="a0be3-112">Esse comando cria uma definição de política chamada LocationDefinition que contém a regra de política especificada em C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="a0be3-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="a0be3-113">O conteúdo de exemplo para o LocationPolicy.jsem arquivo é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="a0be3-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="a0be3-114">Exemplo 2: criar uma definição de política com parâmetros usando parâmetros embutidos</span><span class="sxs-lookup"><span data-stu-id="a0be3-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": "[parameters('listOfAllowedLocations')]"
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="a0be3-115">Esse comando cria uma definição de política chamada LocationDefinition que contém a regra de política especificada em C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="a0be3-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="a0be3-116">A definição de parâmetro para a regra de política é fornecida embutida.</span><span class="sxs-lookup"><span data-stu-id="a0be3-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="a0be3-117">Exemplo 3: criar uma definição de política embutida em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a0be3-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="a0be3-118">Esse comando cria uma definição de política chamada VMPolicyDefinition no grupo de gerenciamento Dept42.</span><span class="sxs-lookup"><span data-stu-id="a0be3-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="a0be3-119">O comando especifica a política como uma cadeia de caracteres em formato JSON válido.</span><span class="sxs-lookup"><span data-stu-id="a0be3-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="a0be3-120">Exemplo 4: criar uma definição de política embutida com metadados</span><span class="sxs-lookup"><span data-stu-id="a0be3-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="a0be3-121">Esse comando cria uma definição de política chamada VMPolicyDefinition com metadados indicando que sua categoria é "máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="a0be3-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="a0be3-122">O comando especifica a política como uma cadeia de caracteres em formato JSON válido.</span><span class="sxs-lookup"><span data-stu-id="a0be3-122">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="a0be3-123">Exemplo 5: criar uma definição de política embutida com Mode</span><span class="sxs-lookup"><span data-stu-id="a0be3-123">Example 5: Create a policy definition inline with mode</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'TagsPolicyDefinition' -Policy '{"if":{"value":"[less(length(field(''tags'')), 3)]","equals":true},"then":{"effect":"deny"}}' -Mode Indexed


Name               : TagsPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
ResourceName       : TagsPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=TagsPolicyDefinition; policyType=Custom; mode=Indexed; metadata=; parameters=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
```

<span data-ttu-id="a0be3-124">Esse comando cria uma definição de política chamada TagsPolicyDefinition com o modo "indexado" indicando que a política deve ser avaliada somente para tipos de recursos que dão suporte a marcas e local.</span><span class="sxs-lookup"><span data-stu-id="a0be3-124">This command creates a policy definition named TagsPolicyDefinition with mode "Indexed" indicating the policy should be evaluated only for resource types that support tags and location.</span></span>

## <span data-ttu-id="a0be3-125">OS</span><span class="sxs-lookup"><span data-stu-id="a0be3-125">PARAMETERS</span></span>

### <span data-ttu-id="a0be3-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a0be3-126">-ApiVersion</span></span>
<span data-ttu-id="a0be3-127">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a0be3-127">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a0be3-128">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="a0be3-128">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a0be3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0be3-129">-DefaultProfile</span></span>
<span data-ttu-id="a0be3-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a0be3-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0be3-131">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a0be3-131">-Description</span></span>
<span data-ttu-id="a0be3-132">Especifica uma descrição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="a0be3-132">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="a0be3-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a0be3-133">-DisplayName</span></span>
<span data-ttu-id="a0be3-134">Especifica um nome de exibição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="a0be3-134">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="a0be3-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a0be3-135">-ManagementGroupName</span></span>
<span data-ttu-id="a0be3-136">O nome do grupo Gerenciamento da nova definição de política.</span><span class="sxs-lookup"><span data-stu-id="a0be3-136">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="a0be3-137">-Metadados</span><span class="sxs-lookup"><span data-stu-id="a0be3-137">-Metadata</span></span>
<span data-ttu-id="a0be3-138">Os metadados da definição da política.</span><span class="sxs-lookup"><span data-stu-id="a0be3-138">The metadata for policy definition.</span></span> <span data-ttu-id="a0be3-139">Pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a0be3-139">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="a0be3-140">-Mode</span><span class="sxs-lookup"><span data-stu-id="a0be3-140">-Mode</span></span>
<span data-ttu-id="a0be3-141">O modo da definição de política</span><span class="sxs-lookup"><span data-stu-id="a0be3-141">The mode of the policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: All
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0be3-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0be3-142">-Name</span></span>
<span data-ttu-id="a0be3-143">Especifica um nome para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="a0be3-143">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="a0be3-144">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0be3-144">-Parameter</span></span>
<span data-ttu-id="a0be3-145">A declaração Parameters para a definição da política.</span><span class="sxs-lookup"><span data-stu-id="a0be3-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="a0be3-146">Isso pode ser um caminho para um nome de arquivo contendo a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a0be3-146">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="a0be3-147">-Política</span><span class="sxs-lookup"><span data-stu-id="a0be3-147">-Policy</span></span>
<span data-ttu-id="a0be3-148">Especifica uma regra de política para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="a0be3-148">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="a0be3-149">Você pode especificar o caminho de um arquivo. JSON ou uma cadeia de caracteres que contém a política em formato JSON.</span><span class="sxs-lookup"><span data-stu-id="a0be3-149">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="a0be3-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="a0be3-150">-Pre</span></span>
<span data-ttu-id="a0be3-151">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="a0be3-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a0be3-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0be3-152">-SubscriptionId</span></span>
<span data-ttu-id="a0be3-153">A ID da assinatura da nova definição de política.</span><span class="sxs-lookup"><span data-stu-id="a0be3-153">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="a0be3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0be3-154">CommonParameters</span></span>
<span data-ttu-id="a0be3-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0be3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0be3-156">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0be3-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0be3-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0be3-157">INPUTS</span></span>

### <span data-ttu-id="a0be3-158">System. String</span><span class="sxs-lookup"><span data-stu-id="a0be3-158">System.String</span></span>

### <span data-ttu-id="a0be3-159">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a0be3-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a0be3-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0be3-160">OUTPUTS</span></span>

### <span data-ttu-id="a0be3-161">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a0be3-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a0be3-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0be3-162">NOTES</span></span>

## <span data-ttu-id="a0be3-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0be3-163">RELATED LINKS</span></span>

[<span data-ttu-id="a0be3-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a0be3-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="a0be3-165">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a0be3-165">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="a0be3-166">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a0be3-166">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)

