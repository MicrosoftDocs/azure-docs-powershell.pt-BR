---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: e02ddb83e40495fbcf729428a737f27e6665d765
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111101"
---
# <span data-ttu-id="135dd-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="135dd-101">Remove-AzVmss</span></span>

## <span data-ttu-id="135dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="135dd-102">SYNOPSIS</span></span>
<span data-ttu-id="135dd-103">Remove o VMSS ou uma máquina virtual que está dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="135dd-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="135dd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="135dd-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="135dd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="135dd-105">DESCRIPTION</span></span>
<span data-ttu-id="135dd-106">O **cmdlet Remove-AzVmss** remove o VMSS (Virtual Machine Scale Set) do Azure.</span><span class="sxs-lookup"><span data-stu-id="135dd-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="135dd-107">Esse cmdlet também pode ser usado para remover uma máquina virtual específica dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="135dd-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="135dd-108">Você pode usar o parâmetro *InstanceId* para remover uma máquina virtual específica dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="135dd-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="135dd-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="135dd-109">EXAMPLES</span></span>

### <span data-ttu-id="135dd-110">Exemplo 1: Remover um VMSS</span><span class="sxs-lookup"><span data-stu-id="135dd-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="135dd-111">Esse comando remove o VMSS chamado VMScaleSet001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="135dd-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="135dd-112">Exemplo 2: Remover uma máquina virtual de dentro de um VMSS</span><span class="sxs-lookup"><span data-stu-id="135dd-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="135dd-113">Esse comando remove a máquina virtual com a ID de instância 3 do VMSS chamado VMScaleSet002 que pertence ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="135dd-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="135dd-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="135dd-114">PARAMETERS</span></span>

### <span data-ttu-id="135dd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="135dd-115">-AsJob</span></span>
<span data-ttu-id="135dd-116">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="135dd-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="135dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="135dd-117">-DefaultProfile</span></span>
<span data-ttu-id="135dd-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="135dd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="135dd-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="135dd-119">-Force</span></span>
<span data-ttu-id="135dd-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="135dd-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="135dd-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="135dd-121">-InstanceId</span></span>
<span data-ttu-id="135dd-122">Especifica, como uma matriz de cadeia de caracteres, a ID das instâncias que precisam ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="135dd-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="135dd-123">Por exemplo: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="135dd-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="135dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="135dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="135dd-125">Especifica o nome do grupo de recursos ao que o VMSS pertence.</span><span class="sxs-lookup"><span data-stu-id="135dd-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="135dd-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="135dd-126">-VMScaleSetName</span></span>
<span data-ttu-id="135dd-127">Especimos o nome do VMSS que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="135dd-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="135dd-128">Se você especificar o parâmetro *InstanceId,* o cmdlet removerá a máquina virtual especificada do VMSS nomeado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="135dd-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="135dd-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="135dd-129">-Confirm</span></span>
<span data-ttu-id="135dd-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="135dd-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135dd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="135dd-131">-WhatIf</span></span>
<span data-ttu-id="135dd-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="135dd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="135dd-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="135dd-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135dd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="135dd-134">CommonParameters</span></span>
<span data-ttu-id="135dd-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="135dd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="135dd-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="135dd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="135dd-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="135dd-137">INPUTS</span></span>

### <span data-ttu-id="135dd-138">System.String</span><span class="sxs-lookup"><span data-stu-id="135dd-138">System.String</span></span>

### <span data-ttu-id="135dd-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="135dd-139">System.String[]</span></span>

## <span data-ttu-id="135dd-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="135dd-140">OUTPUTS</span></span>

### <span data-ttu-id="135dd-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="135dd-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="135dd-142">Notas</span><span class="sxs-lookup"><span data-stu-id="135dd-142">NOTES</span></span>

## <span data-ttu-id="135dd-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="135dd-143">RELATED LINKS</span></span>

[<span data-ttu-id="135dd-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="135dd-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="135dd-145">Novos AzVmss</span><span class="sxs-lookup"><span data-stu-id="135dd-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="135dd-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="135dd-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="135dd-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="135dd-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="135dd-148">Iniciar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="135dd-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="135dd-149">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="135dd-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="135dd-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="135dd-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


