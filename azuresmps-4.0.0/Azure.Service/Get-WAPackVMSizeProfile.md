---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947430"
---
# <span data-ttu-id="51c2e-101">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="51c2e-101">Get-WAPackVMSizeProfile</span></span>

## <span data-ttu-id="51c2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="51c2e-103">Obtém objetos de perfil de tamanho.</span><span class="sxs-lookup"><span data-stu-id="51c2e-103">Gets size profile objects.</span></span>

## <span data-ttu-id="51c2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51c2e-104">SYNTAX</span></span>

### <span data-ttu-id="51c2e-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="51c2e-105">Empty (Default)</span></span>
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="51c2e-106">DEID</span><span class="sxs-lookup"><span data-stu-id="51c2e-106">FromId</span></span>
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="51c2e-107">FromName</span><span class="sxs-lookup"><span data-stu-id="51c2e-107">FromName</span></span>
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="51c2e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51c2e-108">DESCRIPTION</span></span>
<span data-ttu-id="51c2e-109">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="51c2e-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="51c2e-110">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="51c2e-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="51c2e-111">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="51c2e-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="51c2e-112">O cmdlet **Get-WAPackVMSizeProfile** tem o tamanho dos objetos de perfil para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="51c2e-112">The **Get-WAPackVMSizeProfile** cmdlet gets size profile objects for virtual machines.</span></span>

## <span data-ttu-id="51c2e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51c2e-113">EXAMPLES</span></span>

### <span data-ttu-id="51c2e-114">Exemplo 1: obter um perfil de tamanho usando um nome</span><span class="sxs-lookup"><span data-stu-id="51c2e-114">Example 1: Get a size profile by using a name</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

<span data-ttu-id="51c2e-115">Esse comando obtém o perfil de tamanho chamado ContosoSizeProfile07.</span><span class="sxs-lookup"><span data-stu-id="51c2e-115">This command gets the size profile named ContosoSizeProfile07.</span></span>

### <span data-ttu-id="51c2e-116">Exemplo 2: obter um perfil de tamanho usando uma ID</span><span class="sxs-lookup"><span data-stu-id="51c2e-116">Example 2: Get a size profile by using an ID</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="51c2e-117">Esse comando obtém o perfil de tamanho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="51c2e-117">This command gets the size profile that has the specified ID.</span></span>

### <span data-ttu-id="51c2e-118">Exemplo 3: obter todos os perfis de tamanho</span><span class="sxs-lookup"><span data-stu-id="51c2e-118">Example 3: Get all size profiles</span></span>
```
PS C:\> Get-WAPackVMSizeProfile
```

<span data-ttu-id="51c2e-119">Esse comando obtém todos os perfis de tamanho.</span><span class="sxs-lookup"><span data-stu-id="51c2e-119">This command gets all the size profiles.</span></span>

## <span data-ttu-id="51c2e-120">OS</span><span class="sxs-lookup"><span data-stu-id="51c2e-120">PARAMETERS</span></span>

### <span data-ttu-id="51c2e-121">-ID</span><span class="sxs-lookup"><span data-stu-id="51c2e-121">-ID</span></span>
<span data-ttu-id="51c2e-122">Especifica a ID exclusiva de um perfil de tamanho.</span><span class="sxs-lookup"><span data-stu-id="51c2e-122">Specifies the unique ID of a size profile.</span></span>

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

### <span data-ttu-id="51c2e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="51c2e-123">-Name</span></span>
<span data-ttu-id="51c2e-124">Especifica o nome de um perfil de tamanho.</span><span class="sxs-lookup"><span data-stu-id="51c2e-124">Specifies the name of a size profile.</span></span>

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

### <span data-ttu-id="51c2e-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="51c2e-125">-Profile</span></span>
<span data-ttu-id="51c2e-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="51c2e-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51c2e-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="51c2e-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51c2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c2e-128">CommonParameters</span></span>
<span data-ttu-id="51c2e-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51c2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c2e-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51c2e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c2e-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51c2e-131">INPUTS</span></span>

## <span data-ttu-id="51c2e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51c2e-132">OUTPUTS</span></span>

## <span data-ttu-id="51c2e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51c2e-133">NOTES</span></span>

## <span data-ttu-id="51c2e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51c2e-134">RELATED LINKS</span></span>

[<span data-ttu-id="51c2e-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="51c2e-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


