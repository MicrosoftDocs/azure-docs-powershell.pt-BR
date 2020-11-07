---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945828"
---
# <span data-ttu-id="23e5b-101">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="23e5b-101">Set-AzureOSDisk</span></span>

## <span data-ttu-id="23e5b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="23e5b-103">Modifica o modo de cache do host de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="23e5b-103">Modifies the host cache mode of an Azure virtual machine.</span></span>

## <span data-ttu-id="23e5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23e5b-104">SYNTAX</span></span>

### <span data-ttu-id="23e5b-105">NoResize</span><span class="sxs-lookup"><span data-stu-id="23e5b-105">NoResize</span></span>
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="23e5b-106">Dimensiona</span><span class="sxs-lookup"><span data-stu-id="23e5b-106">Resize</span></span>
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="23e5b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23e5b-107">DESCRIPTION</span></span>
<span data-ttu-id="23e5b-108">O cmdlet **set-AzureOSDisk** modifica o modo de cache do host do disco do sistema operacional de uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="23e5b-108">The **Set-AzureOSDisk** cmdlet modifies the host cache mode of the operating system disk of an Azure virtual machine.</span></span>
<span data-ttu-id="23e5b-109">Os modos de cache de host suportados são ReadOnly e ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="23e5b-109">The supported host cache modes are ReadOnly and ReadWrite.</span></span>
<span data-ttu-id="23e5b-110">Se você executar esse cmdlet em uma máquina virtual em execução, essa máquina virtual será reiniciada.</span><span class="sxs-lookup"><span data-stu-id="23e5b-110">If you run this cmdlet on a virtual machine that is running, that virtual machine restarts.</span></span>

## <span data-ttu-id="23e5b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23e5b-111">EXAMPLES</span></span>

### <span data-ttu-id="23e5b-112">Exemplo 1: definir o modo de cache do host como ReadOnly usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="23e5b-112">Example 1: Set the host cache mode to ReadOnly by using the pipeline</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

<span data-ttu-id="23e5b-113">Esse comando obtém a máquina virtual chamada VirtualMachine02 no serviço chamado ContosoService usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="23e5b-113">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="23e5b-114">O comando passa a máquina virtual para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="23e5b-114">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="23e5b-115">O cmdlet atual define o modo de cache do host do disco do sistema operacional da máquina virtual para ser somente leitura.</span><span class="sxs-lookup"><span data-stu-id="23e5b-115">The current cmdlet sets the host cache mode of the operating system disk of that virtual machine to be ReadOnly.</span></span>

### <span data-ttu-id="23e5b-116">Exemplo 2: definir o modo de cache do host como ReadWrite</span><span class="sxs-lookup"><span data-stu-id="23e5b-116">Example 2: Set the host cache mode to ReadWrite</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

<span data-ttu-id="23e5b-117">O primeiro comando obtém a máquina virtual chamada VirtualMachine02 no serviço chamado ContosoService e, em seguida, armazena-a na variável.</span><span class="sxs-lookup"><span data-stu-id="23e5b-117">The first command gets the virtual machine named VirtualMachine02 in the service named ContosoService, and then stores it in the variable.</span></span>

<span data-ttu-id="23e5b-118">O segundo comando define o modo de cache do host do disco do sistema operacional da máquina virtual para ser ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="23e5b-118">The second command sets the host cache mode of the operating system disk of that virtual machine to be ReadWrite.</span></span>

## <span data-ttu-id="23e5b-119">OS</span><span class="sxs-lookup"><span data-stu-id="23e5b-119">PARAMETERS</span></span>

### <span data-ttu-id="23e5b-120">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="23e5b-120">-HostCaching</span></span>
<span data-ttu-id="23e5b-121">Especifica o atributo de cache do host para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="23e5b-121">Specifies the host cache attribute for the operating system disk.</span></span>
<span data-ttu-id="23e5b-122">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="23e5b-122">Valid values are:</span></span> 

- <span data-ttu-id="23e5b-123">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="23e5b-123">ReadOnly</span></span> 
- <span data-ttu-id="23e5b-124">Leitura</span><span class="sxs-lookup"><span data-stu-id="23e5b-124">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e5b-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="23e5b-125">-InformationAction</span></span>
<span data-ttu-id="23e5b-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="23e5b-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23e5b-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="23e5b-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23e5b-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="23e5b-128">Continue</span></span>
- <span data-ttu-id="23e5b-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="23e5b-129">Ignore</span></span>
- <span data-ttu-id="23e5b-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="23e5b-130">Inquire</span></span>
- <span data-ttu-id="23e5b-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23e5b-131">SilentlyContinue</span></span>
- <span data-ttu-id="23e5b-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="23e5b-132">Stop</span></span>
- <span data-ttu-id="23e5b-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="23e5b-133">Suspend</span></span>

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

### <span data-ttu-id="23e5b-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23e5b-134">-InformationVariable</span></span>
<span data-ttu-id="23e5b-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="23e5b-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="23e5b-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="23e5b-136">-Profile</span></span>
<span data-ttu-id="23e5b-137">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="23e5b-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23e5b-138">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="23e5b-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23e5b-139">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="23e5b-139">-ResizedSizeInGB</span></span>
<span data-ttu-id="23e5b-140">Especifica um novo tamanho, em gigabytes, para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="23e5b-140">Specifies a new size, in gigabytes, for the operating system disk.</span></span>
<span data-ttu-id="23e5b-141">O tamanho deve ser maior do que o tamanho atual.</span><span class="sxs-lookup"><span data-stu-id="23e5b-141">The size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e5b-142">-VM</span><span class="sxs-lookup"><span data-stu-id="23e5b-142">-VM</span></span>
<span data-ttu-id="23e5b-143">Especifica a máquina virtual para a qual esse cmdlet modifica o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="23e5b-143">Specifies the virtual machine for which this cmdlet modifies the operating system disk.</span></span>
<span data-ttu-id="23e5b-144">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="23e5b-144">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="23e5b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e5b-145">CommonParameters</span></span>
<span data-ttu-id="23e5b-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e5b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e5b-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23e5b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e5b-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23e5b-148">INPUTS</span></span>

## <span data-ttu-id="23e5b-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23e5b-149">OUTPUTS</span></span>

## <span data-ttu-id="23e5b-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23e5b-150">NOTES</span></span>

## <span data-ttu-id="23e5b-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23e5b-151">RELATED LINKS</span></span>

[<span data-ttu-id="23e5b-152">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="23e5b-152">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="23e5b-153">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="23e5b-153">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)

[<span data-ttu-id="23e5b-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="23e5b-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="23e5b-155">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="23e5b-155">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="23e5b-156">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="23e5b-156">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="23e5b-157">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="23e5b-157">Update-AzureVM</span></span>](./Update-AzureVM.md)


