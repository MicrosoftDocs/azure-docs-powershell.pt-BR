---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 5a7f03cbd4fdac75743fed491697ac2bb4ff6dac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771151"
---
# <span data-ttu-id="d0260-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0260-101">Remove-AzVM</span></span>

## <span data-ttu-id="d0260-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0260-102">SYNOPSIS</span></span>
<span data-ttu-id="d0260-103">Remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0260-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="d0260-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0260-104">SYNTAX</span></span>

### <span data-ttu-id="d0260-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d0260-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0260-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d0260-106">IdParameterSetName</span></span>
```
Remove-AzVM [[-Name] <String>] [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0260-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0260-107">DESCRIPTION</span></span>
<span data-ttu-id="d0260-108">O cmdlet **Remove-AzVM** remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0260-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="d0260-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0260-109">EXAMPLES</span></span>

### <span data-ttu-id="d0260-110">Exemplo 1: remover uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d0260-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="d0260-111">Esse comando Remove a máquina virtual nomeada VirtualMachine07 na ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0260-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="d0260-112">OS</span><span class="sxs-lookup"><span data-stu-id="d0260-112">PARAMETERS</span></span>

### <span data-ttu-id="d0260-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0260-113">-AsJob</span></span>
<span data-ttu-id="d0260-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="d0260-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d0260-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0260-115">-DefaultProfile</span></span>
<span data-ttu-id="d0260-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0260-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0260-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d0260-117">-Force</span></span>
<span data-ttu-id="d0260-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d0260-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0260-119">-ID</span><span class="sxs-lookup"><span data-stu-id="d0260-119">-Id</span></span>
<span data-ttu-id="d0260-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0260-120">The resource group name.</span></span>

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

### <span data-ttu-id="d0260-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0260-121">-Name</span></span>
<span data-ttu-id="d0260-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d0260-122">The resource name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0260-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0260-123">-ResourceGroupName</span></span>
<span data-ttu-id="d0260-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0260-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d0260-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d0260-125">-Confirm</span></span>
<span data-ttu-id="d0260-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0260-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0260-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0260-127">-WhatIf</span></span>
<span data-ttu-id="d0260-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d0260-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0260-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d0260-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0260-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0260-130">CommonParameters</span></span>
<span data-ttu-id="d0260-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0260-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0260-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0260-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0260-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0260-133">INPUTS</span></span>

### <span data-ttu-id="d0260-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d0260-134">System.String</span></span>

## <span data-ttu-id="d0260-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0260-135">OUTPUTS</span></span>

### <span data-ttu-id="d0260-136">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="d0260-136">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="d0260-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0260-137">NOTES</span></span>

## <span data-ttu-id="d0260-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0260-138">RELATED LINKS</span></span>

[<span data-ttu-id="d0260-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0260-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d0260-140">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0260-140">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="d0260-141">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0260-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="d0260-142">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0260-142">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="d0260-143">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0260-143">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="d0260-144">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d0260-144">Update-AzVM</span></span>](./Update-AzVM.md)


