---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CE618AD2-7E28-4012-BF3C-B932B95FFDD5
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07358c37bf30e8d5fc3040cdfd174b800df96e4
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947412"
---
# <span data-ttu-id="01220-101">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="01220-101">Remove-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="01220-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01220-102">SYNOPSIS</span></span>
<span data-ttu-id="01220-103">Remove objetos do pool de endereços IP estáticos.</span><span class="sxs-lookup"><span data-stu-id="01220-103">Removes static IP address pool objects.</span></span>

## <span data-ttu-id="01220-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01220-104">SYNTAX</span></span>

```
Remove-WAPackStaticIPAddressPool -StaticIPAddressPool <StaticIPAddressPool> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="01220-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01220-105">DESCRIPTION</span></span>
<span data-ttu-id="01220-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="01220-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="01220-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="01220-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="01220-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="01220-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="01220-109">O cmdlet **Remove-WAPackStaticIPAddressPool** remove objetos do pool de endereços IP estáticos.</span><span class="sxs-lookup"><span data-stu-id="01220-109">The **Remove-WAPackStaticIPAddressPool** cmdlet removes static IP address pool objects.</span></span>

## <span data-ttu-id="01220-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01220-110">EXAMPLES</span></span>

### <span data-ttu-id="01220-111">Exemplo 1: remover um pool de endereços IP estáticos</span><span class="sxs-lookup"><span data-stu-id="01220-111">Example 1: Remove a static IP address pool</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool01"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool
```

<span data-ttu-id="01220-112">O primeiro comando obtém o pool de endereços IP estáticos chamado ContosoStaticIPAddressPool01 usando o cmdlet **Get-WAPackStaticIPAddressPool** e armazena esse objeto na variável $StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="01220-112">The first command gets the static IP address pool named ContosoStaticIPAddressPool01 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $StaticIPAddressPool variable.</span></span>

<span data-ttu-id="01220-113">O segundo comando Remove o pool de endereços IP estáticos armazenado em $StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="01220-113">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="01220-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="01220-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="01220-115">Exemplo 2: remover um pool de endereços IP estáticos sem confirmação</span><span class="sxs-lookup"><span data-stu-id="01220-115">Example 2: Remove a static IP address pool without confirmation</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool02"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool -Force
```

<span data-ttu-id="01220-116">O primeiro comando obtém o pool de endereços IP estáticos chamado ContosoStaticIPAddressPool02 usando o cmdlet **Get-WAPackStaticIPAddressPool** e, em seguida, armazena esse objeto na variável $ StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="01220-116">The first command gets the static IP address pool named ContosoStaticIPAddressPool02 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $ StaticIPAddressPool variable.</span></span>

<span data-ttu-id="01220-117">O segundo comando Remove o pool de endereços IP estáticos armazenado em $StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="01220-117">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="01220-118">Esse comando inclui o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="01220-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="01220-119">O comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="01220-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="01220-120">OS</span><span class="sxs-lookup"><span data-stu-id="01220-120">PARAMETERS</span></span>

### <span data-ttu-id="01220-121">-Force</span><span class="sxs-lookup"><span data-stu-id="01220-121">-Force</span></span>
<span data-ttu-id="01220-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="01220-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="01220-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01220-123">-PassThru</span></span>
<span data-ttu-id="01220-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="01220-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="01220-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="01220-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="01220-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="01220-126">-Profile</span></span>
<span data-ttu-id="01220-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="01220-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="01220-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="01220-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="01220-129">-StaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="01220-129">-StaticIPAddressPool</span></span>
<span data-ttu-id="01220-130">Especifica um StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="01220-130">Specifies a StaticIPAddressPool.</span></span>
<span data-ttu-id="01220-131">Para obter um pool de endereços IP estático, use o cmdlet **Get-WAPackStaticIPAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="01220-131">To obtain a static IP address pool, use the **Get-WAPackStaticIPAddressPool** cmdlet.</span></span>

```yaml
Type: StaticIPAddressPool
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01220-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01220-132">CommonParameters</span></span>
<span data-ttu-id="01220-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01220-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01220-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01220-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01220-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01220-135">INPUTS</span></span>

## <span data-ttu-id="01220-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01220-136">OUTPUTS</span></span>

## <span data-ttu-id="01220-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01220-137">NOTES</span></span>

## <span data-ttu-id="01220-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01220-138">RELATED LINKS</span></span>

[<span data-ttu-id="01220-139">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="01220-139">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="01220-140">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="01220-140">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


