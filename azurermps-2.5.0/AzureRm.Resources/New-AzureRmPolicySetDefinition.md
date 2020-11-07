---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicysetdefinition
schema: 2.0.0
ms.openlocfilehash: 701c7e11a5b76b2071c5810f8c6948c6024eb1ae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786234"
---
# <span data-ttu-id="b6ed0-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b6ed0-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="b6ed0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ed0-103">Cria uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6ed0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6ed0-104">SYNTAX</span></span>

### <span data-ttu-id="b6ed0-105">NameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6ed0-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6ed0-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6ed0-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6ed0-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6ed0-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6ed0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6ed0-108">DESCRIPTION</span></span>
<span data-ttu-id="b6ed0-109">O cmdlet **New-AzureRmPolicySetDefinition** cria uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-109">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="b6ed0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6ed0-110">EXAMPLES</span></span>

### <span data-ttu-id="b6ed0-111">Exemplo 1: criar uma definição de conjunto de políticas usando um arquivo de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="b6ed0-111">Example 1: Create a policy set definition by using a policy set file</span></span>
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
PS C:\> New-AzureRmPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="b6ed0-112">Esse comando cria uma definição de conjunto de políticas chamada VMPolicyDefinition que contém as definições de política especificadas em C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-112">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="b6ed0-113">O conteúdo de exemplo do VMPolicy.jsativado é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="b6ed0-114">Exemplo 2: criar uma definição de conjunto de políticas com parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6ed0-114">Example 2: Create a parameterized policy set definition</span></span>
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
PS C:\> New-AzureRmPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="b6ed0-115">Esse comando cria uma definição de conjunto de políticas parametrizada chamada VMPolicyDefinition que contém as definições de política especificadas em C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-115">This command creates a parameterized policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="b6ed0-116">O conteúdo de exemplo do VMPolicy.jsativado é fornecido acima.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="b6ed0-117">OS</span><span class="sxs-lookup"><span data-stu-id="b6ed0-117">PARAMETERS</span></span>

### <span data-ttu-id="b6ed0-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b6ed0-118">-ApiVersion</span></span>
<span data-ttu-id="b6ed0-119">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b6ed0-120">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b6ed0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ed0-121">-DefaultProfile</span></span>
<span data-ttu-id="b6ed0-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b6ed0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6ed0-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="b6ed0-123">-Description</span></span>
<span data-ttu-id="b6ed0-124">A descrição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="b6ed0-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b6ed0-125">-DisplayName</span></span>
<span data-ttu-id="b6ed0-126">O nome de exibição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="b6ed0-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ed0-127">-ManagementGroupName</span></span>
<span data-ttu-id="b6ed0-128">O nome do grupo de gerenciamento da nova definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="b6ed0-129">-Metadados</span><span class="sxs-lookup"><span data-stu-id="b6ed0-129">-Metadata</span></span>
<span data-ttu-id="b6ed0-130">Os metadados da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-130">The metadata for policy set definition.</span></span> <span data-ttu-id="b6ed0-131">Pode ser um caminho para um nome de arquivo que contém os metadados ou os metadados como cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="b6ed0-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="b6ed0-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6ed0-132">-Name</span></span>
<span data-ttu-id="b6ed0-133">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="b6ed0-134">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6ed0-134">-Parameter</span></span>
<span data-ttu-id="b6ed0-135">A declaração Parameters para a definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="b6ed0-136">Isso pode ser um caminho para um nome de arquivo contendo a declaração Parameters ou a declaração Parameters como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="b6ed0-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b6ed0-137">-PolicyDefinition</span></span>
<span data-ttu-id="b6ed0-138">Definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-138">The policy set definition.</span></span> <span data-ttu-id="b6ed0-139">Pode ser um caminho para um nome de arquivo que contenha as definições da política ou a definição do conjunto de políticas como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-139">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="b6ed0-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="b6ed0-140">-Pre</span></span>
<span data-ttu-id="b6ed0-141">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b6ed0-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6ed0-142">-SubscriptionId</span></span>
<span data-ttu-id="b6ed0-143">A ID da assinatura da nova definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="b6ed0-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b6ed0-144">-Confirm</span></span>
<span data-ttu-id="b6ed0-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6ed0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6ed0-146">-WhatIf</span></span>
<span data-ttu-id="b6ed0-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6ed0-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6ed0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ed0-149">CommonParameters</span></span>
<span data-ttu-id="b6ed0-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6ed0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ed0-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6ed0-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ed0-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6ed0-152">INPUTS</span></span>

### <span data-ttu-id="b6ed0-153">System. String</span><span class="sxs-lookup"><span data-stu-id="b6ed0-153">System.String</span></span>

### <span data-ttu-id="b6ed0-154">System. Nullable ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b6ed0-154">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b6ed0-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6ed0-155">OUTPUTS</span></span>

### <span data-ttu-id="b6ed0-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b6ed0-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b6ed0-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6ed0-157">NOTES</span></span>

## <span data-ttu-id="b6ed0-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6ed0-158">RELATED LINKS</span></span>
