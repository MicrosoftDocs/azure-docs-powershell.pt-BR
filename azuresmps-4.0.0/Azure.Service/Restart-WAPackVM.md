---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 80820C11-92BB-4E75-8722-496CF21C779E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a92ff041f5a3eb245b76501e7758ca62b24887f9
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947387"
---
# <span data-ttu-id="ef7af-101">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ef7af-101">Restart-WAPackVM</span></span>

## <span data-ttu-id="ef7af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef7af-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7af-103">Reinicia as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="ef7af-103">Restarts virtual machines.</span></span>

## <span data-ttu-id="ef7af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef7af-104">SYNTAX</span></span>

```
Restart-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ef7af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef7af-105">DESCRIPTION</span></span>
<span data-ttu-id="ef7af-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="ef7af-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="ef7af-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ef7af-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ef7af-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ef7af-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ef7af-109">O cmdlet **Restart-WAPackVM** reinicia as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="ef7af-109">The **Restart-WAPackVM** cmdlet restarts virtual machines.</span></span>

## <span data-ttu-id="ef7af-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef7af-110">EXAMPLES</span></span>

### <span data-ttu-id="ef7af-111">Exemplo 1: reiniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="ef7af-111">Example 1: Restart a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Restart-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="ef7af-112">O primeiro comando obtém a máquina virtual chamada ContosoV126 usando o cmdlet **Get-WAPackVM** e armazena esse objeto na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ef7af-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="ef7af-113">O segundo comando reinicia a máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ef7af-113">The second command restarts the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="ef7af-114">OS</span><span class="sxs-lookup"><span data-stu-id="ef7af-114">PARAMETERS</span></span>

### <span data-ttu-id="ef7af-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef7af-115">-PassThru</span></span>
<span data-ttu-id="ef7af-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ef7af-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ef7af-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ef7af-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef7af-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ef7af-118">-Profile</span></span>
<span data-ttu-id="ef7af-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ef7af-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ef7af-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ef7af-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ef7af-121">-VM</span><span class="sxs-lookup"><span data-stu-id="ef7af-121">-VM</span></span>
<span data-ttu-id="ef7af-122">Especifica uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ef7af-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="ef7af-123">Para obter uma máquina virtual, use o cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="ef7af-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="ef7af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7af-124">CommonParameters</span></span>
<span data-ttu-id="ef7af-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef7af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7af-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef7af-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7af-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef7af-127">INPUTS</span></span>

## <span data-ttu-id="ef7af-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef7af-128">OUTPUTS</span></span>

## <span data-ttu-id="ef7af-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef7af-129">NOTES</span></span>

## <span data-ttu-id="ef7af-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef7af-130">RELATED LINKS</span></span>

[<span data-ttu-id="ef7af-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ef7af-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="ef7af-132">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ef7af-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="ef7af-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ef7af-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="ef7af-134">Currículo-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ef7af-134">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="ef7af-135">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ef7af-135">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="ef7af-136">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ef7af-136">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="ef7af-137">Parar-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ef7af-137">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="ef7af-138">Suspender-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="ef7af-138">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


