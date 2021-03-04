---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 375eca319a1db467e97addac50faa3f91fe0ecc5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885744"
---
# <span data-ttu-id="4122c-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="4122c-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="4122c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4122c-102">SYNOPSIS</span></span>
<span data-ttu-id="4122c-103">Obter uma ou mais atribuições de projeto.</span><span class="sxs-lookup"><span data-stu-id="4122c-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="4122c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4122c-104">SYNTAX</span></span>

### <span data-ttu-id="4122c-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4122c-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4122c-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="4122c-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4122c-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="4122c-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4122c-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="4122c-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4122c-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4122c-109">DESCRIPTION</span></span>
<span data-ttu-id="4122c-110">Obter uma ou mais atribuições de projeto.</span><span class="sxs-lookup"><span data-stu-id="4122c-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="4122c-111">As atribuições de projeto existem no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4122c-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="4122c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4122c-112">EXAMPLES</span></span>

### <span data-ttu-id="4122c-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4122c-113">Example 1</span></span>
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

<span data-ttu-id="4122c-114">Obter as atribuições de projeto dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="4122c-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="4122c-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4122c-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="4122c-116">Obter a atribuição de projeto com o nome determinado dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="4122c-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="4122c-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4122c-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="4122c-118">Obter as atribuições de projeto dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="4122c-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="4122c-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="4122c-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="4122c-120">Obter a atribuição de projeto com o nome indicado no grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="4122c-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="4122c-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4122c-121">PARAMETERS</span></span>

### <span data-ttu-id="4122c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4122c-122">-DefaultProfile</span></span>
<span data-ttu-id="4122c-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4122c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4122c-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="4122c-124">-ManagementGroupId</span></span>
<span data-ttu-id="4122c-125">A ID do grupo de gerenciamento onde a atribuição Blueprint é salva.</span><span class="sxs-lookup"><span data-stu-id="4122c-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="4122c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4122c-126">-Name</span></span>
<span data-ttu-id="4122c-127">Nome da atribuição de projeto.</span><span class="sxs-lookup"><span data-stu-id="4122c-127">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="4122c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4122c-128">-SubscriptionId</span></span>
<span data-ttu-id="4122c-129">Id da assinatura para a que a atribuição de projeto é implantada.</span><span class="sxs-lookup"><span data-stu-id="4122c-129">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="4122c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4122c-130">CommonParameters</span></span>
<span data-ttu-id="4122c-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4122c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4122c-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4122c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4122c-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4122c-133">INPUTS</span></span>

### <span data-ttu-id="4122c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4122c-134">System.String</span></span>

## <span data-ttu-id="4122c-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4122c-135">OUTPUTS</span></span>

### <span data-ttu-id="4122c-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="4122c-136">System.Object</span></span>
## <span data-ttu-id="4122c-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="4122c-137">NOTES</span></span>

## <span data-ttu-id="4122c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4122c-138">RELATED LINKS</span></span>
