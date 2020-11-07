---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947407"
---
# <span data-ttu-id="4681c-101">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="4681c-101">Remove-WAPackVMSubnet</span></span>

## <span data-ttu-id="4681c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4681c-102">SYNOPSIS</span></span>
<span data-ttu-id="4681c-103">Remove objetos de sub-rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4681c-103">Removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="4681c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4681c-104">SYNTAX</span></span>

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4681c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4681c-105">DESCRIPTION</span></span>
<span data-ttu-id="4681c-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="4681c-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="4681c-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4681c-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4681c-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="4681c-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4681c-109">O cmdlet **Remove-WAPackVMSubnet** remove objetos de sub-rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4681c-109">The **Remove-WAPackVMSubnet** cmdlet removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="4681c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4681c-110">EXAMPLES</span></span>

### <span data-ttu-id="4681c-111">Exemplo 1: remover uma sub-rede de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="4681c-111">Example 1: Remove a virtual machine subnet</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

<span data-ttu-id="4681c-112">O primeiro comando obtém a sub-rede da máquina virtual chamada ContosoVMSubnet01 usando o cmdlet **Get-WAPackVMSubnet** e armazena esse objeto na variável $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="4681c-112">The first command gets the virtual machine subnet named ContosoVMSubnet01 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="4681c-113">O segundo comando Remove a sub-rede da máquina virtual armazenada em $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="4681c-113">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="4681c-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="4681c-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="4681c-115">Exemplo 2: remover uma máquina virtual sem confirmação</span><span class="sxs-lookup"><span data-stu-id="4681c-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

<span data-ttu-id="4681c-116">O primeiro comando obtém o serviço de nuvem chamado ContosoVMSubnet02 usando o cmdlet **Get-WAPackVMSubnet** e armazena esse objeto na variável $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="4681c-116">The first command gets the cloud service named ContosoVMSubnet02 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="4681c-117">O segundo comando Remove a sub-rede da máquina virtual armazenada em $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="4681c-117">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="4681c-118">Esse comando inclui o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="4681c-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="4681c-119">O comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="4681c-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4681c-120">OS</span><span class="sxs-lookup"><span data-stu-id="4681c-120">PARAMETERS</span></span>

### <span data-ttu-id="4681c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4681c-121">-Force</span></span>
<span data-ttu-id="4681c-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4681c-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4681c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4681c-123">-PassThru</span></span>
<span data-ttu-id="4681c-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="4681c-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4681c-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="4681c-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4681c-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4681c-126">-Profile</span></span>
<span data-ttu-id="4681c-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4681c-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4681c-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4681c-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4681c-129">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="4681c-129">-VMSubnet</span></span>
<span data-ttu-id="4681c-130">Especifica uma sub-rede de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4681c-130">Specifies a virtual machine subnet.</span></span>
<span data-ttu-id="4681c-131">Para obter uma sub-rede de máquina virtual, use o cmdlet **Get-WAPackVMSubnet** .</span><span class="sxs-lookup"><span data-stu-id="4681c-131">To obtain a virtual machine subnet, use the **Get-WAPackVMSubnet** cmdlet.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4681c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4681c-132">CommonParameters</span></span>
<span data-ttu-id="4681c-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4681c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4681c-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4681c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4681c-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4681c-135">INPUTS</span></span>

## <span data-ttu-id="4681c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4681c-136">OUTPUTS</span></span>

## <span data-ttu-id="4681c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4681c-137">NOTES</span></span>

## <span data-ttu-id="4681c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4681c-138">RELATED LINKS</span></span>

[<span data-ttu-id="4681c-139">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="4681c-139">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="4681c-140">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="4681c-140">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)


