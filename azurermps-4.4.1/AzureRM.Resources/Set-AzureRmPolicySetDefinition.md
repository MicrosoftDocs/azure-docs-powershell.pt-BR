---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: a09dae99d7a2b6e08dd255cc19b859aec89808f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430664"
---
# <span data-ttu-id="87b87-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="87b87-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="87b87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87b87-102">SYNOPSIS</span></span>
<span data-ttu-id="87b87-103">Modifica uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="87b87-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87b87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87b87-104">SYNTAX</span></span>

### <span data-ttu-id="87b87-105">O conjunto de parâmetros de nome de definição de política.</span><span class="sxs-lookup"><span data-stu-id="87b87-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="87b87-106">Assume</span><span class="sxs-lookup"><span data-stu-id="87b87-106">(Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87b87-107">O conjunto de parâmetros de ID de definição de política.</span><span class="sxs-lookup"><span data-stu-id="87b87-107">The policy set definition Id parameter set.</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87b87-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87b87-108">DESCRIPTION</span></span>
<span data-ttu-id="87b87-109">O cmdlet **set-AzureRmPolicySetDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="87b87-109">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="87b87-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87b87-110">EXAMPLES</span></span>

### <span data-ttu-id="87b87-111">Exemplo 1: atualizar a descrição de uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="87b87-111">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="87b87-112">O primeiro comando obtém uma definição de conjunto de políticas usando o cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="87b87-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="87b87-113">O comando armazena esse objeto na variável $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="87b87-113">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="87b87-114">O segundo comando atualiza a descrição da definição do conjunto de políticas identificada pela propriedade **ResourceId** de $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="87b87-114">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="87b87-115">OS</span><span class="sxs-lookup"><span data-stu-id="87b87-115">PARAMETERS</span></span>

### <span data-ttu-id="87b87-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="87b87-116">-ApiVersion</span></span>
<span data-ttu-id="87b87-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="87b87-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="87b87-118">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="87b87-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="87b87-119">-Descrição</span><span class="sxs-lookup"><span data-stu-id="87b87-119">-Description</span></span>
<span data-ttu-id="87b87-120">A descrição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="87b87-120">The description for policy set definition.</span></span>

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

### <span data-ttu-id="87b87-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="87b87-121">-DisplayName</span></span>
<span data-ttu-id="87b87-122">O nome de exibição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="87b87-122">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="87b87-123">-ID</span><span class="sxs-lookup"><span data-stu-id="87b87-123">-Id</span></span>
<span data-ttu-id="87b87-124">A ID da definição da política totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="87b87-124">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="87b87-125">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="87b87-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87b87-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="87b87-126">-Name</span></span>
<span data-ttu-id="87b87-127">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="87b87-127">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87b87-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="87b87-128">-PolicyDefinition</span></span>
<span data-ttu-id="87b87-129">Definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="87b87-129">The policy set definition.</span></span> <span data-ttu-id="87b87-130">Pode ser um caminho para um nome de arquivo que contenha as definições da política ou a definição do conjunto de políticas como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="87b87-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="87b87-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="87b87-131">-Pre</span></span>
<span data-ttu-id="87b87-132">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="87b87-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="87b87-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="87b87-133">-Confirm</span></span>
<span data-ttu-id="87b87-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87b87-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87b87-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b87-135">-DefaultProfile</span></span>
<span data-ttu-id="87b87-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87b87-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87b87-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87b87-137">-WhatIf</span></span>
<span data-ttu-id="87b87-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="87b87-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87b87-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87b87-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87b87-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b87-140">CommonParameters</span></span>
<span data-ttu-id="87b87-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b87-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b87-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87b87-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b87-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87b87-143">INPUTS</span></span>

### <span data-ttu-id="87b87-144">System. String</span><span class="sxs-lookup"><span data-stu-id="87b87-144">System.String</span></span>

## <span data-ttu-id="87b87-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87b87-145">OUTPUTS</span></span>

### <span data-ttu-id="87b87-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="87b87-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="87b87-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87b87-147">NOTES</span></span>

## <span data-ttu-id="87b87-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87b87-148">RELATED LINKS</span></span>

