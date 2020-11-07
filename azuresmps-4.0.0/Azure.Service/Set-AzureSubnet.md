---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 69974370-4542-4417-BD9D-3928EB005C31
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81d6e523978196a47b01d21aa8e857027b0b4f40
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945951"
---
# <span data-ttu-id="41bbb-101">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="41bbb-101">Set-AzureSubnet</span></span>

## <span data-ttu-id="41bbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="41bbb-103">Define a lista de sub-rede para uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="41bbb-103">Defines the subnet list for an Azure virtual machine.</span></span>

## <span data-ttu-id="41bbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41bbb-104">SYNTAX</span></span>

```
Set-AzureSubnet [-SubnetNames] <String[]> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="41bbb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41bbb-105">DESCRIPTION</span></span>
<span data-ttu-id="41bbb-106">O cmdlet **set-AzureSubnet** define a lista de sub-rede para uma configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="41bbb-106">The **Set-AzureSubnet** cmdlet sets the subnet list for a virtual machine configuration.</span></span>
<span data-ttu-id="41bbb-107">Use with **New-AzureVM** para definir as sub-redes de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="41bbb-107">Use with **New-AzureVM** to set the subnets for a virtual machine.</span></span>

## <span data-ttu-id="41bbb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41bbb-108">EXAMPLES</span></span>

### <span data-ttu-id="41bbb-109">Exemplo 1: adicionar uma sub-rede a uma configuração de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="41bbb-109">Example 1: Add a subnet to a virtual machine configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine04" -ImageName $image -InstanceSize "Small" | Add-AzureProvisioningConfig -Windows -Password "password" | Set-AzureSubnet "PubSubnet","PrivSubnet" | New-AzureVM -ServiceName "ContosoService03"
```

<span data-ttu-id="41bbb-110">Esse comando adiciona uma sub-rede à configuração da máquina virtual e, em seguida, cria a máquina virtual chamada VirtualMachine04.</span><span class="sxs-lookup"><span data-stu-id="41bbb-110">This command adds a subnet to the virtual machine configuration, and then creates the virtual machine named VirtualMachine04.</span></span>

## <span data-ttu-id="41bbb-111">OS</span><span class="sxs-lookup"><span data-stu-id="41bbb-111">PARAMETERS</span></span>

### <span data-ttu-id="41bbb-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="41bbb-112">-InformationAction</span></span>
<span data-ttu-id="41bbb-113">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="41bbb-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="41bbb-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="41bbb-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41bbb-115">Contínuo</span><span class="sxs-lookup"><span data-stu-id="41bbb-115">Continue</span></span>
- <span data-ttu-id="41bbb-116">Ignorar</span><span class="sxs-lookup"><span data-stu-id="41bbb-116">Ignore</span></span>
- <span data-ttu-id="41bbb-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="41bbb-117">Inquire</span></span>
- <span data-ttu-id="41bbb-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="41bbb-118">SilentlyContinue</span></span>
- <span data-ttu-id="41bbb-119">Finaliza</span><span class="sxs-lookup"><span data-stu-id="41bbb-119">Stop</span></span>
- <span data-ttu-id="41bbb-120">Suspensão</span><span class="sxs-lookup"><span data-stu-id="41bbb-120">Suspend</span></span>

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

### <span data-ttu-id="41bbb-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="41bbb-121">-InformationVariable</span></span>
<span data-ttu-id="41bbb-122">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="41bbb-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="41bbb-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="41bbb-123">-Profile</span></span>
<span data-ttu-id="41bbb-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="41bbb-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41bbb-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="41bbb-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41bbb-126">-Subnetnames</span><span class="sxs-lookup"><span data-stu-id="41bbb-126">-SubnetNames</span></span>
<span data-ttu-id="41bbb-127">Especifica uma matriz que contém a lista de nomes de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="41bbb-127">Specifies an array that contains the list of subnet names.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41bbb-128">-VM</span><span class="sxs-lookup"><span data-stu-id="41bbb-128">-VM</span></span>
<span data-ttu-id="41bbb-129">Especifica o objeto da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="41bbb-129">Specifies the virtual machine object.</span></span>

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

### <span data-ttu-id="41bbb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41bbb-130">CommonParameters</span></span>
<span data-ttu-id="41bbb-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41bbb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41bbb-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41bbb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41bbb-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41bbb-133">INPUTS</span></span>

## <span data-ttu-id="41bbb-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41bbb-134">OUTPUTS</span></span>

## <span data-ttu-id="41bbb-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41bbb-135">NOTES</span></span>

## <span data-ttu-id="41bbb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41bbb-136">RELATED LINKS</span></span>

[<span data-ttu-id="41bbb-137">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="41bbb-137">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="41bbb-138">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="41bbb-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="41bbb-139">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="41bbb-139">Update-AzureVM</span></span>](./Update-AzureVM.md)


