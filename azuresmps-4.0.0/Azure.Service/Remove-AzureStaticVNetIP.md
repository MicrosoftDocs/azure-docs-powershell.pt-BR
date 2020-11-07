---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 94D20309-5F72-4BE5-A150-2D6DD754286A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a9d793bb9bc8d96150b812474bed9f8997adbe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946104"
---
# <span data-ttu-id="f64a2-101">Remove-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="f64a2-101">Remove-AzureStaticVNetIP</span></span>

## <span data-ttu-id="f64a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f64a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f64a2-103">Remove as informações de endereço IP de rede virtual estática de um objeto de máquina virtual, se houver.</span><span class="sxs-lookup"><span data-stu-id="f64a2-103">Removes the static virtual network IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="f64a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f64a2-104">SYNTAX</span></span>

```
Remove-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f64a2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f64a2-105">DESCRIPTION</span></span>
<span data-ttu-id="f64a2-106">O cmdlet **Remove-AzureStaticVNetIP** remove as informações de endereço IP de rede virtual estática (VNet) de um objeto de máquina virtual, se houver.</span><span class="sxs-lookup"><span data-stu-id="f64a2-106">The **Remove-AzureStaticVNetIP** cmdlet removes the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="f64a2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f64a2-107">EXAMPLES</span></span>

### <span data-ttu-id="f64a2-108">1:</span><span class="sxs-lookup"><span data-stu-id="f64a2-108">1:</span></span>
```

```

## <span data-ttu-id="f64a2-109">OS</span><span class="sxs-lookup"><span data-stu-id="f64a2-109">PARAMETERS</span></span>

### <span data-ttu-id="f64a2-110">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f64a2-110">-InformationAction</span></span>
<span data-ttu-id="f64a2-111">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="f64a2-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f64a2-112">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f64a2-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f64a2-113">Contínuo</span><span class="sxs-lookup"><span data-stu-id="f64a2-113">Continue</span></span>
- <span data-ttu-id="f64a2-114">Ignorar</span><span class="sxs-lookup"><span data-stu-id="f64a2-114">Ignore</span></span>
- <span data-ttu-id="f64a2-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="f64a2-115">Inquire</span></span>
- <span data-ttu-id="f64a2-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f64a2-116">SilentlyContinue</span></span>
- <span data-ttu-id="f64a2-117">Finaliza</span><span class="sxs-lookup"><span data-stu-id="f64a2-117">Stop</span></span>
- <span data-ttu-id="f64a2-118">Suspensão</span><span class="sxs-lookup"><span data-stu-id="f64a2-118">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64a2-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f64a2-119">-InformationVariable</span></span>
<span data-ttu-id="f64a2-120">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="f64a2-120">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64a2-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f64a2-121">-Profile</span></span>
<span data-ttu-id="f64a2-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f64a2-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f64a2-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f64a2-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f64a2-124">-VM</span><span class="sxs-lookup"><span data-stu-id="f64a2-124">-VM</span></span>
<span data-ttu-id="f64a2-125">Especifica um objeto de máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="f64a2-125">Specifies a persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f64a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f64a2-126">CommonParameters</span></span>
<span data-ttu-id="f64a2-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f64a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f64a2-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f64a2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f64a2-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f64a2-129">INPUTS</span></span>

## <span data-ttu-id="f64a2-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f64a2-130">OUTPUTS</span></span>

## <span data-ttu-id="f64a2-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f64a2-131">NOTES</span></span>

## <span data-ttu-id="f64a2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f64a2-132">RELATED LINKS</span></span>

[<span data-ttu-id="f64a2-133">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="f64a2-133">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="f64a2-134">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="f64a2-134">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


