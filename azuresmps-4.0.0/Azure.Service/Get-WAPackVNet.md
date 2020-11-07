---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 947D1C09-7CFA-4E97-A6B3-2DA9D7507F0C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0260b452c96b5f6dd60599b5da15cc323b5423d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946263"
---
# <span data-ttu-id="b3cc5-101">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="b3cc5-101">Get-WAPackVNet</span></span>

## <span data-ttu-id="b3cc5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="b3cc5-103">Obtém redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-103">Gets virtual networks.</span></span>

## <span data-ttu-id="b3cc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3cc5-104">SYNTAX</span></span>

### <span data-ttu-id="b3cc5-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="b3cc5-105">Empty (Default)</span></span>
```
Get-WAPackVNet [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b3cc5-106">DEID</span><span class="sxs-lookup"><span data-stu-id="b3cc5-106">FromId</span></span>
```
Get-WAPackVNet -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b3cc5-107">FromName</span><span class="sxs-lookup"><span data-stu-id="b3cc5-107">FromName</span></span>
```
Get-WAPackVNet -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b3cc5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3cc5-108">DESCRIPTION</span></span>
<span data-ttu-id="b3cc5-109">O cmdlet **Get-WAPackVNet** Obtém redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-109">The **Get-WAPackVNet** cmdlet gets virtual networks.</span></span>

## <span data-ttu-id="b3cc5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3cc5-110">EXAMPLES</span></span>

### <span data-ttu-id="b3cc5-111">Exemplo 1: obter todas as redes virtuais</span><span class="sxs-lookup"><span data-stu-id="b3cc5-111">Example 1: Get all virtual networks</span></span>
```
PS C:\> Get-WAPackVNet
```

<span data-ttu-id="b3cc5-112">Esse comando obtém todas as redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-112">This command gets all virtual networks.</span></span>

### <span data-ttu-id="b3cc5-113">Exemplo 2: obter uma rede virtual usando uma ID</span><span class="sxs-lookup"><span data-stu-id="b3cc5-113">Example 2: Get a virtual network by using an ID</span></span>
```
PS C:\> Get-WAPackVNet -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="b3cc5-114">Este comando obtém a rede virtual com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-114">This command gets the virtual network that has the specified ID.</span></span>

### <span data-ttu-id="b3cc5-115">Exemplo 3: obter uma rede virtual usando um nome</span><span class="sxs-lookup"><span data-stu-id="b3cc5-115">Example 3: Get a virtual network by using a name</span></span>
```
PS C:\> Get-WAPackVNet -Name "ContosoVNet08"
```

<span data-ttu-id="b3cc5-116">Esse comando obtém a rede virtual chamada ContosoVNet08.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-116">This command gets the virtual network named ContosoVNet08.</span></span>

## <span data-ttu-id="b3cc5-117">OS</span><span class="sxs-lookup"><span data-stu-id="b3cc5-117">PARAMETERS</span></span>

### <span data-ttu-id="b3cc5-118">-ID</span><span class="sxs-lookup"><span data-stu-id="b3cc5-118">-ID</span></span>
<span data-ttu-id="b3cc5-119">Especifica a ID exclusiva de uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-119">Specifies the unique ID of a virtual network.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3cc5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3cc5-120">-Name</span></span>
<span data-ttu-id="b3cc5-121">Especifica o nome de uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-121">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3cc5-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b3cc5-122">-Profile</span></span>
<span data-ttu-id="b3cc5-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b3cc5-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b3cc5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3cc5-125">CommonParameters</span></span>
<span data-ttu-id="b3cc5-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3cc5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3cc5-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3cc5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3cc5-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3cc5-128">INPUTS</span></span>

## <span data-ttu-id="b3cc5-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3cc5-129">OUTPUTS</span></span>

## <span data-ttu-id="b3cc5-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3cc5-130">NOTES</span></span>

## <span data-ttu-id="b3cc5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3cc5-131">RELATED LINKS</span></span>

