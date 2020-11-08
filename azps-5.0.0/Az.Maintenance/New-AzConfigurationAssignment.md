---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117352"
---
# <span data-ttu-id="e21d0-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="e21d0-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="e21d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e21d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e21d0-103">Registrar a configuração do recurso.</span><span class="sxs-lookup"><span data-stu-id="e21d0-103">Register configuration for resource.</span></span>

## <span data-ttu-id="e21d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e21d0-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e21d0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e21d0-105">DESCRIPTION</span></span>
<span data-ttu-id="e21d0-106">Registre a configuração de manutenção do recurso.</span><span class="sxs-lookup"><span data-stu-id="e21d0-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="e21d0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e21d0-107">EXAMPLES</span></span>

### <span data-ttu-id="e21d0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e21d0-108">Example 1</span></span>
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

<span data-ttu-id="e21d0-109">Registre a configuração de manutenção para o host dedicado.</span><span class="sxs-lookup"><span data-stu-id="e21d0-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="e21d0-110">OS</span><span class="sxs-lookup"><span data-stu-id="e21d0-110">PARAMETERS</span></span>

### <span data-ttu-id="e21d0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e21d0-111">-AsJob</span></span>
<span data-ttu-id="e21d0-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e21d0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e21d0-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e21d0-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="e21d0-114">O nome da atribuição de configuração deve corresponder ao MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="e21d0-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="e21d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e21d0-115">-DefaultProfile</span></span>
<span data-ttu-id="e21d0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e21d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e21d0-117">-Local</span><span class="sxs-lookup"><span data-stu-id="e21d0-117">-Location</span></span>
<span data-ttu-id="e21d0-118">O local sem espaços para o recurso.</span><span class="sxs-lookup"><span data-stu-id="e21d0-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="e21d0-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e21d0-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="e21d0-120">A MaintenanceConfiguration totalmente qualificada.</span><span class="sxs-lookup"><span data-stu-id="e21d0-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="e21d0-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="e21d0-121">-ProviderName</span></span>
<span data-ttu-id="e21d0-122">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="e21d0-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="e21d0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e21d0-123">-ResourceGroupName</span></span>
<span data-ttu-id="e21d0-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e21d0-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="e21d0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e21d0-125">-ResourceId</span></span>
<span data-ttu-id="e21d0-126">O nome da atribuição de configuração deve corresponder ao MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="e21d0-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="e21d0-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e21d0-127">-ResourceName</span></span>
<span data-ttu-id="e21d0-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e21d0-128">The resource name.</span></span>

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

### <span data-ttu-id="e21d0-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="e21d0-129">-ResourceParentName</span></span>
<span data-ttu-id="e21d0-130">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="e21d0-130">The parent resource name.</span></span>

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

### <span data-ttu-id="e21d0-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="e21d0-131">-ResourceParentType</span></span>
<span data-ttu-id="e21d0-132">O tipo de recurso pai.</span><span class="sxs-lookup"><span data-stu-id="e21d0-132">The parent resource type.</span></span>

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

### <span data-ttu-id="e21d0-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e21d0-133">-ResourceType</span></span>
<span data-ttu-id="e21d0-134">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e21d0-134">The resource type.</span></span>

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

### <span data-ttu-id="e21d0-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e21d0-135">-Confirm</span></span>
<span data-ttu-id="e21d0-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e21d0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e21d0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e21d0-137">-WhatIf</span></span>
<span data-ttu-id="e21d0-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e21d0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e21d0-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e21d0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e21d0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21d0-140">CommonParameters</span></span>
<span data-ttu-id="e21d0-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e21d0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21d0-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e21d0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21d0-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e21d0-143">INPUTS</span></span>

### <span data-ttu-id="e21d0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e21d0-144">System.String</span></span>

## <span data-ttu-id="e21d0-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e21d0-145">OUTPUTS</span></span>

### <span data-ttu-id="e21d0-146">Microsoft. Azure. Commands. maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="e21d0-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="e21d0-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e21d0-147">NOTES</span></span>

## <span data-ttu-id="e21d0-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e21d0-148">RELATED LINKS</span></span>
