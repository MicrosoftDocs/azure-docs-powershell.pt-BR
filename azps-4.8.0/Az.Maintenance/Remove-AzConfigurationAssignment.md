---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111643"
---
# <span data-ttu-id="e01cc-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="e01cc-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="e01cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e01cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e01cc-103">Cancelar o registro de configuração do recurso.</span><span class="sxs-lookup"><span data-stu-id="e01cc-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="e01cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e01cc-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e01cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e01cc-105">DESCRIPTION</span></span>
<span data-ttu-id="e01cc-106">Cancelar o registro de configuração do recurso.</span><span class="sxs-lookup"><span data-stu-id="e01cc-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="e01cc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e01cc-107">EXAMPLES</span></span>

### <span data-ttu-id="e01cc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e01cc-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="e01cc-109">Cancelar o registro de configuração do recurso.</span><span class="sxs-lookup"><span data-stu-id="e01cc-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="e01cc-110">OS</span><span class="sxs-lookup"><span data-stu-id="e01cc-110">PARAMETERS</span></span>

### <span data-ttu-id="e01cc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e01cc-111">-AsJob</span></span>
<span data-ttu-id="e01cc-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e01cc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e01cc-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e01cc-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="e01cc-114">O nome da atribuição de configuração.</span><span class="sxs-lookup"><span data-stu-id="e01cc-114">The configuration assignment name.</span></span>

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

### <span data-ttu-id="e01cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e01cc-115">-DefaultProfile</span></span>
<span data-ttu-id="e01cc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e01cc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e01cc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e01cc-117">-Force</span></span>
<span data-ttu-id="e01cc-118">Force remover sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="e01cc-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="e01cc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e01cc-119">-PassThru</span></span>
<span data-ttu-id="e01cc-120">Retorna o status da operação de remoção.</span><span class="sxs-lookup"><span data-stu-id="e01cc-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="e01cc-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e01cc-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e01cc-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="e01cc-122">-ProviderName</span></span>
<span data-ttu-id="e01cc-123">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="e01cc-123">The resource provider Name.</span></span>

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

### <span data-ttu-id="e01cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e01cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="e01cc-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e01cc-125">The resource Group Name.</span></span>

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

### <span data-ttu-id="e01cc-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e01cc-126">-ResourceName</span></span>
<span data-ttu-id="e01cc-127">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e01cc-127">The resource name.</span></span>

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

### <span data-ttu-id="e01cc-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="e01cc-128">-ResourceParentName</span></span>
<span data-ttu-id="e01cc-129">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="e01cc-129">The parent resource name.</span></span>

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

### <span data-ttu-id="e01cc-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="e01cc-130">-ResourceParentType</span></span>
<span data-ttu-id="e01cc-131">O tipo de recurso pai.</span><span class="sxs-lookup"><span data-stu-id="e01cc-131">The parent resource type.</span></span>

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

### <span data-ttu-id="e01cc-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e01cc-132">-ResourceType</span></span>
<span data-ttu-id="e01cc-133">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e01cc-133">The resource type.</span></span>

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

### <span data-ttu-id="e01cc-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e01cc-134">-Confirm</span></span>
<span data-ttu-id="e01cc-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e01cc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e01cc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e01cc-136">-WhatIf</span></span>
<span data-ttu-id="e01cc-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e01cc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e01cc-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e01cc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e01cc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e01cc-139">CommonParameters</span></span>
<span data-ttu-id="e01cc-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e01cc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e01cc-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e01cc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e01cc-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e01cc-142">INPUTS</span></span>

### <span data-ttu-id="e01cc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e01cc-143">System.String</span></span>

## <span data-ttu-id="e01cc-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e01cc-144">OUTPUTS</span></span>

### <span data-ttu-id="e01cc-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e01cc-145">System.Boolean</span></span>

## <span data-ttu-id="e01cc-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e01cc-146">NOTES</span></span>

## <span data-ttu-id="e01cc-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e01cc-147">RELATED LINKS</span></span>
