---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: f7965e43c7a294d50d6f0774f76504a90c9d7148
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776889"
---
# <span data-ttu-id="f6b5d-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6b5d-101">Restart-AzVM</span></span>

## <span data-ttu-id="f6b5d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b5d-103">Reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="f6b5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6b5d-104">SYNTAX</span></span>

### <span data-ttu-id="f6b5d-105">RestartResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f6b5d-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6b5d-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f6b5d-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6b5d-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f6b5d-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6b5d-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f6b5d-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6b5d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6b5d-109">DESCRIPTION</span></span>
<span data-ttu-id="f6b5d-110">O cmdlet **Restart-AzVM** reinicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="f6b5d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6b5d-111">EXAMPLES</span></span>

### <span data-ttu-id="f6b5d-112">Exemplo 1: reiniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="f6b5d-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f6b5d-113">Esse comando reinicia a máquina virtual chamada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="f6b5d-114">OS</span><span class="sxs-lookup"><span data-stu-id="f6b5d-114">PARAMETERS</span></span>

### <span data-ttu-id="f6b5d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6b5d-115">-AsJob</span></span>
<span data-ttu-id="f6b5d-116">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-116">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b5d-117">-DefaultProfile</span></span>
<span data-ttu-id="f6b5d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5d-119">-ID</span><span class="sxs-lookup"><span data-stu-id="f6b5d-119">-Id</span></span>
<span data-ttu-id="f6b5d-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6b5d-121">-Name</span></span>
<span data-ttu-id="f6b5d-122">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5d-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="f6b5d-123">-PerformMaintenance</span></span>
<span data-ttu-id="f6b5d-124">Para executar a manutenção da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-124">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6b5d-125">-ResourceGroupName</span></span>
<span data-ttu-id="f6b5d-126">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5d-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f6b5d-127">-Confirm</span></span>
<span data-ttu-id="f6b5d-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6b5d-129">-WhatIf</span></span>
<span data-ttu-id="f6b5d-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6b5d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b5d-132">CommonParameters</span></span>
<span data-ttu-id="f6b5d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b5d-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6b5d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b5d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6b5d-135">INPUTS</span></span>

### <span data-ttu-id="f6b5d-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f6b5d-136">None</span></span>
<span data-ttu-id="f6b5d-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f6b5d-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6b5d-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6b5d-138">OUTPUTS</span></span>

### <span data-ttu-id="f6b5d-139">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="f6b5d-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="f6b5d-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6b5d-140">NOTES</span></span>

## <span data-ttu-id="f6b5d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6b5d-141">RELATED LINKS</span></span>

[<span data-ttu-id="f6b5d-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6b5d-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f6b5d-143">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6b5d-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="f6b5d-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6b5d-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="f6b5d-145">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6b5d-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="f6b5d-146">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6b5d-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="f6b5d-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f6b5d-147">Update-AzVM</span></span>](./Update-AzVM.md)


