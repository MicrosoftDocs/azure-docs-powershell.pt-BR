---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9CD39F1C-D858-4275-A6DE-10901DC962FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cb2557b411d46ce718f97ba7939efb4571ce025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945444"
---
# <span data-ttu-id="628c1-101">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="628c1-101">Set-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="628c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="628c1-102">SYNOPSIS</span></span>
<span data-ttu-id="628c1-103">Define as propriedades de disco do sistema operacional em uma imagem de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="628c1-103">Sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="628c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="628c1-104">SYNTAX</span></span>

### <span data-ttu-id="628c1-105">UpdateAzureVMImageParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="628c1-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="628c1-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="628c1-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-MediaLink] <Uri> [-OSState] <String> [-OS] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="628c1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="628c1-107">DESCRIPTION</span></span>
<span data-ttu-id="628c1-108">O cmdlet **set-AzureVMImageOSDiskConfig** define as propriedades de disco do sistema operacional em uma imagem de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="628c1-108">The **Set-AzureVMImageOSDiskConfig** cmdlet sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="628c1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="628c1-109">EXAMPLES</span></span>

### <span data-ttu-id="628c1-110">Exemplo 1: definir as propriedades de disco do sistema operacional em uma imagem de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="628c1-110">Example 1: Set the operating system disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="628c1-111">Este exemplo define as propriedades de disco do sistema operacional em uma imagem de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="628c1-111">This example sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="628c1-112">OS</span><span class="sxs-lookup"><span data-stu-id="628c1-112">PARAMETERS</span></span>

### <span data-ttu-id="628c1-113">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="628c1-113">-DiskConfig</span></span>
<span data-ttu-id="628c1-114">Especifica o objeto de configuração de disco que encapsula o disco do sistema operacional e os objetos de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="628c1-114">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="628c1-115">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="628c1-115">-HostCaching</span></span>
<span data-ttu-id="628c1-116">Especifica o atributo de cache do host para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="628c1-116">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="628c1-117">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="628c1-117">Valid values are:</span></span>

<span data-ttu-id="628c1-118">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="628c1-118">--ReadOnly --ReadWrite</span></span>

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

### <span data-ttu-id="628c1-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="628c1-119">-InformationAction</span></span>
<span data-ttu-id="628c1-120">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="628c1-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="628c1-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="628c1-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="628c1-122">Contínuo</span><span class="sxs-lookup"><span data-stu-id="628c1-122">Continue</span></span>
- <span data-ttu-id="628c1-123">Ignorar</span><span class="sxs-lookup"><span data-stu-id="628c1-123">Ignore</span></span>
- <span data-ttu-id="628c1-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="628c1-124">Inquire</span></span>
- <span data-ttu-id="628c1-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="628c1-125">SilentlyContinue</span></span>
- <span data-ttu-id="628c1-126">Finaliza</span><span class="sxs-lookup"><span data-stu-id="628c1-126">Stop</span></span>
- <span data-ttu-id="628c1-127">Suspensão</span><span class="sxs-lookup"><span data-stu-id="628c1-127">Suspend</span></span>

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

### <span data-ttu-id="628c1-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="628c1-128">-InformationVariable</span></span>
<span data-ttu-id="628c1-129">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="628c1-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="628c1-130">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="628c1-130">-MediaLink</span></span>
<span data-ttu-id="628c1-131">Especifica o URI do local onde a nova unidade de disco rígido virtual é criada quando o novo disco de dados é adicionado.</span><span class="sxs-lookup"><span data-stu-id="628c1-131">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628c1-132">-OS</span><span class="sxs-lookup"><span data-stu-id="628c1-132">-OS</span></span>
<span data-ttu-id="628c1-133">Especifica o sistema operacional da configuração de disco.</span><span class="sxs-lookup"><span data-stu-id="628c1-133">Specifies the operating system of the disk configuration.</span></span>

<span data-ttu-id="628c1-134">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="628c1-134">Valid values are:</span></span>

- <span data-ttu-id="628c1-135">Windows</span><span class="sxs-lookup"><span data-stu-id="628c1-135">Windows</span></span>
- <span data-ttu-id="628c1-136">Linux</span><span class="sxs-lookup"><span data-stu-id="628c1-136">Linux</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628c1-137">-OSState</span><span class="sxs-lookup"><span data-stu-id="628c1-137">-OSState</span></span>
<span data-ttu-id="628c1-138">Especifica o estado do sistema operacional para a imagem da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="628c1-138">Specifies the operating system state for virtual machine image</span></span>

<span data-ttu-id="628c1-139">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="628c1-139">Valid values are:</span></span>

- <span data-ttu-id="628c1-140">Generalizado</span><span class="sxs-lookup"><span data-stu-id="628c1-140">Generalized</span></span>
- <span data-ttu-id="628c1-141">Especialistas</span><span class="sxs-lookup"><span data-stu-id="628c1-141">Specialized</span></span>

<span data-ttu-id="628c1-142">O uso desse parâmetro indica sua intenção de capturar a imagem da máquina virtual para o Azure.</span><span class="sxs-lookup"><span data-stu-id="628c1-142">The use of this parameter indicates your intent to capture the virtual machine image to Azure.</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628c1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="628c1-143">CommonParameters</span></span>
<span data-ttu-id="628c1-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="628c1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="628c1-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="628c1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="628c1-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="628c1-146">INPUTS</span></span>

## <span data-ttu-id="628c1-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="628c1-147">OUTPUTS</span></span>

### <span data-ttu-id="628c1-148">Microsoft. WindowsAzure. Commands. onmanagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="628c1-148">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="628c1-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="628c1-149">NOTES</span></span>

## <span data-ttu-id="628c1-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="628c1-150">RELATED LINKS</span></span>

[<span data-ttu-id="628c1-151">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="628c1-151">Remove-AzureVMImageOSDiskConfig</span></span>](./Remove-AzureVMImageOSDiskConfig.md)


