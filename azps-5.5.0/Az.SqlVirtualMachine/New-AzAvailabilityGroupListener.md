---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116120"
---
# <span data-ttu-id="45525-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="45525-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="45525-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45525-102">SYNOPSIS</span></span>
<span data-ttu-id="45525-103">Cria um novo Ouvinte de Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="45525-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="45525-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45525-104">SYNTAX</span></span>

### <span data-ttu-id="45525-105">Nome (Padrão)</span><span class="sxs-lookup"><span data-stu-id="45525-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45525-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="45525-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45525-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="45525-107">DESCRIPTION</span></span>
<span data-ttu-id="45525-108">O New-AzAvailabilityGroupListener cmdlet cria um novo Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="45525-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="45525-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="45525-109">EXAMPLES</span></span>

### <span data-ttu-id="45525-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45525-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="45525-111">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="45525-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="45525-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="45525-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="45525-113">Cria um novo Grupo de Disponibilidade Do Ouvinte AgListener01 para o Grupo de Disponibilidade AvailabilityGroup01 no SQL Virtual Machine Group SqlVmGroup01.</span><span class="sxs-lookup"><span data-stu-id="45525-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="45525-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45525-114">PARAMETERS</span></span>

### <span data-ttu-id="45525-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45525-115">-AsJob</span></span>
<span data-ttu-id="45525-116">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="45525-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="45525-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="45525-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="45525-118">Nome do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="45525-118">Availability Group name.</span></span>

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

### <span data-ttu-id="45525-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45525-119">-DefaultProfile</span></span>
<span data-ttu-id="45525-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45525-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45525-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="45525-121">-IpAddress</span></span>
<span data-ttu-id="45525-122">Endereço Ip Particular</span><span class="sxs-lookup"><span data-stu-id="45525-122">Private Ip Address</span></span>

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

### <span data-ttu-id="45525-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="45525-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="45525-124">ID do Balanceador de Carga</span><span class="sxs-lookup"><span data-stu-id="45525-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="45525-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="45525-125">-Name</span></span>
<span data-ttu-id="45525-126">Nome do Ouvinte do Grupo de Disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="45525-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="45525-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="45525-127">-Port</span></span>
<span data-ttu-id="45525-128">Número da porta do AG Listener.</span><span class="sxs-lookup"><span data-stu-id="45525-128">Port number of AG Listener.</span></span> <span data-ttu-id="45525-129">O Valor Padrão é 1433.</span><span class="sxs-lookup"><span data-stu-id="45525-129">Default Value is 1433.</span></span>

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

### <span data-ttu-id="45525-130">-Eleport</span><span class="sxs-lookup"><span data-stu-id="45525-130">-ProbePort</span></span>
<span data-ttu-id="45525-131">Porta Descarrém</span><span class="sxs-lookup"><span data-stu-id="45525-131">Probe Port</span></span>

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

### <span data-ttu-id="45525-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="45525-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="45525-133">ID do Recurso de Endereço Ip Público</span><span class="sxs-lookup"><span data-stu-id="45525-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="45525-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45525-134">-ResourceGroupName</span></span>
<span data-ttu-id="45525-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45525-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="45525-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="45525-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="45525-137">Lista de IDs de Recursos do Sql VM</span><span class="sxs-lookup"><span data-stu-id="45525-137">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="45525-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="45525-138">-SqlVMGroupName</span></span>
<span data-ttu-id="45525-139">Nome do grupo de máquina virtual SQL.</span><span class="sxs-lookup"><span data-stu-id="45525-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="45525-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="45525-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="45525-141">Objeto do grupo de máquinas virtuais SQL.</span><span class="sxs-lookup"><span data-stu-id="45525-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="45525-142">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="45525-142">-SubnetId</span></span>
<span data-ttu-id="45525-143">ID do Recurso da Sub-rede</span><span class="sxs-lookup"><span data-stu-id="45525-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="45525-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="45525-144">-Confirm</span></span>
<span data-ttu-id="45525-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45525-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45525-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45525-146">-WhatIf</span></span>
<span data-ttu-id="45525-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="45525-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45525-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45525-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45525-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45525-149">CommonParameters</span></span>
<span data-ttu-id="45525-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45525-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45525-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45525-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45525-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="45525-152">INPUTS</span></span>

### <span data-ttu-id="45525-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="45525-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="45525-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="45525-154">OUTPUTS</span></span>

### <span data-ttu-id="45525-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="45525-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="45525-156">Notas</span><span class="sxs-lookup"><span data-stu-id="45525-156">NOTES</span></span>

## <span data-ttu-id="45525-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45525-157">RELATED LINKS</span></span>
