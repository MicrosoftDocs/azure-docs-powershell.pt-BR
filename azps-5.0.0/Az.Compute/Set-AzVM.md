---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280405"
---
# <span data-ttu-id="ae902-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="ae902-101">Set-AzVM</span></span>

## <span data-ttu-id="ae902-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae902-102">SYNOPSIS</span></span>
<span data-ttu-id="ae902-103">Marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="ae902-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="ae902-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae902-104">SYNTAX</span></span>

### <span data-ttu-id="ae902-105">GeneralizeResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae902-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae902-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ae902-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae902-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ae902-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae902-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ae902-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae902-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ae902-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae902-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ae902-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae902-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ae902-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae902-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ae902-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae902-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae902-113">DESCRIPTION</span></span>
<span data-ttu-id="ae902-114">O cmdlet **set-AzVM** marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="ae902-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="ae902-115">Antes de executar este cmdlet, faça logon na máquina virtual e use o Sysprep para preparar o disco rígido.</span><span class="sxs-lookup"><span data-stu-id="ae902-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="ae902-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae902-116">EXAMPLES</span></span>

### <span data-ttu-id="ae902-117">Exemplo 1: marcar uma máquina virtual como generalizada</span><span class="sxs-lookup"><span data-stu-id="ae902-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="ae902-118">Esse comando marca a máquina virtual chamada VirtualMachine07 como generalizada.</span><span class="sxs-lookup"><span data-stu-id="ae902-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="ae902-119">OS</span><span class="sxs-lookup"><span data-stu-id="ae902-119">PARAMETERS</span></span>

### <span data-ttu-id="ae902-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae902-120">-AsJob</span></span>
<span data-ttu-id="ae902-121">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="ae902-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ae902-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae902-122">-DefaultProfile</span></span>
<span data-ttu-id="ae902-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae902-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae902-124">-Generalizado</span><span class="sxs-lookup"><span data-stu-id="ae902-124">-Generalized</span></span>
<span data-ttu-id="ae902-125">Indica que esse cmdlet marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="ae902-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="ae902-126">-ID</span><span class="sxs-lookup"><span data-stu-id="ae902-126">-Id</span></span>
<span data-ttu-id="ae902-127">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae902-127">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="ae902-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae902-128">-Name</span></span>
<span data-ttu-id="ae902-129">Especifica o nome da máquina virtual na qual esse cmdlet funciona.</span><span class="sxs-lookup"><span data-stu-id="ae902-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ae902-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ae902-130">-NoWait</span></span>
<span data-ttu-id="ae902-131">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="ae902-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ae902-132">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="ae902-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ae902-133">-Reaplicar</span><span class="sxs-lookup"><span data-stu-id="ae902-133">-Reapply</span></span>
<span data-ttu-id="ae902-134">Para reaplicar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae902-134">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="ae902-135">-Reimplantar</span><span class="sxs-lookup"><span data-stu-id="ae902-135">-Redeploy</span></span>
<span data-ttu-id="ae902-136">Indica que esse cmdlet reimplanta manualmente a máquina virtual em um host do Azure diferente para corrigir os problemas.</span><span class="sxs-lookup"><span data-stu-id="ae902-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="ae902-137">Se você reimplantar uma máquina virtual, ela será reiniciada, o que resulta na perda dos dados da unidade efêmera.</span><span class="sxs-lookup"><span data-stu-id="ae902-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="ae902-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae902-138">-ResourceGroupName</span></span>
<span data-ttu-id="ae902-139">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae902-139">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ae902-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="ae902-140">-SimulateEviction</span></span>
<span data-ttu-id="ae902-141">Indica que esse cmdlet simula a remoção da máquina virtual Spot.</span><span class="sxs-lookup"><span data-stu-id="ae902-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="ae902-142">A remoção ocorrerá dentro de 30 minutos de chamadas para a API.</span><span class="sxs-lookup"><span data-stu-id="ae902-142">The eviction will occur within 30 minutes of calling the API.</span></span>

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

### <span data-ttu-id="ae902-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae902-143">CommonParameters</span></span>
<span data-ttu-id="ae902-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae902-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae902-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae902-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae902-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae902-146">INPUTS</span></span>

### <span data-ttu-id="ae902-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ae902-147">System.String</span></span>

## <span data-ttu-id="ae902-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae902-148">OUTPUTS</span></span>

### <span data-ttu-id="ae902-149">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="ae902-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="ae902-150">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ae902-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ae902-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae902-151">NOTES</span></span>

## <span data-ttu-id="ae902-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae902-152">RELATED LINKS</span></span>

[<span data-ttu-id="ae902-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ae902-153">Get-AzVM</span></span>](./Get-AzVM.md)


