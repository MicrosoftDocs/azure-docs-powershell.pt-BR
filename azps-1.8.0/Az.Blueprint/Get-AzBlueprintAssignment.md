---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 121811c88493a4f6f069a60c8f9662eb9d11303e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601435"
---
# <span data-ttu-id="4ecd0-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="4ecd0-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="4ecd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ecd0-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecd0-103">Obter uma ou mais atribuições BluePrints.</span><span class="sxs-lookup"><span data-stu-id="4ecd0-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="4ecd0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ecd0-104">SYNTAX</span></span>

### <span data-ttu-id="4ecd0-105">BlueprintAssignmentsBySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ecd0-105">BlueprintAssignmentsBySubscription (Default)</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ecd0-106">BlueprintAssignmentByName</span><span class="sxs-lookup"><span data-stu-id="4ecd0-106">BlueprintAssignmentByName</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ecd0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ecd0-107">DESCRIPTION</span></span>
<span data-ttu-id="4ecd0-108">Obter uma ou mais atribuições BluePrints.</span><span class="sxs-lookup"><span data-stu-id="4ecd0-108">Get one or more blueprint assignments.</span></span> <span data-ttu-id="4ecd0-109">As atribuições Blueprints existem no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4ecd0-109">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="4ecd0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ecd0-110">EXAMPLES</span></span>

### <span data-ttu-id="4ecd0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ecd0-111">Example 1</span></span>
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

<span data-ttu-id="4ecd0-112">Obter as atribuições Blueprints dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="4ecd0-112">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="4ecd0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4ecd0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="4ecd0-114">Obtenha a atribuição Blueprint com o nome especificado na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="4ecd0-114">Get the blueprint assignment with the given name within the specified subscription.</span></span>

## <span data-ttu-id="4ecd0-115">OS</span><span class="sxs-lookup"><span data-stu-id="4ecd0-115">PARAMETERS</span></span>

### <span data-ttu-id="4ecd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecd0-116">-DefaultProfile</span></span>
<span data-ttu-id="4ecd0-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ecd0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ecd0-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ecd0-118">-Name</span></span>
<span data-ttu-id="4ecd0-119">Nome da atribuição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="4ecd0-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd0-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ecd0-120">-SubscriptionId</span></span>
<span data-ttu-id="4ecd0-121">ID da assinatura na qual a atribuição Blueprint é implantada.</span><span class="sxs-lookup"><span data-stu-id="4ecd0-121">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecd0-122">CommonParameters</span></span>
<span data-ttu-id="4ecd0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ecd0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecd0-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ecd0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecd0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ecd0-125">INPUTS</span></span>

### <span data-ttu-id="4ecd0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4ecd0-126">System.String</span></span>

## <span data-ttu-id="4ecd0-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ecd0-127">OUTPUTS</span></span>

### <span data-ttu-id="4ecd0-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="4ecd0-128">System.Object</span></span>
## <span data-ttu-id="4ecd0-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ecd0-129">NOTES</span></span>

## <span data-ttu-id="4ecd0-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ecd0-130">RELATED LINKS</span></span>
