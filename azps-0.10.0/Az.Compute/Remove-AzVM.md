---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 4cdf61c8a5afca78f1701314476d9eacb862cdfb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776924"
---
# <span data-ttu-id="df8fe-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="df8fe-101">Remove-AzVM</span></span>

## <span data-ttu-id="df8fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="df8fe-103">Remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="df8fe-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="df8fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df8fe-104">SYNTAX</span></span>

### <span data-ttu-id="df8fe-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="df8fe-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df8fe-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="df8fe-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df8fe-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df8fe-107">DESCRIPTION</span></span>
<span data-ttu-id="df8fe-108">O cmdlet **Remove-AzVM** remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="df8fe-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="df8fe-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df8fe-109">EXAMPLES</span></span>

### <span data-ttu-id="df8fe-110">Exemplo 1: remover uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="df8fe-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="df8fe-111">Esse comando Remove a máquina virtual nomeada VirtualMachine07 na ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df8fe-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="df8fe-112">OS</span><span class="sxs-lookup"><span data-stu-id="df8fe-112">PARAMETERS</span></span>

### <span data-ttu-id="df8fe-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df8fe-113">-AsJob</span></span>
<span data-ttu-id="df8fe-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="df8fe-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="df8fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df8fe-115">-DefaultProfile</span></span>
<span data-ttu-id="df8fe-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df8fe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df8fe-117">-Force</span><span class="sxs-lookup"><span data-stu-id="df8fe-117">-Force</span></span>
<span data-ttu-id="df8fe-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="df8fe-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8fe-119">-ID</span><span class="sxs-lookup"><span data-stu-id="df8fe-119">-Id</span></span>
<span data-ttu-id="df8fe-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df8fe-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df8fe-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="df8fe-121">-Name</span></span>
<span data-ttu-id="df8fe-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="df8fe-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df8fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df8fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="df8fe-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df8fe-124">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df8fe-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="df8fe-125">-Confirm</span></span>
<span data-ttu-id="df8fe-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df8fe-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8fe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df8fe-127">-WhatIf</span></span>
<span data-ttu-id="df8fe-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df8fe-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="df8fe-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df8fe-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8fe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df8fe-130">CommonParameters</span></span>
<span data-ttu-id="df8fe-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df8fe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df8fe-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df8fe-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df8fe-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df8fe-133">INPUTS</span></span>

### <span data-ttu-id="df8fe-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="df8fe-134">None</span></span>
<span data-ttu-id="df8fe-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="df8fe-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df8fe-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df8fe-136">OUTPUTS</span></span>

### <span data-ttu-id="df8fe-137">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="df8fe-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="df8fe-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df8fe-138">NOTES</span></span>

## <span data-ttu-id="df8fe-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df8fe-139">RELATED LINKS</span></span>

[<span data-ttu-id="df8fe-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="df8fe-140">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="df8fe-141">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="df8fe-141">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="df8fe-142">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="df8fe-142">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="df8fe-143">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="df8fe-143">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="df8fe-144">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="df8fe-144">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="df8fe-145">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="df8fe-145">Update-AzVM</span></span>](./Update-AzVM.md)


