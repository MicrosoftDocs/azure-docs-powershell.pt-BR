---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 206ce916e1a170bbcdf11f791a4610dd5d2172af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610613"
---
# <span data-ttu-id="69870-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69870-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="69870-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69870-102">SYNOPSIS</span></span>
<span data-ttu-id="69870-103">Interrompe o VMSS ou um conjunto de máquinas virtuais dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="69870-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69870-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69870-104">SYNTAX</span></span>

### <span data-ttu-id="69870-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="69870-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69870-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="69870-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69870-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69870-107">DESCRIPTION</span></span>
<span data-ttu-id="69870-108">O cmdlet **Stop-AzureRmVmss** interrompe todas as máquinas virtuais dentro do VMSS (conjunto de dimensionamento de máquina virtual) ou um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="69870-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="69870-109">Você pode usar o parâmetro *InstanceId* para selecionar um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="69870-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="69870-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69870-110">EXAMPLES</span></span>

### <span data-ttu-id="69870-111">Exemplo 1: parar todas as máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="69870-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="69870-112">Esse comando interrompe todas as máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="69870-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="69870-113">Exemplo 2: parar um conjunto específico de máquinas virtuais dentro do VMSS</span><span class="sxs-lookup"><span data-stu-id="69870-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="69870-114">Esse comando para o conjunto específico de máquinas virtuais especificado pela matriz de cadeia de caracteres de ID de instância que pertence ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="69870-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="69870-115">OS</span><span class="sxs-lookup"><span data-stu-id="69870-115">PARAMETERS</span></span>

### <span data-ttu-id="69870-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69870-116">-AsJob</span></span>
<span data-ttu-id="69870-117">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="69870-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="69870-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69870-118">-DefaultProfile</span></span>
<span data-ttu-id="69870-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69870-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69870-120">-Force</span><span class="sxs-lookup"><span data-stu-id="69870-120">-Force</span></span>
<span data-ttu-id="69870-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="69870-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="69870-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="69870-122">-InstanceId</span></span>
<span data-ttu-id="69870-123">Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs das instâncias da máquina virtual em que esse cmdlet para.</span><span class="sxs-lookup"><span data-stu-id="69870-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="69870-124">Por exemplo: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="69870-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="69870-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69870-125">-ResourceGroupName</span></span>
<span data-ttu-id="69870-126">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="69870-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="69870-127">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="69870-127">-StayProvisioned</span></span>
<span data-ttu-id="69870-128">Se especificado, a máquina virtual irá entrar no estado parado.</span><span class="sxs-lookup"><span data-stu-id="69870-128">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="69870-129">Se não for especificado, a máquina virtual entrará no estado parado-desatribuído.</span><span class="sxs-lookup"><span data-stu-id="69870-129">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="69870-130">O usuário ainda é cobrado por VMs no estado parado, mas não para VMs no estado parado-desatribuído.</span><span class="sxs-lookup"><span data-stu-id="69870-130">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

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

### <span data-ttu-id="69870-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="69870-131">-VMScaleSetName</span></span>
<span data-ttu-id="69870-132">Especifica o nome do VMSS para o qual esse cmdlet interrompe as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="69870-132">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="69870-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="69870-133">-Confirm</span></span>
<span data-ttu-id="69870-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69870-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69870-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69870-135">-WhatIf</span></span>
<span data-ttu-id="69870-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69870-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69870-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69870-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69870-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69870-138">CommonParameters</span></span>
<span data-ttu-id="69870-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69870-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69870-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69870-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69870-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69870-141">INPUTS</span></span>

### <span data-ttu-id="69870-142">System. String</span><span class="sxs-lookup"><span data-stu-id="69870-142">System.String</span></span>

### <span data-ttu-id="69870-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="69870-143">System.String[]</span></span>

## <span data-ttu-id="69870-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69870-144">OUTPUTS</span></span>

### <span data-ttu-id="69870-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="69870-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="69870-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69870-146">NOTES</span></span>

## <span data-ttu-id="69870-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69870-147">RELATED LINKS</span></span>

[<span data-ttu-id="69870-148">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69870-148">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="69870-149">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69870-149">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="69870-150">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69870-150">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="69870-151">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69870-151">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="69870-152">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69870-152">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="69870-153">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69870-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="69870-154">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="69870-154">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


