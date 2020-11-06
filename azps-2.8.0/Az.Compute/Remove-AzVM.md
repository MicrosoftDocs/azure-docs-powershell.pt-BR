---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 9256828a338678cb1da12e14cb6e450ee4030ebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597310"
---
# <span data-ttu-id="07d66-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="07d66-101">Remove-AzVM</span></span>

## <span data-ttu-id="07d66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07d66-102">SYNOPSIS</span></span>
<span data-ttu-id="07d66-103">Remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="07d66-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="07d66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07d66-104">SYNTAX</span></span>

### <span data-ttu-id="07d66-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="07d66-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07d66-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="07d66-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07d66-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07d66-107">DESCRIPTION</span></span>
<span data-ttu-id="07d66-108">O cmdlet **Remove-AzVM** remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="07d66-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="07d66-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07d66-109">EXAMPLES</span></span>

### <span data-ttu-id="07d66-110">Exemplo 1: remover uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="07d66-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="07d66-111">Esse comando Remove a máquina virtual nomeada VirtualMachine07 na ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07d66-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="07d66-112">OS</span><span class="sxs-lookup"><span data-stu-id="07d66-112">PARAMETERS</span></span>

### <span data-ttu-id="07d66-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07d66-113">-AsJob</span></span>
<span data-ttu-id="07d66-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="07d66-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="07d66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d66-115">-DefaultProfile</span></span>
<span data-ttu-id="07d66-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07d66-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07d66-117">-Force</span><span class="sxs-lookup"><span data-stu-id="07d66-117">-Force</span></span>
<span data-ttu-id="07d66-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="07d66-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="07d66-119">-ID</span><span class="sxs-lookup"><span data-stu-id="07d66-119">-Id</span></span>
<span data-ttu-id="07d66-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07d66-120">The resource group name.</span></span>

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

### <span data-ttu-id="07d66-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="07d66-121">-Name</span></span>
<span data-ttu-id="07d66-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="07d66-122">The resource name.</span></span>

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

### <span data-ttu-id="07d66-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="07d66-123">-NoWait</span></span>
<span data-ttu-id="07d66-124">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="07d66-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="07d66-125">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="07d66-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="07d66-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07d66-126">-ResourceGroupName</span></span>
<span data-ttu-id="07d66-127">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07d66-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="07d66-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="07d66-128">-Confirm</span></span>
<span data-ttu-id="07d66-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07d66-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07d66-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07d66-130">-WhatIf</span></span>
<span data-ttu-id="07d66-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07d66-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07d66-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07d66-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07d66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d66-133">CommonParameters</span></span>
<span data-ttu-id="07d66-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d66-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07d66-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d66-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07d66-136">INPUTS</span></span>

### <span data-ttu-id="07d66-137">System. String</span><span class="sxs-lookup"><span data-stu-id="07d66-137">System.String</span></span>

## <span data-ttu-id="07d66-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07d66-138">OUTPUTS</span></span>

### <span data-ttu-id="07d66-139">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="07d66-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="07d66-140">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="07d66-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="07d66-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07d66-141">NOTES</span></span>

## <span data-ttu-id="07d66-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07d66-142">RELATED LINKS</span></span>

[<span data-ttu-id="07d66-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="07d66-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="07d66-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="07d66-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="07d66-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="07d66-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="07d66-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="07d66-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="07d66-147">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="07d66-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="07d66-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="07d66-148">Update-AzVM</span></span>](./Update-AzVM.md)


