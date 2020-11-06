---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 1fdd45c36d085b376ed900f0054dd98bc28c7525
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597180"
---
# <span data-ttu-id="d66b4-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="d66b4-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="d66b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d66b4-102">SYNOPSIS</span></span>
<span data-ttu-id="d66b4-103">Modifica o estado de uma instância de VMSS.</span><span class="sxs-lookup"><span data-stu-id="d66b4-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="d66b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d66b4-104">SYNTAX</span></span>

### <span data-ttu-id="d66b4-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="d66b4-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d66b4-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d66b4-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d66b4-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="d66b4-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d66b4-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="d66b4-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d66b4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d66b4-109">DESCRIPTION</span></span>
<span data-ttu-id="d66b4-110">O cmdlet **set-AzVmssVM** modifica o estado de uma instância de VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="d66b4-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="d66b4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d66b4-111">EXAMPLES</span></span>

## <span data-ttu-id="d66b4-112">OS</span><span class="sxs-lookup"><span data-stu-id="d66b4-112">PARAMETERS</span></span>

### <span data-ttu-id="d66b4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d66b4-113">-AsJob</span></span>
<span data-ttu-id="d66b4-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d66b4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d66b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d66b4-115">-DefaultProfile</span></span>
<span data-ttu-id="d66b4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d66b4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d66b4-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d66b4-117">-InstanceId</span></span>
<span data-ttu-id="d66b4-118">Especifica a ID da instância VMSS para a qual esse cmdlet modifica o estado.</span><span class="sxs-lookup"><span data-stu-id="d66b4-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66b4-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="d66b4-119">-PerformMaintenance</span></span>
<span data-ttu-id="d66b4-120">Indica que esse cmdlet executa a manutenção em uma máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="d66b4-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66b4-121">-Reimplantar</span><span class="sxs-lookup"><span data-stu-id="d66b4-121">-Redeploy</span></span>
<span data-ttu-id="d66b4-122">Indica que esse cmdlet reimplanta uma máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="d66b4-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66b4-123">-Nova imagem</span><span class="sxs-lookup"><span data-stu-id="d66b4-123">-Reimage</span></span>
<span data-ttu-id="d66b4-124">Indica que esse cmdlet reimagemia a instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="d66b4-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66b4-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="d66b4-125">-ReimageAll</span></span>
<span data-ttu-id="d66b4-126">Indica que o cmdlet reimagemia todos os discos na instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="d66b4-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66b4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d66b4-127">-ResourceGroupName</span></span>
<span data-ttu-id="d66b4-128">Especifica o nome do grupo de recursos que contém a instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="d66b4-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66b4-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d66b4-129">-VMScaleSetName</span></span>
<span data-ttu-id="d66b4-130">Especifica o nome da instância VMSS que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="d66b4-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66b4-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d66b4-131">-Confirm</span></span>
<span data-ttu-id="d66b4-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d66b4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d66b4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d66b4-133">-WhatIf</span></span>
<span data-ttu-id="d66b4-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d66b4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d66b4-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d66b4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d66b4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66b4-136">CommonParameters</span></span>
<span data-ttu-id="d66b4-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d66b4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66b4-138">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d66b4-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66b4-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d66b4-139">INPUTS</span></span>

### <span data-ttu-id="d66b4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d66b4-140">System.String</span></span>

## <span data-ttu-id="d66b4-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d66b4-141">OUTPUTS</span></span>

### <span data-ttu-id="d66b4-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d66b4-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d66b4-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d66b4-143">NOTES</span></span>

## <span data-ttu-id="d66b4-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d66b4-144">RELATED LINKS</span></span>

[<span data-ttu-id="d66b4-145">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="d66b4-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
