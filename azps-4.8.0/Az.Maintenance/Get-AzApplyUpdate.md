---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111657"
---
# <span data-ttu-id="04f4d-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="04f4d-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="04f4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="04f4d-103">Acompanhar atualizações de manutenção para o recurso</span><span class="sxs-lookup"><span data-stu-id="04f4d-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="04f4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04f4d-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04f4d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04f4d-105">DESCRIPTION</span></span>
<span data-ttu-id="04f4d-106">Acompanhar atualizações de manutenção para o recurso</span><span class="sxs-lookup"><span data-stu-id="04f4d-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="04f4d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04f4d-107">EXAMPLES</span></span>

### <span data-ttu-id="04f4d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04f4d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="04f4d-109">Acompanhar atualizações de manutenção para o recurso</span><span class="sxs-lookup"><span data-stu-id="04f4d-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="04f4d-110">OS</span><span class="sxs-lookup"><span data-stu-id="04f4d-110">PARAMETERS</span></span>

### <span data-ttu-id="04f4d-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="04f4d-111">-ApplyUpdateName</span></span>
<span data-ttu-id="04f4d-112">O nome do recurso aplicar atualização.</span><span class="sxs-lookup"><span data-stu-id="04f4d-112">The apply update resource name.</span></span>

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

### <span data-ttu-id="04f4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f4d-113">-DefaultProfile</span></span>
<span data-ttu-id="04f4d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04f4d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04f4d-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="04f4d-115">-ProviderName</span></span>
<span data-ttu-id="04f4d-116">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="04f4d-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="04f4d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04f4d-117">-ResourceGroupName</span></span>
<span data-ttu-id="04f4d-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="04f4d-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="04f4d-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="04f4d-119">-ResourceName</span></span>
<span data-ttu-id="04f4d-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="04f4d-120">The resource name.</span></span>

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

### <span data-ttu-id="04f4d-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="04f4d-121">-ResourceParentName</span></span>
<span data-ttu-id="04f4d-122">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="04f4d-122">The parent resource name.</span></span>

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

### <span data-ttu-id="04f4d-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="04f4d-123">-ResourceParentType</span></span>
<span data-ttu-id="04f4d-124">O tipo de recurso pai.</span><span class="sxs-lookup"><span data-stu-id="04f4d-124">The parent resource type.</span></span>

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

### <span data-ttu-id="04f4d-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="04f4d-125">-ResourceType</span></span>
<span data-ttu-id="04f4d-126">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="04f4d-126">The resource type.</span></span>

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

### <span data-ttu-id="04f4d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f4d-127">CommonParameters</span></span>
<span data-ttu-id="04f4d-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04f4d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f4d-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04f4d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f4d-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04f4d-130">INPUTS</span></span>

### <span data-ttu-id="04f4d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="04f4d-131">System.String</span></span>

## <span data-ttu-id="04f4d-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04f4d-132">OUTPUTS</span></span>

### <span data-ttu-id="04f4d-133">Microsoft. Azure. Commands. maintenance. Models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="04f4d-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="04f4d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04f4d-134">NOTES</span></span>

## <span data-ttu-id="04f4d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04f4d-135">RELATED LINKS</span></span>
