---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112201"
---
# <span data-ttu-id="48b1d-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="48b1d-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="48b1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="48b1d-103">Remover uma atribuição de planta de uma assinatura ou de um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="48b1d-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="48b1d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48b1d-104">SYNTAX</span></span>

### <span data-ttu-id="48b1d-105">BySubscriptionAndName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="48b1d-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48b1d-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="48b1d-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48b1d-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="48b1d-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48b1d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="48b1d-108">DESCRIPTION</span></span>
<span data-ttu-id="48b1d-109">Remover um diagrama que foi atribuído a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="48b1d-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="48b1d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48b1d-110">EXAMPLES</span></span>

### <span data-ttu-id="48b1d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="48b1d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="48b1d-112">Remova a atribuição de diagrama especificada pelo nome da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="48b1d-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="48b1d-113">O cmdlet solicitará confirmação antes de executar o comando.</span><span class="sxs-lookup"><span data-stu-id="48b1d-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="48b1d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48b1d-114">PARAMETERS</span></span>

### <span data-ttu-id="48b1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b1d-115">-DefaultProfile</span></span>
<span data-ttu-id="48b1d-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48b1d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48b1d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48b1d-117">-InputObject</span></span>
<span data-ttu-id="48b1d-118">Objeto de atribuição de projeto.</span><span class="sxs-lookup"><span data-stu-id="48b1d-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48b1d-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="48b1d-119">-ManagementGroupId</span></span>
<span data-ttu-id="48b1d-120">A ID do grupo de gerenciamento onde a atribuição De plantas é salva.</span><span class="sxs-lookup"><span data-stu-id="48b1d-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48b1d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="48b1d-121">-Name</span></span>
<span data-ttu-id="48b1d-122">Nome da tarefa de diagrama.</span><span class="sxs-lookup"><span data-stu-id="48b1d-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b1d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48b1d-123">-PassThru</span></span>
<span data-ttu-id="48b1d-124">Quando definido, o cmdlet retornará um objeto que representa a atribuição De diagrama removida.</span><span class="sxs-lookup"><span data-stu-id="48b1d-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="48b1d-125">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="48b1d-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="48b1d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48b1d-126">-SubscriptionId</span></span>
<span data-ttu-id="48b1d-127">A ID da assinatura para a atribuição de planta foi implantada.</span><span class="sxs-lookup"><span data-stu-id="48b1d-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48b1d-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="48b1d-128">-Confirm</span></span>
<span data-ttu-id="48b1d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48b1d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48b1d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b1d-130">-WhatIf</span></span>
<span data-ttu-id="48b1d-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="48b1d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48b1d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48b1d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48b1d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b1d-133">CommonParameters</span></span>
<span data-ttu-id="48b1d-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b1d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b1d-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48b1d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b1d-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="48b1d-136">INPUTS</span></span>

### <span data-ttu-id="48b1d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="48b1d-137">System.String</span></span>

### <span data-ttu-id="48b1d-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span><span class="sxs-lookup"><span data-stu-id="48b1d-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="48b1d-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="48b1d-139">OUTPUTS</span></span>

### <span data-ttu-id="48b1d-140">System.Object</span><span class="sxs-lookup"><span data-stu-id="48b1d-140">System.Object</span></span>
## <span data-ttu-id="48b1d-141">Notas</span><span class="sxs-lookup"><span data-stu-id="48b1d-141">NOTES</span></span>

## <span data-ttu-id="48b1d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48b1d-142">RELATED LINKS</span></span>
