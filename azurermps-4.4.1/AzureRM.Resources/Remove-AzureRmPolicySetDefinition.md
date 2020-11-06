---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d3b9d8af81f08786536abf0d26b3c4ba2f2d66bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603326"
---
# <span data-ttu-id="eb7af-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="eb7af-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="eb7af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb7af-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7af-103">Remove uma definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="eb7af-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb7af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb7af-104">SYNTAX</span></span>

### <span data-ttu-id="eb7af-105">O conjunto de parâmetros de nome de definição de política.</span><span class="sxs-lookup"><span data-stu-id="eb7af-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="eb7af-106">Assume</span><span class="sxs-lookup"><span data-stu-id="eb7af-106">(Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb7af-107">O conjunto de parâmetros de ID de definição de política.</span><span class="sxs-lookup"><span data-stu-id="eb7af-107">The policy set definition Id parameter set.</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb7af-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb7af-108">DESCRIPTION</span></span>
<span data-ttu-id="eb7af-109">O cmdlet **Remove-AzureRmPolicySetDefinition** remove uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="eb7af-109">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="eb7af-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb7af-110">EXAMPLES</span></span>

### <span data-ttu-id="eb7af-111">Exemplo 1: remover definição do conjunto de políticas por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="eb7af-111">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="eb7af-112">O primeiro comando obtém uma definição de conjunto de políticas usando o cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="eb7af-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="eb7af-113">O comando o armazena na variável $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="eb7af-113">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="eb7af-114">O segundo comando Remove a definição do conjunto de políticas identificado pela propriedade **ResourceId** de $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="eb7af-114">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="eb7af-115">OS</span><span class="sxs-lookup"><span data-stu-id="eb7af-115">PARAMETERS</span></span>

### <span data-ttu-id="eb7af-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="eb7af-116">-ApiVersion</span></span>
<span data-ttu-id="eb7af-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="eb7af-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="eb7af-118">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="eb7af-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="eb7af-119">-Force</span><span class="sxs-lookup"><span data-stu-id="eb7af-119">-Force</span></span>
<span data-ttu-id="eb7af-120">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="eb7af-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eb7af-121">-ID</span><span class="sxs-lookup"><span data-stu-id="eb7af-121">-Id</span></span>
<span data-ttu-id="eb7af-122">A ID da definição do conjunto de políticas totalmente qualificadas, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="eb7af-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="eb7af-123">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="eb7af-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="eb7af-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb7af-124">-Name</span></span>
<span data-ttu-id="eb7af-125">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="eb7af-125">The policy set definition name.</span></span>

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

### <span data-ttu-id="eb7af-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="eb7af-126">-Pre</span></span>
<span data-ttu-id="eb7af-127">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="eb7af-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="eb7af-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="eb7af-128">-Confirm</span></span>
<span data-ttu-id="eb7af-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb7af-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb7af-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb7af-130">-WhatIf</span></span>
<span data-ttu-id="eb7af-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eb7af-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb7af-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eb7af-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb7af-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7af-133">-DefaultProfile</span></span>
<span data-ttu-id="eb7af-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb7af-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb7af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7af-135">CommonParameters</span></span>
<span data-ttu-id="eb7af-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb7af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7af-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb7af-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7af-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb7af-138">INPUTS</span></span>

### <span data-ttu-id="eb7af-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eb7af-139">System.String</span></span>

## <span data-ttu-id="eb7af-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb7af-140">OUTPUTS</span></span>

### <span data-ttu-id="eb7af-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb7af-141">System.Boolean</span></span>

## <span data-ttu-id="eb7af-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb7af-142">NOTES</span></span>

## <span data-ttu-id="eb7af-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb7af-143">RELATED LINKS</span></span>

