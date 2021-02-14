---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 1845e7f1e76f4b05624c9c79500389b2839d25dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116879"
---
# <span data-ttu-id="88c91-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88c91-101">Start-AzVmss</span></span>

## <span data-ttu-id="88c91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88c91-102">SYNOPSIS</span></span>
<span data-ttu-id="88c91-103">Inicia o VMSS ou um conjunto de máquinas virtuais dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="88c91-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="88c91-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88c91-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88c91-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="88c91-105">DESCRIPTION</span></span>
<span data-ttu-id="88c91-106">O cmdlet **Start-AzVmss** inicia todas as máquinas virtuais no VMSS (Virtual Machine Scale Set) ou em um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="88c91-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="88c91-107">Você pode usar o parâmetro *InstanceId* para selecionar um conjunto de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="88c91-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="88c91-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="88c91-108">EXAMPLES</span></span>

### <span data-ttu-id="88c91-109">Exemplo 1: Iniciar um conjunto específico de máquinas virtuais no VMSS</span><span class="sxs-lookup"><span data-stu-id="88c91-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="88c91-110">Esse comando inicia um conjunto específico de máquinas virtuais especificada pela matriz de cadeia de caracteres de ID de instância que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="88c91-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="88c91-111">Exemplo 2: Iniciar todas as máquinas virtuais no VMSS</span><span class="sxs-lookup"><span data-stu-id="88c91-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="88c91-112">Esse comando inicia todas as máquinas virtuais que pertencem ao VMSS chamado ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="88c91-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="88c91-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88c91-113">PARAMETERS</span></span>

### <span data-ttu-id="88c91-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88c91-114">-AsJob</span></span>
<span data-ttu-id="88c91-115">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="88c91-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="88c91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88c91-116">-DefaultProfile</span></span>
<span data-ttu-id="88c91-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="88c91-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88c91-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="88c91-118">-InstanceId</span></span>
<span data-ttu-id="88c91-119">Especifica, como uma matriz de cadeia de caracteres, a ID ou IDs das instâncias que o cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="88c91-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="88c91-120">Por exemplo: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="88c91-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="88c91-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88c91-121">-ResourceGroupName</span></span>
<span data-ttu-id="88c91-122">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="88c91-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="88c91-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="88c91-123">-VMScaleSetName</span></span>
<span data-ttu-id="88c91-124">Especifica o nome do VMSS que este cmdlet inicia as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="88c91-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="88c91-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="88c91-125">-Confirm</span></span>
<span data-ttu-id="88c91-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88c91-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88c91-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88c91-127">-WhatIf</span></span>
<span data-ttu-id="88c91-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="88c91-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88c91-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88c91-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88c91-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c91-130">CommonParameters</span></span>
<span data-ttu-id="88c91-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88c91-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c91-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88c91-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c91-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="88c91-133">INPUTS</span></span>

### <span data-ttu-id="88c91-134">System.String</span><span class="sxs-lookup"><span data-stu-id="88c91-134">System.String</span></span>

### <span data-ttu-id="88c91-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="88c91-135">System.String[]</span></span>

## <span data-ttu-id="88c91-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="88c91-136">OUTPUTS</span></span>

### <span data-ttu-id="88c91-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="88c91-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="88c91-138">Notas</span><span class="sxs-lookup"><span data-stu-id="88c91-138">NOTES</span></span>

## <span data-ttu-id="88c91-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88c91-139">RELATED LINKS</span></span>

[<span data-ttu-id="88c91-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88c91-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="88c91-141">Novos AzVmss</span><span class="sxs-lookup"><span data-stu-id="88c91-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="88c91-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88c91-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="88c91-143">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88c91-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="88c91-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88c91-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="88c91-145">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88c91-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="88c91-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="88c91-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


