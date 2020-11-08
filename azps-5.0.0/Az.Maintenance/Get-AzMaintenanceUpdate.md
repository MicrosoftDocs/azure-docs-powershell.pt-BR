---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117353"
---
# <span data-ttu-id="8645e-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="8645e-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="8645e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8645e-102">SYNOPSIS</span></span>
<span data-ttu-id="8645e-103">Obtenha atualizações de manutenção pendentes para o recurso.</span><span class="sxs-lookup"><span data-stu-id="8645e-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="8645e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8645e-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8645e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8645e-105">DESCRIPTION</span></span>
<span data-ttu-id="8645e-106">Obtenha atualizações de manutenção pendentes para o recurso.</span><span class="sxs-lookup"><span data-stu-id="8645e-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="8645e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8645e-107">EXAMPLES</span></span>

### <span data-ttu-id="8645e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8645e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="8645e-109">Obtenha atualizações de manutenção pendentes para o recurso.</span><span class="sxs-lookup"><span data-stu-id="8645e-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="8645e-110">OS</span><span class="sxs-lookup"><span data-stu-id="8645e-110">PARAMETERS</span></span>

### <span data-ttu-id="8645e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8645e-111">-DefaultProfile</span></span>
<span data-ttu-id="8645e-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8645e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8645e-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="8645e-113">-ProviderName</span></span>
<span data-ttu-id="8645e-114">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8645e-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="8645e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8645e-115">-ResourceGroupName</span></span>
<span data-ttu-id="8645e-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8645e-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="8645e-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8645e-117">-ResourceName</span></span>
<span data-ttu-id="8645e-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="8645e-118">The resource name.</span></span>

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

### <span data-ttu-id="8645e-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="8645e-119">-ResourceParentName</span></span>
<span data-ttu-id="8645e-120">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="8645e-120">The parent resource name.</span></span>

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

### <span data-ttu-id="8645e-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="8645e-121">-ResourceParentType</span></span>
<span data-ttu-id="8645e-122">O tipo de recurso pai.</span><span class="sxs-lookup"><span data-stu-id="8645e-122">The parent resource type.</span></span>

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

### <span data-ttu-id="8645e-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8645e-123">-ResourceType</span></span>
<span data-ttu-id="8645e-124">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="8645e-124">The resource type.</span></span>

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

### <span data-ttu-id="8645e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8645e-125">CommonParameters</span></span>
<span data-ttu-id="8645e-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8645e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8645e-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8645e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8645e-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8645e-128">INPUTS</span></span>

### <span data-ttu-id="8645e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8645e-129">System.String</span></span>

## <span data-ttu-id="8645e-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8645e-130">OUTPUTS</span></span>

### <span data-ttu-id="8645e-131">Microsoft. Azure. Management. maintenance. Models. Update</span><span class="sxs-lookup"><span data-stu-id="8645e-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="8645e-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8645e-132">NOTES</span></span>

## <span data-ttu-id="8645e-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8645e-133">RELATED LINKS</span></span>
