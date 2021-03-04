---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: c6ebe985d0242e626d0a417d4af3a60388cbc776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892751"
---
# <span data-ttu-id="ef873-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="ef873-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="ef873-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef873-102">SYNOPSIS</span></span>
<span data-ttu-id="ef873-103">Rastrear atualizações de manutenção para o recurso</span><span class="sxs-lookup"><span data-stu-id="ef873-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="ef873-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ef873-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef873-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ef873-105">DESCRIPTION</span></span>
<span data-ttu-id="ef873-106">Rastrear atualizações de manutenção para o recurso</span><span class="sxs-lookup"><span data-stu-id="ef873-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="ef873-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef873-107">EXAMPLES</span></span>

### <span data-ttu-id="ef873-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef873-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="ef873-109">Rastrear atualizações de manutenção para o recurso</span><span class="sxs-lookup"><span data-stu-id="ef873-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="ef873-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ef873-110">PARAMETERS</span></span>

### <span data-ttu-id="ef873-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="ef873-111">-ApplyUpdateName</span></span>
<span data-ttu-id="ef873-112">O nome do recurso aplicar atualização.</span><span class="sxs-lookup"><span data-stu-id="ef873-112">The apply update resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef873-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef873-113">-DefaultProfile</span></span>
<span data-ttu-id="ef873-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef873-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef873-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="ef873-115">-ProviderName</span></span>
<span data-ttu-id="ef873-116">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="ef873-116">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef873-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef873-117">-ResourceGroupName</span></span>
<span data-ttu-id="ef873-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ef873-118">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef873-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ef873-119">-ResourceName</span></span>
<span data-ttu-id="ef873-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ef873-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef873-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="ef873-121">-ResourceParentName</span></span>
<span data-ttu-id="ef873-122">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="ef873-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef873-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="ef873-123">-ResourceParentType</span></span>
<span data-ttu-id="ef873-124">O tipo de recurso pai.</span><span class="sxs-lookup"><span data-stu-id="ef873-124">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef873-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ef873-125">-ResourceType</span></span>
<span data-ttu-id="ef873-126">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="ef873-126">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef873-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef873-127">CommonParameters</span></span>
<span data-ttu-id="ef873-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef873-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef873-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef873-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef873-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef873-130">INPUTS</span></span>

### <span data-ttu-id="ef873-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ef873-131">System.String</span></span>

## <span data-ttu-id="ef873-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ef873-132">OUTPUTS</span></span>

### <span data-ttu-id="ef873-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="ef873-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="ef873-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="ef873-134">NOTES</span></span>

## <span data-ttu-id="ef873-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef873-135">RELATED LINKS</span></span>
