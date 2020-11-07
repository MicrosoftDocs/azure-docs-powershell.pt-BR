---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945924"
---
# <span data-ttu-id="61230-101">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="61230-101">New-AzureDns</span></span>

## <span data-ttu-id="61230-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61230-102">SYNOPSIS</span></span>
<span data-ttu-id="61230-103">Cria um objeto de configurações de DNS do Azure.</span><span class="sxs-lookup"><span data-stu-id="61230-103">Creates an Azure DNS settings object.</span></span>

## <span data-ttu-id="61230-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61230-104">SYNTAX</span></span>

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="61230-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61230-105">DESCRIPTION</span></span>
<span data-ttu-id="61230-106">O cmdlet **New-AzureDns** cria um objeto de configurações de DNS do Azure.</span><span class="sxs-lookup"><span data-stu-id="61230-106">The **New-AzureDns** cmdlet creates an Azure DNS settings object.</span></span>
<span data-ttu-id="61230-107">Você pode usar um objeto de configurações de DNS ao criar uma máquina virtual usando o cmdlet **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="61230-107">You can use a DNS settings object when you create a virtual machine by using the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="61230-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61230-108">EXAMPLES</span></span>

### <span data-ttu-id="61230-109">Exemplo 1: criar um objeto de configurações de DNS</span><span class="sxs-lookup"><span data-stu-id="61230-109">Example 1: Create a DNS settings object</span></span>
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

<span data-ttu-id="61230-110">Esse comando cria um objeto de configurações de DNS do Azure.</span><span class="sxs-lookup"><span data-stu-id="61230-110">This command creates an Azure DNS settings object.</span></span>
<span data-ttu-id="61230-111">O servidor DNS tem o endereço especificado e o nome amigável Dns01.</span><span class="sxs-lookup"><span data-stu-id="61230-111">The DNS server has the specified address and the friendly name Dns01.</span></span>
<span data-ttu-id="61230-112">O comando armazena o objeto na variável $Dns para uso pelo cmdlet **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="61230-112">The command stores the object in the $Dns variable for use by the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="61230-113">OS</span><span class="sxs-lookup"><span data-stu-id="61230-113">PARAMETERS</span></span>

### <span data-ttu-id="61230-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="61230-114">-InformationAction</span></span>
<span data-ttu-id="61230-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="61230-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="61230-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="61230-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61230-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="61230-117">Continue</span></span>
- <span data-ttu-id="61230-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="61230-118">Ignore</span></span>
- <span data-ttu-id="61230-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="61230-119">Inquire</span></span>
- <span data-ttu-id="61230-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="61230-120">SilentlyContinue</span></span>
- <span data-ttu-id="61230-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="61230-121">Stop</span></span>
- <span data-ttu-id="61230-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="61230-122">Suspend</span></span>

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

### <span data-ttu-id="61230-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="61230-123">-InformationVariable</span></span>
<span data-ttu-id="61230-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="61230-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="61230-125">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="61230-125">-IPAddress</span></span>
<span data-ttu-id="61230-126">Especifica o endereço IP do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="61230-126">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="61230-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="61230-127">-Name</span></span>
<span data-ttu-id="61230-128">Especifica um nome amigável para o servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="61230-128">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="61230-129">Esse nome não é necessariamente um nome de domínio totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="61230-129">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="61230-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61230-130">CommonParameters</span></span>
<span data-ttu-id="61230-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61230-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61230-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61230-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61230-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61230-133">INPUTS</span></span>

## <span data-ttu-id="61230-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61230-134">OUTPUTS</span></span>

## <span data-ttu-id="61230-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61230-135">NOTES</span></span>

## <span data-ttu-id="61230-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61230-136">RELATED LINKS</span></span>

[<span data-ttu-id="61230-137">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="61230-137">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="61230-138">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="61230-138">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="61230-139">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="61230-139">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="61230-140">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="61230-140">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="61230-141">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="61230-141">Set-AzureDns</span></span>](./Set-AzureDns.md)


