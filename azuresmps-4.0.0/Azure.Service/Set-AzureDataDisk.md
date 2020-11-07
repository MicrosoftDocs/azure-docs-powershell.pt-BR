---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946066"
---
# <span data-ttu-id="7bd0d-101">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="7bd0d-101">Set-AzureDataDisk</span></span>

## <span data-ttu-id="7bd0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bd0d-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd0d-103">Modifica o cache do host de um disco de dados existente em uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-103">Modifies the host caching of an existing data disk on an Azure virtual machine.</span></span>

## <span data-ttu-id="7bd0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bd0d-104">SYNTAX</span></span>

### <span data-ttu-id="7bd0d-105">NoResize</span><span class="sxs-lookup"><span data-stu-id="7bd0d-105">NoResize</span></span>
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7bd0d-106">Dimensiona</span><span class="sxs-lookup"><span data-stu-id="7bd0d-106">Resize</span></span>
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="7bd0d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bd0d-107">DESCRIPTION</span></span>
<span data-ttu-id="7bd0d-108">O cmdlet **set-AzureDataDisk** modifica os atributos de cache de um disco de dados existente em uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-108">The **Set-AzureDataDisk** cmdlet modifies the cache attributes of an existing data disk on an Azure virtual machine.</span></span>
<span data-ttu-id="7bd0d-109">Especifique qual disco de dados atualizar por seu número de unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="7bd0d-109">Specify which data disk to update by its logical unit number (LUN).</span></span>

## <span data-ttu-id="7bd0d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bd0d-110">EXAMPLES</span></span>

### <span data-ttu-id="7bd0d-111">Exemplo 1: modificar o cache do host para um disco de dados</span><span class="sxs-lookup"><span data-stu-id="7bd0d-111">Example 1: Modify the host caching for a data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

<span data-ttu-id="7bd0d-112">Esse comando obtém as máquinas virtuais executadas no serviço denominado ContosoService usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="7bd0d-112">This command gets the virtual machines that run on the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="7bd0d-113">O comando passa a ele para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-113">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7bd0d-114">Esse cmdlet define o disco de dados na LUN 2 da máquina virtual nomeada VirtualMachine07 para usar o cache do host ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-114">That cmdlet sets the data disk at LUN 2 of the virtual machine named VirtualMachine07 to use ReadOnly host caching.</span></span>
<span data-ttu-id="7bd0d-115">O comando atualiza a máquina virtual para refletir suas alterações usando o cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="7bd0d-115">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="7bd0d-116">Exemplo 2: modificar o cache do host para todos os discos de dados em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="7bd0d-116">Example 2: Modify the host caching for all data disks on a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

<span data-ttu-id="7bd0d-117">Esse comando obtém um objeto para a máquina virtual nomeada VirtualMachine07 no serviço na nuvem do ContosoService.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-117">This command gets an object for the virtual machine named VirtualMachine07 on the ContosoService cloud service.</span></span>
<span data-ttu-id="7bd0d-118">O comando a passa para o cmdlet **Get-AzureDataDisk** , que obtém os discos de dados dessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-118">The command passes it to the **Get-AzureDataDisk** cmdlet, which gets the data disks for that virtual machine.</span></span>
<span data-ttu-id="7bd0d-119">Em seguida, o cmdlet atual define o modo de cache do host de cada disco de dados como ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-119">The current cmdlet then sets the host caching mode of each data disks to ReadWrite.</span></span>
<span data-ttu-id="7bd0d-120">O comando atualiza a máquina virtual para refletir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-120">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="7bd0d-121">OS</span><span class="sxs-lookup"><span data-stu-id="7bd0d-121">PARAMETERS</span></span>

### <span data-ttu-id="7bd0d-122">-Diskname</span><span class="sxs-lookup"><span data-stu-id="7bd0d-122">-DiskName</span></span>
<span data-ttu-id="7bd0d-123">Especifica o nome da configuração de disco de dados que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-123">Specifies the name of the data disk configuration that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd0d-124">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="7bd0d-124">-HostCaching</span></span>

