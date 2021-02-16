---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117917"
---
# <span data-ttu-id="888ae-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="888ae-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="888ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="888ae-102">SYNOPSIS</span></span>
<span data-ttu-id="888ae-103">Obter uma ou mais atribuições de diagrama.</span><span class="sxs-lookup"><span data-stu-id="888ae-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="888ae-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="888ae-104">SYNTAX</span></span>

### <span data-ttu-id="888ae-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="888ae-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="888ae-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="888ae-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="888ae-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="888ae-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="888ae-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="888ae-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="888ae-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="888ae-109">DESCRIPTION</span></span>
<span data-ttu-id="888ae-110">Obter uma ou mais atribuições de diagrama.</span><span class="sxs-lookup"><span data-stu-id="888ae-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="888ae-111">As atribuições de diagrama existem no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="888ae-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="888ae-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="888ae-112">EXAMPLES</span></span>

### <span data-ttu-id="888ae-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="888ae-113">Example 1</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name              : Assignment-PS-BlueprintDefinition
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : AllResourcesReadOnly
ProvisioningState : Succeeded
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="888ae-114">Obter as atribuições de diagrama dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="888ae-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="888ae-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="888ae-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="888ae-116">Obter a atribuição do diagrama com o nome indicado dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="888ae-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="888ae-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="888ae-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="888ae-118">Obter as atribuições de diagrama dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="888ae-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="888ae-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="888ae-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="888ae-120">Obter a atribuição do diagrama com o nome indicado no grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="888ae-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="888ae-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="888ae-121">PARAMETERS</span></span>

### <span data-ttu-id="888ae-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="888ae-122">-DefaultProfile</span></span>
<span data-ttu-id="888ae-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="888ae-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="888ae-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="888ae-124">-ManagementGroupId</span></span>
<span data-ttu-id="888ae-125">A ID do grupo de gerenciamento onde a atribuição De plano de trabalho é salva.</span><span class="sxs-lookup"><span data-stu-id="888ae-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="888ae-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="888ae-126">-Name</span></span>
<span data-ttu-id="888ae-127">Nome da tarefa de diagrama.</span><span class="sxs-lookup"><span data-stu-id="888ae-127">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="888ae-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="888ae-128">-SubscriptionId</span></span>
<span data-ttu-id="888ae-129">A ID da assinatura para a atribuição de plano de trabalho foi implantada.</span><span class="sxs-lookup"><span data-stu-id="888ae-129">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="888ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="888ae-130">CommonParameters</span></span>
<span data-ttu-id="888ae-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="888ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="888ae-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="888ae-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="888ae-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="888ae-133">INPUTS</span></span>

### <span data-ttu-id="888ae-134">System.String</span><span class="sxs-lookup"><span data-stu-id="888ae-134">System.String</span></span>

## <span data-ttu-id="888ae-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="888ae-135">OUTPUTS</span></span>

### <span data-ttu-id="888ae-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="888ae-136">System.Object</span></span>
## <span data-ttu-id="888ae-137">Notas</span><span class="sxs-lookup"><span data-stu-id="888ae-137">NOTES</span></span>

## <span data-ttu-id="888ae-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="888ae-138">RELATED LINKS</span></span>
