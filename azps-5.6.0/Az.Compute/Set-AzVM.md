---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: b42f456b45de0e78b9d9e0c371dca950ada88ded
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888573"
---
# <span data-ttu-id="9d7a8-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="9d7a8-101">Set-AzVM</span></span>

## <span data-ttu-id="9d7a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d7a8-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7a8-103">Marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="9d7a8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9d7a8-104">SYNTAX</span></span>

### <span data-ttu-id="9d7a8-105">GeneralizeResourceGroupNameParameterSetName (Default)</span><span class="sxs-lookup"><span data-stu-id="9d7a8-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d7a8-106">ReployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9d7a8-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d7a8-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9d7a8-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d7a8-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9d7a8-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d7a8-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9d7a8-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d7a8-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9d7a8-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d7a8-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9d7a8-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d7a8-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9d7a8-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d7a8-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9d7a8-113">DESCRIPTION</span></span>
<span data-ttu-id="9d7a8-114">O cmdlet **Set-AzVM** marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="9d7a8-115">Antes de executar esse cmdlet, faça logon na máquina virtual e use o Sysprep para preparar o disco rígido.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="9d7a8-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d7a8-116">EXAMPLES</span></span>

### <span data-ttu-id="9d7a8-117">Exemplo 1: Marcar uma máquina virtual como generalizada</span><span class="sxs-lookup"><span data-stu-id="9d7a8-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="9d7a8-118">Este comando marca a máquina virtual chamada VirtualMachine07 como generalizada.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="9d7a8-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9d7a8-119">PARAMETERS</span></span>

### <span data-ttu-id="9d7a8-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d7a8-120">-AsJob</span></span>
<span data-ttu-id="9d7a8-121">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9d7a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7a8-122">-DefaultProfile</span></span>
<span data-ttu-id="9d7a8-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d7a8-124">-Generalizado</span><span class="sxs-lookup"><span data-stu-id="9d7a8-124">-Generalized</span></span>
<span data-ttu-id="9d7a8-125">Indica que esse cmdlet marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7a8-126">-Id</span><span class="sxs-lookup"><span data-stu-id="9d7a8-126">-Id</span></span>
<span data-ttu-id="9d7a8-127">Especifica a ID de Recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-127">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7a8-128">-Name</span><span class="sxs-lookup"><span data-stu-id="9d7a8-128">-Name</span></span>
<span data-ttu-id="9d7a8-129">Especifica o nome da máquina virtual na qual esse cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7a8-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9d7a8-130">-NoWait</span></span>
<span data-ttu-id="9d7a8-131">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9d7a8-132">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7a8-133">-Reaplicar</span><span class="sxs-lookup"><span data-stu-id="9d7a8-133">-Reapply</span></span>
<span data-ttu-id="9d7a8-134">Para reaplicar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-134">To reapply virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReapplyResourceGroupNameParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7a8-135">-Reimplantação</span><span class="sxs-lookup"><span data-stu-id="9d7a8-135">-Redeploy</span></span>
<span data-ttu-id="9d7a8-136">Indica que esse cmdlet reimplanta manualmente a máquina virtual para um host do Azure diferente para corrigir quaisquer problemas.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="9d7a8-137">Se você reimplantar uma máquina virtual, ela será reiniciada, o que resulta na perda de dados de unidade efêmero.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7a8-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d7a8-138">-ResourceGroupName</span></span>
<span data-ttu-id="9d7a8-139">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-139">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7a8-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="9d7a8-140">-SimulateEviction</span></span>
<span data-ttu-id="9d7a8-141">Indica que esse cmdlet simula o despejo de máquina virtual local.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="9d7a8-142">O despejo ocorrerá dentro de 30 minutos após chamar a API.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-142">The eviction will occur within 30 minutes of calling the API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimulateEvictionResourceGroupNameParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7a8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7a8-143">CommonParameters</span></span>
<span data-ttu-id="9d7a8-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d7a8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7a8-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d7a8-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7a8-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d7a8-146">INPUTS</span></span>

### <span data-ttu-id="9d7a8-147">System.String</span><span class="sxs-lookup"><span data-stu-id="9d7a8-147">System.String</span></span>

## <span data-ttu-id="9d7a8-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9d7a8-148">OUTPUTS</span></span>

### <span data-ttu-id="9d7a8-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="9d7a8-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="9d7a8-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9d7a8-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9d7a8-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="9d7a8-151">NOTES</span></span>

## <span data-ttu-id="9d7a8-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d7a8-152">RELATED LINKS</span></span>

[<span data-ttu-id="9d7a8-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9d7a8-153">Get-AzVM</span></span>](./Get-AzVM.md)


