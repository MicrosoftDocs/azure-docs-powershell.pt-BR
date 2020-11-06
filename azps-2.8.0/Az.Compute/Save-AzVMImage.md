---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: 6ce551cb848a1f63129353aee8a388fb19cb8bfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597261"
---
# <span data-ttu-id="a80db-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a80db-101">Save-AzVMImage</span></span>

## <span data-ttu-id="a80db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a80db-102">SYNOPSIS</span></span>
<span data-ttu-id="a80db-103">Salva uma máquina virtual como uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="a80db-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="a80db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a80db-104">SYNTAX</span></span>

### <span data-ttu-id="a80db-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a80db-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a80db-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a80db-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a80db-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a80db-107">DESCRIPTION</span></span>
<span data-ttu-id="a80db-108">O cmdlet **Save-AzVMImage** salva uma máquina virtual como uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="a80db-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="a80db-109">Antes de criar uma imagem de máquina virtual, Sysprep a máquina virtual e marcá-la como generalizada usando o cmdlet Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="a80db-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="a80db-110">A saída desse cmdlet é um modelo JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="a80db-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="a80db-111">Você pode implantar máquinas virtuais a partir da sua imagem capturada.</span><span class="sxs-lookup"><span data-stu-id="a80db-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="a80db-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a80db-112">EXAMPLES</span></span>

### <span data-ttu-id="a80db-113">Exemplo 1: capturar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="a80db-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="a80db-114">O primeiro comando marca a máquina virtual chamada VirtualMachine07 como generalizada.</span><span class="sxs-lookup"><span data-stu-id="a80db-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="a80db-115">O segundo comando captura uma máquina virtual nomeada VirtualMachine07 como uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="a80db-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="a80db-116">A propriedade **output** retorna um modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="a80db-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="a80db-117">OS</span><span class="sxs-lookup"><span data-stu-id="a80db-117">PARAMETERS</span></span>

### <span data-ttu-id="a80db-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a80db-118">-AsJob</span></span>
<span data-ttu-id="a80db-119">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="a80db-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a80db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a80db-120">-DefaultProfile</span></span>
<span data-ttu-id="a80db-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a80db-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a80db-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="a80db-122">-DestinationContainerName</span></span>
<span data-ttu-id="a80db-123">Especifica o nome de um contêiner dentro do contêiner "sistema" no qual você deseja armazenar as imagens.</span><span class="sxs-lookup"><span data-stu-id="a80db-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="a80db-124">Se o contêiner não existir, ele será criado para você.</span><span class="sxs-lookup"><span data-stu-id="a80db-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="a80db-125">Os VHDs (discos rígidos virtuais) que constituem a VMImage residem no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a80db-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="a80db-126">Se os VHDs estiverem espalhados em várias contas de armazenamento, esse cmdlet cria um contêiner que tem esse nome em cada conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a80db-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="a80db-127">A URL da imagem salva é semelhante a: https:// \< storageAccountName \> . blob.Core.Windows.NET/System/Microsoft.Compute/images/ \< imagesContainer \> / \< vhdPrefix-osDisk \> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.</span><span class="sxs-lookup"><span data-stu-id="a80db-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="a80db-128">-ID</span><span class="sxs-lookup"><span data-stu-id="a80db-128">-Id</span></span>
<span data-ttu-id="a80db-129">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a80db-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="a80db-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="a80db-130">-Name</span></span>
<span data-ttu-id="a80db-131">Especifica um nome.</span><span class="sxs-lookup"><span data-stu-id="a80db-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a80db-132">-Substituir</span><span class="sxs-lookup"><span data-stu-id="a80db-132">-Overwrite</span></span>
<span data-ttu-id="a80db-133">Indica que esse cmdlet substitui todos os VHDs que têm o mesmo prefixo no contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="a80db-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="a80db-134">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a80db-134">-Path</span></span>
<span data-ttu-id="a80db-135">O caminho do arquivo no qual o modelo da imagem capturada está armazenado.</span><span class="sxs-lookup"><span data-stu-id="a80db-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="a80db-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a80db-136">-ResourceGroupName</span></span>
<span data-ttu-id="a80db-137">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a80db-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a80db-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="a80db-138">-VHDNamePrefix</span></span>
<span data-ttu-id="a80db-139">Especifica o prefixo no nome dos BLOBs que constituem o perfil de armazenamento da VMImage.</span><span class="sxs-lookup"><span data-stu-id="a80db-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="a80db-140">Por exemplo, um prefixo vhdPrefix para um disco do sistema operacional resulta no nome vhdPrefix-OSDisk. \< GUID \> . vhd.</span><span class="sxs-lookup"><span data-stu-id="a80db-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="a80db-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a80db-141">CommonParameters</span></span>
<span data-ttu-id="a80db-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a80db-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a80db-143">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a80db-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a80db-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a80db-144">INPUTS</span></span>

### <span data-ttu-id="a80db-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a80db-145">System.String</span></span>

### <span data-ttu-id="a80db-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a80db-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a80db-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a80db-147">OUTPUTS</span></span>

### <span data-ttu-id="a80db-148">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a80db-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="a80db-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a80db-149">NOTES</span></span>

## <span data-ttu-id="a80db-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a80db-150">RELATED LINKS</span></span>

[<span data-ttu-id="a80db-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a80db-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="a80db-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a80db-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="a80db-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a80db-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a80db-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a80db-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="a80db-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="a80db-155">Set-AzVM</span></span>](./Set-AzVM.md)


