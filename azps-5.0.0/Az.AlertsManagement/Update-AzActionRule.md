---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280416"
---
# <span data-ttu-id="52db9-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="52db9-101">Update-AzActionRule</span></span>

## <span data-ttu-id="52db9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52db9-102">SYNOPSIS</span></span>
<span data-ttu-id="52db9-103">Atualiza as propriedades da regra de ação.</span><span class="sxs-lookup"><span data-stu-id="52db9-103">Updates action rule properties.</span></span>

## <span data-ttu-id="52db9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52db9-104">SYNTAX</span></span>

### <span data-ttu-id="52db9-105">ByNameSimplifiedPatch (padrão)</span><span class="sxs-lookup"><span data-stu-id="52db9-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52db9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="52db9-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52db9-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="52db9-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52db9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52db9-108">DESCRIPTION</span></span>
<span data-ttu-id="52db9-109">**Update-AzActionRule cmdlet Update** Propriedades da regra de ação-status e marcas.</span><span class="sxs-lookup"><span data-stu-id="52db9-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="52db9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52db9-110">EXAMPLES</span></span>

### <span data-ttu-id="52db9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52db9-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="52db9-112">Esse cmdlet desabilita a regra de ação.</span><span class="sxs-lookup"><span data-stu-id="52db9-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="52db9-113">OS</span><span class="sxs-lookup"><span data-stu-id="52db9-113">PARAMETERS</span></span>

### <span data-ttu-id="52db9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52db9-114">-DefaultProfile</span></span>
<span data-ttu-id="52db9-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52db9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52db9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52db9-116">-InputObject</span></span>
<span data-ttu-id="52db9-117">O recurso regra de ação</span><span class="sxs-lookup"><span data-stu-id="52db9-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52db9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="52db9-118">-Name</span></span>
<span data-ttu-id="52db9-119">Nome da regra da ação</span><span class="sxs-lookup"><span data-stu-id="52db9-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52db9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52db9-120">-ResourceGroupName</span></span>
<span data-ttu-id="52db9-121">Nome da regra da ação</span><span class="sxs-lookup"><span data-stu-id="52db9-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52db9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52db9-122">-ResourceId</span></span>
<span data-ttu-id="52db9-123">A ID do recurso da regra da ação</span><span class="sxs-lookup"><span data-stu-id="52db9-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52db9-124">-Status</span><span class="sxs-lookup"><span data-stu-id="52db9-124">-Status</span></span>
<span data-ttu-id="52db9-125">Status da regra da ação</span><span class="sxs-lookup"><span data-stu-id="52db9-125">Action rule status</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52db9-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="52db9-126">-Tag</span></span>
<span data-ttu-id="52db9-127">Marcas de regra de ação</span><span class="sxs-lookup"><span data-stu-id="52db9-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52db9-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52db9-128">-Confirm</span></span>
<span data-ttu-id="52db9-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52db9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52db9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52db9-130">-WhatIf</span></span>
<span data-ttu-id="52db9-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52db9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52db9-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52db9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52db9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52db9-133">CommonParameters</span></span>
<span data-ttu-id="52db9-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52db9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52db9-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52db9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52db9-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52db9-136">INPUTS</span></span>

### <span data-ttu-id="52db9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="52db9-137">System.String</span></span>

### <span data-ttu-id="52db9-138">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="52db9-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="52db9-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52db9-139">OUTPUTS</span></span>

### <span data-ttu-id="52db9-140">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="52db9-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="52db9-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52db9-141">NOTES</span></span>

## <span data-ttu-id="52db9-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52db9-142">RELATED LINKS</span></span>
