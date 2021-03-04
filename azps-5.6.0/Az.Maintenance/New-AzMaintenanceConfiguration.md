---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: ac264e048ea428ba68caa683eb6076074c9894b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889664"
---
# <span data-ttu-id="cbea1-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbea1-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="cbea1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbea1-102">SYNOPSIS</span></span>
<span data-ttu-id="cbea1-103">Criar ou atualizar registro de configuração</span><span class="sxs-lookup"><span data-stu-id="cbea1-103">Create or Update configuration record</span></span>

## <span data-ttu-id="cbea1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cbea1-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbea1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cbea1-105">DESCRIPTION</span></span>
<span data-ttu-id="cbea1-106">Criar ou atualizar registro de configuração</span><span class="sxs-lookup"><span data-stu-id="cbea1-106">Create or Update configuration record</span></span>

## <span data-ttu-id="cbea1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbea1-107">EXAMPLES</span></span>

### <span data-ttu-id="cbea1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cbea1-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus -StartDateTime 2020-08-01 00:00 -ExpirationDateTime 2021-08-04 00:00 -TimeZone Pacific Standard Time -Duration 05:00 -RecurEvery Day


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : Host
Visibility          : Custom
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="cbea1-109">Criar uma configuração de manutenção com Host de escopo</span><span class="sxs-lookup"><span data-stu-id="cbea1-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="cbea1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cbea1-110">PARAMETERS</span></span>

### <span data-ttu-id="cbea1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbea1-111">-AsJob</span></span>
<span data-ttu-id="cbea1-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cbea1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbea1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbea1-113">-DefaultProfile</span></span>
<span data-ttu-id="cbea1-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbea1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbea1-115">-Duration</span><span class="sxs-lookup"><span data-stu-id="cbea1-115">-Duration</span></span>
<span data-ttu-id="cbea1-116">A duração</span><span class="sxs-lookup"><span data-stu-id="cbea1-116">The duration</span></span>


```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbea1-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="cbea1-117">-ExpirationDateTime</span></span>
<span data-ttu-id="cbea1-118">O expirationDateTime da agenda no formato YYYY-MM-DD hh:mm</span><span class="sxs-lookup"><span data-stu-id="cbea1-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="cbea1-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="cbea1-119">-ExtensionProperty</span></span>
<span data-ttu-id="cbea1-120">As propriedades Extension por recurso.</span><span class="sxs-lookup"><span data-stu-id="cbea1-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="cbea1-121">-Location</span><span class="sxs-lookup"><span data-stu-id="cbea1-121">-Location</span></span>
<span data-ttu-id="cbea1-122">O local de configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="cbea1-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="cbea1-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="cbea1-123">-MaintenanceScope</span></span>
<span data-ttu-id="cbea1-124">O Escopo de Manutenção.</span><span class="sxs-lookup"><span data-stu-id="cbea1-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="cbea1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cbea1-125">-Name</span></span>
<span data-ttu-id="cbea1-126">Nome da configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="cbea1-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="cbea1-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="cbea1-127">-RecurEvery</span></span>
<span data-ttu-id="cbea1-128">A recorrência de agendamento</span><span class="sxs-lookup"><span data-stu-id="cbea1-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="cbea1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbea1-129">-ResourceGroupName</span></span>
<span data-ttu-id="cbea1-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbea1-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="cbea1-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="cbea1-131">-StartDateTime</span></span>
<span data-ttu-id="cbea1-132">StartDateTime da agenda no formato YYYY-MM-DD hh:mm</span><span class="sxs-lookup"><span data-stu-id="cbea1-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="cbea1-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="cbea1-133">-Tag</span></span>
<span data-ttu-id="cbea1-134">As ARM marcas.</span><span class="sxs-lookup"><span data-stu-id="cbea1-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="cbea1-135">-Timezone</span><span class="sxs-lookup"><span data-stu-id="cbea1-135">-Timezone</span></span>
<span data-ttu-id="cbea1-136">O timezone</span><span class="sxs-lookup"><span data-stu-id="cbea1-136">The timezone</span></span>

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

### <span data-ttu-id="cbea1-137">-Visibility</span><span class="sxs-lookup"><span data-stu-id="cbea1-137">-Visibility</span></span>
<span data-ttu-id="cbea1-138">A visibilidade do escopo</span><span class="sxs-lookup"><span data-stu-id="cbea1-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="cbea1-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbea1-139">-Confirm</span></span>
<span data-ttu-id="cbea1-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbea1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbea1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbea1-141">-WhatIf</span></span>
<span data-ttu-id="cbea1-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cbea1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbea1-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbea1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbea1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbea1-144">CommonParameters</span></span>
<span data-ttu-id="cbea1-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbea1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbea1-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbea1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbea1-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbea1-147">INPUTS</span></span>

### <span data-ttu-id="cbea1-148">System.String</span><span class="sxs-lookup"><span data-stu-id="cbea1-148">System.String</span></span>

## <span data-ttu-id="cbea1-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cbea1-149">OUTPUTS</span></span>

### <span data-ttu-id="cbea1-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbea1-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="cbea1-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="cbea1-151">NOTES</span></span>

## <span data-ttu-id="cbea1-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbea1-152">RELATED LINKS</span></span>
