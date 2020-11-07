---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5CAF2D29-F4AE-4322-AA4F-61267723B955
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2e19ad4b56e5141458f1fe9305a0c33691d024d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945497"
---
# <span data-ttu-id="c096c-101">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="c096c-101">Remove-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="c096c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c096c-102">SYNOPSIS</span></span>
<span data-ttu-id="c096c-103">Remove a configuração de disco de dados do objeto DiskConfigSet.</span><span class="sxs-lookup"><span data-stu-id="c096c-103">Removes the data disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="c096c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c096c-104">SYNTAX</span></span>

### <span data-ttu-id="c096c-105">RemoveByDiskName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c096c-105">RemoveByDiskName (Default)</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c096c-106">RemoveByDiskLun</span><span class="sxs-lookup"><span data-stu-id="c096c-106">RemoveByDiskLun</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c096c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c096c-107">DESCRIPTION</span></span>
<span data-ttu-id="c096c-108">O cmdlet **Remove-AzureVMImageDataDiskConfig** remove a configuração de disco de dados do objeto **DiskConfigSet** .</span><span class="sxs-lookup"><span data-stu-id="c096c-108">The **Remove-AzureVMImageDataDiskConfig** cmdlet removes the data disk configuration from the **DiskConfigSet** object.</span></span>

## <span data-ttu-id="c096c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c096c-109">EXAMPLES</span></span>

### <span data-ttu-id="c096c-110">Exemplo 1: remover a configuração de disco de dados do objeto DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="c096c-110">Example 1: Remove the data disk configuration from the DiskConfigSet object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="c096c-111">Este exemplo cria um **DiskConfigSet** , configura o disco de dados e, em seguida, remove o disco de dados.</span><span class="sxs-lookup"><span data-stu-id="c096c-111">This example creates a **DiskConfigSet** , configures it, then removes the data disk.</span></span>

## <span data-ttu-id="c096c-112">OS</span><span class="sxs-lookup"><span data-stu-id="c096c-112">PARAMETERS</span></span>

### <span data-ttu-id="c096c-113">-Datadiskname</span><span class="sxs-lookup"><span data-stu-id="c096c-113">-DataDiskName</span></span>
<span data-ttu-id="c096c-114">Especifica o nome do disco de dados que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c096c-114">Specifies the name of the data disk that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDiskName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c096c-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="c096c-115">-DiskConfig</span></span>
<span data-ttu-id="c096c-116">Especifica o objeto de configuração de disco que encapsula o disco do sistema operacional e os objetos de disco de dados.</span><span class="sxs-lookup"><span data-stu-id="c096c-116">Specifies the disk configuration object that encapsulates the operating system disk and data disk objects.</span></span>

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

### <span data-ttu-id="c096c-117">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="c096c-117">-InformationAction</span></span>
<span data-ttu-id="c096c-118">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="c096c-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c096c-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c096c-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c096c-120">Contínuo</span><span class="sxs-lookup"><span data-stu-id="c096c-120">Continue</span></span>
- <span data-ttu-id="c096c-121">Ignorar</span><span class="sxs-lookup"><span data-stu-id="c096c-121">Ignore</span></span>
- <span data-ttu-id="c096c-122">Inquire</span><span class="sxs-lookup"><span data-stu-id="c096c-122">Inquire</span></span>
- <span data-ttu-id="c096c-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c096c-123">SilentlyContinue</span></span>
- <span data-ttu-id="c096c-124">Finaliza</span><span class="sxs-lookup"><span data-stu-id="c096c-124">Stop</span></span>
- <span data-ttu-id="c096c-125">Suspensão</span><span class="sxs-lookup"><span data-stu-id="c096c-125">Suspend</span></span>

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

### <span data-ttu-id="c096c-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c096c-126">-InformationVariable</span></span>
<span data-ttu-id="c096c-127">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="c096c-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c096c-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="c096c-128">-Lun</span></span>
<span data-ttu-id="c096c-129">Especifica o slot em que a unidade de dados está montada na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c096c-129">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveByDiskLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c096c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c096c-130">CommonParameters</span></span>
<span data-ttu-id="c096c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c096c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c096c-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c096c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c096c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c096c-133">INPUTS</span></span>

## <span data-ttu-id="c096c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c096c-134">OUTPUTS</span></span>

### <span data-ttu-id="c096c-135">Microsoft. WindowsAzure. Commands. onmanagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="c096c-135">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="c096c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c096c-136">NOTES</span></span>

## <span data-ttu-id="c096c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c096c-137">RELATED LINKS</span></span>

[<span data-ttu-id="c096c-138">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="c096c-138">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


