---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: a1ed1fa266638891507b6853199bff23d23aa1b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117811"
---
# <span data-ttu-id="32bd9-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="32bd9-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="32bd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="32bd9-103">Especifica a imagem de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="32bd9-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="32bd9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32bd9-104">SYNTAX</span></span>

### <span data-ttu-id="32bd9-105">ImageReferenceSkuParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="32bd9-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32bd9-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32bd9-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32bd9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="32bd9-107">DESCRIPTION</span></span>
<span data-ttu-id="32bd9-108">O **cmdlet Set-AzVMSourceImage** especifica a imagem da plataforma a ser usada para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="32bd9-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="32bd9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="32bd9-109">EXAMPLES</span></span>

### <span data-ttu-id="32bd9-110">Exemplo 1: Definir valores para uma imagem</span><span class="sxs-lookup"><span data-stu-id="32bd9-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="32bd9-111">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="32bd9-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="32bd9-112">O segundo comando cria um objeto virtual de máquina e o armazena na variável $VirtualMachine dados.</span><span class="sxs-lookup"><span data-stu-id="32bd9-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="32bd9-113">O comando atribui um nome e um tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="32bd9-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="32bd9-114">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="32bd9-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="32bd9-115">O comando final define valores para nome do editor, oferta, SKU e versão.</span><span class="sxs-lookup"><span data-stu-id="32bd9-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="32bd9-116">Os cmdlets **Get-AzVMImagePublisher,** **Get-AzVMImageOffer,** **Get-AzVMImageSku** e **Get-AzVMImage podem** descobrir essas configurações.</span><span class="sxs-lookup"><span data-stu-id="32bd9-116">The **Get-AzVMImagePublisher**, **Get-AzVMImageOffer**, **Get-AzVMImageSku**, and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="32bd9-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32bd9-117">PARAMETERS</span></span>

### <span data-ttu-id="32bd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bd9-118">-DefaultProfile</span></span>
<span data-ttu-id="32bd9-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="32bd9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32bd9-120">-ID</span><span class="sxs-lookup"><span data-stu-id="32bd9-120">-Id</span></span>
<span data-ttu-id="32bd9-121">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="32bd9-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="32bd9-122">-Oferta</span><span class="sxs-lookup"><span data-stu-id="32bd9-122">-Offer</span></span>
<span data-ttu-id="32bd9-123">Especifica o tipo de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="32bd9-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="32bd9-124">Para obter uma oferta de imagem, use o cmdlet Get-AzVMImageOffer imagem.</span><span class="sxs-lookup"><span data-stu-id="32bd9-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="32bd9-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="32bd9-125">-PublisherName</span></span>
<span data-ttu-id="32bd9-126">Especifica o nome de um editor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="32bd9-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="32bd9-127">Para obter um editor, use o Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32bd9-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="32bd9-128">-SKUS</span><span class="sxs-lookup"><span data-stu-id="32bd9-128">-Skus</span></span>
<span data-ttu-id="32bd9-129">Especifica uma SKU do VMImage.</span><span class="sxs-lookup"><span data-stu-id="32bd9-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="32bd9-130">Para obter SKUs, use o cmdlet Get-AzVMImageSku dados.</span><span class="sxs-lookup"><span data-stu-id="32bd9-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="32bd9-131">-Versão</span><span class="sxs-lookup"><span data-stu-id="32bd9-131">-Version</span></span>
<span data-ttu-id="32bd9-132">Especifica uma versão de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="32bd9-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="32bd9-133">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="32bd9-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="32bd9-134">-VM</span><span class="sxs-lookup"><span data-stu-id="32bd9-134">-VM</span></span>
<span data-ttu-id="32bd9-135">Especifica o objeto de máquina virtual local a ser definido.</span><span class="sxs-lookup"><span data-stu-id="32bd9-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="32bd9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bd9-136">CommonParameters</span></span>
<span data-ttu-id="32bd9-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32bd9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bd9-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32bd9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bd9-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="32bd9-139">INPUTS</span></span>

### <span data-ttu-id="32bd9-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="32bd9-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="32bd9-141">System.String</span><span class="sxs-lookup"><span data-stu-id="32bd9-141">System.String</span></span>

## <span data-ttu-id="32bd9-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="32bd9-142">OUTPUTS</span></span>

### <span data-ttu-id="32bd9-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="32bd9-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="32bd9-144">Notas</span><span class="sxs-lookup"><span data-stu-id="32bd9-144">NOTES</span></span>

## <span data-ttu-id="32bd9-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32bd9-145">RELATED LINKS</span></span>

[<span data-ttu-id="32bd9-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="32bd9-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="32bd9-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="32bd9-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="32bd9-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="32bd9-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="32bd9-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="32bd9-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="32bd9-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="32bd9-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="32bd9-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="32bd9-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


