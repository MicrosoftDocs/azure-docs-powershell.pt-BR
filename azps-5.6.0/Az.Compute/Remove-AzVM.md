---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: d5ce1af197575f96fd21f5355c0edfb98e3b181f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888732"
---
# <span data-ttu-id="6b604-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="6b604-101">Remove-AzVM</span></span>

## <span data-ttu-id="6b604-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b604-102">SYNOPSIS</span></span>
<span data-ttu-id="6b604-103">Remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b604-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="6b604-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6b604-104">SYNTAX</span></span>

### <span data-ttu-id="6b604-105">ResourceGroupNameParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6b604-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b604-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6b604-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b604-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6b604-107">DESCRIPTION</span></span>
<span data-ttu-id="6b604-108">O cmdlet **Remove-AzVM** remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b604-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="6b604-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b604-109">EXAMPLES</span></span>

### <span data-ttu-id="6b604-110">Exemplo 1: Remover uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="6b604-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="6b604-111">Este comando remove a máquina virtual chamada VirtualMachine07 no grupo de recursos ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6b604-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="6b604-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6b604-112">PARAMETERS</span></span>

### <span data-ttu-id="6b604-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b604-113">-AsJob</span></span>
<span data-ttu-id="6b604-114">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="6b604-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6b604-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b604-115">-DefaultProfile</span></span>
<span data-ttu-id="6b604-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6b604-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b604-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6b604-117">-Force</span></span>
<span data-ttu-id="6b604-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6b604-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b604-119">-Id</span><span class="sxs-lookup"><span data-stu-id="6b604-119">-Id</span></span>
<span data-ttu-id="6b604-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b604-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b604-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6b604-121">-Name</span></span>
<span data-ttu-id="6b604-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="6b604-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b604-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6b604-123">-NoWait</span></span>
<span data-ttu-id="6b604-124">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="6b604-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="6b604-125">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="6b604-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="6b604-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b604-126">-ResourceGroupName</span></span>
<span data-ttu-id="6b604-127">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b604-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b604-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b604-128">-Confirm</span></span>
<span data-ttu-id="6b604-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b604-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b604-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b604-130">-WhatIf</span></span>
<span data-ttu-id="6b604-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b604-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b604-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b604-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b604-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b604-133">CommonParameters</span></span>
<span data-ttu-id="6b604-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b604-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b604-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b604-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b604-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b604-136">INPUTS</span></span>

### <span data-ttu-id="6b604-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6b604-137">System.String</span></span>

## <span data-ttu-id="6b604-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6b604-138">OUTPUTS</span></span>

### <span data-ttu-id="6b604-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="6b604-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="6b604-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6b604-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6b604-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="6b604-141">NOTES</span></span>

## <span data-ttu-id="6b604-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b604-142">RELATED LINKS</span></span>

[<span data-ttu-id="6b604-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="6b604-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="6b604-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="6b604-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="6b604-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="6b604-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="6b604-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="6b604-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="6b604-147">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="6b604-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="6b604-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6b604-148">Update-AzVM</span></span>](./Update-AzVM.md)


