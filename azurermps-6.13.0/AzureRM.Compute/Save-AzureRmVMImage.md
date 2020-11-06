---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: b6d8d21eea863683912e204403ebe5a75ac40fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426410"
---
# <span data-ttu-id="95ce6-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="95ce6-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="95ce6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="95ce6-103">Salva uma máquina virtual como uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="95ce6-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95ce6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95ce6-104">SYNTAX</span></span>

### <span data-ttu-id="95ce6-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="95ce6-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95ce6-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="95ce6-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95ce6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95ce6-107">DESCRIPTION</span></span>
<span data-ttu-id="95ce6-108">O cmdlet **Save-AzureRmVMImage** salva uma máquina virtual como uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="95ce6-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="95ce6-109">Antes de criar uma imagem de máquina virtual, Sysprep a máquina virtual e marcá-la como generalizada usando o cmdlet Set-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="95ce6-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="95ce6-110">A saída desse cmdlet é um modelo JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="95ce6-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="95ce6-111">Você pode implantar máquinas virtuais a partir da sua imagem capturada.</span><span class="sxs-lookup"><span data-stu-id="95ce6-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="95ce6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95ce6-112">EXAMPLES</span></span>

### <span data-ttu-id="95ce6-113">Exemplo 1: capturar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="95ce6-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="95ce6-114">O primeiro comando marca a máquina virtual chamada VirtualMachine07 como generalizada.</span><span class="sxs-lookup"><span data-stu-id="95ce6-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="95ce6-115">O segundo comando captura uma máquina virtual nomeada VirtualMachine07 como uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="95ce6-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="95ce6-116">A propriedade **output** retorna um modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="95ce6-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="95ce6-117">OS</span><span class="sxs-lookup"><span data-stu-id="95ce6-117">PARAMETERS</span></span>

### <span data-ttu-id="95ce6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95ce6-118">-AsJob</span></span>
<span data-ttu-id="95ce6-119">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="95ce6-119">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ce6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ce6-120">-DefaultProfile</span></span>
<span data-ttu-id="95ce6-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95ce6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ce6-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="95ce6-122">-DestinationContainerName</span></span>
<span data-ttu-id="95ce6-123">Especifica o nome de um contêiner dentro do contêiner "sistema" no qual você deseja armazenar as imagens.</span><span class="sxs-lookup"><span data-stu-id="95ce6-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="95ce6-124">Se o contêiner não existir, ele será criado para você.</span><span class="sxs-lookup"><span data-stu-id="95ce6-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="95ce6-125">Os VHDs (discos rígidos virtuais) que constituem a VMImage residem no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="95ce6-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="95ce6-126">Se os VHDs estiverem espalhados em várias contas de armazenamento, esse cmdlet cria um contêiner que tem esse nome em cada conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="95ce6-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="95ce6-127">A URL da imagem salva é semelhante a: https:// \<storageAccountName\> . blob.Core.Windows.NET/System/Microsoft.Compute/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="95ce6-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ce6-128">-ID</span><span class="sxs-lookup"><span data-stu-id="95ce6-128">-Id</span></span>
<span data-ttu-id="95ce6-129">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="95ce6-129">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ce6-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="95ce6-130">-Name</span></span>
<span data-ttu-id="95ce6-131">Especifica um nome.</span><span class="sxs-lookup"><span data-stu-id="95ce6-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ce6-132">-Substituir</span><span class="sxs-lookup"><span data-stu-id="95ce6-132">-Overwrite</span></span>
<span data-ttu-id="95ce6-133">Indica que esse cmdlet substitui todos os VHDs que têm o mesmo prefixo no contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="95ce6-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ce6-134">-Caminho</span><span class="sxs-lookup"><span data-stu-id="95ce6-134">-Path</span></span>
<span data-ttu-id="95ce6-135">O caminho do arquivo no qual o modelo da imagem capturada está armazenado.</span><span class="sxs-lookup"><span data-stu-id="95ce6-135">The file path in which the template of the captured image is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ce6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ce6-136">-ResourceGroupName</span></span>
<span data-ttu-id="95ce6-137">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="95ce6-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ce6-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="95ce6-138">-VHDNamePrefix</span></span>
<span data-ttu-id="95ce6-139">Especifica o prefixo no nome dos BLOBs que constituem o perfil de armazenamento da VMImage.</span><span class="sxs-lookup"><span data-stu-id="95ce6-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="95ce6-140">Por exemplo, um prefixo vhdPrefix para um disco do sistema operacional resulta no nome vhdPrefix-OSDisk. \<guid\> . Wim.</span><span class="sxs-lookup"><span data-stu-id="95ce6-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ce6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ce6-141">CommonParameters</span></span>
<span data-ttu-id="95ce6-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ce6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ce6-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95ce6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ce6-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95ce6-144">INPUTS</span></span>

### <span data-ttu-id="95ce6-145">System. String</span><span class="sxs-lookup"><span data-stu-id="95ce6-145">System.String</span></span>

### <span data-ttu-id="95ce6-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="95ce6-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="95ce6-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95ce6-147">OUTPUTS</span></span>

### <span data-ttu-id="95ce6-148">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="95ce6-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="95ce6-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95ce6-149">NOTES</span></span>

## <span data-ttu-id="95ce6-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95ce6-150">RELATED LINKS</span></span>

[<span data-ttu-id="95ce6-151">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="95ce6-151">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="95ce6-152">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="95ce6-152">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="95ce6-153">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="95ce6-153">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="95ce6-154">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="95ce6-154">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="95ce6-155">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95ce6-155">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


