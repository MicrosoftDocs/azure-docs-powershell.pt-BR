---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: c9b7ce0c55ff917839ff8047454dcced42653b3d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940919"
---
# <span data-ttu-id="d83d9-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="d83d9-101">Set-AzVM</span></span>

## <span data-ttu-id="d83d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d83d9-102">SYNOPSIS</span></span>
<span data-ttu-id="d83d9-103">Marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="d83d9-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="d83d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d83d9-104">SYNTAX</span></span>

### <span data-ttu-id="d83d9-105">GeneralizeResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d83d9-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d83d9-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d83d9-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d83d9-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d83d9-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d83d9-108">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d83d9-108">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d83d9-109">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d83d9-109">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d83d9-110">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d83d9-110">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d83d9-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d83d9-111">DESCRIPTION</span></span>
<span data-ttu-id="d83d9-112">O cmdlet **set-AzVM** marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="d83d9-112">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="d83d9-113">Antes de executar este cmdlet, faça logon na máquina virtual e use o Sysprep para preparar o disco rígido.</span><span class="sxs-lookup"><span data-stu-id="d83d9-113">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="d83d9-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d83d9-114">EXAMPLES</span></span>

### <span data-ttu-id="d83d9-115">Exemplo 1: marcar uma máquina virtual como generalizada</span><span class="sxs-lookup"><span data-stu-id="d83d9-115">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="d83d9-116">Esse comando marca a máquina virtual chamada VirtualMachine07 como generalizada.</span><span class="sxs-lookup"><span data-stu-id="d83d9-116">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="d83d9-117">OS</span><span class="sxs-lookup"><span data-stu-id="d83d9-117">PARAMETERS</span></span>

### <span data-ttu-id="d83d9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d83d9-118">-AsJob</span></span>
<span data-ttu-id="d83d9-119">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="d83d9-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d83d9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83d9-120">-DefaultProfile</span></span>
<span data-ttu-id="d83d9-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d83d9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d83d9-122">-Generalizado</span><span class="sxs-lookup"><span data-stu-id="d83d9-122">-Generalized</span></span>
<span data-ttu-id="d83d9-123">Indica que esse cmdlet marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="d83d9-123">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="d83d9-124">-ID</span><span class="sxs-lookup"><span data-stu-id="d83d9-124">-Id</span></span>
<span data-ttu-id="d83d9-125">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d83d9-125">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d83d9-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="d83d9-126">-Name</span></span>
<span data-ttu-id="d83d9-127">Especifica o nome da máquina virtual na qual esse cmdlet funciona.</span><span class="sxs-lookup"><span data-stu-id="d83d9-127">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d83d9-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d83d9-128">-NoWait</span></span>
<span data-ttu-id="d83d9-129">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="d83d9-129">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d83d9-130">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="d83d9-130">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d83d9-131">-Reaplicar</span><span class="sxs-lookup"><span data-stu-id="d83d9-131">-Reapply</span></span>
<span data-ttu-id="d83d9-132">Para reaplicar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d83d9-132">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="d83d9-133">-Reimplantar</span><span class="sxs-lookup"><span data-stu-id="d83d9-133">-Redeploy</span></span>
<span data-ttu-id="d83d9-134">Indica que esse cmdlet reimplanta manualmente a máquina virtual em um host do Azure diferente para corrigir os problemas.</span><span class="sxs-lookup"><span data-stu-id="d83d9-134">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="d83d9-135">Se você reimplantar uma máquina virtual, ela será reiniciada, o que resulta na perda dos dados da unidade efêmera.</span><span class="sxs-lookup"><span data-stu-id="d83d9-135">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="d83d9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d83d9-136">-ResourceGroupName</span></span>
<span data-ttu-id="d83d9-137">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d83d9-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d83d9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83d9-138">CommonParameters</span></span>
<span data-ttu-id="d83d9-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d83d9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83d9-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d83d9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83d9-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d83d9-141">INPUTS</span></span>

### <span data-ttu-id="d83d9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d83d9-142">System.String</span></span>

## <span data-ttu-id="d83d9-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d83d9-143">OUTPUTS</span></span>

### <span data-ttu-id="d83d9-144">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="d83d9-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="d83d9-145">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d83d9-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d83d9-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d83d9-146">NOTES</span></span>

## <span data-ttu-id="d83d9-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d83d9-147">RELATED LINKS</span></span>

[<span data-ttu-id="d83d9-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d83d9-148">Get-AzVM</span></span>](./Get-AzVM.md)


