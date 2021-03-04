---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: f187a2704ed1f23d6cc5ac7dded1c8d9cd8ae954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892693"
---
# <span data-ttu-id="c1e5e-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="c1e5e-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="c1e5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="c1e5e-103">Cria um novo Ouvinte de Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="c1e5e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c1e5e-104">SYNTAX</span></span>

### <span data-ttu-id="c1e5e-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c1e5e-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1e5e-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="c1e5e-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1e5e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c1e5e-107">DESCRIPTION</span></span>
<span data-ttu-id="c1e5e-108">O New-AzAvailabilityGroupListener cmdlet cria um novo Ouvinte de Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="c1e5e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1e5e-109">EXAMPLES</span></span>

### <span data-ttu-id="c1e5e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1e5e-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="c1e5e-111">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e5e-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="c1e5e-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="c1e5e-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="c1e5e-113">Cria um novo Ouvinte do Grupo de Disponibilidade AgListener01 para o Grupo de DisponibilidadeGroup01 no SQL Grupo de Máquinas Virtuais SqlVmGroup01.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="c1e5e-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c1e5e-114">PARAMETERS</span></span>

### <span data-ttu-id="c1e5e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1e5e-115">-AsJob</span></span>
<span data-ttu-id="c1e5e-116">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c1e5e-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e5e-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="c1e5e-118">Nome do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-118">Availability Group name.</span></span>

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

### <span data-ttu-id="c1e5e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1e5e-119">-DefaultProfile</span></span>
<span data-ttu-id="c1e5e-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1e5e-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="c1e5e-121">-IpAddress</span></span>
<span data-ttu-id="c1e5e-122">Endereço Ip Particular</span><span class="sxs-lookup"><span data-stu-id="c1e5e-122">Private Ip Address</span></span>

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

### <span data-ttu-id="c1e5e-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="c1e5e-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="c1e5e-124">ID do Balanceador de Carga</span><span class="sxs-lookup"><span data-stu-id="c1e5e-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="c1e5e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c1e5e-125">-Name</span></span>
<span data-ttu-id="c1e5e-126">Nome do Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e5e-127">-Port</span><span class="sxs-lookup"><span data-stu-id="c1e5e-127">-Port</span></span>
<span data-ttu-id="c1e5e-128">Número da porta do Ouvinte AG.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-128">Port number of AG Listener.</span></span> <span data-ttu-id="c1e5e-129">Valor padrão é 1433.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-129">Default Value is 1433.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e5e-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="c1e5e-130">-ProbePort</span></span>
<span data-ttu-id="c1e5e-131">Porta sonda</span><span class="sxs-lookup"><span data-stu-id="c1e5e-131">Probe Port</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e5e-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="c1e5e-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="c1e5e-133">ID do Recurso de Endereço Ip Público</span><span class="sxs-lookup"><span data-stu-id="c1e5e-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="c1e5e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e5e-134">-ResourceGroupName</span></span>
<span data-ttu-id="c1e5e-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="c1e5e-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c1e5e-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="c1e5e-137">Lista de IDs de Recursos de VM Sql</span><span class="sxs-lookup"><span data-stu-id="c1e5e-137">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1e5e-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="c1e5e-138">-SqlVMGroupName</span></span>
<span data-ttu-id="c1e5e-139">SQL nome do grupo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="c1e5e-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="c1e5e-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="c1e5e-141">SQL objeto Group da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="c1e5e-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c1e5e-142">-SubnetId</span></span>
<span data-ttu-id="c1e5e-143">ID do Recurso de Sub-rede</span><span class="sxs-lookup"><span data-stu-id="c1e5e-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="c1e5e-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1e5e-144">-Confirm</span></span>
<span data-ttu-id="c1e5e-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1e5e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1e5e-146">-WhatIf</span></span>
<span data-ttu-id="c1e5e-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1e5e-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1e5e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1e5e-149">CommonParameters</span></span>
<span data-ttu-id="c1e5e-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1e5e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1e5e-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1e5e-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1e5e-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1e5e-152">INPUTS</span></span>

### <span data-ttu-id="c1e5e-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="c1e5e-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="c1e5e-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c1e5e-154">OUTPUTS</span></span>

### <span data-ttu-id="c1e5e-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="c1e5e-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="c1e5e-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="c1e5e-156">NOTES</span></span>

## <span data-ttu-id="c1e5e-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1e5e-157">RELATED LINKS</span></span>
