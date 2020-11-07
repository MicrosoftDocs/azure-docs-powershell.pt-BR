---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D04D79CE-F183-4A8D-B925-F640D89377BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d7c4e6bd9365ccf45b730024b5841e4356f556a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947408"
---
# <span data-ttu-id="8bcac-101">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8bcac-101">Remove-WAPackVM</span></span>

## <span data-ttu-id="8bcac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bcac-102">SYNOPSIS</span></span>
<span data-ttu-id="8bcac-103">Remove objetos de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8bcac-103">Removes virtual machine objects.</span></span>

## <span data-ttu-id="8bcac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bcac-104">SYNTAX</span></span>

```
Remove-WAPackVM -VM <VirtualMachine> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bcac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bcac-105">DESCRIPTION</span></span>
<span data-ttu-id="8bcac-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="8bcac-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="8bcac-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8bcac-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8bcac-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8bcac-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8bcac-109">O cmdlet **Remove-WAPackVM** remove objetos de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8bcac-109">The **Remove-WAPackVM** cmdlet removes virtual machine objects.</span></span>

## <span data-ttu-id="8bcac-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bcac-110">EXAMPLES</span></span>

### <span data-ttu-id="8bcac-111">Exemplo 1: remover uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8bcac-111">Example 1: Remove a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="8bcac-112">O primeiro comando obtém a máquina virtual chamada ContosoV126 usando o cmdlet **Get-WAPackVM** e armazena esse objeto na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8bcac-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="8bcac-113">O segundo comando Remove a máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8bcac-113">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="8bcac-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="8bcac-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="8bcac-115">Exemplo 2: remover uma máquina virtual sem confirmação</span><span class="sxs-lookup"><span data-stu-id="8bcac-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine -Force
```

<span data-ttu-id="8bcac-116">O primeiro comando obtém a máquina virtual chamada ContosoV126 usando o cmdlet **Get-WAPackVM** e armazena esse objeto na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8bcac-116">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="8bcac-117">O segundo comando Remove a máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8bcac-117">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="8bcac-118">Esse comando inclui o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="8bcac-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="8bcac-119">O comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="8bcac-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8bcac-120">OS</span><span class="sxs-lookup"><span data-stu-id="8bcac-120">PARAMETERS</span></span>

### <span data-ttu-id="8bcac-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8bcac-121">-Force</span></span>
<span data-ttu-id="8bcac-122">Indica que o cmdlet Remove uma máquina virtual sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="8bcac-122">Indicates that the cmdlet removes a virtual machine without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8bcac-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bcac-123">-PassThru</span></span>
<span data-ttu-id="8bcac-124">Indica que o cmdlet retorna um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="8bcac-124">Indicates that the cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="8bcac-125">Se a operação for bem-sucedida, o cmdlet retornará um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="8bcac-125">If the operation succeeds, the cmdlet returns a value of $True.</span></span>
<span data-ttu-id="8bcac-126">Caso contrário, retorna um valor de $False.</span><span class="sxs-lookup"><span data-stu-id="8bcac-126">Otherwise, it returns a value of $False.</span></span>
<span data-ttu-id="8bcac-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8bcac-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8bcac-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8bcac-128">-Profile</span></span>
<span data-ttu-id="8bcac-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="8bcac-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8bcac-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="8bcac-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcac-131">-VM</span><span class="sxs-lookup"><span data-stu-id="8bcac-131">-VM</span></span>
<span data-ttu-id="8bcac-132">Especifica uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8bcac-132">Specifies a virtual machine.</span></span>
<span data-ttu-id="8bcac-133">Para obter uma máquina virtual, use o cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="8bcac-133">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

```yaml
Type: VirtualMachine
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bcac-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8bcac-134">-Confirm</span></span>
<span data-ttu-id="8bcac-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bcac-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bcac-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bcac-136">-WhatIf</span></span>
<span data-ttu-id="8bcac-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bcac-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bcac-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bcac-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bcac-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bcac-139">CommonParameters</span></span>
<span data-ttu-id="8bcac-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bcac-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bcac-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bcac-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bcac-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bcac-142">INPUTS</span></span>

## <span data-ttu-id="8bcac-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bcac-143">OUTPUTS</span></span>

## <span data-ttu-id="8bcac-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bcac-144">NOTES</span></span>

## <span data-ttu-id="8bcac-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bcac-145">RELATED LINKS</span></span>

[<span data-ttu-id="8bcac-146">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8bcac-146">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="8bcac-147">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8bcac-147">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="8bcac-148">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8bcac-148">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="8bcac-149">Currículo-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8bcac-149">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="8bcac-150">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8bcac-150">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="8bcac-151">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8bcac-151">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="8bcac-152">Parar-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8bcac-152">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="8bcac-153">Suspender-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8bcac-153">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


