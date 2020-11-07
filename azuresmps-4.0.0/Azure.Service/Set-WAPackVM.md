---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 08A7556E-C07F-4B3B-B9D6-B241C72860FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b01ac318982b62499164cd54c9d9a51356ad9830
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947385"
---
# <span data-ttu-id="e597b-101">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="e597b-101">Set-WAPackVM</span></span>

## <span data-ttu-id="e597b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e597b-102">SYNOPSIS</span></span>
<span data-ttu-id="e597b-103">Altera as propriedades de tamanho de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e597b-103">Changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="e597b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e597b-104">SYNTAX</span></span>

```
Set-WAPackVM -VM <VirtualMachine> -VMSizeProfile <HardwareProfile> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e597b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e597b-105">DESCRIPTION</span></span>
<span data-ttu-id="e597b-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="e597b-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="e597b-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e597b-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e597b-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e597b-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e597b-109">O cmdlet **set-WAPackVM** altera as propriedades de tamanho de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e597b-109">The **Set-WAPackVM** cmdlet changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="e597b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e597b-110">EXAMPLES</span></span>

### <span data-ttu-id="e597b-111">Exemplo 1: especificar o tamanho de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e597b-111">Example 1: Specify the size for a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> Set-WAPackVM -VM $VirtualMachine -VMSizeProfile $SizeProfile
```

<span data-ttu-id="e597b-112">O primeiro comando obtém a máquina virtual chamada ContosoV126 usando o cmdlet **Get-WAPackVM** e armazena esse objeto na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e597b-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="e597b-113">O segundo comando obtém o perfil de tamanho chamado MediumSizeVM usando o cmdlet **Get-WAPackVMSizeProfile** e armazena esse objeto na variável $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="e597b-113">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores that object in the $SizeProfile variable.</span></span>

<span data-ttu-id="e597b-114">O comando final atribui o perfil de tamanho armazenado em $SizeProfile à máquina virtual armazenada no $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e597b-114">The final command assigns the size profile stored in $SizeProfile to the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="e597b-115">OS</span><span class="sxs-lookup"><span data-stu-id="e597b-115">PARAMETERS</span></span>

### <span data-ttu-id="e597b-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e597b-116">-PassThru</span></span>
<span data-ttu-id="e597b-117">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e597b-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e597b-118">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e597b-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e597b-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e597b-119">-Profile</span></span>
<span data-ttu-id="e597b-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e597b-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e597b-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e597b-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e597b-122">-VM</span><span class="sxs-lookup"><span data-stu-id="e597b-122">-VM</span></span>
<span data-ttu-id="e597b-123">Especifica uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e597b-123">Specifies a virtual machine.</span></span>
<span data-ttu-id="e597b-124">Para obter uma máquina virtual, use o cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="e597b-124">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="e597b-125">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="e597b-125">-VMSizeProfile</span></span>
<span data-ttu-id="e597b-126">Especifica um perfil de tamanho para uma máquina virtual como um objeto **HardwareProfile** .</span><span class="sxs-lookup"><span data-stu-id="e597b-126">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="e597b-127">Para obter um perfil de tamanho, use o cmdlet **Get-WAPackVMSizeProfile** .</span><span class="sxs-lookup"><span data-stu-id="e597b-127">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e597b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e597b-128">CommonParameters</span></span>
<span data-ttu-id="e597b-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e597b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e597b-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e597b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e597b-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e597b-131">INPUTS</span></span>

## <span data-ttu-id="e597b-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e597b-132">OUTPUTS</span></span>

## <span data-ttu-id="e597b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e597b-133">NOTES</span></span>

## <span data-ttu-id="e597b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e597b-134">RELATED LINKS</span></span>

[<span data-ttu-id="e597b-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="e597b-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="e597b-136">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="e597b-136">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="e597b-137">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="e597b-137">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="e597b-138">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="e597b-138">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="e597b-139">Currículo-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="e597b-139">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="e597b-140">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="e597b-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="e597b-141">Parar-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="e597b-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="e597b-142">Suspender-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="e597b-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="e597b-143">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="e597b-143">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)


