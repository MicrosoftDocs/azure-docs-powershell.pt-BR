---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: f71e827769015b7abe4d503064d97ec1d3c1228b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433291"
---
# <span data-ttu-id="6878a-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="6878a-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="6878a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6878a-102">SYNOPSIS</span></span>
<span data-ttu-id="6878a-103">Modifica o estado de uma instância de VMSS.</span><span class="sxs-lookup"><span data-stu-id="6878a-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6878a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6878a-104">SYNTAX</span></span>

### <span data-ttu-id="6878a-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="6878a-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6878a-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="6878a-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6878a-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="6878a-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6878a-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="6878a-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6878a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6878a-109">DESCRIPTION</span></span>
<span data-ttu-id="6878a-110">O cmdlet **set-AzureRmVmssVM** modifica o estado de uma instância de VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="6878a-110">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="6878a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6878a-111">EXAMPLES</span></span>

## <span data-ttu-id="6878a-112">OS</span><span class="sxs-lookup"><span data-stu-id="6878a-112">PARAMETERS</span></span>

### <span data-ttu-id="6878a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6878a-113">-AsJob</span></span>
<span data-ttu-id="6878a-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6878a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6878a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6878a-115">-DefaultProfile</span></span>
<span data-ttu-id="6878a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6878a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6878a-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="6878a-117">-InstanceId</span></span>
<span data-ttu-id="6878a-118">Especifica a ID da instância VMSS para a qual esse cmdlet modifica o estado.</span><span class="sxs-lookup"><span data-stu-id="6878a-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6878a-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="6878a-119">-PerformMaintenance</span></span>
<span data-ttu-id="6878a-120">Indica que esse cmdlet executa a manutenção em uma máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="6878a-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="6878a-121">-Reimplantar</span><span class="sxs-lookup"><span data-stu-id="6878a-121">-Redeploy</span></span>
<span data-ttu-id="6878a-122">Indica que esse cmdlet reimplanta uma máquina virtual no VMSS.</span><span class="sxs-lookup"><span data-stu-id="6878a-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="6878a-123">-Nova imagem</span><span class="sxs-lookup"><span data-stu-id="6878a-123">-Reimage</span></span>
<span data-ttu-id="6878a-124">Indica que esse cmdlet reimagemia a instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="6878a-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="6878a-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="6878a-125">-ReimageAll</span></span>
<span data-ttu-id="6878a-126">Indica que o cmdlet reimagemia todos os discos na instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="6878a-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="6878a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6878a-127">-ResourceGroupName</span></span>
<span data-ttu-id="6878a-128">Especifica o nome do grupo de recursos que contém a instância VMSS.</span><span class="sxs-lookup"><span data-stu-id="6878a-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="6878a-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6878a-129">-VMScaleSetName</span></span>
<span data-ttu-id="6878a-130">Especifica o nome da instância VMSS que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="6878a-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6878a-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6878a-131">-Confirm</span></span>
<span data-ttu-id="6878a-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6878a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6878a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6878a-133">-WhatIf</span></span>
<span data-ttu-id="6878a-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6878a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6878a-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6878a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6878a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6878a-136">CommonParameters</span></span>
<span data-ttu-id="6878a-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6878a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6878a-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6878a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6878a-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6878a-139">INPUTS</span></span>

### <span data-ttu-id="6878a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6878a-140">System.String</span></span>

## <span data-ttu-id="6878a-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6878a-141">OUTPUTS</span></span>

### <span data-ttu-id="6878a-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6878a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6878a-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6878a-143">NOTES</span></span>

## <span data-ttu-id="6878a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6878a-144">RELATED LINKS</span></span>

[<span data-ttu-id="6878a-145">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="6878a-145">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
