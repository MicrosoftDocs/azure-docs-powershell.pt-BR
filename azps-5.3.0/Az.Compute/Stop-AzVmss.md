---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: ac961b4e7032d793cecb46008fe62091dca052f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434161"
---
# <span data-ttu-id="f53d4-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f53d4-101">Stop-AzVmss</span></span>

## <span data-ttu-id="f53d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f53d4-102">SYNOPSIS</span></span>
<span data-ttu-id="f53d4-103">Interrompe o VMSS ou um conjunto de máquinas virtuais dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="f53d4-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="f53d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f53d4-104">SYNTAX</span></span>

### <span data-ttu-id="f53d4-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="f53d4-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f53d4-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="f53d4-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f53d4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f53d4-107">DESCRIPTION</span></span>
<span data-ttu-id="f53d4-108">O cmdlet **Stop-AzVmss** interrompe todas as máquinas virtuais dentro do VMSS (conjunto de dimensionamento de máquina virtual) ou um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="f53d4-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="f53d4-109">Você pode usar o parâmetro *InstanceId* para selecionar um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="f53d4-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="f53d4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f53d4-110">EXAMPLES</span></span>

### <span data-ttu-id="f53d4-111">Exemplo 1: parar todas as máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="f53d4-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="f53d4-112">Esse comando interrompe todas as máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="f53d4-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="f53d4-113">Exemplo 2: parar um conjunto específico de máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="f53d4-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="f53d4-114">Esse comando para o conjunto específico de máquinas virtuais especificado pela matriz de cadeia de caracteres de ID de instância que pertence ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="f53d4-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="f53d4-115">OS</span><span class="sxs-lookup"><span data-stu-id="f53d4-115">PARAMETERS</span></span>

### <span data-ttu-id="f53d4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f53d4-116">-AsJob</span></span>
<span data-ttu-id="f53d4-117">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="f53d4-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f53d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53d4-118">-DefaultProfile</span></span>
<span data-ttu-id="f53d4-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f53d4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f53d4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f53d4-120">-Force</span></span>
<span data-ttu-id="f53d4-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f53d4-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f53d4-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f53d4-122">-InstanceId</span></span>
<span data-ttu-id="f53d4-123">Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs das instâncias da máquina virtual em que esse cmdlet para.</span><span class="sxs-lookup"><span data-stu-id="f53d4-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="f53d4-124">Por exemplo: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="f53d4-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="f53d4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53d4-125">-ResourceGroupName</span></span>
<span data-ttu-id="f53d4-126">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="f53d4-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="f53d4-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="f53d4-127">-SkipShutdown</span></span>
<span data-ttu-id="f53d4-128">Para solicitar o desligamento não-normal da VM</span><span class="sxs-lookup"><span data-stu-id="f53d4-128">To request non-graceful VM shutdown</span></span>

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

### <span data-ttu-id="f53d4-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="f53d4-129">-StayProvisioned</span></span>
<span data-ttu-id="f53d4-130">Se especificado, a máquina virtual irá entrar no estado parado.</span><span class="sxs-lookup"><span data-stu-id="f53d4-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="f53d4-131">Se não for especificado, a máquina virtual entrará no estado parado-desatribuído.</span><span class="sxs-lookup"><span data-stu-id="f53d4-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="f53d4-132">O usuário ainda é cobrado por VMs no estado parado, mas não para VMs no estado parado-desatribuído.</span><span class="sxs-lookup"><span data-stu-id="f53d4-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

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

### <span data-ttu-id="f53d4-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f53d4-133">-VMScaleSetName</span></span>
<span data-ttu-id="f53d4-134">Especifica o nome do VMSS para o qual esse cmdlet interrompe as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="f53d4-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="f53d4-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f53d4-135">-Confirm</span></span>
<span data-ttu-id="f53d4-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f53d4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f53d4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f53d4-137">-WhatIf</span></span>
<span data-ttu-id="f53d4-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f53d4-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f53d4-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f53d4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f53d4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53d4-140">CommonParameters</span></span>
<span data-ttu-id="f53d4-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f53d4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53d4-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f53d4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53d4-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f53d4-143">INPUTS</span></span>

### <span data-ttu-id="f53d4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f53d4-144">System.String</span></span>

### <span data-ttu-id="f53d4-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="f53d4-145">System.String[]</span></span>

## <span data-ttu-id="f53d4-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f53d4-146">OUTPUTS</span></span>

### <span data-ttu-id="f53d4-147">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f53d4-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f53d4-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f53d4-148">NOTES</span></span>

## <span data-ttu-id="f53d4-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f53d4-149">RELATED LINKS</span></span>

[<span data-ttu-id="f53d4-150">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f53d4-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="f53d4-151">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f53d4-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="f53d4-152">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f53d4-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="f53d4-153">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f53d4-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="f53d4-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f53d4-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="f53d4-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f53d4-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="f53d4-156">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f53d4-156">Update-AzVmss</span></span>](./Update-AzVmss.md)


