---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430142"
---
# <span data-ttu-id="4b453-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b453-101">Stop-AzVM</span></span>

## <span data-ttu-id="4b453-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b453-102">SYNOPSIS</span></span>
<span data-ttu-id="4b453-103">Interrompe uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b453-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="4b453-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b453-104">SYNTAX</span></span>

### <span data-ttu-id="4b453-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4b453-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b453-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4b453-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b453-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b453-107">DESCRIPTION</span></span>
<span data-ttu-id="4b453-108">O cmdlet **Stop-AzVM** interrompe uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b453-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="4b453-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b453-109">EXAMPLES</span></span>

### <span data-ttu-id="4b453-110">Exemplo 1: parar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="4b453-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="4b453-111">Esse comando para a máquina virtual nomeada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4b453-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="4b453-112">OS</span><span class="sxs-lookup"><span data-stu-id="4b453-112">PARAMETERS</span></span>

### <span data-ttu-id="4b453-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b453-113">-AsJob</span></span>
<span data-ttu-id="4b453-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="4b453-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4b453-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b453-115">-DefaultProfile</span></span>
<span data-ttu-id="4b453-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b453-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b453-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4b453-117">-Force</span></span>
<span data-ttu-id="4b453-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4b453-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4b453-119">-ID</span><span class="sxs-lookup"><span data-stu-id="4b453-119">-Id</span></span>
<span data-ttu-id="4b453-120">A ID da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4b453-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="4b453-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b453-121">-Name</span></span>
<span data-ttu-id="4b453-122">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4b453-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="4b453-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4b453-123">-NoWait</span></span>
<span data-ttu-id="4b453-124">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="4b453-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="4b453-125">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="4b453-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="4b453-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b453-126">-ResourceGroupName</span></span>
<span data-ttu-id="4b453-127">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4b453-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4b453-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="4b453-128">-SkipShutdown</span></span>
<span data-ttu-id="4b453-129">Para solicitar o desligamento não-normal da VM ao manter a VM provisionada.</span><span class="sxs-lookup"><span data-stu-id="4b453-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="4b453-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="4b453-130">-StayProvisioned</span></span>
<span data-ttu-id="4b453-131">O cmdlet interrompe todas as máquinas virtuais dentro do VMSS, mas não as desatribui.</span><span class="sxs-lookup"><span data-stu-id="4b453-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="4b453-132">A conta é cobrada pelas máquinas virtuais interrompidas.</span><span class="sxs-lookup"><span data-stu-id="4b453-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="4b453-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b453-133">-Confirm</span></span>
<span data-ttu-id="4b453-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b453-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b453-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b453-135">-WhatIf</span></span>
<span data-ttu-id="4b453-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b453-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b453-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b453-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b453-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b453-138">CommonParameters</span></span>
<span data-ttu-id="4b453-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b453-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b453-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b453-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b453-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b453-141">INPUTS</span></span>

### <span data-ttu-id="4b453-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4b453-142">System.String</span></span>

## <span data-ttu-id="4b453-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b453-143">OUTPUTS</span></span>

### <span data-ttu-id="4b453-144">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="4b453-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="4b453-145">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4b453-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4b453-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b453-146">NOTES</span></span>

## <span data-ttu-id="4b453-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b453-147">RELATED LINKS</span></span>

[<span data-ttu-id="4b453-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b453-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4b453-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b453-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="4b453-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b453-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="4b453-151">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b453-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="4b453-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b453-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="4b453-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4b453-153">Update-AzVM</span></span>](./Update-AzVM.md)


