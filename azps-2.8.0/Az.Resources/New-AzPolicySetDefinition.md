---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 838fe6f4ed7ff1e69a6bdf99a8816f00fc0ab019
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773342"
---
# <span data-ttu-id="2d09b-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="2d09b-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="2d09b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d09b-102">SYNOPSIS</span></span>
<span data-ttu-id="2d09b-103">Cria uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="2d09b-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="2d09b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d09b-104">SYNTAX</span></span>

### <span data-ttu-id="2d09b-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2d09b-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d09b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d09b-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d09b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d09b-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d09b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d09b-108">DESCRIPTION</span></span>
<span data-ttu-id="2d09b-109">O cmdlet **New-AzPolicySetDefinition** cria uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="2d09b-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="2d09b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d09b-110">EXAMPLES</span></span>

### <span data-ttu-id="2d09b-111">Exemplo 1: criar uma definição de conjunto de políticas com metadados usando um arquivo de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="2d09b-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="2d09b-112">Esse comando cria uma definição de conjunto de políticas denominada VMPolicySetDefinition com metadados indicando que sua categoria é "máquina virtual" que contém as definições de política especificadas em C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="2d09b-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="2d09b-113">O conteúdo de exemplo do VMPolicy.jsativado é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="2d09b-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="2d09b-114">Exemplo 2: criar uma definição de conjunto de políticas com parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d09b-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="2d09b-115">Esse comando cria uma definição de conjunto de políticas parametrizada chamada VMPolicySetDefinition que contém as definições de política especificadas em C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="2d09b-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="2d09b-116">O conteúdo de exemplo do VMPolicy.jsativado é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="2d09b-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="2d09b-117">OS</span><span class="sxs-lookup"><span data-stu-id="2d09b-117">PARAMETERS</span></span>

### <span data-ttu-id="2d09b-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2d09b-118">-ApiVersion</span></span>
<span data-ttu-id="2d09b-119">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="2d09b-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2d09b-120">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="2d09b-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2d09b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d09b-121">-DefaultProfile</span></span>
<span data-ttu-id="2d09b-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2d09b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d09b-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="2d09b-123">-Description</span></span>
<span data-ttu-id="2d09b-124">A descrição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="2d09b-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="2d09b-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2d09b-125">-DisplayName</span></span>
<span data-ttu-id="2d09b-126">O nome de exibição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="2d09b-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="2d09b-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="2d09b-127">-ManagementGroupName</span></span>
<span data-ttu-id="2d09b-128">O nome do grupo de gerenciamento da nova definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="2d09b-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="2d09b-129">-Metadados</span><span class="sxs-lookup"><span data-stu-id="2d09b-129">-Metadata</span></span>
<span data-ttu-id="2d09b-130">Os metadados da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="2d09b-130">The metadata for policy set definition.</span></span> <span data-ttu-id="2d09b-131">Pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="2d09b-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="2d09b-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d09b-132">-Name</span></span>
<span data-ttu-id="2d09b-133">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="2d09b-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="2d09b-134">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d09b-134">-Parameter</span></span>
<span data-ttu-id="2d09b-135">A declaração Parameters para a definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="2d09b-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="2d09b-136">Isso pode ser um caminho para um nome de arquivo contendo a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2d09b-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="2d09b-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d09b-137">-PolicyDefinition</span></span>
<span data-ttu-id="2d09b-138">As definições de política.</span><span class="sxs-lookup"><span data-stu-id="2d09b-138">The policy definitions.</span></span> <span data-ttu-id="2d09b-139">Pode ser um caminho para um nome de arquivo que contenha as definições da política ou as definições da política como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2d09b-139">This can either be a path to a file name containing the policy definitions, or the policy definitions as string.</span></span>

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

### <span data-ttu-id="2d09b-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="2d09b-140">-Pre</span></span>
<span data-ttu-id="2d09b-141">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="2d09b-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2d09b-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d09b-142">-SubscriptionId</span></span>
<span data-ttu-id="2d09b-143">A ID da assinatura da nova definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="2d09b-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="2d09b-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2d09b-144">-Confirm</span></span>
<span data-ttu-id="2d09b-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d09b-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d09b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d09b-146">-WhatIf</span></span>
<span data-ttu-id="2d09b-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d09b-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d09b-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d09b-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d09b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d09b-149">CommonParameters</span></span>
<span data-ttu-id="2d09b-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d09b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d09b-151">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d09b-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d09b-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d09b-152">INPUTS</span></span>

### <span data-ttu-id="2d09b-153">System. String</span><span class="sxs-lookup"><span data-stu-id="2d09b-153">System.String</span></span>

### <span data-ttu-id="2d09b-154">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2d09b-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2d09b-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d09b-155">OUTPUTS</span></span>

### <span data-ttu-id="2d09b-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2d09b-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2d09b-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d09b-157">NOTES</span></span>

## <span data-ttu-id="2d09b-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d09b-158">RELATED LINKS</span></span>
