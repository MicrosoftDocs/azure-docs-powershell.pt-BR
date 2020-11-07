---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947381"
---
# <span data-ttu-id="1ad68-101">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="1ad68-101">New-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="1ad68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ad68-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad68-103">Cria um pool de endereços IP estáticos.</span><span class="sxs-lookup"><span data-stu-id="1ad68-103">Creates a static IP address pool.</span></span>

## <span data-ttu-id="1ad68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ad68-104">SYNTAX</span></span>

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1ad68-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ad68-105">DESCRIPTION</span></span>
<span data-ttu-id="1ad68-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="1ad68-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="1ad68-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ad68-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1ad68-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1ad68-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1ad68-109">O cmdlet **New-WAPackStaticIPAddressPool** cria um pool de endereços IP estáticos.</span><span class="sxs-lookup"><span data-stu-id="1ad68-109">The **New-WAPackStaticIPAddressPool** cmdlet creates a static IP address pool.</span></span>

## <span data-ttu-id="1ad68-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ad68-110">EXAMPLES</span></span>

### <span data-ttu-id="1ad68-111">Exemplo 1: criar um pool de endereços IP estáticos</span><span class="sxs-lookup"><span data-stu-id="1ad68-111">Example 1: Create a static IP address pool</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

<span data-ttu-id="1ad68-112">O primeiro comando recupera a rede da máquina virtual à qual queremos adicionar o pool de endereços IP estático.</span><span class="sxs-lookup"><span data-stu-id="1ad68-112">The first command first retrieves the virtual machine network to which we want to add the static IP address pool.</span></span>
<span data-ttu-id="1ad68-113">Esta rede de máquina virtual se chama ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="1ad68-113">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="1ad68-114">O segundo comando usa a rede de máquina virtual recuperada anteriormente para obter a sub-rede da máquina virtual chamada ContosoVMSubnet01 à qual queremos adicionar o pool de endereços IP estático.</span><span class="sxs-lookup"><span data-stu-id="1ad68-114">The second command uses the previously retrieved virtual machine network to get the virtual machine subnet named ContosoVMSubnet01 to which we want to add the static IP address pool.</span></span>

<span data-ttu-id="1ad68-115">O último comando cria um novo pool de endereços IP estáticos com um nome ContosoStaticIpAddressPool01 e um intervalo de início 192.168.1.0 e um final de um intervalo 192.168.1.10.</span><span class="sxs-lookup"><span data-stu-id="1ad68-115">The last command creates a new static IP address pool with a name ContosoStaticIpAddressPool01 and a range start 192.168.1.0 and a range end 192.168.1.10.</span></span>

## <span data-ttu-id="1ad68-116">OS</span><span class="sxs-lookup"><span data-stu-id="1ad68-116">PARAMETERS</span></span>

### <span data-ttu-id="1ad68-117">-IPAddressRangeEnd</span><span class="sxs-lookup"><span data-stu-id="1ad68-117">-IPAddressRangeEnd</span></span>
<span data-ttu-id="1ad68-118">Especifica um final de intervalo de endereços IP para o pool de endereços IP estáticos.</span><span class="sxs-lookup"><span data-stu-id="1ad68-118">Specifies an IP address range end for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad68-119">-IPAddressRangeStart</span><span class="sxs-lookup"><span data-stu-id="1ad68-119">-IPAddressRangeStart</span></span>
<span data-ttu-id="1ad68-120">Especifica um início de intervalo de endereços IP para o pool de endereços IP estáticos.</span><span class="sxs-lookup"><span data-stu-id="1ad68-120">Specifies an IP address range start for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad68-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ad68-121">-Name</span></span>
<span data-ttu-id="1ad68-122">Especifica um nome para o pool de endereços IP estáticos.</span><span class="sxs-lookup"><span data-stu-id="1ad68-122">Specifies a name for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad68-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1ad68-123">-Profile</span></span>
<span data-ttu-id="1ad68-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1ad68-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ad68-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1ad68-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ad68-126">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="1ad68-126">-VMSubnet</span></span>
<span data-ttu-id="1ad68-127">Especifica um VMSubnet associado ao pool de endereços IP estáticos.</span><span class="sxs-lookup"><span data-stu-id="1ad68-127">Specifies a VMSubnet associated with the static IP address pool.</span></span>

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

### <span data-ttu-id="1ad68-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad68-128">CommonParameters</span></span>
<span data-ttu-id="1ad68-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ad68-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad68-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ad68-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad68-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ad68-131">INPUTS</span></span>

## <span data-ttu-id="1ad68-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ad68-132">OUTPUTS</span></span>

## <span data-ttu-id="1ad68-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ad68-133">NOTES</span></span>

## <span data-ttu-id="1ad68-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ad68-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ad68-135">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="1ad68-135">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="1ad68-136">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="1ad68-136">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


