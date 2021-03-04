---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: eca73d71d213b31c0bbc339708cc744b3bf64d2a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886792"
---
# <span data-ttu-id="8387b-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="8387b-101">Restart-AzVM</span></span>

## <span data-ttu-id="8387b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8387b-102">SYNOPSIS</span></span>
<span data-ttu-id="8387b-103">Reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8387b-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="8387b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8387b-104">SYNTAX</span></span>

### <span data-ttu-id="8387b-105">RestartResourceGroupNameParameterSetName (Default)</span><span class="sxs-lookup"><span data-stu-id="8387b-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8387b-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8387b-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8387b-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8387b-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8387b-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8387b-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8387b-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8387b-109">DESCRIPTION</span></span>
<span data-ttu-id="8387b-110">O cmdlet **Restart-AzVM** reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8387b-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="8387b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8387b-111">EXAMPLES</span></span>

### <span data-ttu-id="8387b-112">Exemplo 1: Reiniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8387b-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8387b-113">Este comando reinicia a máquina virtual chamada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8387b-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="8387b-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8387b-114">PARAMETERS</span></span>

### <span data-ttu-id="8387b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8387b-115">-AsJob</span></span>
<span data-ttu-id="8387b-116">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="8387b-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8387b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8387b-117">-DefaultProfile</span></span>
<span data-ttu-id="8387b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8387b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8387b-119">-Id</span><span class="sxs-lookup"><span data-stu-id="8387b-119">-Id</span></span>
<span data-ttu-id="8387b-120">A ID da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8387b-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8387b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8387b-121">-Name</span></span>
<span data-ttu-id="8387b-122">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8387b-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8387b-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8387b-123">-NoWait</span></span>
<span data-ttu-id="8387b-124">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="8387b-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="8387b-125">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="8387b-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="8387b-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="8387b-126">-PerformMaintenance</span></span>
<span data-ttu-id="8387b-127">Para executar a manutenção da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8387b-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8387b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8387b-128">-ResourceGroupName</span></span>
<span data-ttu-id="8387b-129">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8387b-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8387b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8387b-130">-Confirm</span></span>
<span data-ttu-id="8387b-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8387b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8387b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8387b-132">-WhatIf</span></span>
<span data-ttu-id="8387b-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8387b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8387b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8387b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8387b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8387b-135">CommonParameters</span></span>
<span data-ttu-id="8387b-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8387b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8387b-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8387b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8387b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8387b-138">INPUTS</span></span>

### <span data-ttu-id="8387b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8387b-139">System.String</span></span>

### <span data-ttu-id="8387b-140">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8387b-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8387b-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8387b-141">OUTPUTS</span></span>

### <span data-ttu-id="8387b-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="8387b-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="8387b-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8387b-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8387b-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="8387b-144">NOTES</span></span>

## <span data-ttu-id="8387b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8387b-145">RELATED LINKS</span></span>

[<span data-ttu-id="8387b-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8387b-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8387b-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8387b-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="8387b-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="8387b-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="8387b-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="8387b-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="8387b-150">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="8387b-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="8387b-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8387b-151">Update-AzVM</span></span>](./Update-AzVM.md)


