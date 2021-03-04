---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: d979e89583b19270dfd13bae85a3afe1505ed55e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891409"
---
# <span data-ttu-id="bdd9e-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="bdd9e-101">Save-AzVMImage</span></span>

## <span data-ttu-id="bdd9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdd9e-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd9e-103">Salva uma máquina virtual como uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="bdd9e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bdd9e-104">SYNTAX</span></span>

### <span data-ttu-id="bdd9e-105">ResourceGroupNameParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bdd9e-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bdd9e-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bdd9e-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdd9e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bdd9e-107">DESCRIPTION</span></span>
<span data-ttu-id="bdd9e-108">O cmdlet **Save-AzVMImage** salva uma máquina virtual como uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="bdd9e-109">Antes de criar uma imagem de máquina virtual, sysprep a máquina virtual e marcá-la como generalizada usando o cmdlet Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="bdd9e-110">A saída desse cmdlet é um modelo JSON (Notação de Objeto JavaScript).</span><span class="sxs-lookup"><span data-stu-id="bdd9e-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="bdd9e-111">Você pode implantar máquinas virtuais a partir de sua imagem capturada.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="bdd9e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdd9e-112">EXAMPLES</span></span>

### <span data-ttu-id="bdd9e-113">Exemplo 1: Capturar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="bdd9e-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="bdd9e-114">O primeiro comando marca a máquina virtual chamada VirtualMachine07 como generalizada.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="bdd9e-115">O segundo comando captura uma máquina virtual chamada VirtualMachine07 como uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="bdd9e-116">A **propriedade Output** retorna um modelo JSON.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="bdd9e-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bdd9e-117">PARAMETERS</span></span>

### <span data-ttu-id="bdd9e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdd9e-118">-AsJob</span></span>
<span data-ttu-id="bdd9e-119">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bdd9e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd9e-120">-DefaultProfile</span></span>
<span data-ttu-id="bdd9e-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdd9e-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="bdd9e-122">-DestinationContainerName</span></span>
<span data-ttu-id="bdd9e-123">Especifica o nome de um contêiner dentro do contêiner "sistema" que você deseja manter suas imagens.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="bdd9e-124">Se o contêiner não existir, ele será criado para você.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="bdd9e-125">Os discos rígidos virtuais (VHDs) que constituem o VMImage residem no contêiner especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="bdd9e-126">Se os VHDs estão espalhados por várias contas de armazenamento, esse cmdlet criará um contêiner com esse nome em cada conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="bdd9e-127">A URL da imagem salva é semelhante a: https:// \<storageAccountName\> \<imagesContainer\> / \<vhdPrefix-osDisk\> .blob.core.windows.net/system/Microsoft.Compute/Images/ .xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="bdd9e-128">-Id</span><span class="sxs-lookup"><span data-stu-id="bdd9e-128">-Id</span></span>
<span data-ttu-id="bdd9e-129">Especifica a ID de Recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="bdd9e-130">-Name</span><span class="sxs-lookup"><span data-stu-id="bdd9e-130">-Name</span></span>
<span data-ttu-id="bdd9e-131">Especifica um nome.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-131">Specifies a name.</span></span>

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

### <span data-ttu-id="bdd9e-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="bdd9e-132">-Overwrite</span></span>
<span data-ttu-id="bdd9e-133">Indica que esse cmdlet substitui quaisquer VHDs que tenham o mesmo prefixo no contêiner de destino.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="bdd9e-134">-Path</span><span class="sxs-lookup"><span data-stu-id="bdd9e-134">-Path</span></span>
<span data-ttu-id="bdd9e-135">O caminho do arquivo no qual o modelo da imagem capturada é armazenado.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="bdd9e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd9e-136">-ResourceGroupName</span></span>
<span data-ttu-id="bdd9e-137">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bdd9e-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="bdd9e-138">-VHDNamePrefix</span></span>
<span data-ttu-id="bdd9e-139">Especifica o prefixo no nome dos blobs que constituem o perfil de armazenamento do VMImage.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="bdd9e-140">Por exemplo, um prefixo vhdPrefix para um disco do sistema operacional resulta no nome vhdPrefix-osdisk. \<guid\> . vhd.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="bdd9e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd9e-141">CommonParameters</span></span>
<span data-ttu-id="bdd9e-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdd9e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd9e-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdd9e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd9e-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdd9e-144">INPUTS</span></span>

### <span data-ttu-id="bdd9e-145">System.String</span><span class="sxs-lookup"><span data-stu-id="bdd9e-145">System.String</span></span>

### <span data-ttu-id="bdd9e-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bdd9e-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bdd9e-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bdd9e-147">OUTPUTS</span></span>

### <span data-ttu-id="bdd9e-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="bdd9e-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="bdd9e-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="bdd9e-149">NOTES</span></span>

## <span data-ttu-id="bdd9e-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdd9e-150">RELATED LINKS</span></span>

[<span data-ttu-id="bdd9e-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="bdd9e-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="bdd9e-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="bdd9e-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="bdd9e-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="bdd9e-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="bdd9e-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="bdd9e-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="bdd9e-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="bdd9e-155">Set-AzVM</span></span>](./Set-AzVM.md)


