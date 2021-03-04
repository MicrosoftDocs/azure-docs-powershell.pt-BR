---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: c94f1e842697a64dd95f7d5ccb90e389484a61e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887292"
---
# <span data-ttu-id="ee774-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="ee774-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="ee774-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee774-102">SYNOPSIS</span></span>
<span data-ttu-id="ee774-103">Atualiza o Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="ee774-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="ee774-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ee774-104">SYNTAX</span></span>

### <span data-ttu-id="ee774-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ee774-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee774-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ee774-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee774-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee774-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee774-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="ee774-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee774-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ee774-109">DESCRIPTION</span></span>
<span data-ttu-id="ee774-110">O cmdlet Update-AzAvailabilityGroupListener atualiza um Ouvinte de Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="ee774-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="ee774-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee774-111">EXAMPLES</span></span>

### <span data-ttu-id="ee774-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ee774-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="ee774-113">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="ee774-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="ee774-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="ee774-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="ee774-115">Atualiza a lista de SQL Virtuais para o Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="ee774-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="ee774-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ee774-116">PARAMETERS</span></span>

### <span data-ttu-id="ee774-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee774-117">-AsJob</span></span>
<span data-ttu-id="ee774-118">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ee774-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ee774-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee774-119">-DefaultProfile</span></span>
<span data-ttu-id="ee774-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee774-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee774-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee774-121">-InputObject</span></span>
<span data-ttu-id="ee774-122">Objeto Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="ee774-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="ee774-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ee774-123">-Name</span></span>
<span data-ttu-id="ee774-124">Nome do Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="ee774-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="ee774-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee774-125">-ResourceGroupName</span></span>
<span data-ttu-id="ee774-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee774-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ee774-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee774-127">-ResourceId</span></span>
<span data-ttu-id="ee774-128">ID do Recurso ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="ee774-128">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="ee774-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="ee774-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="ee774-130">Lista de IDs de Recursos de VM Sql</span><span class="sxs-lookup"><span data-stu-id="ee774-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="ee774-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="ee774-131">-SqlVMGroupName</span></span>
<span data-ttu-id="ee774-132">SQL nome do grupo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee774-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="ee774-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="ee774-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="ee774-134">SQL objeto Group da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee774-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="ee774-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee774-135">-Confirm</span></span>
<span data-ttu-id="ee774-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee774-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee774-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee774-137">-WhatIf</span></span>
<span data-ttu-id="ee774-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee774-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee774-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee774-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee774-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee774-140">CommonParameters</span></span>
<span data-ttu-id="ee774-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee774-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee774-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee774-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee774-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee774-143">INPUTS</span></span>

### <span data-ttu-id="ee774-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="ee774-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="ee774-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ee774-145">System.String</span></span>

### <span data-ttu-id="ee774-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="ee774-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="ee774-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ee774-147">OUTPUTS</span></span>

### <span data-ttu-id="ee774-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="ee774-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="ee774-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="ee774-149">NOTES</span></span>

## <span data-ttu-id="ee774-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee774-150">RELATED LINKS</span></span>
