---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: 5fcb99a6e909675b47d245755ffd42e3c058a37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428524"
---
# <span data-ttu-id="36051-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36051-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="36051-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36051-102">SYNOPSIS</span></span>
<span data-ttu-id="36051-103">Define ações específicas em um VMSS especificado.</span><span class="sxs-lookup"><span data-stu-id="36051-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36051-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36051-104">SYNTAX</span></span>

### <span data-ttu-id="36051-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="36051-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36051-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="36051-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36051-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="36051-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36051-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="36051-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36051-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36051-109">DESCRIPTION</span></span>
<span data-ttu-id="36051-110">O cmdlet **set-AzureRmVmss** define ações específicas no conjunto de dimensionamento de máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="36051-110">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="36051-111">A única ação aceita por este cmdlet é a reimagem.</span><span class="sxs-lookup"><span data-stu-id="36051-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="36051-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36051-112">EXAMPLES</span></span>

### <span data-ttu-id="36051-113">Exemplo 1: reimagem de um VMSS</span><span class="sxs-lookup"><span data-stu-id="36051-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="36051-114">Esse comando faz a nova imagem do VMSS chamado ContosoVMSS que pertence ao grupo de recursos chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="36051-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="36051-115">OS</span><span class="sxs-lookup"><span data-stu-id="36051-115">PARAMETERS</span></span>

### <span data-ttu-id="36051-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36051-116">-AsJob</span></span>
<span data-ttu-id="36051-117">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="36051-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="36051-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36051-118">-DefaultProfile</span></span>
<span data-ttu-id="36051-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36051-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36051-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="36051-120">-InstanceId</span></span>
<span data-ttu-id="36051-121">A ID de instância da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="36051-121">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36051-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="36051-122">-PerformMaintenance</span></span>
<span data-ttu-id="36051-123">Indica que esse cmdlet executa a manutenção de uma ou mais máquinas virtuais no VMSS.</span><span class="sxs-lookup"><span data-stu-id="36051-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="36051-124">-Reimplantar</span><span class="sxs-lookup"><span data-stu-id="36051-124">-Redeploy</span></span>
<span data-ttu-id="36051-125">Indica que o cmdlet implanta uma ou mais máquinas virtuais no VMSS.</span><span class="sxs-lookup"><span data-stu-id="36051-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="36051-126">-Nova imagem</span><span class="sxs-lookup"><span data-stu-id="36051-126">-Reimage</span></span>
<span data-ttu-id="36051-127">Indica que o cmdlet reimagemia o VMSS.</span><span class="sxs-lookup"><span data-stu-id="36051-127">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="36051-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="36051-128">-ReimageAll</span></span>
<span data-ttu-id="36051-129">Indica que o cmdlet reimagemia todos os discos no VMSS.</span><span class="sxs-lookup"><span data-stu-id="36051-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="36051-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36051-130">-ResourceGroupName</span></span>
<span data-ttu-id="36051-131">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="36051-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36051-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="36051-132">-VMScaleSetName</span></span>
<span data-ttu-id="36051-133">Especifica o nome do VMSS para o qual esse cmdlet define ações.</span><span class="sxs-lookup"><span data-stu-id="36051-133">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36051-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="36051-134">-Confirm</span></span>
<span data-ttu-id="36051-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36051-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36051-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36051-136">-WhatIf</span></span>
<span data-ttu-id="36051-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36051-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36051-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36051-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36051-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36051-139">CommonParameters</span></span>
<span data-ttu-id="36051-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36051-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36051-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36051-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36051-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36051-142">INPUTS</span></span>

### <span data-ttu-id="36051-143">System. String</span><span class="sxs-lookup"><span data-stu-id="36051-143">System.String</span></span>

### <span data-ttu-id="36051-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="36051-144">System.String[]</span></span>

## <span data-ttu-id="36051-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36051-145">OUTPUTS</span></span>

### <span data-ttu-id="36051-146">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="36051-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="36051-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36051-147">NOTES</span></span>

## <span data-ttu-id="36051-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36051-148">RELATED LINKS</span></span>

[<span data-ttu-id="36051-149">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36051-149">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="36051-150">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36051-150">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="36051-151">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36051-151">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="36051-152">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36051-152">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="36051-153">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36051-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="36051-154">Parar-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36051-154">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="36051-155">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="36051-155">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


