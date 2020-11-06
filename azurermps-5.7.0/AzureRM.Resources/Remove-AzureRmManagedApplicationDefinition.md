---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 3479a3d720554f0c062e2410d0c4b838f655909a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609947"
---
# <span data-ttu-id="112e2-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="112e2-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="112e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="112e2-102">SYNOPSIS</span></span>
<span data-ttu-id="112e2-103">Remove uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="112e2-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="112e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="112e2-104">SYNTAX</span></span>

### <span data-ttu-id="112e2-105">RemoveByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="112e2-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="112e2-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="112e2-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="112e2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="112e2-107">DESCRIPTION</span></span>
<span data-ttu-id="112e2-108">O cmdlet **Remove-AzureRmManagedApplicationDefinition** remove uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="112e2-108">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="112e2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="112e2-109">EXAMPLES</span></span>

### <span data-ttu-id="112e2-110">Exemplo 1: remover a definição do aplicativo gerenciado por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="112e2-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="112e2-111">O primeiro comando obtém uma definição de aplicativo gerenciado chamada myAppDef usando o cmdlet Get-AzureRmManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="112e2-111">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="112e2-112">O comando o armazena na variável $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="112e2-112">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="112e2-113">O segundo comando Remove a definição do aplicativo gerenciado identificada pela propriedade **ResourceId** de $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="112e2-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="112e2-114">OS</span><span class="sxs-lookup"><span data-stu-id="112e2-114">PARAMETERS</span></span>

### <span data-ttu-id="112e2-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="112e2-115">-ApiVersion</span></span>
<span data-ttu-id="112e2-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="112e2-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="112e2-117">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="112e2-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="112e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112e2-118">-DefaultProfile</span></span>
<span data-ttu-id="112e2-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="112e2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="112e2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="112e2-120">-Force</span></span>
<span data-ttu-id="112e2-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="112e2-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="112e2-122">-ID</span><span class="sxs-lookup"><span data-stu-id="112e2-122">-Id</span></span>
<span data-ttu-id="112e2-123">A ID da definição do aplicativo gerenciado totalmente qualificado, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="112e2-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="112e2-124">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="112e2-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="112e2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="112e2-125">-Name</span></span>
<span data-ttu-id="112e2-126">O nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="112e2-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="112e2-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="112e2-127">-Pre</span></span>
<span data-ttu-id="112e2-128">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="112e2-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="112e2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="112e2-129">-ResourceGroupName</span></span>
<span data-ttu-id="112e2-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="112e2-130">The resource group name.</span></span>

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

### <span data-ttu-id="112e2-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="112e2-131">-Confirm</span></span>
<span data-ttu-id="112e2-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="112e2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="112e2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="112e2-133">-WhatIf</span></span>
<span data-ttu-id="112e2-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="112e2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="112e2-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="112e2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="112e2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112e2-136">CommonParameters</span></span>
<span data-ttu-id="112e2-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="112e2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112e2-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="112e2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112e2-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="112e2-139">INPUTS</span></span>

### <span data-ttu-id="112e2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="112e2-140">System.String</span></span>

## <span data-ttu-id="112e2-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="112e2-141">OUTPUTS</span></span>

### <span data-ttu-id="112e2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="112e2-142">System.Boolean</span></span>

## <span data-ttu-id="112e2-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="112e2-143">NOTES</span></span>

## <span data-ttu-id="112e2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="112e2-144">RELATED LINKS</span></span>
