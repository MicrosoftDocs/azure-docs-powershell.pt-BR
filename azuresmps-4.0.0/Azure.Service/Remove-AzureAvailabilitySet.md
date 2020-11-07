---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F956CC89-A2CA-4D73-8014-C36778C51927
online version: ''
schema: 2.0.0
ms.openlocfilehash: eba992b183795d016108419834c38bcf64a82d41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946168"
---
# <span data-ttu-id="0ab48-101">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0ab48-101">Remove-AzureAvailabilitySet</span></span>

## <span data-ttu-id="0ab48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ab48-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab48-103">Remove um conjunto de disponibilidade de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab48-103">Removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="0ab48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ab48-104">SYNTAX</span></span>

```
Remove-AzureAvailabilitySet -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0ab48-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0ab48-105">DESCRIPTION</span></span>
<span data-ttu-id="0ab48-106">O cmdlet **Remove-AzureAvailabilitySet** remove um conjunto de disponibilidade de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab48-106">The **Remove-AzureAvailabilitySet** cmdlet removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="0ab48-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ab48-107">EXAMPLES</span></span>

### <span data-ttu-id="0ab48-108">1:</span><span class="sxs-lookup"><span data-stu-id="0ab48-108">1:</span></span>
```

```

## <span data-ttu-id="0ab48-109">OS</span><span class="sxs-lookup"><span data-stu-id="0ab48-109">PARAMETERS</span></span>

### <span data-ttu-id="0ab48-110">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="0ab48-110">-InformationAction</span></span>
<span data-ttu-id="0ab48-111">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="0ab48-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0ab48-112">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0ab48-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ab48-113">Contínuo</span><span class="sxs-lookup"><span data-stu-id="0ab48-113">Continue</span></span>
- <span data-ttu-id="0ab48-114">Ignorar</span><span class="sxs-lookup"><span data-stu-id="0ab48-114">Ignore</span></span>
- <span data-ttu-id="0ab48-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="0ab48-115">Inquire</span></span>
- <span data-ttu-id="0ab48-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0ab48-116">SilentlyContinue</span></span>
- <span data-ttu-id="0ab48-117">Finaliza</span><span class="sxs-lookup"><span data-stu-id="0ab48-117">Stop</span></span>
- <span data-ttu-id="0ab48-118">Suspensão</span><span class="sxs-lookup"><span data-stu-id="0ab48-118">Suspend</span></span>

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

### <span data-ttu-id="0ab48-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0ab48-119">-InformationVariable</span></span>
<span data-ttu-id="0ab48-120">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="0ab48-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0ab48-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="0ab48-121">-Profile</span></span>
<span data-ttu-id="0ab48-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="0ab48-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ab48-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="0ab48-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0ab48-124">-VM</span><span class="sxs-lookup"><span data-stu-id="0ab48-124">-VM</span></span>
<span data-ttu-id="0ab48-125">Especifica a máquina virtual a partir da qual esse cmdlet Remove um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="0ab48-125">Specifies the virtual machine from which this cmdlet removes an availability set.</span></span>

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

### <span data-ttu-id="0ab48-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab48-126">CommonParameters</span></span>
<span data-ttu-id="0ab48-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab48-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab48-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab48-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab48-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0ab48-129">INPUTS</span></span>

## <span data-ttu-id="0ab48-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0ab48-130">OUTPUTS</span></span>

## <span data-ttu-id="0ab48-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0ab48-131">NOTES</span></span>

## <span data-ttu-id="0ab48-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ab48-132">RELATED LINKS</span></span>

[<span data-ttu-id="0ab48-133">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0ab48-133">Set-AzureAvailabilitySet</span></span>](./Set-AzureAvailabilitySet.md)


