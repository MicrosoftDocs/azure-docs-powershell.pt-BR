---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6617AA59-CDD1-4BA9-84A7-F3914BF1D4B7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14e201dc916f15b63b0e825f4ca2e37015aaa9bc
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947390"
---
# <span data-ttu-id="1fad1-101">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="1fad1-101">New-WAPackVMRole</span></span>

## <span data-ttu-id="1fad1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fad1-102">SYNOPSIS</span></span>
<span data-ttu-id="1fad1-103">Cria uma função de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1fad1-103">Creates a virtual machine role.</span></span>

## <span data-ttu-id="1fad1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fad1-104">SYNTAX</span></span>

### <span data-ttu-id="1fad1-105">QuickCreate (padrão)</span><span class="sxs-lookup"><span data-stu-id="1fad1-105">QuickCreate (Default)</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1fad1-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="1fad1-106">FromCloudService</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 -CloudService <CloudService> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1fad1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fad1-107">DESCRIPTION</span></span>
<span data-ttu-id="1fad1-108">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="1fad1-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="1fad1-109">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1fad1-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1fad1-110">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1fad1-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1fad1-111">O cmdlet **New-WAPackVMRole** cria uma função de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1fad1-111">The **New-WAPackVMRole** cmdlet creates a virtual machine role.</span></span>

## <span data-ttu-id="1fad1-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fad1-112">EXAMPLES</span></span>

### <span data-ttu-id="1fad1-113">Exemplo 1: criar uma função de máquina virtual (comportamento de emulação de WAP)</span><span class="sxs-lookup"><span data-stu-id="1fad1-113">Example 1: Create a virtual machine role (emulating WAP behavior)</span></span>
```
PS C:\> New-WAPackVMRole -Name "ContosoVMRole01" -Label "ContosoVMRoleLabel01" -ResourceDefinition $resdef
```

<span data-ttu-id="1fad1-114">Como não especificamos qualquer serviço na nuvem (comportamento de emulação de WAP), o comando criará um serviço na nuvem para nós que terá o mesmo nome que a função da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1fad1-114">Since we do not specify any cloud service (emulating WAP behavior), the command will create a cloud service for us which will have the same name as the virtual machine role.</span></span>
<span data-ttu-id="1fad1-115">Nesse caso, o comando a seguir criará uma função de máquina virtual com o nome ContosoVMRole01, Label ContosoVMRoleLabel01.</span><span class="sxs-lookup"><span data-stu-id="1fad1-115">In this case, the following command will create a virtual machine role with the name ContosoVMRole01, label ContosoVMRoleLabel01.</span></span>
<span data-ttu-id="1fad1-116">Observe que a definição do recurso que está sendo usado aqui deve ser criada manualmente, embora o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1fad1-116">Note that the resource definition being used here has to be manually created though PowerShell.</span></span>

## <span data-ttu-id="1fad1-117">OS</span><span class="sxs-lookup"><span data-stu-id="1fad1-117">PARAMETERS</span></span>

### <span data-ttu-id="1fad1-118">-CloudService</span><span class="sxs-lookup"><span data-stu-id="1fad1-118">-CloudService</span></span>
<span data-ttu-id="1fad1-119">Especifica um serviço na nuvem para a função de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1fad1-119">Specifies a cloud service for the virtual machine role.</span></span>

```yaml
Type: CloudService
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fad1-120">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="1fad1-120">-Label</span></span>
<span data-ttu-id="1fad1-121">Especifica um rótulo para a função de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1fad1-121">Specifies a label for the virtual machine role.</span></span>

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

### <span data-ttu-id="1fad1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fad1-122">-Name</span></span>
<span data-ttu-id="1fad1-123">Especifica um nome para a função da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1fad1-123">Specifies a name for the virtual machine role.</span></span>

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

### <span data-ttu-id="1fad1-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1fad1-124">-Profile</span></span>
<span data-ttu-id="1fad1-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1fad1-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1fad1-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1fad1-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1fad1-127">-ResourceDefinition</span><span class="sxs-lookup"><span data-stu-id="1fad1-127">-ResourceDefinition</span></span>
<span data-ttu-id="1fad1-128">Especifica uma definição de recurso para a função de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1fad1-128">Specifies a resource definition for the virtual machine role.</span></span>

```yaml
Type: VMRoleResourceDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fad1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fad1-129">CommonParameters</span></span>
<span data-ttu-id="1fad1-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fad1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fad1-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fad1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fad1-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fad1-132">INPUTS</span></span>

## <span data-ttu-id="1fad1-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fad1-133">OUTPUTS</span></span>

## <span data-ttu-id="1fad1-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fad1-134">NOTES</span></span>

## <span data-ttu-id="1fad1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fad1-135">RELATED LINKS</span></span>

[<span data-ttu-id="1fad1-136">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="1fad1-136">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="1fad1-137">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="1fad1-137">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="1fad1-138">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="1fad1-138">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


