---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127078"
---
# <span data-ttu-id="46de6-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="46de6-101">Set-AzVM</span></span>

## <span data-ttu-id="46de6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46de6-102">SYNOPSIS</span></span>
<span data-ttu-id="46de6-103">Marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="46de6-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="46de6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46de6-104">SYNTAX</span></span>

### <span data-ttu-id="46de6-105">GeneralizeResourceGroupNameParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="46de6-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46de6-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="46de6-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46de6-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="46de6-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46de6-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="46de6-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46de6-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="46de6-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46de6-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="46de6-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46de6-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="46de6-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46de6-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="46de6-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46de6-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="46de6-113">DESCRIPTION</span></span>
<span data-ttu-id="46de6-114">O **cmdlet Set-AzVM** marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="46de6-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="46de6-115">Antes de executar este cmdlet, faça logon na máquina virtual e use o Sysprep para preparar o disco rígido.</span><span class="sxs-lookup"><span data-stu-id="46de6-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="46de6-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46de6-116">EXAMPLES</span></span>

### <span data-ttu-id="46de6-117">Exemplo 1: Marcar uma máquina virtual como generalizada</span><span class="sxs-lookup"><span data-stu-id="46de6-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="46de6-118">Esse comando marca a máquina virtual chamada VirtualMachine07 como generalizada.</span><span class="sxs-lookup"><span data-stu-id="46de6-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="46de6-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46de6-119">PARAMETERS</span></span>

### <span data-ttu-id="46de6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46de6-120">-AsJob</span></span>
<span data-ttu-id="46de6-121">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="46de6-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="46de6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46de6-122">-DefaultProfile</span></span>
<span data-ttu-id="46de6-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="46de6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46de6-124">-Generalizado</span><span class="sxs-lookup"><span data-stu-id="46de6-124">-Generalized</span></span>
<span data-ttu-id="46de6-125">Indica que esse cmdlet marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="46de6-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="46de6-126">-ID</span><span class="sxs-lookup"><span data-stu-id="46de6-126">-Id</span></span>
<span data-ttu-id="46de6-127">Especifica a ID do Recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46de6-127">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="46de6-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="46de6-128">-Name</span></span>
<span data-ttu-id="46de6-129">Especifica o nome da máquina virtual na qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="46de6-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="46de6-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="46de6-130">-NoWait</span></span>
<span data-ttu-id="46de6-131">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="46de6-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="46de6-132">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="46de6-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="46de6-133">-Reaplicar</span><span class="sxs-lookup"><span data-stu-id="46de6-133">-Reapply</span></span>
<span data-ttu-id="46de6-134">Para reaplicar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46de6-134">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="46de6-135">-Reimplantar</span><span class="sxs-lookup"><span data-stu-id="46de6-135">-Redeploy</span></span>
<span data-ttu-id="46de6-136">Indica que esse cmdlet reimplanta manualmente a máquina virtual para um host diferente do Azure para corrigir quaisquer problemas.</span><span class="sxs-lookup"><span data-stu-id="46de6-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="46de6-137">Se você reimplantar uma máquina virtual, ela será reiniciada, o que resulta na perda de dados da unidade efémémera.</span><span class="sxs-lookup"><span data-stu-id="46de6-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="46de6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46de6-138">-ResourceGroupName</span></span>
<span data-ttu-id="46de6-139">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46de6-139">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="46de6-140">-Simulação de serviço</span><span class="sxs-lookup"><span data-stu-id="46de6-140">-SimulateEviction</span></span>
<span data-ttu-id="46de6-141">Indica que esse cmdlet simula a simulação da máquina virtual de local.</span><span class="sxs-lookup"><span data-stu-id="46de6-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="46de6-142">A desapropriação ocorrerá dentro de 30 minutos após a chamada da API.</span><span class="sxs-lookup"><span data-stu-id="46de6-142">The eviction will occur within 30 minutes of calling the API.</span></span>

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

### <span data-ttu-id="46de6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46de6-143">CommonParameters</span></span>
<span data-ttu-id="46de6-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46de6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46de6-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46de6-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46de6-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="46de6-146">INPUTS</span></span>

### <span data-ttu-id="46de6-147">System.String</span><span class="sxs-lookup"><span data-stu-id="46de6-147">System.String</span></span>

## <span data-ttu-id="46de6-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="46de6-148">OUTPUTS</span></span>

### <span data-ttu-id="46de6-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="46de6-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="46de6-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="46de6-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="46de6-151">Notas</span><span class="sxs-lookup"><span data-stu-id="46de6-151">NOTES</span></span>

## <span data-ttu-id="46de6-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46de6-152">RELATED LINKS</span></span>

[<span data-ttu-id="46de6-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="46de6-153">Get-AzVM</span></span>](./Get-AzVM.md)


