---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 22c8ea5c93a301796b2b42184a54744e9841163d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93601955"
---
# <span data-ttu-id="71b05-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71b05-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="71b05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71b05-102">SYNOPSIS</span></span>
<span data-ttu-id="71b05-103">Cria uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="71b05-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71b05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71b05-104">SYNTAX</span></span>

### <span data-ttu-id="71b05-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="71b05-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="71b05-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="71b05-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="71b05-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71b05-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="71b05-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71b05-108">DESCRIPTION</span></span>
<span data-ttu-id="71b05-109">O cmdlet **New-AzureRmPolicyDefinition** cria uma definição de política que inclui uma regra de política no formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="71b05-109">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="71b05-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71b05-110">EXAMPLES</span></span>

### <span data-ttu-id="71b05-111">Exemplo 1: criar uma definição de política usando um arquivo de política</span><span class="sxs-lookup"><span data-stu-id="71b05-111">Example 1: Create a policy definition by using a policy file</span></span>
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
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="71b05-112">Esse comando cria uma definição de política chamada LocationDefinition que contém a regra de política especificada em C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="71b05-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="71b05-113">O conteúdo de exemplo para o LocationPolicy.jsem arquivo é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="71b05-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="71b05-114">Exemplo 2: criar uma definição de política com parâmetros usando parâmetros embutidos</span><span class="sxs-lookup"><span data-stu-id="71b05-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="71b05-115">Esse comando cria uma definição de política chamada LocationDefinition que contém a regra de política especificada em C:\LocationPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="71b05-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="71b05-116">A definição de parâmetro para a regra de política é fornecida embutida.</span><span class="sxs-lookup"><span data-stu-id="71b05-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="71b05-117">Exemplo 3: criar uma definição de política embutida em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="71b05-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="71b05-118">Esse comando cria uma definição de política chamada VMPolicyDefinition no grupo de gerenciamento Dept42.</span><span class="sxs-lookup"><span data-stu-id="71b05-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="71b05-119">O comando especifica a política como uma cadeia de caracteres em formato JSON válido.</span><span class="sxs-lookup"><span data-stu-id="71b05-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="71b05-120">Exemplo 4: criar uma definição de política embutida com metadados</span><span class="sxs-lookup"><span data-stu-id="71b05-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="71b05-121">Esse comando cria uma definição de política chamada VMPolicyDefinition com metadados indicando que sua categoria é "máquina virtual".</span><span class="sxs-lookup"><span data-stu-id="71b05-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="71b05-122">O comando especifica a política como uma cadeia de caracteres em formato JSON válido.</span><span class="sxs-lookup"><span data-stu-id="71b05-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="71b05-123">OS</span><span class="sxs-lookup"><span data-stu-id="71b05-123">PARAMETERS</span></span>

### <span data-ttu-id="71b05-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="71b05-124">-ApiVersion</span></span>
<span data-ttu-id="71b05-125">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="71b05-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="71b05-126">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="71b05-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="71b05-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b05-127">-DefaultProfile</span></span>
<span data-ttu-id="71b05-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="71b05-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b05-129">-Descrição</span><span class="sxs-lookup"><span data-stu-id="71b05-129">-Description</span></span>
<span data-ttu-id="71b05-130">Especifica uma descrição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="71b05-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="71b05-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="71b05-131">-DisplayName</span></span>
<span data-ttu-id="71b05-132">Especifica um nome de exibição para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="71b05-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="71b05-133">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="71b05-133">-InformationAction</span></span>
<span data-ttu-id="71b05-134">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="71b05-134">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="71b05-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="71b05-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71b05-136">Contínuo</span><span class="sxs-lookup"><span data-stu-id="71b05-136">Continue</span></span>
- <span data-ttu-id="71b05-137">Ignorar</span><span class="sxs-lookup"><span data-stu-id="71b05-137">Ignore</span></span>
- <span data-ttu-id="71b05-138">Inquire</span><span class="sxs-lookup"><span data-stu-id="71b05-138">Inquire</span></span>
- <span data-ttu-id="71b05-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="71b05-139">SilentlyContinue</span></span>
- <span data-ttu-id="71b05-140">Finaliza</span><span class="sxs-lookup"><span data-stu-id="71b05-140">Stop</span></span>
- <span data-ttu-id="71b05-141">Suspensão</span><span class="sxs-lookup"><span data-stu-id="71b05-141">Suspend</span></span>

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

### <span data-ttu-id="71b05-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="71b05-142">-InformationVariable</span></span>
<span data-ttu-id="71b05-143">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="71b05-143">Specifies an information variable.</span></span>

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

### <span data-ttu-id="71b05-144">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="71b05-144">-ManagementGroupName</span></span>
<span data-ttu-id="71b05-145">O nome do grupo Gerenciamento da nova definição de política.</span><span class="sxs-lookup"><span data-stu-id="71b05-145">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="71b05-146">-Metadados</span><span class="sxs-lookup"><span data-stu-id="71b05-146">-Metadata</span></span>
<span data-ttu-id="71b05-147">Os metadados da definição da política.</span><span class="sxs-lookup"><span data-stu-id="71b05-147">The metadata for policy definition.</span></span> <span data-ttu-id="71b05-148">Pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="71b05-148">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="71b05-149">-Mode</span><span class="sxs-lookup"><span data-stu-id="71b05-149">-Mode</span></span>
<span data-ttu-id="71b05-150">O modo da definição de política</span><span class="sxs-lookup"><span data-stu-id="71b05-150">The mode of the policy definition</span></span>

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

### <span data-ttu-id="71b05-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="71b05-151">-Name</span></span>
<span data-ttu-id="71b05-152">Especifica um nome para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="71b05-152">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="71b05-153">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="71b05-153">-Parameter</span></span>
<span data-ttu-id="71b05-154">A declaração Parameters para a definição da política.</span><span class="sxs-lookup"><span data-stu-id="71b05-154">The parameters declaration for policy definition.</span></span> <span data-ttu-id="71b05-155">Isso pode ser um caminho para um nome de arquivo contendo a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="71b05-155">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="71b05-156">-Política</span><span class="sxs-lookup"><span data-stu-id="71b05-156">-Policy</span></span>
<span data-ttu-id="71b05-157">Especifica uma regra de política para a definição de política.</span><span class="sxs-lookup"><span data-stu-id="71b05-157">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="71b05-158">Você pode especificar o caminho de um arquivo. JSON ou uma cadeia de caracteres que contém a política em formato JSON.</span><span class="sxs-lookup"><span data-stu-id="71b05-158">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="71b05-159">-Pre</span><span class="sxs-lookup"><span data-stu-id="71b05-159">-Pre</span></span>
<span data-ttu-id="71b05-160">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="71b05-160">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="71b05-161">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71b05-161">-SubscriptionId</span></span>
<span data-ttu-id="71b05-162">A ID da assinatura da nova definição de política.</span><span class="sxs-lookup"><span data-stu-id="71b05-162">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="71b05-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b05-163">CommonParameters</span></span>
<span data-ttu-id="71b05-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b05-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b05-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71b05-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b05-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71b05-166">INPUTS</span></span>

## <span data-ttu-id="71b05-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71b05-167">OUTPUTS</span></span>

## <span data-ttu-id="71b05-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71b05-168">NOTES</span></span>

## <span data-ttu-id="71b05-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71b05-169">RELATED LINKS</span></span>

[<span data-ttu-id="71b05-170">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71b05-170">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="71b05-171">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71b05-171">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="71b05-172">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71b05-172">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


