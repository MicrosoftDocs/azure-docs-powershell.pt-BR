---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 761317FE-55FD-4DCC-B997-4F27D041470F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77f58c4f3ee1c440e35c43648f92d21793efddc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946145"
---
# <span data-ttu-id="2da5d-101">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="2da5d-101">Remove-AzureReservedIP</span></span>

## <span data-ttu-id="2da5d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2da5d-102">SYNOPSIS</span></span>
<span data-ttu-id="2da5d-103">Remove um endereço IP reservado de acordo com o nome.</span><span class="sxs-lookup"><span data-stu-id="2da5d-103">Removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="2da5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2da5d-104">SYNTAX</span></span>

```
Remove-AzureReservedIP [-ReservedIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2da5d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2da5d-105">DESCRIPTION</span></span>
<span data-ttu-id="2da5d-106">O cmdlet **Remove-AzureReservedIP** remove um endereço IP reservado pelo nome.</span><span class="sxs-lookup"><span data-stu-id="2da5d-106">The **Remove-AzureReservedIP** cmdlet removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="2da5d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2da5d-107">EXAMPLES</span></span>

### <span data-ttu-id="2da5d-108">Exemplo 1: remover um endereço IP reservado pelo nome</span><span class="sxs-lookup"><span data-stu-id="2da5d-108">Example 1: Remove a reserved IP address by its name</span></span>
```
PS C:\> Remove-AzureReservedIP -ReservedIPName $name
```

<span data-ttu-id="2da5d-109">Esse comando Remove um endereço IP reservado pelo nome.</span><span class="sxs-lookup"><span data-stu-id="2da5d-109">This command removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="2da5d-110">OS</span><span class="sxs-lookup"><span data-stu-id="2da5d-110">PARAMETERS</span></span>

### <span data-ttu-id="2da5d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2da5d-111">-Force</span></span>
<span data-ttu-id="2da5d-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2da5d-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2da5d-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="2da5d-113">-InformationAction</span></span>
<span data-ttu-id="2da5d-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="2da5d-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2da5d-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2da5d-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2da5d-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="2da5d-116">Continue</span></span>
- <span data-ttu-id="2da5d-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="2da5d-117">Ignore</span></span>
- <span data-ttu-id="2da5d-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="2da5d-118">Inquire</span></span>
- <span data-ttu-id="2da5d-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2da5d-119">SilentlyContinue</span></span>
- <span data-ttu-id="2da5d-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="2da5d-120">Stop</span></span>
- <span data-ttu-id="2da5d-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="2da5d-121">Suspend</span></span>

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

### <span data-ttu-id="2da5d-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2da5d-122">-InformationVariable</span></span>
<span data-ttu-id="2da5d-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="2da5d-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2da5d-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="2da5d-124">-Profile</span></span>
<span data-ttu-id="2da5d-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="2da5d-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2da5d-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="2da5d-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2da5d-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="2da5d-127">-ReservedIPName</span></span>
<span data-ttu-id="2da5d-128">Especifica o nome do endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="2da5d-128">Specifies the name of the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da5d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da5d-129">CommonParameters</span></span>
<span data-ttu-id="2da5d-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2da5d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da5d-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2da5d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da5d-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2da5d-132">INPUTS</span></span>

## <span data-ttu-id="2da5d-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2da5d-133">OUTPUTS</span></span>

## <span data-ttu-id="2da5d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2da5d-134">NOTES</span></span>

## <span data-ttu-id="2da5d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2da5d-135">RELATED LINKS</span></span>

[<span data-ttu-id="2da5d-136">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="2da5d-136">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="2da5d-137">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="2da5d-137">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="2da5d-138">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="2da5d-138">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


