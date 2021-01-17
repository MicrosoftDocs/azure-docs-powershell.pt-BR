---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 358b24c403c4b08b221f97ad99271112ee0852be
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434223"
---
# <span data-ttu-id="7f6d8-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="7f6d8-101">Restart-AzVM</span></span>

## <span data-ttu-id="7f6d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f6d8-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6d8-103">Reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="7f6d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f6d8-104">SYNTAX</span></span>

### <span data-ttu-id="7f6d8-105">RestartResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7f6d8-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f6d8-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7f6d8-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f6d8-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7f6d8-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f6d8-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7f6d8-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f6d8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f6d8-109">DESCRIPTION</span></span>
<span data-ttu-id="7f6d8-110">O cmdlet **Restart-AzVM** reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="7f6d8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f6d8-111">EXAMPLES</span></span>

### <span data-ttu-id="7f6d8-112">Exemplo 1: reiniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7f6d8-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="7f6d8-113">Esse comando reinicia a máquina virtual chamada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="7f6d8-114">OS</span><span class="sxs-lookup"><span data-stu-id="7f6d8-114">PARAMETERS</span></span>

### <span data-ttu-id="7f6d8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f6d8-115">-AsJob</span></span>
<span data-ttu-id="7f6d8-116">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7f6d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6d8-117">-DefaultProfile</span></span>
<span data-ttu-id="7f6d8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f6d8-119">-ID</span><span class="sxs-lookup"><span data-stu-id="7f6d8-119">-Id</span></span>
<span data-ttu-id="7f6d8-120">A ID da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="7f6d8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f6d8-121">-Name</span></span>
<span data-ttu-id="7f6d8-122">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="7f6d8-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7f6d8-123">-NoWait</span></span>
<span data-ttu-id="7f6d8-124">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="7f6d8-125">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="7f6d8-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="7f6d8-126">-PerformMaintenance</span></span>
<span data-ttu-id="7f6d8-127">Para executar a manutenção da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-127">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="7f6d8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f6d8-128">-ResourceGroupName</span></span>
<span data-ttu-id="7f6d8-129">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7f6d8-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7f6d8-130">-Confirm</span></span>
<span data-ttu-id="7f6d8-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f6d8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f6d8-132">-WhatIf</span></span>
<span data-ttu-id="7f6d8-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f6d8-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f6d8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6d8-135">CommonParameters</span></span>
<span data-ttu-id="7f6d8-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f6d8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6d8-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f6d8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6d8-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f6d8-138">INPUTS</span></span>

### <span data-ttu-id="7f6d8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7f6d8-139">System.String</span></span>

### <span data-ttu-id="7f6d8-140">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f6d8-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7f6d8-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f6d8-141">OUTPUTS</span></span>

### <span data-ttu-id="7f6d8-142">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="7f6d8-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="7f6d8-143">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7f6d8-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7f6d8-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f6d8-144">NOTES</span></span>

## <span data-ttu-id="7f6d8-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f6d8-145">RELATED LINKS</span></span>

[<span data-ttu-id="7f6d8-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7f6d8-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7f6d8-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7f6d8-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="7f6d8-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="7f6d8-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="7f6d8-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="7f6d8-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="7f6d8-150">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="7f6d8-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="7f6d8-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7f6d8-151">Update-AzVM</span></span>](./Update-AzVM.md)


