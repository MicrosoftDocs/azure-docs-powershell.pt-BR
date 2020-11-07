---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947391"
---
# <span data-ttu-id="b6aec-101">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="b6aec-101">Get-WAPackVMTemplate</span></span>

## <span data-ttu-id="b6aec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6aec-102">SYNOPSIS</span></span>
<span data-ttu-id="b6aec-103">Obtém modelos de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b6aec-103">Gets virtual machine templates.</span></span>

## <span data-ttu-id="b6aec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6aec-104">SYNTAX</span></span>

### <span data-ttu-id="b6aec-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6aec-105">Empty (Default)</span></span>
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b6aec-106">DEID</span><span class="sxs-lookup"><span data-stu-id="b6aec-106">FromId</span></span>
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b6aec-107">FromName</span><span class="sxs-lookup"><span data-stu-id="b6aec-107">FromName</span></span>
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b6aec-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6aec-108">DESCRIPTION</span></span>
<span data-ttu-id="b6aec-109">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="b6aec-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="b6aec-110">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b6aec-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b6aec-111">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b6aec-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b6aec-112">O cmdlet **Get-WAPackVMTemplate** Obtém modelos de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b6aec-112">The **Get-WAPackVMTemplate** cmdlet gets virtual machine templates.</span></span>

## <span data-ttu-id="b6aec-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6aec-113">EXAMPLES</span></span>

### <span data-ttu-id="b6aec-114">Exemplo 1: obter um modelo de máquina virtual usando um nome</span><span class="sxs-lookup"><span data-stu-id="b6aec-114">Example 1: Get a virtual machine template by using a name</span></span>
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

<span data-ttu-id="b6aec-115">Esse comando obtém o modelo de máquina virtual chamado ContosoTemplate04.</span><span class="sxs-lookup"><span data-stu-id="b6aec-115">This command gets the virtual machine template named ContosoTemplate04.</span></span>

### <span data-ttu-id="b6aec-116">Exemplo 2: obter um modelo de máquina virtual usando uma ID</span><span class="sxs-lookup"><span data-stu-id="b6aec-116">Example 2: Get a virtual machine template by using an ID</span></span>
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="b6aec-117">Esse comando obtém o modelo de máquina virtual com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="b6aec-117">This command gets the virtual machine template that has the specified ID.</span></span>

### <span data-ttu-id="b6aec-118">Exemplo 3: obter todos os modelos de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="b6aec-118">Example 3: Get all virtual machine templates</span></span>
```
PS C:\> Get-WAPackVMTemplate
```

<span data-ttu-id="b6aec-119">Esse comando obtém todos os modelos de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b6aec-119">This command gets all the virtual machine templates.</span></span>

## <span data-ttu-id="b6aec-120">OS</span><span class="sxs-lookup"><span data-stu-id="b6aec-120">PARAMETERS</span></span>

### <span data-ttu-id="b6aec-121">-ID</span><span class="sxs-lookup"><span data-stu-id="b6aec-121">-ID</span></span>
<span data-ttu-id="b6aec-122">Especifica a ID exclusiva de um modelo.</span><span class="sxs-lookup"><span data-stu-id="b6aec-122">Specifies the unique ID of a template.</span></span>

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

### <span data-ttu-id="b6aec-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6aec-123">-Name</span></span>
<span data-ttu-id="b6aec-124">Especifica o nome de um modelo.</span><span class="sxs-lookup"><span data-stu-id="b6aec-124">Specifies the name of a template.</span></span>

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

### <span data-ttu-id="b6aec-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b6aec-125">-Profile</span></span>
<span data-ttu-id="b6aec-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b6aec-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6aec-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b6aec-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6aec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6aec-128">CommonParameters</span></span>
<span data-ttu-id="b6aec-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6aec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6aec-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6aec-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6aec-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6aec-131">INPUTS</span></span>

## <span data-ttu-id="b6aec-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6aec-132">OUTPUTS</span></span>

## <span data-ttu-id="b6aec-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6aec-133">NOTES</span></span>

## <span data-ttu-id="b6aec-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6aec-134">RELATED LINKS</span></span>

[<span data-ttu-id="b6aec-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="b6aec-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


