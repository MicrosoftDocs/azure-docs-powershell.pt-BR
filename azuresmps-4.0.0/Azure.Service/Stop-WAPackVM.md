---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4FB7096E-DDA1-474C-BF0C-D910681BE58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4ef4660761ab29e738050c0445534602accda6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947396"
---
# <span data-ttu-id="13fbf-101">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="13fbf-101">Stop-WAPackVM</span></span>

## <span data-ttu-id="13fbf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="13fbf-103">Interrompe uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="13fbf-103">Stops a virtual machine.</span></span>

## <span data-ttu-id="13fbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13fbf-104">SYNTAX</span></span>

```
Stop-WAPackVM [-Shutdown] -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="13fbf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13fbf-105">DESCRIPTION</span></span>
<span data-ttu-id="13fbf-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="13fbf-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="13fbf-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="13fbf-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="13fbf-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="13fbf-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="13fbf-109">O cmdlet **Stop-WAPackVM** interrompe uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="13fbf-109">The **Stop-WAPackVM** cmdlet stops a virtual machine.</span></span>

## <span data-ttu-id="13fbf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13fbf-110">EXAMPLES</span></span>

### <span data-ttu-id="13fbf-111">Exemplo 1: parar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="13fbf-111">Example 1: Stop a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Stop-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="13fbf-112">O primeiro comando obtém a máquina virtual chamada ContosoV126 usando o cmdlet **Get-WAPackVM** e armazena esse objeto na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="13fbf-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="13fbf-113">O segundo comando interrompe a máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="13fbf-113">The second command stops the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="13fbf-114">OS</span><span class="sxs-lookup"><span data-stu-id="13fbf-114">PARAMETERS</span></span>

### <span data-ttu-id="13fbf-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13fbf-115">-PassThru</span></span>
<span data-ttu-id="13fbf-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="13fbf-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="13fbf-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="13fbf-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="13fbf-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="13fbf-118">-Profile</span></span>
<span data-ttu-id="13fbf-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="13fbf-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13fbf-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="13fbf-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13fbf-121">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="13fbf-121">-Shutdown</span></span>
<span data-ttu-id="13fbf-122">Indica que o cmdlet desliga o sistema operacional da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="13fbf-122">Indicates that the cmdlet shuts down the operating system of the virtual machine.</span></span>

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

### <span data-ttu-id="13fbf-123">-VM</span><span class="sxs-lookup"><span data-stu-id="13fbf-123">-VM</span></span>
<span data-ttu-id="13fbf-124">Especifica uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="13fbf-124">Specifies a virtual machine.</span></span>
<span data-ttu-id="13fbf-125">Para obter uma máquina virtual, use o cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="13fbf-125">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="13fbf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13fbf-126">CommonParameters</span></span>
<span data-ttu-id="13fbf-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13fbf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13fbf-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13fbf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13fbf-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13fbf-129">INPUTS</span></span>

## <span data-ttu-id="13fbf-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13fbf-130">OUTPUTS</span></span>

## <span data-ttu-id="13fbf-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13fbf-131">NOTES</span></span>

## <span data-ttu-id="13fbf-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13fbf-132">RELATED LINKS</span></span>

[<span data-ttu-id="13fbf-133">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="13fbf-133">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="13fbf-134">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="13fbf-134">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="13fbf-135">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="13fbf-135">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="13fbf-136">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="13fbf-136">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="13fbf-137">Currículo-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="13fbf-137">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="13fbf-138">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="13fbf-138">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="13fbf-139">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="13fbf-139">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="13fbf-140">Suspender-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="13fbf-140">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


