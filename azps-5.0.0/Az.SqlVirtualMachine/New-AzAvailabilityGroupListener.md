---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124719"
---
# <span data-ttu-id="7b0f8-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="7b0f8-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="7b0f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b0f8-102">SYNOPSIS</span></span>
<span data-ttu-id="7b0f8-103">Cria um novo ouvinte de grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="7b0f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b0f8-104">SYNTAX</span></span>

### <span data-ttu-id="7b0f8-105">Nome (padrão)</span><span class="sxs-lookup"><span data-stu-id="7b0f8-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b0f8-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="7b0f8-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b0f8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b0f8-107">DESCRIPTION</span></span>
<span data-ttu-id="7b0f8-108">O cmdlet New-AzAvailabilityGroupListener cria um novo ouvinte de grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="7b0f8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b0f8-109">EXAMPLES</span></span>

### <span data-ttu-id="7b0f8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7b0f8-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="7b0f8-111">Nome ResourceGroupName Nome_do_grupo AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="7b0f8-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="7b0f8-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="7b0f8-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="7b0f8-113">Cria um novo ouvinte de escuta do grupo de AgListener01 para o AvailabilityGroup01 do grupo de disponibilidade no grupo SqlVmGroup01 do grupo da máquina virtual do SQL.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="7b0f8-114">OS</span><span class="sxs-lookup"><span data-stu-id="7b0f8-114">PARAMETERS</span></span>

### <span data-ttu-id="7b0f8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b0f8-115">-AsJob</span></span>
<span data-ttu-id="7b0f8-116">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7b0f8-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="7b0f8-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="7b0f8-118">Nome do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-118">Availability Group name.</span></span>

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

### <span data-ttu-id="7b0f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b0f8-119">-DefaultProfile</span></span>
<span data-ttu-id="7b0f8-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b0f8-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="7b0f8-121">-IpAddress</span></span>
<span data-ttu-id="7b0f8-122">Endereço IP privado</span><span class="sxs-lookup"><span data-stu-id="7b0f8-122">Private Ip Address</span></span>

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

### <span data-ttu-id="7b0f8-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="7b0f8-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="7b0f8-124">ID do balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="7b0f8-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="7b0f8-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b0f8-125">-Name</span></span>
<span data-ttu-id="7b0f8-126">Nome do ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="7b0f8-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="7b0f8-127">-Port</span></span>
<span data-ttu-id="7b0f8-128">Número da porta do ouvinte AG.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-128">Port number of AG Listener.</span></span> <span data-ttu-id="7b0f8-129">O valor padrão é 1433.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-129">Default Value is 1433.</span></span>

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

### <span data-ttu-id="7b0f8-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="7b0f8-130">-ProbePort</span></span>
<span data-ttu-id="7b0f8-131">Porta de investigação</span><span class="sxs-lookup"><span data-stu-id="7b0f8-131">Probe Port</span></span>

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

### <span data-ttu-id="7b0f8-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="7b0f8-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="7b0f8-133">ID do recurso do endereço IP público</span><span class="sxs-lookup"><span data-stu-id="7b0f8-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="7b0f8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b0f8-134">-ResourceGroupName</span></span>
<span data-ttu-id="7b0f8-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="7b0f8-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="7b0f8-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="7b0f8-137">Lista de IDs de recursos de VM do SQL</span><span class="sxs-lookup"><span data-stu-id="7b0f8-137">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="7b0f8-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="7b0f8-138">-SqlVMGroupName</span></span>
<span data-ttu-id="7b0f8-139">Nome do grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="7b0f8-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="7b0f8-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="7b0f8-141">Objeto de grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="7b0f8-142">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="7b0f8-142">-SubnetId</span></span>
<span data-ttu-id="7b0f8-143">ID do recurso de sub-rede</span><span class="sxs-lookup"><span data-stu-id="7b0f8-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="7b0f8-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7b0f8-144">-Confirm</span></span>
<span data-ttu-id="7b0f8-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b0f8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b0f8-146">-WhatIf</span></span>
<span data-ttu-id="7b0f8-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b0f8-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b0f8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b0f8-149">CommonParameters</span></span>
<span data-ttu-id="7b0f8-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b0f8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b0f8-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b0f8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b0f8-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b0f8-152">INPUTS</span></span>

### <span data-ttu-id="7b0f8-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="7b0f8-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="7b0f8-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b0f8-154">OUTPUTS</span></span>

### <span data-ttu-id="7b0f8-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="7b0f8-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="7b0f8-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b0f8-156">NOTES</span></span>

## <span data-ttu-id="7b0f8-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b0f8-157">RELATED LINKS</span></span>
