---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C0EEC51F-F8AB-4A6C-8F99-2B2DFFE9BB26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b5f4d5319e705c4f0481edcb5a44a579f4ff01d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945618"
---
# <span data-ttu-id="72f77-101">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="72f77-101">Get-AzureReservedIP</span></span>

## <span data-ttu-id="72f77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72f77-102">SYNOPSIS</span></span>
<span data-ttu-id="72f77-103">Obtém um endereço IP reservado por seu nome ou lista todos os endereços IP reservados na assinatura.</span><span class="sxs-lookup"><span data-stu-id="72f77-103">Gets a reserved IP address by its name or lists all the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="72f77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72f77-104">SYNTAX</span></span>

```
Get-AzureReservedIP [[-ReservedIPName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="72f77-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72f77-105">DESCRIPTION</span></span>
<span data-ttu-id="72f77-106">O cmdlet **Get-AzureReservedIP** Obtém um endereço IP reservado por seu nome ou lista todos os endereços IP reservados na assinatura.</span><span class="sxs-lookup"><span data-stu-id="72f77-106">The **Get-AzureReservedIP** cmdlet gets a reserved IP address by its name or lists all of the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="72f77-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72f77-107">EXAMPLES</span></span>

### <span data-ttu-id="72f77-108">Exemplo 1: obter todos os endereços IP reservados</span><span class="sxs-lookup"><span data-stu-id="72f77-108">Example 1: Get all reserved IP addresses</span></span>
```
PS C:\> Get-AzureReservedIP
```

<span data-ttu-id="72f77-109">Esse comando obtém todos os endereços IP reservados.</span><span class="sxs-lookup"><span data-stu-id="72f77-109">This command gets all reserved IP addresses.</span></span>

### <span data-ttu-id="72f77-110">Exemplo 2: obter um endereço IP reservado com um nome especificado</span><span class="sxs-lookup"><span data-stu-id="72f77-110">Example 2: Get a reserved IP address with a specified name</span></span>
```
PS C:\> Get-AzureReservedIP -ReservedIPName $IpName
```

<span data-ttu-id="72f77-111">Esse comando obtém o endereço IP reservado que tem o nome especificado pela variável $IpName.</span><span class="sxs-lookup"><span data-stu-id="72f77-111">This command gets the reserved IP address that has the name specified by the $IpName variable.</span></span>

## <span data-ttu-id="72f77-112">OS</span><span class="sxs-lookup"><span data-stu-id="72f77-112">PARAMETERS</span></span>

### <span data-ttu-id="72f77-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="72f77-113">-InformationAction</span></span>
<span data-ttu-id="72f77-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="72f77-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="72f77-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="72f77-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="72f77-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="72f77-116">Continue</span></span>
- <span data-ttu-id="72f77-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="72f77-117">Ignore</span></span>
- <span data-ttu-id="72f77-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="72f77-118">Inquire</span></span>
- <span data-ttu-id="72f77-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="72f77-119">SilentlyContinue</span></span>
- <span data-ttu-id="72f77-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="72f77-120">Stop</span></span>
- <span data-ttu-id="72f77-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="72f77-121">Suspend</span></span>

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

### <span data-ttu-id="72f77-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="72f77-122">-InformationVariable</span></span>
<span data-ttu-id="72f77-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="72f77-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="72f77-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="72f77-124">-Profile</span></span>
<span data-ttu-id="72f77-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="72f77-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="72f77-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="72f77-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="72f77-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="72f77-127">-ReservedIPName</span></span>
<span data-ttu-id="72f77-128">Especifica o nome do IP reservado.</span><span class="sxs-lookup"><span data-stu-id="72f77-128">Specifies the reserved IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f77-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f77-129">CommonParameters</span></span>
<span data-ttu-id="72f77-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72f77-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f77-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72f77-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f77-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72f77-132">INPUTS</span></span>

## <span data-ttu-id="72f77-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72f77-133">OUTPUTS</span></span>

## <span data-ttu-id="72f77-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72f77-134">NOTES</span></span>

## <span data-ttu-id="72f77-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72f77-135">RELATED LINKS</span></span>

[<span data-ttu-id="72f77-136">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="72f77-136">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="72f77-137">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="72f77-137">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


