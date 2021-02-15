---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114287"
---
# <span data-ttu-id="fe86f-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe86f-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="fe86f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe86f-102">SYNOPSIS</span></span>
<span data-ttu-id="fe86f-103">Criar ou atualizar registro de configuração</span><span class="sxs-lookup"><span data-stu-id="fe86f-103">Create or Update configuration record</span></span>

## <span data-ttu-id="fe86f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe86f-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe86f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe86f-105">DESCRIPTION</span></span>
<span data-ttu-id="fe86f-106">Criar ou atualizar registro de configuração</span><span class="sxs-lookup"><span data-stu-id="fe86f-106">Create or Update configuration record</span></span>

## <span data-ttu-id="fe86f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fe86f-107">EXAMPLES</span></span>

### <span data-ttu-id="fe86f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe86f-108">Example 1</span></span>
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

<span data-ttu-id="fe86f-109">Criar uma configuração de manutenção com o Host de escopo</span><span class="sxs-lookup"><span data-stu-id="fe86f-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="fe86f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe86f-110">PARAMETERS</span></span>

### <span data-ttu-id="fe86f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe86f-111">-AsJob</span></span>
<span data-ttu-id="fe86f-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fe86f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe86f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe86f-113">-DefaultProfile</span></span>
<span data-ttu-id="fe86f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe86f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe86f-115">-Duração</span><span class="sxs-lookup"><span data-stu-id="fe86f-115">-Duration</span></span>
<span data-ttu-id="fe86f-116">A duração</span><span class="sxs-lookup"><span data-stu-id="fe86f-116">The duration</span></span>


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

### <span data-ttu-id="fe86f-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="fe86f-117">-ExpirationDateTime</span></span>
<span data-ttu-id="fe86f-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span><span class="sxs-lookup"><span data-stu-id="fe86f-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="fe86f-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="fe86f-119">-ExtensionProperty</span></span>
<span data-ttu-id="fe86f-120">As propriedades de extensão por recurso.</span><span class="sxs-lookup"><span data-stu-id="fe86f-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="fe86f-121">-Local</span><span class="sxs-lookup"><span data-stu-id="fe86f-121">-Location</span></span>
<span data-ttu-id="fe86f-122">O local de configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="fe86f-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="fe86f-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="fe86f-123">-MaintenanceScope</span></span>
<span data-ttu-id="fe86f-124">O Escopo de Manutenção.</span><span class="sxs-lookup"><span data-stu-id="fe86f-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="fe86f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe86f-125">-Name</span></span>
<span data-ttu-id="fe86f-126">Nome da configuração de manutenção.</span><span class="sxs-lookup"><span data-stu-id="fe86f-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="fe86f-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="fe86f-127">-RecurEvery</span></span>
<span data-ttu-id="fe86f-128">A recorrência do cronograma</span><span class="sxs-lookup"><span data-stu-id="fe86f-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="fe86f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe86f-129">-ResourceGroupName</span></span>
<span data-ttu-id="fe86f-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe86f-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="fe86f-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="fe86f-131">-StartDateTime</span></span>
<span data-ttu-id="fe86f-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span><span class="sxs-lookup"><span data-stu-id="fe86f-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="fe86f-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe86f-133">-Tag</span></span>
<span data-ttu-id="fe86f-134">As marcas ARM.</span><span class="sxs-lookup"><span data-stu-id="fe86f-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="fe86f-135">-Timezone</span><span class="sxs-lookup"><span data-stu-id="fe86f-135">-Timezone</span></span>
<span data-ttu-id="fe86f-136">O período de tempo</span><span class="sxs-lookup"><span data-stu-id="fe86f-136">The timezone</span></span>

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

### <span data-ttu-id="fe86f-137">-Visibilidade</span><span class="sxs-lookup"><span data-stu-id="fe86f-137">-Visibility</span></span>
<span data-ttu-id="fe86f-138">A visibilidade do escopo</span><span class="sxs-lookup"><span data-stu-id="fe86f-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="fe86f-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fe86f-139">-Confirm</span></span>
<span data-ttu-id="fe86f-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe86f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe86f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe86f-141">-WhatIf</span></span>
<span data-ttu-id="fe86f-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fe86f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe86f-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe86f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe86f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe86f-144">CommonParameters</span></span>
<span data-ttu-id="fe86f-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe86f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe86f-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe86f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe86f-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="fe86f-147">INPUTS</span></span>

### <span data-ttu-id="fe86f-148">System.String</span><span class="sxs-lookup"><span data-stu-id="fe86f-148">System.String</span></span>

## <span data-ttu-id="fe86f-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="fe86f-149">OUTPUTS</span></span>

### <span data-ttu-id="fe86f-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe86f-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="fe86f-151">Notas</span><span class="sxs-lookup"><span data-stu-id="fe86f-151">NOTES</span></span>

## <span data-ttu-id="fe86f-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe86f-152">RELATED LINKS</span></span>
