---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 73CEA6A8-46C9-4772-9A67-03F532696CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1287b3a0bb1cc39dea78fb4e92d2dcc4508c6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945543"
---
# <span data-ttu-id="51ffa-101">Get-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="51ffa-101">Get-AzureSubnet</span></span>

## <span data-ttu-id="51ffa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="51ffa-103">Obtém uma lista de sub-redes associadas à máquina virtual do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="51ffa-103">Gets a list of subnets associated with the specified Azure virtual machine.</span></span>

## <span data-ttu-id="51ffa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51ffa-104">SYNTAX</span></span>

```
Get-AzureSubnet -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="51ffa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51ffa-105">DESCRIPTION</span></span>
<span data-ttu-id="51ffa-106">O cmdlet **Get-AzureSubnet** retorna uma lista das sub-redes associadas à máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="51ffa-106">The **Get-AzureSubnet** cmdlet returns a list the subnets associated with the specified virtual machine.</span></span>
<span data-ttu-id="51ffa-107">Use **Get-AzureVM** para especificar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51ffa-107">Use **Get-AzureVM** to specify the virtual machine.</span></span>

## <span data-ttu-id="51ffa-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51ffa-108">EXAMPLES</span></span>

### <span data-ttu-id="51ffa-109">Exemplo 1: obter sub-redes para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="51ffa-109">Example 1: Get subnets for a virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine01"
C:\PS> Get-AzureSubnet -VM $VM
```

<span data-ttu-id="51ffa-110">O primeiro comando obtém uma máquina virtual chamada VirtualMachine01 no serviço chamado ContosoService03 e, em seguida, armazena-a na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="51ffa-110">The first command gets a virtual machine named VirtualMachine01 in the service named ContosoService03, and then stores it in the $VM variable.</span></span>

<span data-ttu-id="51ffa-111">O segundo comando obtém as sub-redes do Azure para a máquina virtual em $VM.</span><span class="sxs-lookup"><span data-stu-id="51ffa-111">The second command gets the Azure subnets for the virtual machine in $VM.</span></span>

## <span data-ttu-id="51ffa-112">OS</span><span class="sxs-lookup"><span data-stu-id="51ffa-112">PARAMETERS</span></span>

### <span data-ttu-id="51ffa-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="51ffa-113">-InformationAction</span></span>
<span data-ttu-id="51ffa-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="51ffa-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="51ffa-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="51ffa-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51ffa-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="51ffa-116">Continue</span></span>
- <span data-ttu-id="51ffa-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="51ffa-117">Ignore</span></span>
- <span data-ttu-id="51ffa-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="51ffa-118">Inquire</span></span>
- <span data-ttu-id="51ffa-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="51ffa-119">SilentlyContinue</span></span>
- <span data-ttu-id="51ffa-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="51ffa-120">Stop</span></span>
- <span data-ttu-id="51ffa-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="51ffa-121">Suspend</span></span>

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

### <span data-ttu-id="51ffa-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="51ffa-122">-InformationVariable</span></span>
<span data-ttu-id="51ffa-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="51ffa-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="51ffa-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="51ffa-124">-Profile</span></span>
<span data-ttu-id="51ffa-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="51ffa-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51ffa-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="51ffa-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51ffa-127">-VM</span><span class="sxs-lookup"><span data-stu-id="51ffa-127">-VM</span></span>
<span data-ttu-id="51ffa-128">Especifica o objeto da máquina virtual a partir da qual obter a lista de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="51ffa-128">Specifies the virtual machine object from which to get the subnet list.</span></span>

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

### <span data-ttu-id="51ffa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ffa-129">CommonParameters</span></span>
<span data-ttu-id="51ffa-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51ffa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ffa-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51ffa-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ffa-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51ffa-132">INPUTS</span></span>

## <span data-ttu-id="51ffa-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51ffa-133">OUTPUTS</span></span>

## <span data-ttu-id="51ffa-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51ffa-134">NOTES</span></span>

## <span data-ttu-id="51ffa-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51ffa-135">RELATED LINKS</span></span>

[<span data-ttu-id="51ffa-136">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="51ffa-136">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="51ffa-137">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="51ffa-137">Set-AzureSubnet</span></span>](./Set-AzureSubnet.md)


