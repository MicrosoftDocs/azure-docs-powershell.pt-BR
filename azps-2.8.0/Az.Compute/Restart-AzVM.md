---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 8fe939bfb959a1a6bc2dc043dbc3948943aa2c05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597267"
---
# <span data-ttu-id="08232-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="08232-101">Restart-AzVM</span></span>

## <span data-ttu-id="08232-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08232-102">SYNOPSIS</span></span>
<span data-ttu-id="08232-103">Reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="08232-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="08232-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08232-104">SYNTAX</span></span>

### <span data-ttu-id="08232-105">RestartResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="08232-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08232-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="08232-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08232-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="08232-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08232-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="08232-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08232-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08232-109">DESCRIPTION</span></span>
<span data-ttu-id="08232-110">O cmdlet **Restart-AzVM** reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="08232-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="08232-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08232-111">EXAMPLES</span></span>

### <span data-ttu-id="08232-112">Exemplo 1: reiniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="08232-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="08232-113">Esse comando reinicia a máquina virtual chamada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="08232-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="08232-114">OS</span><span class="sxs-lookup"><span data-stu-id="08232-114">PARAMETERS</span></span>

### <span data-ttu-id="08232-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08232-115">-AsJob</span></span>
<span data-ttu-id="08232-116">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="08232-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="08232-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08232-117">-DefaultProfile</span></span>
<span data-ttu-id="08232-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08232-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08232-119">-ID</span><span class="sxs-lookup"><span data-stu-id="08232-119">-Id</span></span>
<span data-ttu-id="08232-120">A ID da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="08232-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="08232-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="08232-121">-Name</span></span>
<span data-ttu-id="08232-122">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="08232-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="08232-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="08232-123">-NoWait</span></span>
<span data-ttu-id="08232-124">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="08232-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="08232-125">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="08232-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="08232-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="08232-126">-PerformMaintenance</span></span>
<span data-ttu-id="08232-127">Para executar a manutenção da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="08232-127">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="08232-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08232-128">-ResourceGroupName</span></span>
<span data-ttu-id="08232-129">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="08232-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="08232-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="08232-130">-Confirm</span></span>
<span data-ttu-id="08232-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08232-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08232-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08232-132">-WhatIf</span></span>
<span data-ttu-id="08232-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="08232-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08232-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08232-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08232-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08232-135">CommonParameters</span></span>
<span data-ttu-id="08232-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08232-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08232-137">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08232-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08232-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08232-138">INPUTS</span></span>

### <span data-ttu-id="08232-139">System. String</span><span class="sxs-lookup"><span data-stu-id="08232-139">System.String</span></span>

### <span data-ttu-id="08232-140">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="08232-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="08232-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08232-141">OUTPUTS</span></span>

### <span data-ttu-id="08232-142">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="08232-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="08232-143">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="08232-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="08232-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08232-144">NOTES</span></span>

## <span data-ttu-id="08232-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08232-145">RELATED LINKS</span></span>

[<span data-ttu-id="08232-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="08232-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="08232-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="08232-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="08232-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="08232-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="08232-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="08232-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="08232-150">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="08232-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="08232-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="08232-151">Update-AzVM</span></span>](./Update-AzVM.md)


