---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947400"
---
# <span data-ttu-id="1081c-101">New-WAPackQuickVM</span><span class="sxs-lookup"><span data-stu-id="1081c-101">New-WAPackQuickVM</span></span>

## <span data-ttu-id="1081c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1081c-102">SYNOPSIS</span></span>
<span data-ttu-id="1081c-103">Cria uma máquina virtual com base em um modelo.</span><span class="sxs-lookup"><span data-stu-id="1081c-103">Creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="1081c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1081c-104">SYNTAX</span></span>

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1081c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1081c-105">DESCRIPTION</span></span>
<span data-ttu-id="1081c-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="1081c-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="1081c-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1081c-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1081c-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1081c-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1081c-109">O cmdlet **New-WAPackQuickVM** cria uma máquina virtual com base em um modelo.</span><span class="sxs-lookup"><span data-stu-id="1081c-109">The **New-WAPackQuickVM** cmdlet creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="1081c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1081c-110">EXAMPLES</span></span>

### <span data-ttu-id="1081c-111">Exemplo 1: criar uma máquina virtual com base em um modelo</span><span class="sxs-lookup"><span data-stu-id="1081c-111">Example 1: Create a virtual machine based on a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

<span data-ttu-id="1081c-112">O primeiro comando cria um objeto **PSCredential** e, em seguida, armazena-o na variável $Credentials.</span><span class="sxs-lookup"><span data-stu-id="1081c-112">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="1081c-113">O cmdlet solicita uma conta e uma senha.</span><span class="sxs-lookup"><span data-stu-id="1081c-113">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="1081c-114">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1081c-114">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="1081c-115">O segundo comando obtém um modelo usando o cmdlet **Get-WAPackVMTemplate** .</span><span class="sxs-lookup"><span data-stu-id="1081c-115">The second command gets a template by using the **Get-WAPackVMTemplate** cmdlet.</span></span>
<span data-ttu-id="1081c-116">O comando especifica a ID de um modelo.</span><span class="sxs-lookup"><span data-stu-id="1081c-116">The command specifies the ID of a template.</span></span>
<span data-ttu-id="1081c-117">O comando armazena o objeto de modelo na variável $TemplateID.</span><span class="sxs-lookup"><span data-stu-id="1081c-117">The command stores the template object in the $TemplateID variable.</span></span>

<span data-ttu-id="1081c-118">O comando final cria uma máquina virtual chamada VirtualMachine023.</span><span class="sxs-lookup"><span data-stu-id="1081c-118">The final command creates a virtual machine named VirtualMachine023.</span></span>
<span data-ttu-id="1081c-119">O comando baseia a máquina virtual no modelo armazenado em $TemplateId.</span><span class="sxs-lookup"><span data-stu-id="1081c-119">The command bases the virtual machine on the template stored in $TemplateId.</span></span>

## <span data-ttu-id="1081c-120">OS</span><span class="sxs-lookup"><span data-stu-id="1081c-120">PARAMETERS</span></span>

### <span data-ttu-id="1081c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1081c-121">-Name</span></span>
<span data-ttu-id="1081c-122">Especifica um nome para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1081c-122">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1081c-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1081c-123">-Profile</span></span>
<span data-ttu-id="1081c-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1081c-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1081c-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1081c-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1081c-126">-Modelo</span><span class="sxs-lookup"><span data-stu-id="1081c-126">-Template</span></span>
<span data-ttu-id="1081c-127">Especifica um modelo.</span><span class="sxs-lookup"><span data-stu-id="1081c-127">Specifies a template.</span></span>
<span data-ttu-id="1081c-128">O cmdlet cria uma máquina virtual com base no modelo que você especificar.</span><span class="sxs-lookup"><span data-stu-id="1081c-128">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="1081c-129">Para obter um objeto de modelo, use o cmdlet **Get-WAPackVMTemplate** .</span><span class="sxs-lookup"><span data-stu-id="1081c-129">To obtain a template object, use the **Get-WAPackVMTemplate** cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1081c-130">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="1081c-130">-VMCredential</span></span>
<span data-ttu-id="1081c-131">Especifica a credencial para a conta de administrador local.</span><span class="sxs-lookup"><span data-stu-id="1081c-131">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="1081c-132">Para obter um objeto **PSCredential** , use o cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="1081c-132">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="1081c-133">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1081c-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1081c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1081c-134">CommonParameters</span></span>
<span data-ttu-id="1081c-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1081c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1081c-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1081c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1081c-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1081c-137">INPUTS</span></span>

## <span data-ttu-id="1081c-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1081c-138">OUTPUTS</span></span>

## <span data-ttu-id="1081c-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1081c-139">NOTES</span></span>

## <span data-ttu-id="1081c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1081c-140">RELATED LINKS</span></span>

[<span data-ttu-id="1081c-141">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="1081c-141">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="1081c-142">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="1081c-142">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)


