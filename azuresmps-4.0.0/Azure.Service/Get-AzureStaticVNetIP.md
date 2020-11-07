---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 12BF47AA-9E82-425E-A1EB-BAD64D800943
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3be6496993ed6de248103b9a222df4cbe15ed2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946557"
---
# <span data-ttu-id="74599-101">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="74599-101">Get-AzureStaticVNetIP</span></span>

## <span data-ttu-id="74599-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74599-102">SYNOPSIS</span></span>
<span data-ttu-id="74599-103">Obtém as informações de endereço IP da VNet estático de um objeto de máquina virtual, se houver.</span><span class="sxs-lookup"><span data-stu-id="74599-103">Gets the static VNet IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="74599-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74599-104">SYNTAX</span></span>

```
Get-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="74599-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74599-105">DESCRIPTION</span></span>
<span data-ttu-id="74599-106">O cmdlet **Get-AzureStaticVNetIP** Obtém as informações de endereço IP de rede virtual estática (VNet) de um objeto de máquina virtual, se houver.</span><span class="sxs-lookup"><span data-stu-id="74599-106">The **Get-AzureStaticVNetIP** cmdlet gets the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="74599-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74599-107">EXAMPLES</span></span>

### <span data-ttu-id="74599-108">1:</span><span class="sxs-lookup"><span data-stu-id="74599-108">1:</span></span>
```

```

## <span data-ttu-id="74599-109">OS</span><span class="sxs-lookup"><span data-stu-id="74599-109">PARAMETERS</span></span>

### <span data-ttu-id="74599-110">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="74599-110">-InformationAction</span></span>
<span data-ttu-id="74599-111">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="74599-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="74599-112">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="74599-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="74599-113">Contínuo</span><span class="sxs-lookup"><span data-stu-id="74599-113">Continue</span></span>
- <span data-ttu-id="74599-114">Ignorar</span><span class="sxs-lookup"><span data-stu-id="74599-114">Ignore</span></span>
- <span data-ttu-id="74599-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="74599-115">Inquire</span></span>
- <span data-ttu-id="74599-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="74599-116">SilentlyContinue</span></span>
- <span data-ttu-id="74599-117">Finaliza</span><span class="sxs-lookup"><span data-stu-id="74599-117">Stop</span></span>
- <span data-ttu-id="74599-118">Suspensão</span><span class="sxs-lookup"><span data-stu-id="74599-118">Suspend</span></span>

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

### <span data-ttu-id="74599-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="74599-119">-InformationVariable</span></span>
<span data-ttu-id="74599-120">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="74599-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="74599-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="74599-121">-Profile</span></span>
<span data-ttu-id="74599-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="74599-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="74599-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="74599-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="74599-124">-VM</span><span class="sxs-lookup"><span data-stu-id="74599-124">-VM</span></span>
<span data-ttu-id="74599-125">Especifica um objeto de máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="74599-125">Specifies a persistent virtual machine object.</span></span>

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

### <span data-ttu-id="74599-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74599-126">CommonParameters</span></span>
<span data-ttu-id="74599-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74599-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74599-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74599-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74599-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74599-129">INPUTS</span></span>

## <span data-ttu-id="74599-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74599-130">OUTPUTS</span></span>

## <span data-ttu-id="74599-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74599-131">NOTES</span></span>

## <span data-ttu-id="74599-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74599-132">RELATED LINKS</span></span>

[<span data-ttu-id="74599-133">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="74599-133">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


