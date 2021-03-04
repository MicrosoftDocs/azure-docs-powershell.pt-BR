---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 993c1968d144a5a1a56a0bd3dff46a9920a90264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893266"
---
# <span data-ttu-id="4af1e-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="4af1e-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="4af1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4af1e-102">SYNOPSIS</span></span>
<span data-ttu-id="4af1e-103">Registre a configuração do recurso.</span><span class="sxs-lookup"><span data-stu-id="4af1e-103">Register configuration for resource.</span></span>

## <span data-ttu-id="4af1e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4af1e-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4af1e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4af1e-105">DESCRIPTION</span></span>
<span data-ttu-id="4af1e-106">Registre a configuração de manutenção do recurso.</span><span class="sxs-lookup"><span data-stu-id="4af1e-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="4af1e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4af1e-107">EXAMPLES</span></span>

### <span data-ttu-id="4af1e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4af1e-108">Example 1</span></span>
```powershell
PS C:\> New-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName -MaintenanceConfigurationId $maintenanceConfigurationCreated.Id -Location $location


Location                   : westus2
MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
ResourceId                 : 7b32ed22-dc7b-4a17-9c42-36c024f4c9f9
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="4af1e-109">Registre a configuração de manutenção para host dedicado.</span><span class="sxs-lookup"><span data-stu-id="4af1e-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="4af1e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4af1e-110">PARAMETERS</span></span>

### <span data-ttu-id="4af1e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4af1e-111">-AsJob</span></span>
<span data-ttu-id="4af1e-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4af1e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4af1e-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="4af1e-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="4af1e-114">O nome da atribuição de configuração deve corresponder ao MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="4af1e-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="4af1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af1e-115">-DefaultProfile</span></span>
<span data-ttu-id="4af1e-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4af1e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4af1e-117">-Location</span><span class="sxs-lookup"><span data-stu-id="4af1e-117">-Location</span></span>
<span data-ttu-id="4af1e-118">O local sem espaços para o recurso.</span><span class="sxs-lookup"><span data-stu-id="4af1e-118">The location without spaces for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af1e-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4af1e-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="4af1e-120">O MaintenanceConfiguration totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="4af1e-120">The fully qualified MaintenanceConfiguration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af1e-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="4af1e-121">-ProviderName</span></span>
<span data-ttu-id="4af1e-122">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="4af1e-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="4af1e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4af1e-123">-ResourceGroupName</span></span>
<span data-ttu-id="4af1e-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4af1e-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="4af1e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4af1e-125">-ResourceId</span></span>
<span data-ttu-id="4af1e-126">O nome da atribuição de configuração deve corresponder ao MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="4af1e-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="4af1e-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4af1e-127">-ResourceName</span></span>
<span data-ttu-id="4af1e-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4af1e-128">The resource name.</span></span>

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

### <span data-ttu-id="4af1e-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="4af1e-129">-ResourceParentName</span></span>
<span data-ttu-id="4af1e-130">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="4af1e-130">The parent resource name.</span></span>

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

### <span data-ttu-id="4af1e-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="4af1e-131">-ResourceParentType</span></span>
<span data-ttu-id="4af1e-132">O tipo de recurso pai.</span><span class="sxs-lookup"><span data-stu-id="4af1e-132">The parent resource type.</span></span>

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

### <span data-ttu-id="4af1e-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4af1e-133">-ResourceType</span></span>
<span data-ttu-id="4af1e-134">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="4af1e-134">The resource type.</span></span>

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

### <span data-ttu-id="4af1e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4af1e-135">-Confirm</span></span>
<span data-ttu-id="4af1e-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4af1e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4af1e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4af1e-137">-WhatIf</span></span>
<span data-ttu-id="4af1e-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4af1e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4af1e-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4af1e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4af1e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af1e-140">CommonParameters</span></span>
<span data-ttu-id="4af1e-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4af1e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af1e-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4af1e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af1e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4af1e-143">INPUTS</span></span>

### <span data-ttu-id="4af1e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="4af1e-144">System.String</span></span>

## <span data-ttu-id="4af1e-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4af1e-145">OUTPUTS</span></span>

### <span data-ttu-id="4af1e-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="4af1e-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="4af1e-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="4af1e-147">NOTES</span></span>

## <span data-ttu-id="4af1e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4af1e-148">RELATED LINKS</span></span>
