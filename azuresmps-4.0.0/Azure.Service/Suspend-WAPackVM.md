---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: ABF5B4EB-0908-4103-B0BF-69A68A21D69C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 296a37d00c97bc3af849886593e09a1a0a9ff863
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947367"
---
# <span data-ttu-id="23144-101">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="23144-101">Suspend-WAPackVM</span></span>

## <span data-ttu-id="23144-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23144-102">SYNOPSIS</span></span>
<span data-ttu-id="23144-103">Suspende uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="23144-103">Suspends a virtual machine.</span></span>

## <span data-ttu-id="23144-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23144-104">SYNTAX</span></span>

```
Suspend-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="23144-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23144-105">DESCRIPTION</span></span>
<span data-ttu-id="23144-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="23144-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="23144-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="23144-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="23144-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="23144-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="23144-109">O cmdlet **Suspend-WAPackVM** suspende uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="23144-109">The **Suspend-WAPackVM** cmdlet suspends a virtual machine.</span></span>

## <span data-ttu-id="23144-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23144-110">EXAMPLES</span></span>

### <span data-ttu-id="23144-111">Exemplo 1: suspender uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="23144-111">Example 1: Suspend a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Suspend-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="23144-112">O primeiro comando obtém a máquina virtual chamada ContosoV126 usando o cmdlet **Get-WAPackVM** e armazena esse objeto na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="23144-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="23144-113">O segundo comando suspende a máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="23144-113">The second command suspends the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="23144-114">OS</span><span class="sxs-lookup"><span data-stu-id="23144-114">PARAMETERS</span></span>

### <span data-ttu-id="23144-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23144-115">-PassThru</span></span>
<span data-ttu-id="23144-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="23144-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="23144-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="23144-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="23144-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="23144-118">-Profile</span></span>
<span data-ttu-id="23144-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="23144-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23144-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="23144-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23144-121">-VM</span><span class="sxs-lookup"><span data-stu-id="23144-121">-VM</span></span>
<span data-ttu-id="23144-122">Especifica uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="23144-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="23144-123">Para obter uma máquina virtual, use o cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="23144-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="23144-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23144-124">CommonParameters</span></span>
<span data-ttu-id="23144-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23144-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23144-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23144-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23144-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23144-127">INPUTS</span></span>

## <span data-ttu-id="23144-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23144-128">OUTPUTS</span></span>

## <span data-ttu-id="23144-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23144-129">NOTES</span></span>

## <span data-ttu-id="23144-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23144-130">RELATED LINKS</span></span>

[<span data-ttu-id="23144-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="23144-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="23144-132">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="23144-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="23144-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="23144-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="23144-134">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="23144-134">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="23144-135">Currículo-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="23144-135">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="23144-136">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="23144-136">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="23144-137">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="23144-137">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="23144-138">Parar-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="23144-138">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)


