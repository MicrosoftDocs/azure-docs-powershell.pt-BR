---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 41f59b46595d45932010b1fcbedae07cdeca5f78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887858"
---
# <span data-ttu-id="6e5d9-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="6e5d9-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="6e5d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="6e5d9-103">Remove um aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="6e5d9-103">Removes a managed application</span></span>

## <span data-ttu-id="6e5d9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6e5d9-104">SYNTAX</span></span>

### <span data-ttu-id="6e5d9-105">RemoveByNameAndResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6e5d9-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e5d9-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="6e5d9-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e5d9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6e5d9-107">DESCRIPTION</span></span>
<span data-ttu-id="6e5d9-108">O cmdlet **Remove-AzManagedApplication** remove um aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="6e5d9-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="6e5d9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e5d9-109">EXAMPLES</span></span>

### <span data-ttu-id="6e5d9-110">Exemplo 1: Remover aplicativo gerenciado por ID de recurso</span><span class="sxs-lookup"><span data-stu-id="6e5d9-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="6e5d9-111">O primeiro comando obtém um aplicativo gerenciado chamado myApp usando Get-AzManagedApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="6e5d9-112">O comando armazena-o na variável $Application.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="6e5d9-113">O segundo comando remove o aplicativo gerenciado identificado pela **propriedade ResourceId** do $Application.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="6e5d9-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6e5d9-114">PARAMETERS</span></span>

### <span data-ttu-id="6e5d9-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6e5d9-115">-ApiVersion</span></span>
<span data-ttu-id="6e5d9-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6e5d9-117">Se não for especificada, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6e5d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e5d9-118">-DefaultProfile</span></span>
<span data-ttu-id="6e5d9-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e5d9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6e5d9-120">-Force</span></span>
<span data-ttu-id="6e5d9-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6e5d9-122">-Id</span><span class="sxs-lookup"><span data-stu-id="6e5d9-122">-Id</span></span>
<span data-ttu-id="6e5d9-123">A ID do aplicativo gerenciado totalmente qualificado, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="6e5d9-124">por exemplo, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="6e5d9-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e5d9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6e5d9-125">-Name</span></span>
<span data-ttu-id="6e5d9-126">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e5d9-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="6e5d9-127">-Pre</span></span>
<span data-ttu-id="6e5d9-128">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6e5d9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e5d9-129">-ResourceGroupName</span></span>
<span data-ttu-id="6e5d9-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e5d9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e5d9-131">-Confirm</span></span>
<span data-ttu-id="6e5d9-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e5d9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e5d9-133">-WhatIf</span></span>
<span data-ttu-id="6e5d9-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e5d9-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e5d9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e5d9-136">CommonParameters</span></span>
<span data-ttu-id="6e5d9-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e5d9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e5d9-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e5d9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e5d9-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e5d9-139">INPUTS</span></span>

### <span data-ttu-id="6e5d9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6e5d9-140">System.String</span></span>

## <span data-ttu-id="6e5d9-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6e5d9-141">OUTPUTS</span></span>

### <span data-ttu-id="6e5d9-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e5d9-142">System.Boolean</span></span>

## <span data-ttu-id="6e5d9-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="6e5d9-143">NOTES</span></span>

## <span data-ttu-id="6e5d9-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e5d9-144">RELATED LINKS</span></span>
