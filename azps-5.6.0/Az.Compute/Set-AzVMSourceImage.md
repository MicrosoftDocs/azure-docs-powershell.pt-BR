---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: ac02e3c54500e1ba104c4deb323bb7257fa3e71b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889553"
---
# <span data-ttu-id="d533c-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="d533c-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="d533c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d533c-102">SYNOPSIS</span></span>
<span data-ttu-id="d533c-103">Especifica a imagem de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d533c-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="d533c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d533c-104">SYNTAX</span></span>

### <span data-ttu-id="d533c-105">ImageReferenceSkuParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d533c-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d533c-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d533c-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d533c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d533c-107">DESCRIPTION</span></span>
<span data-ttu-id="d533c-108">O cmdlet **Set-AzVMSourceImage** especifica a imagem da plataforma a ser usada para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d533c-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="d533c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d533c-109">EXAMPLES</span></span>

### <span data-ttu-id="d533c-110">Exemplo 1: Definir valores para uma imagem</span><span class="sxs-lookup"><span data-stu-id="d533c-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="d533c-111">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="d533c-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="d533c-112">O segundo comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d533c-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d533c-113">O comando atribui um nome e tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d533c-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="d533c-114">A máquina virtual pertence ao conjunto de disponibilidade armazenado $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="d533c-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="d533c-115">O comando final define valores para nome do editor, oferta, SKU e versão.</span><span class="sxs-lookup"><span data-stu-id="d533c-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="d533c-116">Os cmdlets **Get-AzVMImagePublisher**, **Get-AzVMImageOffer,** **Get-AzVMImageSku** e **Get-AzVMImage** podem descobrir essas configurações.</span><span class="sxs-lookup"><span data-stu-id="d533c-116">The **Get-AzVMImagePublisher**, **Get-AzVMImageOffer**, **Get-AzVMImageSku**, and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="d533c-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d533c-117">PARAMETERS</span></span>

### <span data-ttu-id="d533c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d533c-118">-DefaultProfile</span></span>
<span data-ttu-id="d533c-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d533c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d533c-120">-Id</span><span class="sxs-lookup"><span data-stu-id="d533c-120">-Id</span></span>
<span data-ttu-id="d533c-121">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="d533c-121">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d533c-122">-Offer</span><span class="sxs-lookup"><span data-stu-id="d533c-122">-Offer</span></span>
<span data-ttu-id="d533c-123">Especifica o tipo de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="d533c-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="d533c-124">Para obter uma oferta de imagem, use Get-AzVMImageOffer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d533c-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d533c-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="d533c-125">-PublisherName</span></span>
<span data-ttu-id="d533c-126">Especifica o nome de um editor de um VMImage.</span><span class="sxs-lookup"><span data-stu-id="d533c-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="d533c-127">Para obter um editor, use o Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d533c-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d533c-128">-Skus</span><span class="sxs-lookup"><span data-stu-id="d533c-128">-Skus</span></span>
<span data-ttu-id="d533c-129">Especifica um SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="d533c-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="d533c-130">Para obter SKUs, use o cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="d533c-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d533c-131">-Version</span><span class="sxs-lookup"><span data-stu-id="d533c-131">-Version</span></span>
<span data-ttu-id="d533c-132">Especifica uma versão de um VMImage.</span><span class="sxs-lookup"><span data-stu-id="d533c-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="d533c-133">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="d533c-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d533c-134">-VM</span><span class="sxs-lookup"><span data-stu-id="d533c-134">-VM</span></span>
<span data-ttu-id="d533c-135">Especifica o objeto da máquina virtual local a ser definido.</span><span class="sxs-lookup"><span data-stu-id="d533c-135">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d533c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d533c-136">CommonParameters</span></span>
<span data-ttu-id="d533c-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d533c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d533c-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d533c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d533c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d533c-139">INPUTS</span></span>

### <span data-ttu-id="d533c-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d533c-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="d533c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d533c-141">System.String</span></span>

## <span data-ttu-id="d533c-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d533c-142">OUTPUTS</span></span>

### <span data-ttu-id="d533c-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d533c-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d533c-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="d533c-144">NOTES</span></span>

## <span data-ttu-id="d533c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d533c-145">RELATED LINKS</span></span>

[<span data-ttu-id="d533c-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d533c-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="d533c-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d533c-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="d533c-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d533c-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="d533c-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d533c-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="d533c-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d533c-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="d533c-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d533c-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


