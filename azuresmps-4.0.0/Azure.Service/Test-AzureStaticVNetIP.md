---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E059EF1-740C-4AEB-AF41-BF6003BE15F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: a52f2585771ec10d6acf52b14c88bd1ed0af0427
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945936"
---
# <span data-ttu-id="9a9d3-101">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="9a9d3-101">Test-AzureStaticVNetIP</span></span>

## <span data-ttu-id="9a9d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="9a9d3-103">Testa a disponibilidade de um endereço IP de rede virtual estática e obtém uma lista de sugestões se o endereço consultado não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="9a9d3-103">Tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="9a9d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a9d3-104">SYNTAX</span></span>

```
Test-AzureStaticVNetIP [-VNetName] <String> [-IPAddress] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9a9d3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a9d3-105">DESCRIPTION</span></span>
<span data-ttu-id="9a9d3-106">O cmdlet **Test-AzureStaticVNetIP** testa a disponibilidade de um endereço IP de rede virtual estática e obtém uma lista de sugestões se o endereço consultado não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="9a9d3-106">The **Test-AzureStaticVNetIP** cmdlet tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="9a9d3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a9d3-107">EXAMPLES</span></span>

### <span data-ttu-id="9a9d3-108">1:</span><span class="sxs-lookup"><span data-stu-id="9a9d3-108">1:</span></span>
```

```

## <span data-ttu-id="9a9d3-109">OS</span><span class="sxs-lookup"><span data-stu-id="9a9d3-109">PARAMETERS</span></span>

### <span data-ttu-id="9a9d3-110">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9a9d3-110">-InformationAction</span></span>
<span data-ttu-id="9a9d3-111">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="9a9d3-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9a9d3-112">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9a9d3-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9a9d3-113">Contínuo</span><span class="sxs-lookup"><span data-stu-id="9a9d3-113">Continue</span></span>
- <span data-ttu-id="9a9d3-114">Ignorar</span><span class="sxs-lookup"><span data-stu-id="9a9d3-114">Ignore</span></span>
- <span data-ttu-id="9a9d3-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="9a9d3-115">Inquire</span></span>
- <span data-ttu-id="9a9d3-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9a9d3-116">SilentlyContinue</span></span>
- <span data-ttu-id="9a9d3-117">Finaliza</span><span class="sxs-lookup"><span data-stu-id="9a9d3-117">Stop</span></span>
- <span data-ttu-id="9a9d3-118">Suspensão</span><span class="sxs-lookup"><span data-stu-id="9a9d3-118">Suspend</span></span>

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

### <span data-ttu-id="9a9d3-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9a9d3-119">-InformationVariable</span></span>
<span data-ttu-id="9a9d3-120">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="9a9d3-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9a9d3-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="9a9d3-121">-IPAddress</span></span>
<span data-ttu-id="9a9d3-122">Especifica o endereço IP de rede virtual estática a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="9a9d3-122">Specifies the static virtual network IP address to query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9d3-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9a9d3-123">-Profile</span></span>
<span data-ttu-id="9a9d3-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9a9d3-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9a9d3-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9a9d3-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9a9d3-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="9a9d3-126">-VNetName</span></span>
<span data-ttu-id="9a9d3-127">Especifica o nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9a9d3-127">Specifies the Name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a9d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a9d3-128">CommonParameters</span></span>
<span data-ttu-id="9a9d3-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a9d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a9d3-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a9d3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a9d3-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a9d3-131">INPUTS</span></span>

## <span data-ttu-id="9a9d3-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a9d3-132">OUTPUTS</span></span>

## <span data-ttu-id="9a9d3-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a9d3-133">NOTES</span></span>

## <span data-ttu-id="9a9d3-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a9d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="9a9d3-135">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="9a9d3-135">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="9a9d3-136">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="9a9d3-136">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


