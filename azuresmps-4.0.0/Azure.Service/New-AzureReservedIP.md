---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9C22F5D7-1FD0-4699-83D7-1D72C5234DEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d09173c43de9c01056055f714217db5eb4c58225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945993"
---
# <span data-ttu-id="2778f-101">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="2778f-101">New-AzureReservedIP</span></span>

## <span data-ttu-id="2778f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2778f-102">SYNOPSIS</span></span>
<span data-ttu-id="2778f-103">Cria um endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="2778f-103">Creates a reserved IP address.</span></span>

## <span data-ttu-id="2778f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2778f-104">SYNTAX</span></span>

### <span data-ttu-id="2778f-105">CreateNewReservedIP (padrão)</span><span class="sxs-lookup"><span data-stu-id="2778f-105">CreateNewReservedIP (Default)</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="2778f-106">CreateInUseReservedIPUsingSlot</span><span class="sxs-lookup"><span data-stu-id="2778f-106">CreateInUseReservedIPUsingSlot</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="2778f-107">CreateInUseReservedIP</span><span class="sxs-lookup"><span data-stu-id="2778f-107">CreateInUseReservedIP</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2778f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2778f-108">DESCRIPTION</span></span>
<span data-ttu-id="2778f-109">O cmdlet **New-AzureReservedIP** cria um endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="2778f-109">The **New-AzureReservedIP** cmdlet creates a reserved IP address.</span></span>

## <span data-ttu-id="2778f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2778f-110">EXAMPLES</span></span>

### <span data-ttu-id="2778f-111">Exemplo 1: criar um novo IP reservado</span><span class="sxs-lookup"><span data-stu-id="2778f-111">Example 1: Create a new reserved IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName $Name -Label $Label -Location $Location
```

<span data-ttu-id="2778f-112">Esse comando cria um novo endereço IP reservado na assinatura, que pode ser usado para a criação de serviços de nuvem que incluem máquinas da Web, de trabalhador e de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2778f-112">This command creates a new reserved IP address in the subscription, which can be used for creating cloud services that include Web, Worker, and Virtual Machines.</span></span>

### <span data-ttu-id="2778f-113">Exemplo 2: criar um IP reservado com base em um IP existente</span><span class="sxs-lookup"><span data-stu-id="2778f-113">Example 2: Create a reserved IP based on an existing IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName resip14 -Location "West Europe" -ServiceName piptestwesteurope
```

<span data-ttu-id="2778f-114">Esse comando cria um VIP existente (IP virtual) no serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="2778f-114">This command creates an existing VIP (Virtual IP) on the specified service.</span></span>

## <span data-ttu-id="2778f-115">OS</span><span class="sxs-lookup"><span data-stu-id="2778f-115">PARAMETERS</span></span>

### <span data-ttu-id="2778f-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="2778f-116">-InformationAction</span></span>
<span data-ttu-id="2778f-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="2778f-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2778f-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2778f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2778f-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="2778f-119">Continue</span></span>
- <span data-ttu-id="2778f-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="2778f-120">Ignore</span></span>
- <span data-ttu-id="2778f-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="2778f-121">Inquire</span></span>
- <span data-ttu-id="2778f-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2778f-122">SilentlyContinue</span></span>
- <span data-ttu-id="2778f-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="2778f-123">Stop</span></span>
- <span data-ttu-id="2778f-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="2778f-124">Suspend</span></span>

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

### <span data-ttu-id="2778f-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2778f-125">-InformationVariable</span></span>
<span data-ttu-id="2778f-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="2778f-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2778f-127">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="2778f-127">-Label</span></span>
<span data-ttu-id="2778f-128">Especifica um rótulo para o endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="2778f-128">Specifies a label for the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2778f-129">-Local</span><span class="sxs-lookup"><span data-stu-id="2778f-129">-Location</span></span>
<span data-ttu-id="2778f-130">Especifica um local no qual criar o endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="2778f-130">Specifies a location at which to create the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2778f-131">-Perfil</span><span class="sxs-lookup"><span data-stu-id="2778f-131">-Profile</span></span>
<span data-ttu-id="2778f-132">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="2778f-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2778f-133">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="2778f-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2778f-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="2778f-134">-ReservedIPName</span></span>
<span data-ttu-id="2778f-135">Especifica o nome do endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="2778f-135">Specifies the reserved IP address name.</span></span>

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

### <span data-ttu-id="2778f-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2778f-136">-ServiceName</span></span>
<span data-ttu-id="2778f-137">Especifica um nome de serviço.</span><span class="sxs-lookup"><span data-stu-id="2778f-137">Specifies a service name.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2778f-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="2778f-138">-Slot</span></span>
<span data-ttu-id="2778f-139">Especifica o slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="2778f-139">Specifies the deployment slot.</span></span>
<span data-ttu-id="2778f-140">Os valores aceitáveis para esse parâmetro são: preparação, produção.</span><span class="sxs-lookup"><span data-stu-id="2778f-140">The acceptable values for this parameter are: Staging, Production.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2778f-141">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="2778f-141">-VirtualIPName</span></span>
<span data-ttu-id="2778f-142">Especifica que esse cmdlet usa o parâmetro **VirtualIPName** para reservar um endereço IP virtual existente (VIP) em sua implantação.</span><span class="sxs-lookup"><span data-stu-id="2778f-142">Specifies that this cmdlet uses the **VirtualIPName** parameter to reserve an existing virtual IP address (VIP) in your deployment.</span></span>
<span data-ttu-id="2778f-143">Se esse parâmetro não for especificado, esse cmdlet reservará um novo VIP.</span><span class="sxs-lookup"><span data-stu-id="2778f-143">If this parameter is not specified, this cmdlet reserves a new VIP.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2778f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2778f-144">CommonParameters</span></span>
<span data-ttu-id="2778f-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2778f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2778f-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2778f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2778f-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2778f-147">INPUTS</span></span>

## <span data-ttu-id="2778f-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2778f-148">OUTPUTS</span></span>

## <span data-ttu-id="2778f-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2778f-149">NOTES</span></span>

## <span data-ttu-id="2778f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2778f-150">RELATED LINKS</span></span>

[<span data-ttu-id="2778f-151">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="2778f-151">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="2778f-152">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="2778f-152">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


