---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0E358CEF-69E4-4639-918C-CE593E97B189
online version: ''
schema: 2.0.0
ms.openlocfilehash: d534a1734a49739db648558e8d7e62b22e43d561
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947355"
---
# <span data-ttu-id="99d4c-101">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="99d4c-101">Get-WAPackVMSubnet</span></span>

## <span data-ttu-id="99d4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="99d4c-103">Obtém objetos de sub-rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99d4c-103">Gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="99d4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99d4c-104">SYNTAX</span></span>

### <span data-ttu-id="99d4c-105">FromVMNetworkObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="99d4c-105">FromVMNetworkObject (Default)</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="99d4c-106">FromName</span><span class="sxs-lookup"><span data-stu-id="99d4c-106">FromName</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="99d4c-107">DEID</span><span class="sxs-lookup"><span data-stu-id="99d4c-107">FromId</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="99d4c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99d4c-108">DESCRIPTION</span></span>
<span data-ttu-id="99d4c-109">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="99d4c-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="99d4c-110">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="99d4c-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="99d4c-111">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="99d4c-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="99d4c-112">O cmdlet **Get-WAPackVMSubnet** obtém objetos de sub-rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99d4c-112">The **Get-WAPackVMSubnet** cmdlet gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="99d4c-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99d4c-113">EXAMPLES</span></span>

### <span data-ttu-id="99d4c-114">Exemplo 1: obter uma sub-rede de máquina virtual usando um nome</span><span class="sxs-lookup"><span data-stu-id="99d4c-114">Example 1: Get a virtual machine subnet by using a name</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMTemplate -VNet $VNet -Name "ContosoSubnet01"
```

<span data-ttu-id="99d4c-115">Esse comando obtém a sub-rede da máquina virtual chamada ContosoSubnet01.</span><span class="sxs-lookup"><span data-stu-id="99d4c-115">This command gets the virtual machine subnet named ContosoSubnet01.</span></span>

### <span data-ttu-id="99d4c-116">Exemplo 2: obter uma sub-rede de máquina virtual usando uma ID</span><span class="sxs-lookup"><span data-stu-id="99d4c-116">Example 2: Get a virtual machine subnet by using an ID</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="99d4c-117">Este comando obtém a sub-rede da máquina virtual com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="99d4c-117">This command gets the virtual machine subnet that has the specified ID.</span></span>

### <span data-ttu-id="99d4c-118">Exemplo 3: obter todas as sub-redes de máquina virtual de uma determinada rede virtualizada</span><span class="sxs-lookup"><span data-stu-id="99d4c-118">Example 3: Get all virtual machine subnets from a given virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet
```

<span data-ttu-id="99d4c-119">Esse comando obtém todas as sub-redes de máquina virtual de uma determinada rede virtualizada.</span><span class="sxs-lookup"><span data-stu-id="99d4c-119">This command gets all the virtual machine subnets from a given virtualized network.</span></span>

## <span data-ttu-id="99d4c-120">OS</span><span class="sxs-lookup"><span data-stu-id="99d4c-120">PARAMETERS</span></span>

### <span data-ttu-id="99d4c-121">-ID</span><span class="sxs-lookup"><span data-stu-id="99d4c-121">-ID</span></span>
<span data-ttu-id="99d4c-122">Especifica a ID exclusiva de uma sub-rede da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99d4c-122">Specifies the unique ID of a virtual machine subnet.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d4c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="99d4c-123">-Name</span></span>
<span data-ttu-id="99d4c-124">Especifica o nome de uma sub-rede de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99d4c-124">Specifies the name of a virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d4c-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="99d4c-125">-Profile</span></span>
<span data-ttu-id="99d4c-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="99d4c-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="99d4c-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="99d4c-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="99d4c-128">-VNet</span><span class="sxs-lookup"><span data-stu-id="99d4c-128">-VNet</span></span>
<span data-ttu-id="99d4c-129">Especifica a VNet associada a uma sub-rede de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="99d4c-129">Specifies the VNet associated with a virtual machine subnet.</span></span>

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

### <span data-ttu-id="99d4c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d4c-130">CommonParameters</span></span>
<span data-ttu-id="99d4c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d4c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d4c-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d4c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d4c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99d4c-133">INPUTS</span></span>

## <span data-ttu-id="99d4c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99d4c-134">OUTPUTS</span></span>

## <span data-ttu-id="99d4c-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99d4c-135">NOTES</span></span>

## <span data-ttu-id="99d4c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99d4c-136">RELATED LINKS</span></span>

[<span data-ttu-id="99d4c-137">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="99d4c-137">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="99d4c-138">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="99d4c-138">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)

[<span data-ttu-id="99d4c-139">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="99d4c-139">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


