---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111642"
---
# <span data-ttu-id="d2782-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="d2782-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="d2782-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2782-102">SYNOPSIS</span></span>
<span data-ttu-id="d2782-103">Aplicar atualizações de manutenção ao recurso</span><span class="sxs-lookup"><span data-stu-id="d2782-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="d2782-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2782-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2782-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2782-105">DESCRIPTION</span></span>
<span data-ttu-id="d2782-106">Aplicar atualizações de manutenção ao recurso</span><span class="sxs-lookup"><span data-stu-id="d2782-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="d2782-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2782-107">EXAMPLES</span></span>

### <span data-ttu-id="d2782-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2782-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="d2782-109">Aplicar atualizações de manutenção ao recurso</span><span class="sxs-lookup"><span data-stu-id="d2782-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="d2782-110">OS</span><span class="sxs-lookup"><span data-stu-id="d2782-110">PARAMETERS</span></span>

### <span data-ttu-id="d2782-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2782-111">-AsJob</span></span>
<span data-ttu-id="d2782-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d2782-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2782-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2782-113">-DefaultProfile</span></span>
<span data-ttu-id="d2782-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2782-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2782-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="d2782-115">-ProviderName</span></span>
<span data-ttu-id="d2782-116">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2782-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="d2782-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2782-117">-ResourceGroupName</span></span>
<span data-ttu-id="d2782-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2782-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="d2782-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d2782-119">-ResourceName</span></span>
<span data-ttu-id="d2782-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d2782-120">The resource name.</span></span>

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

### <span data-ttu-id="d2782-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="d2782-121">-ResourceParentName</span></span>
<span data-ttu-id="d2782-122">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="d2782-122">The parent resource name.</span></span>

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

### <span data-ttu-id="d2782-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="d2782-123">-ResourceParentType</span></span>
<span data-ttu-id="d2782-124">O tipo de recurso pai.</span><span class="sxs-lookup"><span data-stu-id="d2782-124">The parent resource type.</span></span>

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

### <span data-ttu-id="d2782-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d2782-125">-ResourceType</span></span>
<span data-ttu-id="d2782-126">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="d2782-126">The resource type.</span></span>

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

### <span data-ttu-id="d2782-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2782-127">-Confirm</span></span>
<span data-ttu-id="d2782-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2782-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2782-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2782-129">-WhatIf</span></span>
<span data-ttu-id="d2782-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2782-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2782-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2782-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2782-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2782-132">CommonParameters</span></span>
<span data-ttu-id="d2782-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2782-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2782-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2782-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2782-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2782-135">INPUTS</span></span>

### <span data-ttu-id="d2782-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d2782-136">System.String</span></span>

## <span data-ttu-id="d2782-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2782-137">OUTPUTS</span></span>

### <span data-ttu-id="d2782-138">Microsoft. Azure. Commands. maintenance. Models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="d2782-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="d2782-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2782-139">NOTES</span></span>

## <span data-ttu-id="d2782-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2782-140">RELATED LINKS</span></span>
