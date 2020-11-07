---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7EB9FE4-BDEB-43A5-B6D3-FEAB16BC2711
online version: ''
schema: 2.0.0
ms.openlocfilehash: 388277115281cbbacfb634ebdac5cdd9aa86b709
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947414"
---
# <span data-ttu-id="7cb0c-101">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7cb0c-101">Get-WAPackVMRole</span></span>

## <span data-ttu-id="7cb0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7cb0c-102">SYNOPSIS</span></span>

## <span data-ttu-id="7cb0c-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cb0c-103">SYNTAX</span></span>

### <span data-ttu-id="7cb0c-104">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="7cb0c-104">Empty (Default)</span></span>
```
Get-WAPackVMRole [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7cb0c-105">FromName</span><span class="sxs-lookup"><span data-stu-id="7cb0c-105">FromName</span></span>
```
Get-WAPackVMRole -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7cb0c-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="7cb0c-106">FromCloudService</span></span>
```
Get-WAPackVMRole -Name <String> -CloudServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7cb0c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7cb0c-107">DESCRIPTION</span></span>
<span data-ttu-id="7cb0c-108">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7cb0c-109">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7cb0c-110">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7cb0c-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="7cb0c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cb0c-111">EXAMPLES</span></span>

### <span data-ttu-id="7cb0c-112">Exemplo 1: obter uma função de máquina virtual (criada por meio do Portal)</span><span class="sxs-lookup"><span data-stu-id="7cb0c-112">Example 1: Get a virtual machine role (created through the portal)</span></span>
```
PS C:\> Get-WAPackVMRole -Name "ContosoVMRole01"
```

<span data-ttu-id="7cb0c-113">Esse comando obtém uma função de máquina virtual que foi criada por meio do portal chamado ContosoVMRole01.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-113">This command gets a virtual machine role which has been created through the portal named ContosoVMRole01.</span></span>

### <span data-ttu-id="7cb0c-114">Exemplo 2: obter uma função de máquina virtual usando um nome e um nome de serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="7cb0c-114">Example 2: Get a virtual machine role by using a name and a cloud service name</span></span>
```
PS C:\> Get-WAPackVMRole -CloudServiceName "ContosoCloudService01" -Name "ContosoVMRole02"
```

<span data-ttu-id="7cb0c-115">Esse comando obtém uma função de máquina virtual chamada ContosoVMRole02 que representa um serviço de nuvem chamado ContosoCloudService01.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-115">This command gets a virtual machine role named ContosoVMRole02 which stand on a cloud service named ContosoCloudService01.</span></span>

### <span data-ttu-id="7cb0c-116">Exemplo 3: obter toda a função da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7cb0c-116">Example 3: Get all virtual machine role</span></span>
```
PS C:\> Get-WAPackVMRole
```

<span data-ttu-id="7cb0c-117">Este comando obtém toda a função de máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-117">This command gets all existing virtual machine role.</span></span>

## <span data-ttu-id="7cb0c-118">OS</span><span class="sxs-lookup"><span data-stu-id="7cb0c-118">PARAMETERS</span></span>

### <span data-ttu-id="7cb0c-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="7cb0c-119">-CloudServiceName</span></span>
<span data-ttu-id="7cb0c-120">Especifica o nome do serviço em nuvem da função da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-120">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cb0c-121">-Name</span></span>
<span data-ttu-id="7cb0c-122">Especifica o nome de uma função de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-122">Specifies the name of a virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromName, FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb0c-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7cb0c-123">-Profile</span></span>
<span data-ttu-id="7cb0c-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7cb0c-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7cb0c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb0c-126">CommonParameters</span></span>
<span data-ttu-id="7cb0c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb0c-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cb0c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb0c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7cb0c-129">INPUTS</span></span>

## <span data-ttu-id="7cb0c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7cb0c-130">OUTPUTS</span></span>

## <span data-ttu-id="7cb0c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7cb0c-131">NOTES</span></span>

## <span data-ttu-id="7cb0c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cb0c-132">RELATED LINKS</span></span>

[<span data-ttu-id="7cb0c-133">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7cb0c-133">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="7cb0c-134">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7cb0c-134">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="7cb0c-135">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7cb0c-135">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


