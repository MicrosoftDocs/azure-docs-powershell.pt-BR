---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: b3e060680ee5df25708f153b239ec6c13b4e8a35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597234"
---
# <span data-ttu-id="69ea8-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="69ea8-101">Set-AzVM</span></span>

## <span data-ttu-id="69ea8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="69ea8-103">Marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="69ea8-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="69ea8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69ea8-104">SYNTAX</span></span>

### <span data-ttu-id="69ea8-105">GeneralizeResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="69ea8-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69ea8-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="69ea8-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69ea8-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="69ea8-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69ea8-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="69ea8-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69ea8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69ea8-109">DESCRIPTION</span></span>
<span data-ttu-id="69ea8-110">O cmdlet **set-AzVM** marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="69ea8-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="69ea8-111">Antes de executar este cmdlet, faça logon na máquina virtual e use o Sysprep para preparar o disco rígido.</span><span class="sxs-lookup"><span data-stu-id="69ea8-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="69ea8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69ea8-112">EXAMPLES</span></span>

### <span data-ttu-id="69ea8-113">Exemplo 1: marcar uma máquina virtual como generalizada</span><span class="sxs-lookup"><span data-stu-id="69ea8-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="69ea8-114">Esse comando marca a máquina virtual chamada VirtualMachine07 como generalizada.</span><span class="sxs-lookup"><span data-stu-id="69ea8-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="69ea8-115">OS</span><span class="sxs-lookup"><span data-stu-id="69ea8-115">PARAMETERS</span></span>

### <span data-ttu-id="69ea8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69ea8-116">-AsJob</span></span>
<span data-ttu-id="69ea8-117">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="69ea8-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="69ea8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ea8-118">-DefaultProfile</span></span>
<span data-ttu-id="69ea8-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69ea8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69ea8-120">-Generalizado</span><span class="sxs-lookup"><span data-stu-id="69ea8-120">-Generalized</span></span>
<span data-ttu-id="69ea8-121">Indica que esse cmdlet marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="69ea8-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="69ea8-122">-ID</span><span class="sxs-lookup"><span data-stu-id="69ea8-122">-Id</span></span>
<span data-ttu-id="69ea8-123">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="69ea8-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ea8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="69ea8-124">-Name</span></span>
<span data-ttu-id="69ea8-125">Especifica o nome da máquina virtual na qual esse cmdlet funciona.</span><span class="sxs-lookup"><span data-stu-id="69ea8-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ea8-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="69ea8-126">-NoWait</span></span>
<span data-ttu-id="69ea8-127">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="69ea8-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="69ea8-128">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="69ea8-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ea8-129">-Reimplantar</span><span class="sxs-lookup"><span data-stu-id="69ea8-129">-Redeploy</span></span>
<span data-ttu-id="69ea8-130">Indica que esse cmdlet reimplanta manualmente a máquina virtual em um host do Azure diferente para corrigir os problemas.</span><span class="sxs-lookup"><span data-stu-id="69ea8-130">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="69ea8-131">Se você reimplantar uma máquina virtual, ela será reiniciada, o que resulta na perda dos dados da unidade efêmera.</span><span class="sxs-lookup"><span data-stu-id="69ea8-131">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="69ea8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ea8-132">-ResourceGroupName</span></span>
<span data-ttu-id="69ea8-133">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="69ea8-133">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ea8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ea8-134">CommonParameters</span></span>
<span data-ttu-id="69ea8-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ea8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ea8-136">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69ea8-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ea8-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69ea8-137">INPUTS</span></span>

### <span data-ttu-id="69ea8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="69ea8-138">System.String</span></span>

## <span data-ttu-id="69ea8-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69ea8-139">OUTPUTS</span></span>

### <span data-ttu-id="69ea8-140">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="69ea8-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="69ea8-141">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="69ea8-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="69ea8-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69ea8-142">NOTES</span></span>

## <span data-ttu-id="69ea8-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69ea8-143">RELATED LINKS</span></span>

[<span data-ttu-id="69ea8-144">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="69ea8-144">Get-AzVM</span></span>](./Get-AzVM.md)


