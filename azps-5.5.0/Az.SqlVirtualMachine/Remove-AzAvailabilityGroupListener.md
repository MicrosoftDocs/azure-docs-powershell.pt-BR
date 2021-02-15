---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112528"
---
# <span data-ttu-id="e36d4-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="e36d4-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="e36d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e36d4-102">SYNOPSIS</span></span>
<span data-ttu-id="e36d4-103">Exclui um Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="e36d4-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="e36d4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e36d4-104">SYNTAX</span></span>

### <span data-ttu-id="e36d4-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e36d4-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e36d4-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="e36d4-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e36d4-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="e36d4-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e36d4-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="e36d4-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e36d4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e36d4-109">DESCRIPTION</span></span>
<span data-ttu-id="e36d4-110">O cmdlet Remove-AzAvailabilityGroupListener exclui um Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="e36d4-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="e36d4-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e36d4-111">EXAMPLES</span></span>

### <span data-ttu-id="e36d4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e36d4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="e36d4-113">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="e36d4-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="e36d4-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="e36d4-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="e36d4-115">Exclui o Grupo de Disponibilidade Do Ouvinte AgListener01 no Grupo de Disponibilidade AvailabilityGroup01.</span><span class="sxs-lookup"><span data-stu-id="e36d4-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="e36d4-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e36d4-116">PARAMETERS</span></span>

### <span data-ttu-id="e36d4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e36d4-117">-AsJob</span></span>
<span data-ttu-id="e36d4-118">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="e36d4-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e36d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36d4-119">-DefaultProfile</span></span>
<span data-ttu-id="e36d4-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e36d4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e36d4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e36d4-121">-InputObject</span></span>
<span data-ttu-id="e36d4-122">Objeto Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="e36d4-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e36d4-123">-Name</span></span>
<span data-ttu-id="e36d4-124">Nome do Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="e36d4-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e36d4-125">-PassThru</span></span>
<span data-ttu-id="e36d4-126">Especifica se o recurso excluído será saída no final da execução do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e36d4-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="e36d4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e36d4-127">-ResourceGroupName</span></span>
<span data-ttu-id="e36d4-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e36d4-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e36d4-129">-ResourceId</span></span>
<span data-ttu-id="e36d4-130">ID do Recurso de Ouvinte do Grupo de Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="e36d4-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="e36d4-131">-SqlVMGroupName</span></span>
<span data-ttu-id="e36d4-132">Nome do grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="e36d4-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="e36d4-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="e36d4-134">Objeto do grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="e36d4-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e36d4-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e36d4-135">-Confirm</span></span>
<span data-ttu-id="e36d4-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e36d4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e36d4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e36d4-137">-WhatIf</span></span>
<span data-ttu-id="e36d4-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e36d4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e36d4-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e36d4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e36d4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36d4-140">CommonParameters</span></span>
<span data-ttu-id="e36d4-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36d4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36d4-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e36d4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36d4-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="e36d4-143">INPUTS</span></span>

### <span data-ttu-id="e36d4-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="e36d4-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="e36d4-145">System.String</span><span class="sxs-lookup"><span data-stu-id="e36d4-145">System.String</span></span>

### <span data-ttu-id="e36d4-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="e36d4-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="e36d4-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="e36d4-147">OUTPUTS</span></span>

### <span data-ttu-id="e36d4-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="e36d4-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="e36d4-149">Notas</span><span class="sxs-lookup"><span data-stu-id="e36d4-149">NOTES</span></span>

## <span data-ttu-id="e36d4-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e36d4-150">RELATED LINKS</span></span>
