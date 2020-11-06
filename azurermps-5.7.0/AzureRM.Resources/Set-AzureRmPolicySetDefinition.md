---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 16a27c7756a25c4b8e4270a0c363f8a04528d12c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426612"
---
# <span data-ttu-id="b2c4d-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b2c4d-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="b2c4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c4d-103">Modifica uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="b2c4d-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2c4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2c4d-104">SYNTAX</span></span>

### <span data-ttu-id="b2c4d-105">SetByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="b2c4d-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2c4d-106">SetById</span><span class="sxs-lookup"><span data-stu-id="b2c4d-106">SetById</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c4d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2c4d-107">DESCRIPTION</span></span>
<span data-ttu-id="b2c4d-108">O cmdlet **set-AzureRmPolicySetDefinition** modifica uma definição de política.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-108">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="b2c4d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2c4d-109">EXAMPLES</span></span>

### <span data-ttu-id="b2c4d-110">Exemplo 1: atualizar a descrição de uma definição de conjunto de políticas</span><span class="sxs-lookup"><span data-stu-id="b2c4d-110">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="b2c4d-111">O primeiro comando obtém uma definição de conjunto de políticas usando o cmdlet Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="b2c4d-112">O comando armazena esse objeto na variável $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-112">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="b2c4d-113">O segundo comando atualiza a descrição da definição do conjunto de políticas identificada pela propriedade **ResourceId** de $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-113">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="b2c4d-114">OS</span><span class="sxs-lookup"><span data-stu-id="b2c4d-114">PARAMETERS</span></span>

### <span data-ttu-id="b2c4d-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b2c4d-115">-ApiVersion</span></span>
<span data-ttu-id="b2c4d-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b2c4d-117">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b2c4d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c4d-118">-DefaultProfile</span></span>
<span data-ttu-id="b2c4d-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b2c4d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2c4d-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="b2c4d-120">-Description</span></span>
<span data-ttu-id="b2c4d-121">A descrição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-121">The description for policy set definition.</span></span>

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

### <span data-ttu-id="b2c4d-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b2c4d-122">-DisplayName</span></span>
<span data-ttu-id="b2c4d-123">O nome de exibição da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-123">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="b2c4d-124">-ID</span><span class="sxs-lookup"><span data-stu-id="b2c4d-124">-Id</span></span>
<span data-ttu-id="b2c4d-125">A ID da definição da política totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-125">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="b2c4d-126">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b2c4d-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c4d-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2c4d-127">-Name</span></span>
<span data-ttu-id="b2c4d-128">O nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-128">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2c4d-129">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b2c4d-129">-PolicyDefinition</span></span>
<span data-ttu-id="b2c4d-130">Definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-130">The policy set definition.</span></span> <span data-ttu-id="b2c4d-131">Pode ser um caminho para um nome de arquivo que contenha as definições da política ou a definição do conjunto de políticas como cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-131">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="b2c4d-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="b2c4d-132">-Pre</span></span>
<span data-ttu-id="b2c4d-133">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b2c4d-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2c4d-134">-Confirm</span></span>
<span data-ttu-id="b2c4d-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c4d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c4d-136">-WhatIf</span></span>
<span data-ttu-id="b2c4d-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2c4d-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c4d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c4d-139">CommonParameters</span></span>
<span data-ttu-id="b2c4d-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c4d-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c4d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c4d-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2c4d-142">INPUTS</span></span>

### <span data-ttu-id="b2c4d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b2c4d-143">System.String</span></span>

## <span data-ttu-id="b2c4d-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2c4d-144">OUTPUTS</span></span>

### <span data-ttu-id="b2c4d-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b2c4d-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b2c4d-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2c4d-146">NOTES</span></span>

## <span data-ttu-id="b2c4d-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2c4d-147">RELATED LINKS</span></span>
