---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947352"
---
# <span data-ttu-id="53956-101">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="53956-101">Get-WAPackVMOSDisk</span></span>

## <span data-ttu-id="53956-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53956-102">SYNOPSIS</span></span>
<span data-ttu-id="53956-103">Obtém objetos de disco do sistema operacional para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="53956-103">Gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="53956-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53956-104">SYNTAX</span></span>

### <span data-ttu-id="53956-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="53956-105">Empty (Default)</span></span>
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="53956-106">DEID</span><span class="sxs-lookup"><span data-stu-id="53956-106">FromId</span></span>
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="53956-107">FromName</span><span class="sxs-lookup"><span data-stu-id="53956-107">FromName</span></span>
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="53956-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53956-108">DESCRIPTION</span></span>
<span data-ttu-id="53956-109">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="53956-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="53956-110">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="53956-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="53956-111">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="53956-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="53956-112">O cmdlet **Get-WAPackVMOSDisk** obtém objetos de disco do sistema operacional para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="53956-112">The **Get-WAPackVMOSDisk** cmdlet gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="53956-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53956-113">EXAMPLES</span></span>

### <span data-ttu-id="53956-114">Exemplo 1: obter um disco do sistema operacional usando um nome</span><span class="sxs-lookup"><span data-stu-id="53956-114">Example 1: Get an operating system disk by using a name</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

<span data-ttu-id="53956-115">Esse comando obtém um disco do sistema operacional chamado ContosoOSDisk.</span><span class="sxs-lookup"><span data-stu-id="53956-115">This command gets an operating system disk named ContosoOSDisk.</span></span>

### <span data-ttu-id="53956-116">Exemplo 2: obter um disco do sistema operacional usando uma ID</span><span class="sxs-lookup"><span data-stu-id="53956-116">Example 2: Get an operating system disk by using an ID</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="53956-117">Esse comando obtém o disco do sistema operacional que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="53956-117">This command gets the operating system disk that has the specified ID.</span></span>

### <span data-ttu-id="53956-118">Exemplo 3: obter todos os discos do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="53956-118">Example 3: Get all operating system disks</span></span>
```
PS C:\> Get-WAPackVMOSDisk
```

<span data-ttu-id="53956-119">Este comando obtém todos os discos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="53956-119">This command gets all operating system disks.</span></span>

## <span data-ttu-id="53956-120">OS</span><span class="sxs-lookup"><span data-stu-id="53956-120">PARAMETERS</span></span>

### <span data-ttu-id="53956-121">-ID</span><span class="sxs-lookup"><span data-stu-id="53956-121">-ID</span></span>
<span data-ttu-id="53956-122">Especifica a ID exclusiva de um disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="53956-122">Specifies the unique ID of an operating system disk.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53956-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="53956-123">-Name</span></span>
<span data-ttu-id="53956-124">Especifica o nome de um disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="53956-124">Specifies the name of an operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53956-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="53956-125">-Profile</span></span>
<span data-ttu-id="53956-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="53956-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53956-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="53956-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53956-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53956-128">CommonParameters</span></span>
<span data-ttu-id="53956-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53956-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53956-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53956-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53956-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53956-131">INPUTS</span></span>

## <span data-ttu-id="53956-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53956-132">OUTPUTS</span></span>

## <span data-ttu-id="53956-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53956-133">NOTES</span></span>

## <span data-ttu-id="53956-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53956-134">RELATED LINKS</span></span>

[<span data-ttu-id="53956-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="53956-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


