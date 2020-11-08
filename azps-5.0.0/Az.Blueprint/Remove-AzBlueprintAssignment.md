---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116097"
---
# <span data-ttu-id="d8a08-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="d8a08-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="d8a08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8a08-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a08-103">Remova uma atribuição Blueprint de uma assinatura ou um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d8a08-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="d8a08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8a08-104">SYNTAX</span></span>

### <span data-ttu-id="d8a08-105">BySubscriptionAndName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8a08-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8a08-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="d8a08-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8a08-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="d8a08-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8a08-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8a08-108">DESCRIPTION</span></span>
<span data-ttu-id="d8a08-109">Remover um plano gráfico atribuído a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d8a08-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="d8a08-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8a08-110">EXAMPLES</span></span>

### <span data-ttu-id="d8a08-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d8a08-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="d8a08-112">Remover a atribuição Blueprint especificada pelo nome da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="d8a08-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="d8a08-113">O cmdlet pedirá confirmação antes de executar o comando.</span><span class="sxs-lookup"><span data-stu-id="d8a08-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="d8a08-114">OS</span><span class="sxs-lookup"><span data-stu-id="d8a08-114">PARAMETERS</span></span>

### <span data-ttu-id="d8a08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a08-115">-DefaultProfile</span></span>
<span data-ttu-id="d8a08-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8a08-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8a08-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8a08-117">-InputObject</span></span>
<span data-ttu-id="d8a08-118">Objeto de atribuição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="d8a08-118">Blueprint assignment object.</span></span>

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

### <span data-ttu-id="d8a08-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d8a08-119">-ManagementGroupId</span></span>
<span data-ttu-id="d8a08-120">A ID do grupo de gerenciamento em que a atribuição Blueprint é salva.</span><span class="sxs-lookup"><span data-stu-id="d8a08-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="d8a08-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8a08-121">-Name</span></span>
<span data-ttu-id="d8a08-122">Nome da atribuição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="d8a08-122">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="d8a08-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8a08-123">-PassThru</span></span>
<span data-ttu-id="d8a08-124">Quando definido, o cmdlet retornará um objeto que representa a atribuição Blueprint removida.</span><span class="sxs-lookup"><span data-stu-id="d8a08-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="d8a08-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d8a08-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d8a08-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8a08-126">-SubscriptionId</span></span>
<span data-ttu-id="d8a08-127">ID da assinatura na qual a atribuição Blueprint é implantada.</span><span class="sxs-lookup"><span data-stu-id="d8a08-127">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="d8a08-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8a08-128">-Confirm</span></span>
<span data-ttu-id="d8a08-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8a08-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8a08-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8a08-130">-WhatIf</span></span>
<span data-ttu-id="d8a08-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8a08-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8a08-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8a08-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8a08-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a08-133">CommonParameters</span></span>
<span data-ttu-id="d8a08-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8a08-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a08-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8a08-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a08-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8a08-136">INPUTS</span></span>

### <span data-ttu-id="d8a08-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d8a08-137">System.String</span></span>

### <span data-ttu-id="d8a08-138">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="d8a08-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="d8a08-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8a08-139">OUTPUTS</span></span>

### <span data-ttu-id="d8a08-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="d8a08-140">System.Object</span></span>
## <span data-ttu-id="d8a08-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8a08-141">NOTES</span></span>

## <span data-ttu-id="d8a08-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8a08-142">RELATED LINKS</span></span>
