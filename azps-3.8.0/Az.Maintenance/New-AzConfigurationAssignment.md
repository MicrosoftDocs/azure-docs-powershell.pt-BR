---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: f0c5c52773d5750b86ce82d696e9130df76f4700
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944222"
---
# <span data-ttu-id="e0dce-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="e0dce-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="e0dce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0dce-102">SYNOPSIS</span></span>
<span data-ttu-id="e0dce-103">Registrar a configuração do recurso.</span><span class="sxs-lookup"><span data-stu-id="e0dce-103">Register configuration for resource.</span></span>

## <span data-ttu-id="e0dce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0dce-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0dce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0dce-105">DESCRIPTION</span></span>
<span data-ttu-id="e0dce-106">Registre a configuração de manutenção do recurso.</span><span class="sxs-lookup"><span data-stu-id="e0dce-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="e0dce-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0dce-107">EXAMPLES</span></span>

### <span data-ttu-id="e0dce-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0dce-108">Example 1</span></span>
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

<span data-ttu-id="e0dce-109">Registre a configuração de manutenção para o host didicated.</span><span class="sxs-lookup"><span data-stu-id="e0dce-109">Register maintenance configuration for didicated host.</span></span>

## <span data-ttu-id="e0dce-110">OS</span><span class="sxs-lookup"><span data-stu-id="e0dce-110">PARAMETERS</span></span>

### <span data-ttu-id="e0dce-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0dce-111">-AsJob</span></span>
<span data-ttu-id="e0dce-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e0dce-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0dce-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e0dce-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="e0dce-114">O nome da atribuição de configuração deve corresponder ao MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="e0dce-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="e0dce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0dce-115">-DefaultProfile</span></span>
<span data-ttu-id="e0dce-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0dce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0dce-117">-Local</span><span class="sxs-lookup"><span data-stu-id="e0dce-117">-Location</span></span>
<span data-ttu-id="e0dce-118">O local sem espaços para o recurso.</span><span class="sxs-lookup"><span data-stu-id="e0dce-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="e0dce-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e0dce-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="e0dce-120">A MaintenanceConfiguration totalmente qualificada.</span><span class="sxs-lookup"><span data-stu-id="e0dce-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="e0dce-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="e0dce-121">-ProviderName</span></span>
<span data-ttu-id="e0dce-122">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0dce-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="e0dce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0dce-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0dce-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0dce-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="e0dce-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0dce-125">-ResourceId</span></span>
<span data-ttu-id="e0dce-126">O nome da atribuição de configuração deve corresponder ao MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="e0dce-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="e0dce-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e0dce-127">-ResourceName</span></span>
<span data-ttu-id="e0dce-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e0dce-128">The resource name.</span></span>

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

### <span data-ttu-id="e0dce-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="e0dce-129">-ResourceParentName</span></span>
<span data-ttu-id="e0dce-130">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="e0dce-130">The parent resource name.</span></span>

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

### <span data-ttu-id="e0dce-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="e0dce-131">-ResourceParentType</span></span>
<span data-ttu-id="e0dce-132">O tipo de recurso pai.</span><span class="sxs-lookup"><span data-stu-id="e0dce-132">The parent resource type.</span></span>

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

### <span data-ttu-id="e0dce-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e0dce-133">-ResourceType</span></span>
<span data-ttu-id="e0dce-134">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e0dce-134">The resource type.</span></span>

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

### <span data-ttu-id="e0dce-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0dce-135">-Confirm</span></span>
<span data-ttu-id="e0dce-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0dce-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0dce-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0dce-137">-WhatIf</span></span>
<span data-ttu-id="e0dce-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0dce-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0dce-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0dce-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0dce-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0dce-140">CommonParameters</span></span>
<span data-ttu-id="e0dce-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0dce-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0dce-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0dce-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0dce-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0dce-143">INPUTS</span></span>

### <span data-ttu-id="e0dce-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e0dce-144">System.String</span></span>

## <span data-ttu-id="e0dce-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0dce-145">OUTPUTS</span></span>

### <span data-ttu-id="e0dce-146">Microsoft. Azure. Commands. maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="e0dce-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="e0dce-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0dce-147">NOTES</span></span>

## <span data-ttu-id="e0dce-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0dce-148">RELATED LINKS</span></span>
