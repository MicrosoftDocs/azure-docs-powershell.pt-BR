---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A269A53-8FB2-4D4E-8FBB-A84BE658F75F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 002834bda663dda1c9ebe5f24bb0f1aa0007655c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946332"
---
# <span data-ttu-id="08956-101">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="08956-101">Get-AzureOSDisk</span></span>

## <span data-ttu-id="08956-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08956-102">SYNOPSIS</span></span>
<span data-ttu-id="08956-103">Obtém o disco do sistema operacional de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="08956-103">Gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="08956-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08956-104">SYNTAX</span></span>

```
Get-AzureOSDisk -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="08956-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08956-105">DESCRIPTION</span></span>
<span data-ttu-id="08956-106">O cmdlet **Get-AzureOSDisk** Obtém o disco do sistema operacional de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="08956-106">The **Get-AzureOSDisk** cmdlet gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="08956-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08956-107">EXAMPLES</span></span>

### <span data-ttu-id="08956-108">Exemplo 1: obter um disco do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="08956-108">Example 1: Get an operating system disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Get-AzureOSDisk
```

<span data-ttu-id="08956-109">Esse comando obtém a máquina virtual chamada VirtualMachine02 no serviço chamado ContosoService usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="08956-109">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="08956-110">O comando passa a máquina virtual para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="08956-110">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="08956-111">O cmdlet atual Obtém o disco do sistema operacional da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="08956-111">The current cmdlet gets the operating system disk of that virtual machine.</span></span>

## <span data-ttu-id="08956-112">OS</span><span class="sxs-lookup"><span data-stu-id="08956-112">PARAMETERS</span></span>

### <span data-ttu-id="08956-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="08956-113">-InformationAction</span></span>
<span data-ttu-id="08956-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="08956-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="08956-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="08956-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08956-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="08956-116">Continue</span></span>
- <span data-ttu-id="08956-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="08956-117">Ignore</span></span>
- <span data-ttu-id="08956-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="08956-118">Inquire</span></span>
- <span data-ttu-id="08956-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="08956-119">SilentlyContinue</span></span>
- <span data-ttu-id="08956-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="08956-120">Stop</span></span>
- <span data-ttu-id="08956-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="08956-121">Suspend</span></span>

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

### <span data-ttu-id="08956-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="08956-122">-InformationVariable</span></span>
<span data-ttu-id="08956-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="08956-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="08956-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="08956-124">-Profile</span></span>
<span data-ttu-id="08956-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="08956-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="08956-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="08956-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08956-127">-VM</span><span class="sxs-lookup"><span data-stu-id="08956-127">-VM</span></span>
<span data-ttu-id="08956-128">Especifica a máquina virtual para a qual esse cmdlet obtém o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="08956-128">Specifies the virtual machine for which this cmdlet gets the operating system disk.</span></span>
<span data-ttu-id="08956-129">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="08956-129">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="08956-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08956-130">CommonParameters</span></span>
<span data-ttu-id="08956-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08956-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08956-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08956-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08956-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08956-133">INPUTS</span></span>

## <span data-ttu-id="08956-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08956-134">OUTPUTS</span></span>

## <span data-ttu-id="08956-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08956-135">NOTES</span></span>

## <span data-ttu-id="08956-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08956-136">RELATED LINKS</span></span>

[<span data-ttu-id="08956-137">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="08956-137">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="08956-138">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="08956-138">Set-AzureOSDisk</span></span>](./Set-AzureOSDisk.md)


