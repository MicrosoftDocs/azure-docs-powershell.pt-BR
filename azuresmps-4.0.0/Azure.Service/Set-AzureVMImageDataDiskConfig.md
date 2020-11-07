---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6C7CB0AE-C788-4E6F-AD48-E30B547A2269
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7512ef446227742c2a3564c5f3e5f38f1e2ccce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945436"
---
# <span data-ttu-id="cda44-101">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="cda44-101">Set-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="cda44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cda44-102">SYNOPSIS</span></span>
<span data-ttu-id="cda44-103">Define as propriedades do disco de dados na imagem da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cda44-103">Sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="cda44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cda44-104">SYNTAX</span></span>

### <span data-ttu-id="cda44-105">UpdateAzureVMImageParamSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cda44-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-Lun] <Int32> [-HostCaching] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="cda44-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="cda44-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-HostCaching] <String> [-MediaLink] <Uri> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cda44-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cda44-107">DESCRIPTION</span></span>
<span data-ttu-id="cda44-108">O cmdlet **set-AzureVMImageDataDiskConfig** define as propriedades do disco de dados na imagem da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cda44-108">The **Set-AzureVMImageDataDiskConfig** cmdlet sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="cda44-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cda44-109">EXAMPLES</span></span>

### <span data-ttu-id="cda44-110">Exemplo 1: definir propriedades de disco de dados em uma imagem de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="cda44-110">Example 1: Set Data Disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="cda44-111">Esse comando define as propriedades do disco de dados em uma máquina virtual e atualiza a imagem da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cda44-111">This command sets data disk properties on a virtual machine then updates the virtual machine image.</span></span>

## <span data-ttu-id="cda44-112">OS</span><span class="sxs-lookup"><span data-stu-id="cda44-112">PARAMETERS</span></span>

### <span data-ttu-id="cda44-113">-Datadiskname</span><span class="sxs-lookup"><span data-stu-id="cda44-113">-DataDiskName</span></span>
<span data-ttu-id="cda44-114">Especifica o nome do disco de dados que este cmdlet configura.</span><span class="sxs-lookup"><span data-stu-id="cda44-114">Specifies the name of the data disk that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: UpdateAzureVMImageParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda44-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="cda44-115">-DiskConfig</span></span>
<span data-ttu-id="cda44-116">Especifica o objeto de configuração de disco que encapsula o disco do sistema operacional e os objetos de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="cda44-116">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="cda44-117">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="cda44-117">-HostCaching</span></span>
<span data-ttu-id="cda44-118">Especifica o atributo de cache do host para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cda44-118">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="cda44-119">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="cda44-119">Valid values are:</span></span>

<span data-ttu-id="cda44-120">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cda44-120">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda44-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="cda44-121">-InformationAction</span></span>
<span data-ttu-id="cda44-122">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="cda44-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cda44-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cda44-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cda44-124">Contínuo</span><span class="sxs-lookup"><span data-stu-id="cda44-124">Continue</span></span>
- <span data-ttu-id="cda44-125">Ignorar</span><span class="sxs-lookup"><span data-stu-id="cda44-125">Ignore</span></span>
- <span data-ttu-id="cda44-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="cda44-126">Inquire</span></span>
- <span data-ttu-id="cda44-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cda44-127">SilentlyContinue</span></span>
- <span data-ttu-id="cda44-128">Finaliza</span><span class="sxs-lookup"><span data-stu-id="cda44-128">Stop</span></span>
- <span data-ttu-id="cda44-129">Suspensão</span><span class="sxs-lookup"><span data-stu-id="cda44-129">Suspend</span></span>

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

### <span data-ttu-id="cda44-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cda44-130">-InformationVariable</span></span>
<span data-ttu-id="cda44-131">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="cda44-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cda44-132">-LUN</span><span class="sxs-lookup"><span data-stu-id="cda44-132">-Lun</span></span>
<span data-ttu-id="cda44-133">Especifica o slot em que a unidade de dados está montada na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cda44-133">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda44-134">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="cda44-134">-MediaLink</span></span>
<span data-ttu-id="cda44-135">Especifica o URI do local onde a nova unidade de disco rígido virtual é criada quando o novo disco de dados é adicionado.</span><span class="sxs-lookup"><span data-stu-id="cda44-135">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda44-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda44-136">CommonParameters</span></span>
<span data-ttu-id="cda44-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda44-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda44-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cda44-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda44-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cda44-139">INPUTS</span></span>

## <span data-ttu-id="cda44-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cda44-140">OUTPUTS</span></span>

### <span data-ttu-id="cda44-141">Microsoft. WindowsAzure. Commands. onmanagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="cda44-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="cda44-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cda44-142">NOTES</span></span>

## <span data-ttu-id="cda44-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cda44-143">RELATED LINKS</span></span>

[<span data-ttu-id="cda44-144">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="cda44-144">Remove-AzureVMImageDataDiskConfig</span></span>](./Remove-AzureVMImageDataDiskConfig.md)


