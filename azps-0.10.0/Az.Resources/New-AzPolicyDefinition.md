---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 8879f013983888ff0400c0f43ec4e570c495760f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776392"
---
# <span data-ttu-id="0c1d6-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0c1d6-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="0c1d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c1d6-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1d6-103">Cria uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-103">Creates a policy definition.</span></span>

## <span data-ttu-id="0c1d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c1d6-104">SYNTAX</span></span>

### <span data-ttu-id="0c1d6-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0c1d6-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0c1d6-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c1d6-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0c1d6-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c1d6-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0c1d6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c1d6-108">DESCRIPTION</span></span>
<span data-ttu-id="0c1d6-109">O cmdlet **New-AzPolicyDefinition** cria uma definição de política que inclui uma regra de política no formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="0c1d6-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="0c1d6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c1d6-110">EXAMPLES</span></span>

### <span data-ttu-id="0c1d6-111">Exemplo 1: criar uma definição de política usando um arquivo de política</span><span class="sxs-lookup"><span data-stu-id="0c1d6-111">Example 1: Create a policy definition by using a policy file</span></span>
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

<span data-ttu-id="0c1d6-112">Esse comando cria uma definição de política chamada LocationDefinition que contém a regra de política especificada em C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="0c1d6-113">O conteúdo de exemplo para o LocationPolicy.jsem arquivo é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="0c1d6-114">Exemplo 2: criar uma definição de política com parâmetros usando parâmetros embutidos</span><span class="sxs-lookup"><span data-stu-id="0c1d6-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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

<span data-ttu-id="0c1d6-115">Esse comando cria uma definição de política chamada LocationDefinition que contém a regra de política especificada em C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="0c1d6-116">A definição de parâmetro para a regra de política é fornecida embutida.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="0c1d6-117">Exemplo 3: criar uma definição de política embutida em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="0c1d6-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="0c1d6-118">Esse comando cria uma definição de política chamada VMPolicyDefinition no grupo de gerenciamento Dept42.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="0c1d6-119">O comando especifica a política como uma cadeia de caracteres em formato JSON válido.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="0c1d6-120">Exemplo 4: criar uma definição de política embutida com metadados</span><span class="sxs-lookup"><span data-stu-id="0c1d6-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="0c1d6-121">Esse comando cria uma definição de política chamada VMPolicyDefinition com metadados indicando que sua categoria é "máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="0c1d6-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="0c1d6-122">O comando especifica a política como uma cadeia de caracteres em formato JSON válido.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="0c1d6-123">OS</span><span class="sxs-lookup"><span data-stu-id="0c1d6-123">PARAMETERS</span></span>

### <span data-ttu-id="0c1d6-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0c1d6-124">-ApiVersion</span></span>
<span data-ttu-id="0c1d6-125">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0c1d6-126">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0c1d6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c1d6-127">-DefaultProfile</span></span>
<span data-ttu-id="0c1d6-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0c1d6-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c1d6-129">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0c1d6-129">-Description</span></span>
<span data-ttu-id="0c1d6-130">Especifica uma descrição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="0c1d6-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0c1d6-131">-DisplayName</span></span>
<span data-ttu-id="0c1d6-132">Especifica um nome de exibição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="0c1d6-133">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="0c1d6-133">-InformationAction</span></span>
<span data-ttu-id="0c1d6-134">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-134">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="0c1d6-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0c1d6-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c1d6-136">Contínuo</span><span class="sxs-lookup"><span data-stu-id="0c1d6-136">Continue</span></span>
- <span data-ttu-id="0c1d6-137">Ignorar</span><span class="sxs-lookup"><span data-stu-id="0c1d6-137">Ignore</span></span>
- <span data-ttu-id="0c1d6-138">Inquire</span><span class="sxs-lookup"><span data-stu-id="0c1d6-138">Inquire</span></span>
- <span data-ttu-id="0c1d6-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0c1d6-139">SilentlyContinue</span></span>
- <span data-ttu-id="0c1d6-140">Finaliza</span><span class="sxs-lookup"><span data-stu-id="0c1d6-140">Stop</span></span>
- <span data-ttu-id="0c1d6-141">Suspensão</span><span class="sxs-lookup"><span data-stu-id="0c1d6-141">Suspend</span></span>

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

### <span data-ttu-id="0c1d6-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0c1d6-142">-InformationVariable</span></span>
<span data-ttu-id="0c1d6-143">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-143">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0c1d6-144">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0c1d6-144">-ManagementGroupName</span></span>
<span data-ttu-id="0c1d6-145">O nome do grupo Gerenciamento da nova definição de política.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-145">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="0c1d6-146">-Metadados</span><span class="sxs-lookup"><span data-stu-id="0c1d6-146">-Metadata</span></span>
<span data-ttu-id="0c1d6-147">Os metadados da definição da política.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-147">The metadata for policy definition.</span></span> <span data-ttu-id="0c1d6-148">Pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="0c1d6-148">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="0c1d6-149">-Mode</span><span class="sxs-lookup"><span data-stu-id="0c1d6-149">-Mode</span></span>
<span data-ttu-id="0c1d6-150">O modo da definição de política</span><span class="sxs-lookup"><span data-stu-id="0c1d6-150">The mode of the policy definition</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c1d6-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c1d6-151">-Name</span></span>
<span data-ttu-id="0c1d6-152">Especifica um nome para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-152">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="0c1d6-153">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c1d6-153">-Parameter</span></span>
<span data-ttu-id="0c1d6-154">A declaração Parameters para a definição da política.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-154">The parameters declaration for policy definition.</span></span> <span data-ttu-id="0c1d6-155">Isso pode ser um caminho para um nome de arquivo contendo a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-155">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="0c1d6-156">-Política</span><span class="sxs-lookup"><span data-stu-id="0c1d6-156">-Policy</span></span>
<span data-ttu-id="0c1d6-157">Especifica uma regra de política para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-157">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="0c1d6-158">Você pode especificar o caminho de um arquivo. JSON ou uma cadeia de caracteres que contém a política em formato JSON.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-158">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="0c1d6-159">-Pre</span><span class="sxs-lookup"><span data-stu-id="0c1d6-159">-Pre</span></span>
<span data-ttu-id="0c1d6-160">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-160">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0c1d6-161">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c1d6-161">-SubscriptionId</span></span>
<span data-ttu-id="0c1d6-162">A ID da assinatura da nova definição de política.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-162">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="0c1d6-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1d6-163">CommonParameters</span></span>
<span data-ttu-id="0c1d6-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c1d6-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c1d6-165">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c1d6-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1d6-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c1d6-166">INPUTS</span></span>

## <span data-ttu-id="0c1d6-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c1d6-167">OUTPUTS</span></span>

## <span data-ttu-id="0c1d6-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c1d6-168">NOTES</span></span>

## <span data-ttu-id="0c1d6-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c1d6-169">RELATED LINKS</span></span>

[<span data-ttu-id="0c1d6-170">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0c1d6-170">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="0c1d6-171">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0c1d6-171">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="0c1d6-172">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0c1d6-172">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


