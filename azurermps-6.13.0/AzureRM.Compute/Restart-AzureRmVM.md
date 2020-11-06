---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVM.md
ms.openlocfilehash: f8451f4164b58c2d6599778ab86dfca4e5ff79dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428531"
---
# <span data-ttu-id="587c8-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="587c8-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="587c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="587c8-102">SYNOPSIS</span></span>
<span data-ttu-id="587c8-103">Reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="587c8-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="587c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="587c8-104">SYNTAX</span></span>

### <span data-ttu-id="587c8-105">RestartResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="587c8-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="587c8-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="587c8-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="587c8-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="587c8-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="587c8-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="587c8-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="587c8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="587c8-109">DESCRIPTION</span></span>
<span data-ttu-id="587c8-110">O cmdlet **Restart-AzureRmVM** reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="587c8-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="587c8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="587c8-111">EXAMPLES</span></span>

### <span data-ttu-id="587c8-112">Exemplo 1: reiniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="587c8-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="587c8-113">Esse comando reinicia a máquina virtual chamada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="587c8-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="587c8-114">OS</span><span class="sxs-lookup"><span data-stu-id="587c8-114">PARAMETERS</span></span>

### <span data-ttu-id="587c8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="587c8-115">-AsJob</span></span>
<span data-ttu-id="587c8-116">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="587c8-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="587c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="587c8-117">-DefaultProfile</span></span>
<span data-ttu-id="587c8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="587c8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="587c8-119">-ID</span><span class="sxs-lookup"><span data-stu-id="587c8-119">-Id</span></span>
<span data-ttu-id="587c8-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="587c8-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587c8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="587c8-121">-Name</span></span>
<span data-ttu-id="587c8-122">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="587c8-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="587c8-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="587c8-123">-PerformMaintenance</span></span>
<span data-ttu-id="587c8-124">Para executar a manutenção da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="587c8-124">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587c8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="587c8-125">-ResourceGroupName</span></span>
<span data-ttu-id="587c8-126">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="587c8-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587c8-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="587c8-127">-Confirm</span></span>
<span data-ttu-id="587c8-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="587c8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="587c8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="587c8-129">-WhatIf</span></span>
<span data-ttu-id="587c8-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="587c8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="587c8-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="587c8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="587c8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="587c8-132">CommonParameters</span></span>
<span data-ttu-id="587c8-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="587c8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="587c8-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="587c8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="587c8-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="587c8-135">INPUTS</span></span>

### <span data-ttu-id="587c8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="587c8-136">System.String</span></span>

### <span data-ttu-id="587c8-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="587c8-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="587c8-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="587c8-138">OUTPUTS</span></span>

### <span data-ttu-id="587c8-139">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="587c8-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="587c8-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="587c8-140">NOTES</span></span>

## <span data-ttu-id="587c8-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="587c8-141">RELATED LINKS</span></span>

[<span data-ttu-id="587c8-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="587c8-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="587c8-143">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="587c8-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="587c8-144">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="587c8-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="587c8-145">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="587c8-145">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="587c8-146">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="587c8-146">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="587c8-147">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="587c8-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


