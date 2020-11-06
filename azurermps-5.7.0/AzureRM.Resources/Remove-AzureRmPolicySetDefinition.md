---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: fa96d686d66f9ef94322896974dc4dd3b81ad154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431624"
---
# <span data-ttu-id="6e8c7-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="6e8c7-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="6e8c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8c7-103">Remove uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e8c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e8c7-104">SYNTAX</span></span>

### <span data-ttu-id="6e8c7-105">RemoveByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="6e8c7-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e8c7-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="6e8c7-106">RemoveById</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e8c7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e8c7-107">DESCRIPTION</span></span>
<span data-ttu-id="6e8c7-108">O cmdlet **Remove-AzureRmPolicySetDefinition** remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-108">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="6e8c7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e8c7-109">EXAMPLES</span></span>

### <span data-ttu-id="6e8c7-110">Exemplo 1: remover definição do conjunto de políticas por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="6e8c7-110">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="6e8c7-111">O primeiro comando obtém uma definição de conjunto de políticas usando o cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="6e8c7-112">O comando o armazena na variável $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-112">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="6e8c7-113">O segundo comando Remove a definição do conjunto de políticas identificado pela propriedade **ResourceId** de $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-113">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="6e8c7-114">OS</span><span class="sxs-lookup"><span data-stu-id="6e8c7-114">PARAMETERS</span></span>

### <span data-ttu-id="6e8c7-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6e8c7-115">-ApiVersion</span></span>
<span data-ttu-id="6e8c7-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6e8c7-117">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6e8c7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e8c7-118">-DefaultProfile</span></span>
<span data-ttu-id="6e8c7-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6e8c7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e8c7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6e8c7-120">-Force</span></span>
<span data-ttu-id="6e8c7-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6e8c7-122">-ID</span><span class="sxs-lookup"><span data-stu-id="6e8c7-122">-Id</span></span>
<span data-ttu-id="6e8c7-123">A ID da definição do conjunto de políticas totalmente qualificadas, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-123">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="6e8c7-124">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="6e8c7-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8c7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e8c7-125">-Name</span></span>
<span data-ttu-id="6e8c7-126">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-126">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8c7-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="6e8c7-127">-Pre</span></span>
<span data-ttu-id="6e8c7-128">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6e8c7-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6e8c7-129">-Confirm</span></span>
<span data-ttu-id="6e8c7-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e8c7-131">-WhatIf</span></span>
<span data-ttu-id="6e8c7-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e8c7-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8c7-134">CommonParameters</span></span>
<span data-ttu-id="6e8c7-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e8c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8c7-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e8c7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8c7-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e8c7-137">INPUTS</span></span>

### <span data-ttu-id="6e8c7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6e8c7-138">System.String</span></span>

## <span data-ttu-id="6e8c7-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e8c7-139">OUTPUTS</span></span>

### <span data-ttu-id="6e8c7-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e8c7-140">System.Boolean</span></span>

## <span data-ttu-id="6e8c7-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e8c7-141">NOTES</span></span>

## <span data-ttu-id="6e8c7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e8c7-142">RELATED LINKS</span></span>
