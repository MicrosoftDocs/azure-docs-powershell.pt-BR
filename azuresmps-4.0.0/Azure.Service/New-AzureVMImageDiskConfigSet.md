---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946198"
---
# <span data-ttu-id="08e18-101">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="08e18-101">New-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="08e18-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08e18-102">SYNOPSIS</span></span>
<span data-ttu-id="08e18-103">Cria um objeto do conjunto de configuração de disco.</span><span class="sxs-lookup"><span data-stu-id="08e18-103">Creates a disk configuration set object.</span></span>

## <span data-ttu-id="08e18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08e18-104">SYNTAX</span></span>

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="08e18-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08e18-105">DESCRIPTION</span></span>
<span data-ttu-id="08e18-106">O cmdlet **New-AzureVMImageDiskConfigSet** cria um objeto do conjunto de configuração de disco que é passado para o cmdlet de atualização de imagem.</span><span class="sxs-lookup"><span data-stu-id="08e18-106">The **New-AzureVMImageDiskConfigSet** cmdlet creates a disk configuration set object that is passed to the image update cmdlet.</span></span>
<span data-ttu-id="08e18-107">Ele encapsula o OSDiskConfig e o objeto DataDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="08e18-107">It encapsulates the OSDiskConfig and the DataDiskConfig object.</span></span>
<span data-ttu-id="08e18-108">Use os cmdlets **set-AzureVMImageOSDiskConfig** e **set-AzureVMImageDataDiskConfig** para definir as propriedades do disco do sistema operacional e do disco de dados para a imagem da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="08e18-108">Use the **Set-AzureVMImageOSDiskConfig** and **Set-AzureVMImageDataDiskConfig** cmdlets to set the OS Disk and Data Disk properties for the virtual machine image.</span></span>

## <span data-ttu-id="08e18-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08e18-109">EXAMPLES</span></span>

### <span data-ttu-id="08e18-110">Exemplo 1: criar um objeto do conjunto de configuração de disco</span><span class="sxs-lookup"><span data-stu-id="08e18-110">Example 1: Create a disk configuration set object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="08e18-111">Esse comando cria um objeto do conjunto de configuração de disco e armazena os resultados na variável chamada $Disk.</span><span class="sxs-lookup"><span data-stu-id="08e18-111">This command creates a disk configuration set object and stores the results in the variable named $Disk.</span></span>
<span data-ttu-id="08e18-112">Após a criação da configuração do disco, ele é usado para definir o OSDiskConfig e o DataDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="08e18-112">After the disk configuration is created, it is used to set the OSDiskConfig and DataDiskConfig.</span></span>
<span data-ttu-id="08e18-113">Em seguida, a máquina virtual é atualizada com a configuração.</span><span class="sxs-lookup"><span data-stu-id="08e18-113">Then the virtual machine is updated with the configuration.</span></span>

## <span data-ttu-id="08e18-114">OS</span><span class="sxs-lookup"><span data-stu-id="08e18-114">PARAMETERS</span></span>

### <span data-ttu-id="08e18-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="08e18-115">-InformationAction</span></span>
<span data-ttu-id="08e18-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="08e18-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="08e18-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="08e18-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08e18-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="08e18-118">Continue</span></span>
- <span data-ttu-id="08e18-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="08e18-119">Ignore</span></span>
- <span data-ttu-id="08e18-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="08e18-120">Inquire</span></span>
- <span data-ttu-id="08e18-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="08e18-121">SilentlyContinue</span></span>
- <span data-ttu-id="08e18-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="08e18-122">Stop</span></span>
- <span data-ttu-id="08e18-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="08e18-123">Suspend</span></span>

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

### <span data-ttu-id="08e18-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="08e18-124">-InformationVariable</span></span>
<span data-ttu-id="08e18-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="08e18-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="08e18-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e18-126">CommonParameters</span></span>
<span data-ttu-id="08e18-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e18-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e18-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e18-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e18-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08e18-129">INPUTS</span></span>

## <span data-ttu-id="08e18-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08e18-130">OUTPUTS</span></span>

### <span data-ttu-id="08e18-131">Microsoft. WindowsAzure. Commands. onmanagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="08e18-131">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="08e18-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08e18-132">NOTES</span></span>

## <span data-ttu-id="08e18-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08e18-133">RELATED LINKS</span></span>

[<span data-ttu-id="08e18-134">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="08e18-134">Get-AzureVMImageDiskConfigSet</span></span>](./Get-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="08e18-135">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="08e18-135">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="08e18-136">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="08e18-136">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


