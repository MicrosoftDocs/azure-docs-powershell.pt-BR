---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D51BE56-C0A2-4A32-BB7F-8FA9CC67F8F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 986d4998119c4ede1780fa35ad6baadce4574a81
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947354"
---
# <span data-ttu-id="2ccec-101">Get-WAPackLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="2ccec-101">Get-WAPackLogicalNetwork</span></span>

## <span data-ttu-id="2ccec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ccec-102">SYNOPSIS</span></span>
<span data-ttu-id="2ccec-103">Obtém objetos lógicos da rede.</span><span class="sxs-lookup"><span data-stu-id="2ccec-103">Gets logical network objects.</span></span>

## <span data-ttu-id="2ccec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ccec-104">SYNTAX</span></span>

### <span data-ttu-id="2ccec-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="2ccec-105">Empty (Default)</span></span>
```
Get-WAPackLogicalNetwork [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2ccec-106">FromName</span><span class="sxs-lookup"><span data-stu-id="2ccec-106">FromName</span></span>
```
Get-WAPackLogicalNetwork [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2ccec-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ccec-107">DESCRIPTION</span></span>
<span data-ttu-id="2ccec-108">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="2ccec-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="2ccec-109">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ccec-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2ccec-110">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2ccec-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2ccec-111">O cmdlet **Get-WAPackLogicalNetwork** obtém objetos lógicos de rede.</span><span class="sxs-lookup"><span data-stu-id="2ccec-111">The **Get-WAPackLogicalNetwork** cmdlet gets logical network objects.</span></span>

## <span data-ttu-id="2ccec-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ccec-112">EXAMPLES</span></span>

### <span data-ttu-id="2ccec-113">Exemplo 1: obter uma rede lógica usando um nome</span><span class="sxs-lookup"><span data-stu-id="2ccec-113">Example 1: Get a logical network by using a name</span></span>
```
PS C:\> Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
```

<span data-ttu-id="2ccec-114">Esse comando obtém uma rede lógica chamada ContosoLogicalNetwork01.</span><span class="sxs-lookup"><span data-stu-id="2ccec-114">This command gets a logical network named ContosoLogicalNetwork01.</span></span>

### <span data-ttu-id="2ccec-115">Exemplo 2: obter todas as redes lógicas</span><span class="sxs-lookup"><span data-stu-id="2ccec-115">Example 2: Get all logical networks</span></span>
```
PS C:\> Get-WAPackLogicalNetwork
```

<span data-ttu-id="2ccec-116">Esse comando obtém todas as redes lógicas.</span><span class="sxs-lookup"><span data-stu-id="2ccec-116">This command gets all logical networks.</span></span>

## <span data-ttu-id="2ccec-117">OS</span><span class="sxs-lookup"><span data-stu-id="2ccec-117">PARAMETERS</span></span>

### <span data-ttu-id="2ccec-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ccec-118">-Name</span></span>
<span data-ttu-id="2ccec-119">Especifica o nome de uma rede lógica.</span><span class="sxs-lookup"><span data-stu-id="2ccec-119">Specifies the name of a logical network.</span></span>

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

### <span data-ttu-id="2ccec-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="2ccec-120">-Profile</span></span>
<span data-ttu-id="2ccec-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="2ccec-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ccec-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="2ccec-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ccec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ccec-123">CommonParameters</span></span>
<span data-ttu-id="2ccec-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ccec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ccec-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ccec-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ccec-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ccec-126">INPUTS</span></span>

## <span data-ttu-id="2ccec-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ccec-127">OUTPUTS</span></span>

## <span data-ttu-id="2ccec-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ccec-128">NOTES</span></span>

## <span data-ttu-id="2ccec-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ccec-129">RELATED LINKS</span></span>

