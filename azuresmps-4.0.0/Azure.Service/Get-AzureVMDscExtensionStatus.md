---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 19A87B24-C5A6-4505-BB54-973B24BCC68E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821927fc465ed5af048a2f27ed84da8c12b9caa5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946536"
---
# <span data-ttu-id="b6772-101">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="b6772-101">Get-AzureVMDscExtensionStatus</span></span>

## <span data-ttu-id="b6772-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6772-102">SYNOPSIS</span></span>
<span data-ttu-id="b6772-103">Obtém o status da extensão DSC para todas as máquinas virtuais implantadas em um serviço na nuvem ou para uma máquina virtual em particular no serviço.</span><span class="sxs-lookup"><span data-stu-id="b6772-103">Gets the DSC extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="b6772-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6772-104">SYNTAX</span></span>

### <span data-ttu-id="b6772-105">GetStatusByServiceAndVMName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6772-105">GetStatusByServiceAndVMName (Default)</span></span>
```
Get-AzureVMDscExtensionStatus [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b6772-106">GetStatusByVM</span><span class="sxs-lookup"><span data-stu-id="b6772-106">GetStatusByVM</span></span>
```
Get-AzureVMDscExtensionStatus -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b6772-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6772-107">DESCRIPTION</span></span>
<span data-ttu-id="b6772-108">O cmdlet **Get-AzureVMDscExtensionStatus** Obtém o status da extensão da extensão de estado desejado (DSC) para todas as máquinas virtuais implantadas em um serviço na nuvem ou para uma máquina virtual em particular no serviço.</span><span class="sxs-lookup"><span data-stu-id="b6772-108">The **Get-AzureVMDscExtensionStatus** cmdlet gets the Desired State Configuration (DSC) extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="b6772-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6772-109">EXAMPLES</span></span>

### <span data-ttu-id="b6772-110">1:</span><span class="sxs-lookup"><span data-stu-id="b6772-110">1:</span></span>
```

```

## <span data-ttu-id="b6772-111">OS</span><span class="sxs-lookup"><span data-stu-id="b6772-111">PARAMETERS</span></span>

### <span data-ttu-id="b6772-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b6772-112">-InformationAction</span></span>
<span data-ttu-id="b6772-113">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b6772-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b6772-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b6772-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6772-115">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b6772-115">Continue</span></span>
- <span data-ttu-id="b6772-116">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b6772-116">Ignore</span></span>
- <span data-ttu-id="b6772-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="b6772-117">Inquire</span></span>
- <span data-ttu-id="b6772-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b6772-118">SilentlyContinue</span></span>
- <span data-ttu-id="b6772-119">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b6772-119">Stop</span></span>
- <span data-ttu-id="b6772-120">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b6772-120">Suspend</span></span>

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

### <span data-ttu-id="b6772-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b6772-121">-InformationVariable</span></span>
<span data-ttu-id="b6772-122">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b6772-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b6772-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6772-123">-Name</span></span>
<span data-ttu-id="b6772-124">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b6772-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6772-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b6772-125">-Profile</span></span>
<span data-ttu-id="b6772-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b6772-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6772-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b6772-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6772-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b6772-128">-ServiceName</span></span>
<span data-ttu-id="b6772-129">Especifica o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="b6772-129">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6772-130">-VM</span><span class="sxs-lookup"><span data-stu-id="b6772-130">-VM</span></span>
<span data-ttu-id="b6772-131">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="b6772-131">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: GetStatusByVM
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6772-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6772-132">CommonParameters</span></span>
<span data-ttu-id="b6772-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6772-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6772-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6772-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6772-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6772-135">INPUTS</span></span>

## <span data-ttu-id="b6772-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6772-136">OUTPUTS</span></span>

### <span data-ttu-id="b6772-137">Microsoft. WindowsAzure. Commands. onmanagement. IaaS. Extensions. VirtualMachineDscExtensionStatusContext</span><span class="sxs-lookup"><span data-stu-id="b6772-137">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionStatusContext</span></span>

## <span data-ttu-id="b6772-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6772-138">NOTES</span></span>

## <span data-ttu-id="b6772-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6772-139">RELATED LINKS</span></span>

[<span data-ttu-id="b6772-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="b6772-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="b6772-141">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="b6772-141">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="b6772-142">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="b6772-142">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


