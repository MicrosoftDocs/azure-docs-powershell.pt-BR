---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: c686eec33a2f4a9f972acbdb7261f86fc45a6fa1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117838"
---
# <span data-ttu-id="e9c8a-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e9c8a-101">Restart-AzVmss</span></span>

## <span data-ttu-id="e9c8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c8a-103">Reinicia o VMSS ou uma máquina virtual dentro do VMSS.</span><span class="sxs-lookup"><span data-stu-id="e9c8a-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="e9c8a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9c8a-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9c8a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9c8a-105">DESCRIPTION</span></span>
<span data-ttu-id="e9c8a-106">O **cmdlet Restart-AzVmss** reinicia o VMSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="e9c8a-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e9c8a-107">Esse cmdlet também pode ser usado para reiniciar uma máquina virtual específica dentro do VMSS usando o parâmetro *InstanceId.*</span><span class="sxs-lookup"><span data-stu-id="e9c8a-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="e9c8a-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e9c8a-108">EXAMPLES</span></span>

### <span data-ttu-id="e9c8a-109">Exemplo 1: Reiniciar o VMSS</span><span class="sxs-lookup"><span data-stu-id="e9c8a-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="e9c8a-110">Esse comando reinicia o VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="e9c8a-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="e9c8a-111">Exemplo 2: Reiniciar uma máquina virtual específica no VMSS</span><span class="sxs-lookup"><span data-stu-id="e9c8a-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="e9c8a-112">Esse comando reinicia uma máquina virtual que tem a ID de instância 1 no VMSS chamado VMSS001 que pertence ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="e9c8a-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="e9c8a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9c8a-113">PARAMETERS</span></span>

### <span data-ttu-id="e9c8a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9c8a-114">-AsJob</span></span>
<span data-ttu-id="e9c8a-115">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="e9c8a-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e9c8a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c8a-116">-DefaultProfile</span></span>
<span data-ttu-id="e9c8a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e9c8a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9c8a-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e9c8a-118">-InstanceId</span></span>
<span data-ttu-id="e9c8a-119">Especifica, como uma matriz de cadeia de caracteres, a ID das instâncias que precisam ser reiniciadas.</span><span class="sxs-lookup"><span data-stu-id="e9c8a-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="e9c8a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9c8a-120">-ResourceGroupName</span></span>
<span data-ttu-id="e9c8a-121">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="e9c8a-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="e9c8a-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e9c8a-122">-VMScaleSetName</span></span>
<span data-ttu-id="e9c8a-123">Especimos o nome do VMSS que este cmdlet reinicia.</span><span class="sxs-lookup"><span data-stu-id="e9c8a-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="e9c8a-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e9c8a-124">-Confirm</span></span>
<span data-ttu-id="e9c8a-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9c8a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9c8a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9c8a-126">-WhatIf</span></span>
<span data-ttu-id="e9c8a-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e9c8a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9c8a-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9c8a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9c8a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c8a-129">CommonParameters</span></span>
<span data-ttu-id="e9c8a-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c8a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c8a-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9c8a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c8a-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="e9c8a-132">INPUTS</span></span>

### <span data-ttu-id="e9c8a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e9c8a-133">System.String</span></span>

### <span data-ttu-id="e9c8a-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e9c8a-134">System.String[]</span></span>

## <span data-ttu-id="e9c8a-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="e9c8a-135">OUTPUTS</span></span>

### <span data-ttu-id="e9c8a-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e9c8a-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e9c8a-137">Notas</span><span class="sxs-lookup"><span data-stu-id="e9c8a-137">NOTES</span></span>

## <span data-ttu-id="e9c8a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9c8a-138">RELATED LINKS</span></span>

[<span data-ttu-id="e9c8a-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e9c8a-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="e9c8a-140">Novos AzVmss</span><span class="sxs-lookup"><span data-stu-id="e9c8a-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="e9c8a-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e9c8a-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="e9c8a-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e9c8a-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="e9c8a-143">Iniciar-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e9c8a-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="e9c8a-144">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e9c8a-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="e9c8a-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e9c8a-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


