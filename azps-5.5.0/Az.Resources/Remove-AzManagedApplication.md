---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113309"
---
# <span data-ttu-id="52da2-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="52da2-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="52da2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52da2-102">SYNOPSIS</span></span>
<span data-ttu-id="52da2-103">Remove um aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="52da2-103">Removes a managed application</span></span>

## <span data-ttu-id="52da2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52da2-104">SYNTAX</span></span>

### <span data-ttu-id="52da2-105">RemoveByNameAndResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="52da2-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52da2-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="52da2-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52da2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="52da2-107">DESCRIPTION</span></span>
<span data-ttu-id="52da2-108">O cmdlet **Remove-AzManagedApplication** remove um aplicativo gerenciado</span><span class="sxs-lookup"><span data-stu-id="52da2-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="52da2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="52da2-109">EXAMPLES</span></span>

### <span data-ttu-id="52da2-110">Exemplo 1: Remover aplicativo gerenciado por ID de recurso</span><span class="sxs-lookup"><span data-stu-id="52da2-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="52da2-111">O primeiro comando obtém um aplicativo gerenciado chamado myApp usando Get-AzManagedApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52da2-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="52da2-112">O comando o armazena na variável $Application dados.</span><span class="sxs-lookup"><span data-stu-id="52da2-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="52da2-113">O segundo comando remove o aplicativo gerenciado identificado pela propriedade **ResourceId** do $Application.</span><span class="sxs-lookup"><span data-stu-id="52da2-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="52da2-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52da2-114">PARAMETERS</span></span>

### <span data-ttu-id="52da2-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="52da2-115">-ApiVersion</span></span>
<span data-ttu-id="52da2-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="52da2-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="52da2-117">Se não especificado, a versão da API será determinada automaticamente como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="52da2-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="52da2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52da2-118">-DefaultProfile</span></span>
<span data-ttu-id="52da2-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="52da2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52da2-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="52da2-120">-Force</span></span>
<span data-ttu-id="52da2-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="52da2-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="52da2-122">-ID</span><span class="sxs-lookup"><span data-stu-id="52da2-122">-Id</span></span>
<span data-ttu-id="52da2-123">A ID de aplicativo gerenciado totalmente qualificada, incluindo a assinatura.</span><span class="sxs-lookup"><span data-stu-id="52da2-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="52da2-124">por exemplo, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="52da2-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="52da2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="52da2-125">-Name</span></span>
<span data-ttu-id="52da2-126">O nome do aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="52da2-126">The managed application name.</span></span>

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

### <span data-ttu-id="52da2-127">-Pré-</span><span class="sxs-lookup"><span data-stu-id="52da2-127">-Pre</span></span>
<span data-ttu-id="52da2-128">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="52da2-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="52da2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52da2-129">-ResourceGroupName</span></span>
<span data-ttu-id="52da2-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52da2-130">The resource group name.</span></span>

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

### <span data-ttu-id="52da2-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="52da2-131">-Confirm</span></span>
<span data-ttu-id="52da2-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52da2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52da2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52da2-133">-WhatIf</span></span>
<span data-ttu-id="52da2-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="52da2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52da2-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52da2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52da2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52da2-136">CommonParameters</span></span>
<span data-ttu-id="52da2-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52da2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52da2-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52da2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52da2-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="52da2-139">INPUTS</span></span>

### <span data-ttu-id="52da2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="52da2-140">System.String</span></span>

## <span data-ttu-id="52da2-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="52da2-141">OUTPUTS</span></span>

### <span data-ttu-id="52da2-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52da2-142">System.Boolean</span></span>

## <span data-ttu-id="52da2-143">Notas</span><span class="sxs-lookup"><span data-stu-id="52da2-143">NOTES</span></span>

## <span data-ttu-id="52da2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52da2-144">RELATED LINKS</span></span>
