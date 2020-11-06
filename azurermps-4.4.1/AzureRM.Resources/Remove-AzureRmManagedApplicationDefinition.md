---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 2e951452789d57d6d5e126fca80713ef7fd2c584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440188"
---
# <span data-ttu-id="dc028-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="dc028-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="dc028-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc028-102">SYNOPSIS</span></span>
<span data-ttu-id="dc028-103">Remove uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="dc028-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc028-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc028-104">SYNTAX</span></span>

### <span data-ttu-id="dc028-105">O conjunto de parâmetros do nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="dc028-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="dc028-106">Assume</span><span class="sxs-lookup"><span data-stu-id="dc028-106">(Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc028-107">O conjunto de parâmetros de ID de definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="dc028-107">The managed application definition Id parameter set.</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc028-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc028-108">DESCRIPTION</span></span>
<span data-ttu-id="dc028-109">O cmdlet **Remove-AzureRmManagedApplicationDefinition** remove uma definição de aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="dc028-109">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="dc028-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc028-110">EXAMPLES</span></span>

### <span data-ttu-id="dc028-111">Exemplo 1: remover a definição do aplicativo gerenciado por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="dc028-111">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="dc028-112">O primeiro comando obtém uma definição de aplicativo gerenciado chamada myAppDef usando o cmdlet Get-AzureRmManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="dc028-112">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="dc028-113">O comando o armazena na variável $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="dc028-113">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="dc028-114">O segundo comando Remove a definição do aplicativo gerenciado identificada pela propriedade **ResourceId** de $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="dc028-114">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="dc028-115">OS</span><span class="sxs-lookup"><span data-stu-id="dc028-115">PARAMETERS</span></span>

### <span data-ttu-id="dc028-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dc028-116">-ApiVersion</span></span>
<span data-ttu-id="dc028-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="dc028-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="dc028-118">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="dc028-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="dc028-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc028-119">-DefaultProfile</span></span>
<span data-ttu-id="dc028-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc028-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc028-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dc028-121">-Force</span></span>
<span data-ttu-id="dc028-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="dc028-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dc028-123">-ID</span><span class="sxs-lookup"><span data-stu-id="dc028-123">-Id</span></span>
<span data-ttu-id="dc028-124">A ID da definição do aplicativo gerenciado totalmente qualificado, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="dc028-124">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="dc028-125">por exemplo,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="dc028-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc028-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc028-126">-Name</span></span>
<span data-ttu-id="dc028-127">O nome da definição do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="dc028-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc028-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="dc028-128">-Pre</span></span>
<span data-ttu-id="dc028-129">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="dc028-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="dc028-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc028-130">-ResourceGroupName</span></span>
<span data-ttu-id="dc028-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc028-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc028-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dc028-132">-Confirm</span></span>
<span data-ttu-id="dc028-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc028-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc028-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc028-134">-WhatIf</span></span>
<span data-ttu-id="dc028-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc028-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc028-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc028-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc028-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc028-137">CommonParameters</span></span>
<span data-ttu-id="dc028-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc028-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc028-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc028-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc028-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc028-140">INPUTS</span></span>

### <span data-ttu-id="dc028-141">System. String</span><span class="sxs-lookup"><span data-stu-id="dc028-141">System.String</span></span>

## <span data-ttu-id="dc028-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc028-142">OUTPUTS</span></span>

### <span data-ttu-id="dc028-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc028-143">System.Boolean</span></span>

## <span data-ttu-id="dc028-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc028-144">NOTES</span></span>

## <span data-ttu-id="dc028-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc028-145">RELATED LINKS</span></span>

