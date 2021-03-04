---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: 152be66a2e1582d9f8377e09e250d3cf044c64db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893000"
---
# <span data-ttu-id="db033-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="db033-101">Stop-AzVmss</span></span>

## <span data-ttu-id="db033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db033-102">SYNOPSIS</span></span>
<span data-ttu-id="db033-103">Interrompe o VMSS ou um conjunto de máquinas virtuais dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="db033-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="db033-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="db033-104">SYNTAX</span></span>

### <span data-ttu-id="db033-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="db033-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db033-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="db033-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db033-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="db033-107">DESCRIPTION</span></span>
<span data-ttu-id="db033-108">O cmdlet **Stop-AzVmss** interrompe todas as máquinas virtuais dentro do Conjunto de Escala de Máquina Virtual (VMSS) ou um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="db033-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="db033-109">Você pode usar o *parâmetro InstanceId* para selecionar um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="db033-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="db033-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db033-110">EXAMPLES</span></span>

### <span data-ttu-id="db033-111">Exemplo 1: Pare todas as máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="db033-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="db033-112">Este comando interrompe todas as máquinas virtuais que pertencem à VMSS chamada ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="db033-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="db033-113">Exemplo 2: Pare um conjunto específico de máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="db033-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="db033-114">Este comando interrompe um conjunto específico de máquinas virtuais especificadas pela matriz de cadeia de caracteres de ID de instância que pertencem à VMSS chamada ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="db033-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="db033-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="db033-115">PARAMETERS</span></span>

### <span data-ttu-id="db033-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db033-116">-AsJob</span></span>
<span data-ttu-id="db033-117">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="db033-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="db033-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db033-118">-DefaultProfile</span></span>
<span data-ttu-id="db033-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="db033-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db033-120">-Force</span><span class="sxs-lookup"><span data-stu-id="db033-120">-Force</span></span>
<span data-ttu-id="db033-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="db033-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="db033-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="db033-122">-InstanceId</span></span>
<span data-ttu-id="db033-123">Especifica, como uma matriz de cadeia de caracteres, as IDs ou IDs das instâncias da máquina virtual que esse cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="db033-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="db033-124">Por exemplo: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="db033-124">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db033-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db033-125">-ResourceGroupName</span></span>
<span data-ttu-id="db033-126">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="db033-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="db033-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="db033-127">-SkipShutdown</span></span>
<span data-ttu-id="db033-128">Para solicitar desligamento de VM não-graciosa</span><span class="sxs-lookup"><span data-stu-id="db033-128">To request non-graceful VM shutdown</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db033-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="db033-129">-StayProvisioned</span></span>
<span data-ttu-id="db033-130">Se especificado, a máquina virtual entrará no estado parado.</span><span class="sxs-lookup"><span data-stu-id="db033-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="db033-131">Se não for especificado, a máquina virtual entrará em estado de parada.</span><span class="sxs-lookup"><span data-stu-id="db033-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="db033-132">O usuário ainda é cobrado por VMs em estado interrompido, mas não por VMs em estado de parada.</span><span class="sxs-lookup"><span data-stu-id="db033-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db033-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="db033-133">-VMScaleSetName</span></span>
<span data-ttu-id="db033-134">Especifica o nome do VMSS para o qual este cmdlet interrompe as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="db033-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db033-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db033-135">-Confirm</span></span>
<span data-ttu-id="db033-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db033-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db033-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db033-137">-WhatIf</span></span>
<span data-ttu-id="db033-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db033-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db033-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db033-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db033-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db033-140">CommonParameters</span></span>
<span data-ttu-id="db033-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db033-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db033-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db033-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db033-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db033-143">INPUTS</span></span>

### <span data-ttu-id="db033-144">System.String</span><span class="sxs-lookup"><span data-stu-id="db033-144">System.String</span></span>

### <span data-ttu-id="db033-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="db033-145">System.String[]</span></span>

## <span data-ttu-id="db033-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="db033-146">OUTPUTS</span></span>

### <span data-ttu-id="db033-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="db033-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="db033-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="db033-148">NOTES</span></span>

## <span data-ttu-id="db033-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db033-149">RELATED LINKS</span></span>

[<span data-ttu-id="db033-150">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="db033-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="db033-151">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="db033-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="db033-152">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="db033-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="db033-153">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="db033-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="db033-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="db033-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="db033-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="db033-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="db033-156">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="db033-156">Update-AzVmss</span></span>](./Update-AzVmss.md)