> [!WARNING]
> <span data-ttu-id="7bd0d-125">O cache de disco não é compatível com os discos 4 a TiB e maiores.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-125">Disk Caching is not supported for disks 4 TiB and larger.</span></span> <span data-ttu-id="7bd0d-126">Se vários discos estiverem conectados à sua VM, cada disco menor do que 4 TiB será compatível com o cache.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-126">If multiple disks are attached to your VM, each disk that is smaller than 4 TiB will support caching.</span></span>
>
> <span data-ttu-id="7bd0d-127">Alterar a configuração do cache de um disco do Azure desconecta e anexa novamente o disco de destino.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-127">Changing the cache setting of an Azure disk detaches and re-attaches the target disk.</span></span> <span data-ttu-id="7bd0d-128">Se for o disco do sistema operacional, a VM será reiniciada.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-128">If it is the operating system disk, the VM is restarted.</span></span> <span data-ttu-id="7bd0d-129">Pare todos os aplicativos/serviços que possam ser afetados por essa interrupção antes de alterar a configuração do cache de disco.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-129">Stop all applications/services that might be affected by this disruption before changing the disk cache setting.</span></span> <span data-ttu-id="7bd0d-130">Não seguir essas recomendações pode levar à corrupção de dados.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-130">Not following those recommendations could lead to data corruption.</span></span>

<span data-ttu-id="7bd0d-131">Especifica as configurações de cache do nível do host do disco.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-131">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="7bd0d-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="7bd0d-132">Valid values are:</span></span>

- <span data-ttu-id="7bd0d-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7bd0d-133">None</span></span>
- <span data-ttu-id="7bd0d-134">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="7bd0d-134">ReadOnly</span></span>
- <span data-ttu-id="7bd0d-135">Leitura</span><span class="sxs-lookup"><span data-stu-id="7bd0d-135">ReadWrite</span></span>

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

### <span data-ttu-id="7bd0d-136">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="7bd0d-136">-InformationAction</span></span>
<span data-ttu-id="7bd0d-137">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7bd0d-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7bd0d-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7bd0d-139">Contínuo</span><span class="sxs-lookup"><span data-stu-id="7bd0d-139">Continue</span></span>
- <span data-ttu-id="7bd0d-140">Ignorar</span><span class="sxs-lookup"><span data-stu-id="7bd0d-140">Ignore</span></span>
- <span data-ttu-id="7bd0d-141">Inquire</span><span class="sxs-lookup"><span data-stu-id="7bd0d-141">Inquire</span></span>
- <span data-ttu-id="7bd0d-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7bd0d-142">SilentlyContinue</span></span>
- <span data-ttu-id="7bd0d-143">Finaliza</span><span class="sxs-lookup"><span data-stu-id="7bd0d-143">Stop</span></span>
- <span data-ttu-id="7bd0d-144">Suspensão</span><span class="sxs-lookup"><span data-stu-id="7bd0d-144">Suspend</span></span>

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

### <span data-ttu-id="7bd0d-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7bd0d-145">-InformationVariable</span></span>
<span data-ttu-id="7bd0d-146">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-146">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7bd0d-147">-LUN</span><span class="sxs-lookup"><span data-stu-id="7bd0d-147">-LUN</span></span>
<span data-ttu-id="7bd0d-148">Especifica o LUN para a unidade de dados na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-148">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="7bd0d-149">Os valores válidos são: de 0 a 15.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-149">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd0d-150">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7bd0d-150">-Profile</span></span>
<span data-ttu-id="7bd0d-151">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7bd0d-152">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7bd0d-153">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="7bd0d-153">-ResizedSizeInGB</span></span>
<span data-ttu-id="7bd0d-154">Especifica o novo tamanho, em gigabytes, para o disco de dados.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-154">Specifies the new size, in gigabytes, for the data disk.</span></span>
<span data-ttu-id="7bd0d-155">O novo tamanho deve ser maior do que o tamanho atual.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-155">The new size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd0d-156">-VM</span><span class="sxs-lookup"><span data-stu-id="7bd0d-156">-VM</span></span>
<span data-ttu-id="7bd0d-157">Especifica o objeto da máquina virtual que está anexado ao disco de dados.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-157">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="7bd0d-158">Para obter um objeto de máquina virtual, use o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="7bd0d-158">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="7bd0d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd0d-159">CommonParameters</span></span>
<span data-ttu-id="7bd0d-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd0d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd0d-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bd0d-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd0d-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bd0d-162">INPUTS</span></span>

## <span data-ttu-id="7bd0d-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bd0d-163">OUTPUTS</span></span>

## <span data-ttu-id="7bd0d-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bd0d-164">NOTES</span></span>

## <span data-ttu-id="7bd0d-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bd0d-165">RELATED LINKS</span></span>

[<span data-ttu-id="7bd0d-166">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="7bd0d-166">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="7bd0d-167">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7bd0d-167">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="7bd0d-168">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="7bd0d-168">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="7bd0d-169">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="7bd0d-169">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="7bd0d-170">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7bd0d-170">Update-AzureVM</span></span>](./Update-AzureVM.md)


