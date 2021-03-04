---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 36d86f701bfdeea67869b45512a79eeee45c0457
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890298"
---
# <span data-ttu-id="3ccf8-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="3ccf8-101">Stop-AzVM</span></span>

## <span data-ttu-id="3ccf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ccf8-102">SYNOPSIS</span></span>
<span data-ttu-id="3ccf8-103">Interrompe uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="3ccf8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3ccf8-104">SYNTAX</span></span>

### <span data-ttu-id="3ccf8-105">ResourceGroupNameParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3ccf8-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ccf8-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3ccf8-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ccf8-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3ccf8-107">DESCRIPTION</span></span>
<span data-ttu-id="3ccf8-108">O cmdlet **Stop-AzVM** interrompe uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="3ccf8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ccf8-109">EXAMPLES</span></span>

### <span data-ttu-id="3ccf8-110">Exemplo 1: Parar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="3ccf8-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="3ccf8-111">Este comando interrompe a máquina virtual chamada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="3ccf8-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3ccf8-112">PARAMETERS</span></span>

### <span data-ttu-id="3ccf8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ccf8-113">-AsJob</span></span>
<span data-ttu-id="3ccf8-114">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3ccf8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ccf8-115">-DefaultProfile</span></span>
<span data-ttu-id="3ccf8-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ccf8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3ccf8-117">-Force</span></span>
<span data-ttu-id="3ccf8-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ccf8-119">-Id</span><span class="sxs-lookup"><span data-stu-id="3ccf8-119">-Id</span></span>
<span data-ttu-id="3ccf8-120">A ID da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ccf8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3ccf8-121">-Name</span></span>
<span data-ttu-id="3ccf8-122">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ccf8-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3ccf8-123">-NoWait</span></span>
<span data-ttu-id="3ccf8-124">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3ccf8-125">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3ccf8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ccf8-126">-ResourceGroupName</span></span>
<span data-ttu-id="3ccf8-127">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-127">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ccf8-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="3ccf8-128">-SkipShutdown</span></span>
<span data-ttu-id="3ccf8-129">Para solicitar o desligamento de VM não-graciosa ao manter a VM provisionada.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="3ccf8-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="3ccf8-130">-StayProvisioned</span></span>
<span data-ttu-id="3ccf8-131">O cmdlet interrompe todas as máquinas virtuais dentro do VMSS, mas não as negocia.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="3ccf8-132">A conta é cobrada pelas máquinas virtuais paradas.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="3ccf8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ccf8-133">-Confirm</span></span>
<span data-ttu-id="3ccf8-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ccf8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ccf8-135">-WhatIf</span></span>
<span data-ttu-id="3ccf8-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ccf8-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ccf8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ccf8-138">CommonParameters</span></span>
<span data-ttu-id="3ccf8-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ccf8-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ccf8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ccf8-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ccf8-141">INPUTS</span></span>

### <span data-ttu-id="3ccf8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3ccf8-142">System.String</span></span>

## <span data-ttu-id="3ccf8-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3ccf8-143">OUTPUTS</span></span>

### <span data-ttu-id="3ccf8-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="3ccf8-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="3ccf8-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3ccf8-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3ccf8-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="3ccf8-146">NOTES</span></span>

## <span data-ttu-id="3ccf8-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ccf8-147">RELATED LINKS</span></span>

[<span data-ttu-id="3ccf8-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3ccf8-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3ccf8-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="3ccf8-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="3ccf8-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="3ccf8-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="3ccf8-151">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="3ccf8-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="3ccf8-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="3ccf8-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="3ccf8-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3ccf8-153">Update-AzVM</span></span>](./Update-AzVM.md)


