---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 623ebc278b2903fb0563c7ea196bd6123f495388
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944621"
---
# <span data-ttu-id="02589-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="02589-101">Set-AzVmss</span></span>

## <span data-ttu-id="02589-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02589-102">SYNOPSIS</span></span>
<span data-ttu-id="02589-103">Define ações específicas em um VMSS especificado.</span><span class="sxs-lookup"><span data-stu-id="02589-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="02589-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02589-104">SYNTAX</span></span>

### <span data-ttu-id="02589-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="02589-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-TempDisk]
 [-Reimage] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02589-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="02589-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02589-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="02589-107">RedeployMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02589-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="02589-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02589-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02589-109">DESCRIPTION</span></span>
<span data-ttu-id="02589-110">O cmdlet **set-AzVmss** define ações específicas no conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="02589-110">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="02589-111">A única ação aceita por este cmdlet é a reimagem.</span><span class="sxs-lookup"><span data-stu-id="02589-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="02589-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02589-112">EXAMPLES</span></span>

### <span data-ttu-id="02589-113">Exemplo 1: reimagem de um VMSS</span><span class="sxs-lookup"><span data-stu-id="02589-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="02589-114">Esse comando faz a nova imagem do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="02589-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="02589-115">OS</span><span class="sxs-lookup"><span data-stu-id="02589-115">PARAMETERS</span></span>

### <span data-ttu-id="02589-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02589-116">-AsJob</span></span>
<span data-ttu-id="02589-117">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="02589-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="02589-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02589-118">-DefaultProfile</span></span>
<span data-ttu-id="02589-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02589-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02589-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="02589-120">-InstanceId</span></span>
<span data-ttu-id="02589-121">A ID de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="02589-121">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02589-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="02589-122">-PerformMaintenance</span></span>
<span data-ttu-id="02589-123">Indica que esse cmdlet executa a manutenção de uma ou mais máquinas virtuais no VMSS.</span><span class="sxs-lookup"><span data-stu-id="02589-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="02589-124">-Reimplantar</span><span class="sxs-lookup"><span data-stu-id="02589-124">-Redeploy</span></span>
<span data-ttu-id="02589-125">Indica que o cmdlet implanta uma ou mais máquinas virtuais no VMSS.</span><span class="sxs-lookup"><span data-stu-id="02589-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="02589-126">-Nova imagem</span><span class="sxs-lookup"><span data-stu-id="02589-126">-Reimage</span></span>
<span data-ttu-id="02589-127">Indica que o cmdlet reimagemia o VMSS.</span><span class="sxs-lookup"><span data-stu-id="02589-127">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="02589-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="02589-128">-ReimageAll</span></span>
<span data-ttu-id="02589-129">Indica que o cmdlet reimagemia todos os discos no VMSS.</span><span class="sxs-lookup"><span data-stu-id="02589-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="02589-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02589-130">-ResourceGroupName</span></span>
<span data-ttu-id="02589-131">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="02589-131">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="02589-132">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="02589-132">-TempDisk</span></span>
<span data-ttu-id="02589-133">Especifica se a reimagem do disco temporário será renovada.</span><span class="sxs-lookup"><span data-stu-id="02589-133">Specifies whether to reimage temp disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02589-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="02589-134">-VMScaleSetName</span></span>
<span data-ttu-id="02589-135">Especifica o nome do VMSS para o qual esse cmdlet define ações.</span><span class="sxs-lookup"><span data-stu-id="02589-135">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="02589-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="02589-136">-Confirm</span></span>
<span data-ttu-id="02589-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02589-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02589-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02589-138">-WhatIf</span></span>
<span data-ttu-id="02589-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02589-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02589-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02589-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02589-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02589-141">CommonParameters</span></span>
<span data-ttu-id="02589-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02589-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02589-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02589-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02589-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02589-144">INPUTS</span></span>

### <span data-ttu-id="02589-145">System. String</span><span class="sxs-lookup"><span data-stu-id="02589-145">System.String</span></span>

### <span data-ttu-id="02589-146">System. String []</span><span class="sxs-lookup"><span data-stu-id="02589-146">System.String[]</span></span>

## <span data-ttu-id="02589-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02589-147">OUTPUTS</span></span>

### <span data-ttu-id="02589-148">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="02589-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="02589-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02589-149">NOTES</span></span>

## <span data-ttu-id="02589-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02589-150">RELATED LINKS</span></span>

[<span data-ttu-id="02589-151">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="02589-151">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="02589-152">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="02589-152">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="02589-153">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="02589-153">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="02589-154">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="02589-154">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="02589-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="02589-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="02589-156">Parar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="02589-156">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="02589-157">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="02589-157">Update-AzVmss</span></span>](./Update-AzVmss.md)


