---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4414EA89-8573-416E-A611-DA2135E350BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75b216b512c364a3285df185a3365b1fc85a3d94
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947431"
---
# <span data-ttu-id="c62d1-101">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="c62d1-101">Get-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="c62d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c62d1-102">SYNOPSIS</span></span>
<span data-ttu-id="c62d1-103">Obtém objetos do pool de endereços IP estáticos.</span><span class="sxs-lookup"><span data-stu-id="c62d1-103">Gets static IP address pool objects.</span></span>

## <span data-ttu-id="c62d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c62d1-104">SYNTAX</span></span>

### <span data-ttu-id="c62d1-105">FromVMSubnetObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="c62d1-105">FromVMSubnetObject (Default)</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c62d1-106">FromName</span><span class="sxs-lookup"><span data-stu-id="c62d1-106">FromName</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c62d1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c62d1-107">DESCRIPTION</span></span>
<span data-ttu-id="c62d1-108">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="c62d1-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="c62d1-109">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c62d1-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c62d1-110">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c62d1-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c62d1-111">O cmdlet **Get-WAPackStaticIPAddressPool** obtém objetos do pool de endereços IP estáticos.</span><span class="sxs-lookup"><span data-stu-id="c62d1-111">The **Get-WAPackStaticIPAddressPool** cmdlet gets static IP address pool objects.</span></span>

## <span data-ttu-id="c62d1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c62d1-112">EXAMPLES</span></span>

### <span data-ttu-id="c62d1-113">Exemplo 1: obter um pool de endereços IP estáticos de um determinado VMSubnet</span><span class="sxs-lookup"><span data-stu-id="c62d1-113">Example 1: Get a static IP address pool from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet -Name "ContosoStaticIPAddressPool01"
```

<span data-ttu-id="c62d1-114">Esse comando obtém o pool de endereços IP estáticos chamado ContosoStaticIPAddressPool01 de um VMSubnet especificado.</span><span class="sxs-lookup"><span data-stu-id="c62d1-114">This command gets the static IP address pool named ContosoStaticIPAddressPool01 from a specified VMSubnet.</span></span>

### <span data-ttu-id="c62d1-115">Exemplo 2: obter todos os pools de endereços IP estáticos de um determinado VMSubnet</span><span class="sxs-lookup"><span data-stu-id="c62d1-115">Example 2: Get all static IP address pools from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet
```

<span data-ttu-id="c62d1-116">Esse comando obtém todos os pools IP estáticos de um VMSubet especificado.</span><span class="sxs-lookup"><span data-stu-id="c62d1-116">This command gets all the static IP pools from a specified VMSubet.</span></span>

## <span data-ttu-id="c62d1-117">OS</span><span class="sxs-lookup"><span data-stu-id="c62d1-117">PARAMETERS</span></span>

### <span data-ttu-id="c62d1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c62d1-118">-Name</span></span>
<span data-ttu-id="c62d1-119">Especifica o nome de um pool de endereços IP estáticos.</span><span class="sxs-lookup"><span data-stu-id="c62d1-119">Specifies the name of a static IP address pool.</span></span>

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

### <span data-ttu-id="c62d1-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c62d1-120">-Profile</span></span>
<span data-ttu-id="c62d1-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c62d1-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c62d1-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c62d1-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c62d1-123">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="c62d1-123">-VMSubnet</span></span>
<span data-ttu-id="c62d1-124">Especifica o objeto **VMSubnet** associado ao pool de endereços IP estáticos.</span><span class="sxs-lookup"><span data-stu-id="c62d1-124">Specifies the **VMSubnet** object associated to the static IP address pool.</span></span>

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

### <span data-ttu-id="c62d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c62d1-125">CommonParameters</span></span>
<span data-ttu-id="c62d1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c62d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c62d1-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c62d1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c62d1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c62d1-128">INPUTS</span></span>

## <span data-ttu-id="c62d1-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c62d1-129">OUTPUTS</span></span>

## <span data-ttu-id="c62d1-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c62d1-130">NOTES</span></span>

## <span data-ttu-id="c62d1-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c62d1-131">RELATED LINKS</span></span>

[<span data-ttu-id="c62d1-132">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="c62d1-132">New-WAPackStaticIPAddressPool</span></span>](./New-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="c62d1-133">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="c62d1-133">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


