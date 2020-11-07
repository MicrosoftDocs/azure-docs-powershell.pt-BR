---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 047C5FBD-CB0D-47BF-AE03-4DF32B4FAD87
online version: ''
schema: 2.0.0
ms.openlocfilehash: a546c9fdb066aaf1203055fd62d8eb01258569c8
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947356"
---
# <span data-ttu-id="228ab-101">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="228ab-101">Get-WAPackVM</span></span>

## <span data-ttu-id="228ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="228ab-102">SYNOPSIS</span></span>
<span data-ttu-id="228ab-103">Obtém objetos de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="228ab-103">Gets virtual machine objects.</span></span>

## <span data-ttu-id="228ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="228ab-104">SYNTAX</span></span>

### <span data-ttu-id="228ab-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="228ab-105">Empty (Default)</span></span>
```
Get-WAPackVM [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="228ab-106">FromName</span><span class="sxs-lookup"><span data-stu-id="228ab-106">FromName</span></span>
```
Get-WAPackVM [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="228ab-107">DEID</span><span class="sxs-lookup"><span data-stu-id="228ab-107">FromId</span></span>
```
Get-WAPackVM [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="228ab-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="228ab-108">DESCRIPTION</span></span>
<span data-ttu-id="228ab-109">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="228ab-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="228ab-110">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="228ab-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="228ab-111">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="228ab-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="228ab-112">O cmdlet **Get-WAPackVM** obtém objetos de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="228ab-112">The **Get-WAPackVM** cmdlet gets virtual machine objects.</span></span>

## <span data-ttu-id="228ab-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="228ab-113">EXAMPLES</span></span>

### <span data-ttu-id="228ab-114">Exemplo 1: obter uma máquina virtual usando um nome</span><span class="sxs-lookup"><span data-stu-id="228ab-114">Example 1: Get a virtual machine by using a name</span></span>
```
PS C:\> Get-WAPackVM -Name "ContosoV126"
```

<span data-ttu-id="228ab-115">Esse comando obtém a máquina virtual chamada ContosoV126.</span><span class="sxs-lookup"><span data-stu-id="228ab-115">This command gets the virtual machine named ContosoV126.</span></span>

### <span data-ttu-id="228ab-116">Exemplo 2: obter uma máquina virtual usando uma ID</span><span class="sxs-lookup"><span data-stu-id="228ab-116">Example 2: Get a virtual machine by using an ID</span></span>
```
PS C:\> Get-WAPackVM -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="228ab-117">Este comando obtém a máquina virtual com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="228ab-117">This command gets the virtual machine that has the specified ID.</span></span>

### <span data-ttu-id="228ab-118">Exemplo 3: obter todas as máquinas virtuais</span><span class="sxs-lookup"><span data-stu-id="228ab-118">Example 3: Get all virtual machines</span></span>
```
PS C:\> Get-WAPackVM
```

<span data-ttu-id="228ab-119">Este comando obtém todas as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="228ab-119">This command gets all virtual machines.</span></span>

## <span data-ttu-id="228ab-120">OS</span><span class="sxs-lookup"><span data-stu-id="228ab-120">PARAMETERS</span></span>

### <span data-ttu-id="228ab-121">-ID</span><span class="sxs-lookup"><span data-stu-id="228ab-121">-ID</span></span>
<span data-ttu-id="228ab-122">Especifica a ID exclusiva de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="228ab-122">Specifies the unique ID of a virtual machine.</span></span>

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

### <span data-ttu-id="228ab-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="228ab-123">-Name</span></span>
<span data-ttu-id="228ab-124">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="228ab-124">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="228ab-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="228ab-125">-Profile</span></span>
<span data-ttu-id="228ab-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="228ab-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="228ab-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="228ab-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="228ab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="228ab-128">CommonParameters</span></span>
<span data-ttu-id="228ab-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="228ab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="228ab-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="228ab-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="228ab-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="228ab-131">INPUTS</span></span>

## <span data-ttu-id="228ab-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="228ab-132">OUTPUTS</span></span>

## <span data-ttu-id="228ab-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="228ab-133">NOTES</span></span>

## <span data-ttu-id="228ab-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="228ab-134">RELATED LINKS</span></span>

[<span data-ttu-id="228ab-135">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="228ab-135">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="228ab-136">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="228ab-136">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="228ab-137">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="228ab-137">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="228ab-138">Currículo-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="228ab-138">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="228ab-139">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="228ab-139">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="228ab-140">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="228ab-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="228ab-141">Parar-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="228ab-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="228ab-142">Suspender-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="228ab-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="228ab-143">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="228ab-143">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


