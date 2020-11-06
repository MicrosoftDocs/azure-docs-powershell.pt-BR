---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: 8f3aebe1e9e79423d7251fa79084d6fa85407b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440498"
---
# <span data-ttu-id="8275e-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8275e-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="8275e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8275e-102">SYNOPSIS</span></span>
<span data-ttu-id="8275e-103">Salva uma máquina virtual como uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="8275e-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8275e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8275e-104">SYNTAX</span></span>

### <span data-ttu-id="8275e-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8275e-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [<CommonParameters>]
```

### <span data-ttu-id="8275e-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8275e-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [<CommonParameters>]
```

## <span data-ttu-id="8275e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8275e-107">DESCRIPTION</span></span>
<span data-ttu-id="8275e-108">O cmdlet **Save-AzureRmVMImage** salva uma máquina virtual como uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="8275e-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="8275e-109">Antes de criar uma imagem de máquina virtual, Sysprep a máquina virtual e marcá-la como generalizada usando o cmdlet Set-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="8275e-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="8275e-110">A saída desse cmdlet é um modelo JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="8275e-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="8275e-111">Você pode implantar máquinas virtuais a partir da sua imagem capturada.</span><span class="sxs-lookup"><span data-stu-id="8275e-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="8275e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8275e-112">EXAMPLES</span></span>

### <span data-ttu-id="8275e-113">Exemplo 1: capturar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8275e-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="8275e-114">O primeiro comando marca a máquina virtual chamada VirtualMachine07 como generalizada.</span><span class="sxs-lookup"><span data-stu-id="8275e-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="8275e-115">O segundo comando captura uma máquina virtual nomeada VirtualMachine07 como uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="8275e-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="8275e-116">A propriedade **output** retorna um modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="8275e-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="8275e-117">OS</span><span class="sxs-lookup"><span data-stu-id="8275e-117">PARAMETERS</span></span>

### <span data-ttu-id="8275e-118">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="8275e-118">-DestinationContainerName</span></span>
<span data-ttu-id="8275e-119">Especifica o nome de um contêiner dentro do contêiner "sistema" no qual você deseja armazenar as imagens.</span><span class="sxs-lookup"><span data-stu-id="8275e-119">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="8275e-120">Se o contêiner não existir, ele será criado para você.</span><span class="sxs-lookup"><span data-stu-id="8275e-120">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="8275e-121">Os VHDs (discos rígidos virtuais) que constituem a VMImage residem no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="8275e-121">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="8275e-122">Se os VHDs estiverem espalhados em várias contas de armazenamento, esse cmdlet cria um contêiner que tem esse nome em cada conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8275e-122">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="8275e-123">A URL da imagem salva é semelhante a:</span><span class="sxs-lookup"><span data-stu-id="8275e-123">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="8275e-124"> https:// \<storageAccountName\> . blob.Core.Windows.NET/System/Microsoft.Compute/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="8275e-124">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8275e-125">-ID</span><span class="sxs-lookup"><span data-stu-id="8275e-125">-Id</span></span>
<span data-ttu-id="8275e-126">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8275e-126">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8275e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="8275e-127">-Name</span></span>
<span data-ttu-id="8275e-128">Especifica um nome.</span><span class="sxs-lookup"><span data-stu-id="8275e-128">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8275e-129">-Substituir</span><span class="sxs-lookup"><span data-stu-id="8275e-129">-Overwrite</span></span>
<span data-ttu-id="8275e-130">Indica que esse cmdlet substitui todos os VHDs que têm o mesmo prefixo no contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="8275e-130">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8275e-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="8275e-131">-Path</span></span>
<span data-ttu-id="8275e-132">Especifica o caminho do VHD.</span><span class="sxs-lookup"><span data-stu-id="8275e-132">Specifies the path of the VHD.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8275e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8275e-133">-ResourceGroupName</span></span>
<span data-ttu-id="8275e-134">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8275e-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8275e-135">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="8275e-135">-VHDNamePrefix</span></span>
<span data-ttu-id="8275e-136">Especifica o prefixo no nome dos BLOBs que constituem o perfil de armazenamento da VMImage.</span><span class="sxs-lookup"><span data-stu-id="8275e-136">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="8275e-137">Por exemplo, um prefixo vhdPrefix para um disco do sistema operacional resulta no nome vhdPrefix-OSDisk. \<guid\> . Wim.</span><span class="sxs-lookup"><span data-stu-id="8275e-137">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8275e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8275e-138">CommonParameters</span></span>
<span data-ttu-id="8275e-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8275e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8275e-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8275e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8275e-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8275e-141">INPUTS</span></span>

### <span data-ttu-id="8275e-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8275e-142">None</span></span>
<span data-ttu-id="8275e-143">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8275e-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8275e-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8275e-144">OUTPUTS</span></span>

## <span data-ttu-id="8275e-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8275e-145">NOTES</span></span>

## <span data-ttu-id="8275e-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8275e-146">RELATED LINKS</span></span>

[<span data-ttu-id="8275e-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8275e-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="8275e-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8275e-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="8275e-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8275e-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="8275e-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8275e-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="8275e-151">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8275e-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


