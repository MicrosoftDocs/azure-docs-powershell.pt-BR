---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 69FBF1E7-E69A-42B5-AC17-C7CF8CAB3C9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da323d5284de94aaadfc92abdf819f861695335
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947383"
---
# <span data-ttu-id="46d96-101">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="46d96-101">Set-WAPackVMRole</span></span>

## <span data-ttu-id="46d96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46d96-102">SYNOPSIS</span></span>
<span data-ttu-id="46d96-103">Altera a propriedade de contagem de instâncias de uma função de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46d96-103">Changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="46d96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46d96-104">SYNTAX</span></span>

```
Set-WAPackVMRole -VMRole <VMRole> -InstanceCount <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="46d96-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46d96-105">DESCRIPTION</span></span>
<span data-ttu-id="46d96-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="46d96-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="46d96-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46d96-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="46d96-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="46d96-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="46d96-109">O cmdlet **set-WAPackVMRole** altera a propriedade Count da instância de uma função de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46d96-109">The **Set-WAPackVMRole** cmdlet changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="46d96-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46d96-110">EXAMPLES</span></span>

### <span data-ttu-id="46d96-111">Exemplo 1: especificar a contagem de instâncias para uma função de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="46d96-111">Example 1: Specify the instance count for a virtual machine role</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Set-WAPackVMRole -VMRole $VMRole -InstanceCount 3
```

<span data-ttu-id="46d96-112">O primeiro comando obtém a função da máquina virtual chamada ContosoVMRole01 usando o cmdlet **Get-WAPackVMRole** e armazena esse objeto na variável $VMRole.</span><span class="sxs-lookup"><span data-stu-id="46d96-112">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="46d96-113">O segundo comando e último define a nova contagem de instâncias da função de máquina virtual armazenada em $VMRole para 3.</span><span class="sxs-lookup"><span data-stu-id="46d96-113">The second and final command sets the new instance count of the virtual machine role stored in $VMRole to 3.</span></span>

## <span data-ttu-id="46d96-114">OS</span><span class="sxs-lookup"><span data-stu-id="46d96-114">PARAMETERS</span></span>

### <span data-ttu-id="46d96-115">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="46d96-115">-InstanceCount</span></span>
<span data-ttu-id="46d96-116">Especifica a contagem de instâncias para uma função de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46d96-116">Specifies the instance count for a virtual machine role.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d96-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46d96-117">-PassThru</span></span>
<span data-ttu-id="46d96-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="46d96-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="46d96-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="46d96-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="46d96-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="46d96-120">-Profile</span></span>
<span data-ttu-id="46d96-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="46d96-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46d96-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="46d96-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46d96-123">-VMRole</span><span class="sxs-lookup"><span data-stu-id="46d96-123">-VMRole</span></span>
<span data-ttu-id="46d96-124">Especifica uma função de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="46d96-124">Specifies a virtual machine role.</span></span>
<span data-ttu-id="46d96-125">Para obter uma função de máquina virtual, use o cmdlet **Get-WAPackVMRole** .</span><span class="sxs-lookup"><span data-stu-id="46d96-125">To obtain a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d96-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d96-126">CommonParameters</span></span>
<span data-ttu-id="46d96-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d96-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d96-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d96-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d96-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46d96-129">INPUTS</span></span>

## <span data-ttu-id="46d96-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46d96-130">OUTPUTS</span></span>

## <span data-ttu-id="46d96-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46d96-131">NOTES</span></span>

## <span data-ttu-id="46d96-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46d96-132">RELATED LINKS</span></span>

[<span data-ttu-id="46d96-133">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="46d96-133">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="46d96-134">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="46d96-134">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="46d96-135">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="46d96-135">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)


