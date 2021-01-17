---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433545"
---
# <span data-ttu-id="f032b-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="f032b-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="f032b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f032b-102">SYNOPSIS</span></span>
<span data-ttu-id="f032b-103">Registrar a configuração do recurso.</span><span class="sxs-lookup"><span data-stu-id="f032b-103">Register configuration for resource.</span></span>

## <span data-ttu-id="f032b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f032b-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f032b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f032b-105">DESCRIPTION</span></span>
<span data-ttu-id="f032b-106">Registre a configuração de manutenção do recurso.</span><span class="sxs-lookup"><span data-stu-id="f032b-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="f032b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f032b-107">EXAMPLES</span></span>

### <span data-ttu-id="f032b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f032b-108">Example 1</span></span>
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

<span data-ttu-id="f032b-109">Registre a configuração de manutenção para o host dedicado.</span><span class="sxs-lookup"><span data-stu-id="f032b-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="f032b-110">OS</span><span class="sxs-lookup"><span data-stu-id="f032b-110">PARAMETERS</span></span>

### <span data-ttu-id="f032b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f032b-111">-AsJob</span></span>
<span data-ttu-id="f032b-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f032b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f032b-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f032b-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="f032b-114">O nome da atribuição de configuração deve corresponder ao MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="f032b-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="f032b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f032b-115">-DefaultProfile</span></span>
<span data-ttu-id="f032b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f032b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f032b-117">-Local</span><span class="sxs-lookup"><span data-stu-id="f032b-117">-Location</span></span>
<span data-ttu-id="f032b-118">O local sem espaços para o recurso.</span><span class="sxs-lookup"><span data-stu-id="f032b-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="f032b-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f032b-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="f032b-120">A MaintenanceConfiguration totalmente qualificada.</span><span class="sxs-lookup"><span data-stu-id="f032b-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="f032b-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="f032b-121">-ProviderName</span></span>
<span data-ttu-id="f032b-122">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="f032b-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="f032b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f032b-123">-ResourceGroupName</span></span>
<span data-ttu-id="f032b-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f032b-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="f032b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f032b-125">-ResourceId</span></span>
<span data-ttu-id="f032b-126">O nome da atribuição de configuração deve corresponder ao MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="f032b-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="f032b-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f032b-127">-ResourceName</span></span>
<span data-ttu-id="f032b-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f032b-128">The resource name.</span></span>

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

### <span data-ttu-id="f032b-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="f032b-129">-ResourceParentName</span></span>
<span data-ttu-id="f032b-130">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="f032b-130">The parent resource name.</span></span>

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

### <span data-ttu-id="f032b-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="f032b-131">-ResourceParentType</span></span>
<span data-ttu-id="f032b-132">O tipo de recurso pai.</span><span class="sxs-lookup"><span data-stu-id="f032b-132">The parent resource type.</span></span>

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

### <span data-ttu-id="f032b-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f032b-133">-ResourceType</span></span>
<span data-ttu-id="f032b-134">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="f032b-134">The resource type.</span></span>

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

### <span data-ttu-id="f032b-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f032b-135">-Confirm</span></span>
<span data-ttu-id="f032b-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f032b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f032b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f032b-137">-WhatIf</span></span>
<span data-ttu-id="f032b-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f032b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f032b-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f032b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f032b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f032b-140">CommonParameters</span></span>
<span data-ttu-id="f032b-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f032b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f032b-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f032b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f032b-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f032b-143">INPUTS</span></span>

### <span data-ttu-id="f032b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f032b-144">System.String</span></span>

## <span data-ttu-id="f032b-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f032b-145">OUTPUTS</span></span>

### <span data-ttu-id="f032b-146">Microsoft. Azure. Commands. maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="f032b-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="f032b-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f032b-147">NOTES</span></span>

## <span data-ttu-id="f032b-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f032b-148">RELATED LINKS</span></span>
