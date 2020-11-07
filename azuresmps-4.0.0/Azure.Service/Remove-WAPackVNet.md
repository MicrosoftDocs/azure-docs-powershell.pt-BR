---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947406"
---
# <span data-ttu-id="e5996-101">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="e5996-101">Remove-WAPackVNet</span></span>

## <span data-ttu-id="e5996-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5996-102">SYNOPSIS</span></span>
<span data-ttu-id="e5996-103">Remove os objetos de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e5996-103">Removes virtual network objects.</span></span>

## <span data-ttu-id="e5996-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5996-104">SYNTAX</span></span>

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e5996-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5996-105">DESCRIPTION</span></span>
<span data-ttu-id="e5996-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="e5996-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="e5996-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e5996-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e5996-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e5996-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e5996-109">O cmdlet **Remove-WAPackVNet** remove objetos de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e5996-109">The **Remove-WAPackVNet** cmdlet removes virtual network objects.</span></span>

## <span data-ttu-id="e5996-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5996-110">EXAMPLES</span></span>

### <span data-ttu-id="e5996-111">Exemplo 1: remover uma rede virtualizada</span><span class="sxs-lookup"><span data-stu-id="e5996-111">Example 1: Remove a virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

<span data-ttu-id="e5996-112">O primeiro comando obtém a rede virtualizada chamada ContosoVNet01 usando o cmdlet **Get-WAPackVNet** e armazena esse objeto na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="e5996-112">The first command gets the virtualized network named ContosoVNet01 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="e5996-113">O segundo comando Remove a rede virtualizada armazenada em $VNet.</span><span class="sxs-lookup"><span data-stu-id="e5996-113">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="e5996-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="e5996-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="e5996-115">Exemplo 2: remover uma rede virtualizada sem confirmação</span><span class="sxs-lookup"><span data-stu-id="e5996-115">Example 2: Remove a virtualized network without confirmation</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

<span data-ttu-id="e5996-116">O primeiro comando obtém o serviço de nuvem chamado ContosoVNet02 usando o cmdlet **Get-WAPackVNet** e armazena esse objeto na variável $VNet.</span><span class="sxs-lookup"><span data-stu-id="e5996-116">The first command gets the cloud service named ContosoVNet02 by using the **Get-WAPackVNet** cmdlet, and then stores that object in the $VNet variable.</span></span>
<span data-ttu-id="e5996-117">O segundo comando Remove a rede virtualizada armazenada em $VNet.</span><span class="sxs-lookup"><span data-stu-id="e5996-117">The second command removes the virtualized network stored in $VNet.</span></span>
<span data-ttu-id="e5996-118">Esse comando inclui o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="e5996-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="e5996-119">O comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="e5996-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e5996-120">OS</span><span class="sxs-lookup"><span data-stu-id="e5996-120">PARAMETERS</span></span>

### <span data-ttu-id="e5996-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e5996-121">-Force</span></span>
<span data-ttu-id="e5996-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e5996-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5996-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5996-123">-PassThru</span></span>
<span data-ttu-id="e5996-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e5996-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5996-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e5996-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e5996-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e5996-126">-Profile</span></span>
<span data-ttu-id="e5996-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e5996-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5996-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e5996-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5996-129">-VNet</span><span class="sxs-lookup"><span data-stu-id="e5996-129">-VNet</span></span>
<span data-ttu-id="e5996-130">Especifica uma rede virtualizada.</span><span class="sxs-lookup"><span data-stu-id="e5996-130">Specifies a virtualized network.</span></span>
<span data-ttu-id="e5996-131">Para obter uma rede virtualizada, use o cmdlet **Get-WAPackVNet** .</span><span class="sxs-lookup"><span data-stu-id="e5996-131">To obtain a virtualized network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5996-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5996-132">CommonParameters</span></span>
<span data-ttu-id="e5996-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5996-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5996-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5996-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5996-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5996-135">INPUTS</span></span>

## <span data-ttu-id="e5996-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5996-136">OUTPUTS</span></span>

## <span data-ttu-id="e5996-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5996-137">NOTES</span></span>

## <span data-ttu-id="e5996-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5996-138">RELATED LINKS</span></span>

[<span data-ttu-id="e5996-139">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="e5996-139">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="e5996-140">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="e5996-140">New-WAPackVNet</span></span>](./New-WAPackVNet.md)


