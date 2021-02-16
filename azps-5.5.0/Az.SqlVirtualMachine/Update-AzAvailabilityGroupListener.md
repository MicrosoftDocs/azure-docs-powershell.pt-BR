---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113699"
---
# <span data-ttu-id="47344-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="47344-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="47344-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47344-102">SYNOPSIS</span></span>
<span data-ttu-id="47344-103">Atualiza o Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="47344-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="47344-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47344-104">SYNTAX</span></span>

### <span data-ttu-id="47344-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="47344-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47344-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="47344-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47344-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="47344-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47344-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="47344-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47344-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="47344-109">DESCRIPTION</span></span>
<span data-ttu-id="47344-110">O Update-AzAvailabilityGroupListener cmdlet atualiza um Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="47344-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="47344-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47344-111">EXAMPLES</span></span>

### <span data-ttu-id="47344-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="47344-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="47344-113">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="47344-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="47344-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="47344-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="47344-115">Atualiza a lista de MÁQUINAS Virtuais SQL para o Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="47344-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="47344-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47344-116">PARAMETERS</span></span>

### <span data-ttu-id="47344-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47344-117">-AsJob</span></span>
<span data-ttu-id="47344-118">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="47344-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="47344-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47344-119">-DefaultProfile</span></span>
<span data-ttu-id="47344-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47344-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47344-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47344-121">-InputObject</span></span>
<span data-ttu-id="47344-122">Objeto Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="47344-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="47344-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="47344-123">-Name</span></span>
<span data-ttu-id="47344-124">Nome do Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="47344-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="47344-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47344-125">-ResourceGroupName</span></span>
<span data-ttu-id="47344-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="47344-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="47344-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47344-127">-ResourceId</span></span>
<span data-ttu-id="47344-128">ID do Recurso de Ouvinte do Grupo de Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="47344-128">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: AvailabilityGroupListenerId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47344-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="47344-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="47344-130">Lista de IDs de Recursos do Sql VM</span><span class="sxs-lookup"><span data-stu-id="47344-130">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47344-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="47344-131">-SqlVMGroupName</span></span>
<span data-ttu-id="47344-132">Nome do grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="47344-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="47344-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="47344-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="47344-134">Objeto do grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="47344-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="47344-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="47344-135">-Confirm</span></span>
<span data-ttu-id="47344-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47344-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47344-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47344-137">-WhatIf</span></span>
<span data-ttu-id="47344-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="47344-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47344-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47344-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47344-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47344-140">CommonParameters</span></span>
<span data-ttu-id="47344-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47344-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47344-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47344-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47344-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="47344-143">INPUTS</span></span>

### <span data-ttu-id="47344-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="47344-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="47344-145">System.String</span><span class="sxs-lookup"><span data-stu-id="47344-145">System.String</span></span>

### <span data-ttu-id="47344-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="47344-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="47344-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="47344-147">OUTPUTS</span></span>

### <span data-ttu-id="47344-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="47344-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="47344-149">Notas</span><span class="sxs-lookup"><span data-stu-id="47344-149">NOTES</span></span>

## <span data-ttu-id="47344-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47344-150">RELATED LINKS</span></span>
