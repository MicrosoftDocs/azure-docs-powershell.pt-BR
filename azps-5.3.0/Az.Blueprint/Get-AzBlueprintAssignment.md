---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430367"
---
# <span data-ttu-id="1f1e7-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="1f1e7-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="1f1e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f1e7-102">SYNOPSIS</span></span>
<span data-ttu-id="1f1e7-103">Obter uma ou mais atribuições BluePrints.</span><span class="sxs-lookup"><span data-stu-id="1f1e7-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="1f1e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f1e7-104">SYNTAX</span></span>

### <span data-ttu-id="1f1e7-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="1f1e7-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f1e7-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="1f1e7-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f1e7-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="1f1e7-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f1e7-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="1f1e7-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f1e7-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f1e7-109">DESCRIPTION</span></span>
<span data-ttu-id="1f1e7-110">Obter uma ou mais atribuições BluePrints.</span><span class="sxs-lookup"><span data-stu-id="1f1e7-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="1f1e7-111">As atribuições Blueprints existem no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="1f1e7-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="1f1e7-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f1e7-112">EXAMPLES</span></span>

### <span data-ttu-id="1f1e7-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f1e7-113">Example 1</span></span>
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

<span data-ttu-id="1f1e7-114">Obter as atribuições Blueprints dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="1f1e7-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="1f1e7-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1f1e7-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="1f1e7-116">Obtenha a atribuição Blueprint com o nome especificado na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="1f1e7-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="1f1e7-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1f1e7-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="1f1e7-118">Obter as atribuições Blueprints dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="1f1e7-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="1f1e7-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="1f1e7-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="1f1e7-120">Obtenha a atribuição Blueprint com o nome especificado dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="1f1e7-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="1f1e7-121">OS</span><span class="sxs-lookup"><span data-stu-id="1f1e7-121">PARAMETERS</span></span>

### <span data-ttu-id="1f1e7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f1e7-122">-DefaultProfile</span></span>
<span data-ttu-id="1f1e7-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f1e7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f1e7-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1f1e7-124">-ManagementGroupId</span></span>
<span data-ttu-id="1f1e7-125">A ID do grupo de gerenciamento em que a atribuição Blueprint é salva.</span><span class="sxs-lookup"><span data-stu-id="1f1e7-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="1f1e7-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f1e7-126">-Name</span></span>
<span data-ttu-id="1f1e7-127">Nome da atribuição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="1f1e7-127">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="1f1e7-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f1e7-128">-SubscriptionId</span></span>
<span data-ttu-id="1f1e7-129">ID da assinatura na qual a atribuição Blueprint é implantada.</span><span class="sxs-lookup"><span data-stu-id="1f1e7-129">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="1f1e7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f1e7-130">CommonParameters</span></span>
<span data-ttu-id="1f1e7-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f1e7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f1e7-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f1e7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f1e7-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f1e7-133">INPUTS</span></span>

### <span data-ttu-id="1f1e7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1f1e7-134">System.String</span></span>

## <span data-ttu-id="1f1e7-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f1e7-135">OUTPUTS</span></span>

### <span data-ttu-id="1f1e7-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="1f1e7-136">System.Object</span></span>
## <span data-ttu-id="1f1e7-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f1e7-137">NOTES</span></span>

## <span data-ttu-id="1f1e7-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f1e7-138">RELATED LINKS</span></span>
