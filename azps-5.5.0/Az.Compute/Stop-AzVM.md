---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111084"
---
# <span data-ttu-id="30884-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="30884-101">Stop-AzVM</span></span>

## <span data-ttu-id="30884-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30884-102">SYNOPSIS</span></span>
<span data-ttu-id="30884-103">Interrompe uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="30884-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="30884-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30884-104">SYNTAX</span></span>

### <span data-ttu-id="30884-105">ResourceGroupNameParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="30884-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30884-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="30884-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30884-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="30884-107">DESCRIPTION</span></span>
<span data-ttu-id="30884-108">O **cmdlet Stop-AzVM** interrompe uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="30884-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="30884-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30884-109">EXAMPLES</span></span>

### <span data-ttu-id="30884-110">Exemplo 1: Parar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="30884-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="30884-111">Esse comando interrompe a máquina virtual chamada VirtualMachine07 no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="30884-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="30884-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30884-112">PARAMETERS</span></span>

### <span data-ttu-id="30884-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30884-113">-AsJob</span></span>
<span data-ttu-id="30884-114">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="30884-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="30884-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30884-115">-DefaultProfile</span></span>
<span data-ttu-id="30884-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="30884-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30884-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="30884-117">-Force</span></span>
<span data-ttu-id="30884-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="30884-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="30884-119">-ID</span><span class="sxs-lookup"><span data-stu-id="30884-119">-Id</span></span>
<span data-ttu-id="30884-120">A ID da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="30884-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="30884-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="30884-121">-Name</span></span>
<span data-ttu-id="30884-122">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="30884-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="30884-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="30884-123">-NoWait</span></span>
<span data-ttu-id="30884-124">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="30884-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="30884-125">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="30884-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="30884-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30884-126">-ResourceGroupName</span></span>
<span data-ttu-id="30884-127">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="30884-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="30884-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="30884-128">-SkipShutdown</span></span>
<span data-ttu-id="30884-129">Para solicitar parada total de VM ao manter o VM provisionado.</span><span class="sxs-lookup"><span data-stu-id="30884-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="30884-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="30884-130">-StayProvisioned</span></span>
<span data-ttu-id="30884-131">O cmdlet interrompe todas as máquinas virtuais dentro do VMSS, mas não as trata.</span><span class="sxs-lookup"><span data-stu-id="30884-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="30884-132">A conta é cobrada pelos máquinas virtuais paradas.</span><span class="sxs-lookup"><span data-stu-id="30884-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="30884-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="30884-133">-Confirm</span></span>
<span data-ttu-id="30884-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30884-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30884-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30884-135">-WhatIf</span></span>
<span data-ttu-id="30884-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="30884-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30884-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="30884-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30884-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30884-138">CommonParameters</span></span>
<span data-ttu-id="30884-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30884-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30884-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30884-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30884-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="30884-141">INPUTS</span></span>

### <span data-ttu-id="30884-142">System.String</span><span class="sxs-lookup"><span data-stu-id="30884-142">System.String</span></span>

## <span data-ttu-id="30884-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="30884-143">OUTPUTS</span></span>

### <span data-ttu-id="30884-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="30884-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="30884-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="30884-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="30884-146">Notas</span><span class="sxs-lookup"><span data-stu-id="30884-146">NOTES</span></span>

## <span data-ttu-id="30884-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30884-147">RELATED LINKS</span></span>

[<span data-ttu-id="30884-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="30884-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="30884-149">Novo-AzVM</span><span class="sxs-lookup"><span data-stu-id="30884-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="30884-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="30884-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="30884-151">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="30884-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="30884-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="30884-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="30884-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="30884-153">Update-AzVM</span></span>](./Update-AzVM.md)


