---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E54E4D16-DB2A-4626-B543-773C187B2E08
online version: ''
schema: 2.0.0
ms.openlocfilehash: d242418117b1bb576206f9ebb5fd568bd3e63cd1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945862"
---
# <span data-ttu-id="ccd23-101">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="ccd23-101">Set-AzureStaticVNetIP</span></span>

## <span data-ttu-id="ccd23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccd23-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd23-103">Define as informações de endereço IP da VNet estático para um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ccd23-103">Sets the static VNet IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="ccd23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccd23-104">SYNTAX</span></span>

```
Set-AzureStaticVNetIP [-IPAddress] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ccd23-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ccd23-105">DESCRIPTION</span></span>
<span data-ttu-id="ccd23-106">O cmdlet **set-AzureStaticVNetIP** define as informações de endereço IP de rede virtual estática (VNet) para um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ccd23-106">The **Set-AzureStaticVNetIP** cmdlet sets the static virtual network (VNet) IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="ccd23-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ccd23-107">EXAMPLES</span></span>

### <span data-ttu-id="ccd23-108">Exemplo 1: definir o endereço IP de rede virtual associado a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="ccd23-108">Example 1: Set the virtual network IP address associated with a virtual machine</span></span>
```
PS C:\> # Prerequisite: VNet has been set up with SubNet
          # Set-AzureVNetConfig -ConfigurationPath $vnetConfigPath;

          $vm = New-AzureVMConfig -Name $vmname -ImageName $img -InstanceSize $sz | Add-AzureProvisioningConfig -Windows -Password $pwd -AdminUsername $usr;
          $vm = Set-AzureSubNet -VM $vm -SubNetNames $sn;
          Set-AzureStaticVNetIP -IPAddress $ip -VM $vm;
          New-AzureVM -ServiceName $svc -VMs $vm -VNetName $vnetName -Location $loc;
```

<span data-ttu-id="ccd23-109">O primeiro comando define o caminho de configuração de uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ccd23-109">The first command sets the configuration path for a virtual network.</span></span>

<span data-ttu-id="ccd23-110">O segundo comando cria uma configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ccd23-110">The second command creates a virtual machine configuration.</span></span>

<span data-ttu-id="ccd23-111">O terceiro comando define a sub-rede para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ccd23-111">The third command sets the subnet for the virtual machine.</span></span>

<span data-ttu-id="ccd23-112">O quarto comando define o endereço IP para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ccd23-112">The fourth command sets the IP address for the virtual machine.</span></span>

<span data-ttu-id="ccd23-113">O quinto comando cria uma máquina virtual usando a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ccd23-113">The fifth command creates a virtual machine using the virtual machine.</span></span>

## <span data-ttu-id="ccd23-114">OS</span><span class="sxs-lookup"><span data-stu-id="ccd23-114">PARAMETERS</span></span>

### <span data-ttu-id="ccd23-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ccd23-115">-InformationAction</span></span>
<span data-ttu-id="ccd23-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="ccd23-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ccd23-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ccd23-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ccd23-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="ccd23-118">Continue</span></span>
- <span data-ttu-id="ccd23-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="ccd23-119">Ignore</span></span>
- <span data-ttu-id="ccd23-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="ccd23-120">Inquire</span></span>
- <span data-ttu-id="ccd23-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ccd23-121">SilentlyContinue</span></span>
- <span data-ttu-id="ccd23-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="ccd23-122">Stop</span></span>
- <span data-ttu-id="ccd23-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="ccd23-123">Suspend</span></span>

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

### <span data-ttu-id="ccd23-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ccd23-124">-InformationVariable</span></span>
<span data-ttu-id="ccd23-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="ccd23-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ccd23-126">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="ccd23-126">-IPAddress</span></span>
<span data-ttu-id="ccd23-127">Especifica o endereço IP da VNet estático</span><span class="sxs-lookup"><span data-stu-id="ccd23-127">Specifies the static VNet IP address</span></span>

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

### <span data-ttu-id="ccd23-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ccd23-128">-Profile</span></span>
<span data-ttu-id="ccd23-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ccd23-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ccd23-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ccd23-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ccd23-131">-VM</span><span class="sxs-lookup"><span data-stu-id="ccd23-131">-VM</span></span>
<span data-ttu-id="ccd23-132">Especifica um objeto de máquina virtual persistente para o qual definir o endereço IP VNet estático.</span><span class="sxs-lookup"><span data-stu-id="ccd23-132">Specifies a persistent virtual machine object for which to set the static VNet IP address.</span></span>

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

### <span data-ttu-id="ccd23-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd23-133">CommonParameters</span></span>
<span data-ttu-id="ccd23-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccd23-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd23-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccd23-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd23-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ccd23-136">INPUTS</span></span>

## <span data-ttu-id="ccd23-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ccd23-137">OUTPUTS</span></span>

## <span data-ttu-id="ccd23-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ccd23-138">NOTES</span></span>

## <span data-ttu-id="ccd23-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccd23-139">RELATED LINKS</span></span>

[<span data-ttu-id="ccd23-140">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="ccd23-140">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="ccd23-141">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="ccd23-141">Test-AzureStaticVNetIP</span></span>](./Test-AzureStaticVNetIP.md)


