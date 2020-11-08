---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: a1ed1fa266638891507b6853199bff23d23aa1b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112413"
---
# <span data-ttu-id="35681-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="35681-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="35681-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35681-102">SYNOPSIS</span></span>
<span data-ttu-id="35681-103">Especifica a imagem de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35681-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="35681-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35681-104">SYNTAX</span></span>

### <span data-ttu-id="35681-105">ImageReferenceSkuParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="35681-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35681-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35681-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35681-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35681-107">DESCRIPTION</span></span>
<span data-ttu-id="35681-108">O cmdlet **set-AzVMSourceImage** especifica a imagem da plataforma a ser usada para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35681-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="35681-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35681-109">EXAMPLES</span></span>

### <span data-ttu-id="35681-110">Exemplo 1: definir valores para uma imagem</span><span class="sxs-lookup"><span data-stu-id="35681-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="35681-111">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="35681-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="35681-112">O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="35681-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="35681-113">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35681-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="35681-114">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="35681-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="35681-115">O comando final define valores para nome, oferta, SKU e versão do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="35681-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="35681-116">Os cmdlets **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** e **Get-AzVMImage** podem descobrir essas configurações.</span><span class="sxs-lookup"><span data-stu-id="35681-116">The **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** , and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="35681-117">OS</span><span class="sxs-lookup"><span data-stu-id="35681-117">PARAMETERS</span></span>

### <span data-ttu-id="35681-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35681-118">-DefaultProfile</span></span>
<span data-ttu-id="35681-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35681-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35681-120">-ID</span><span class="sxs-lookup"><span data-stu-id="35681-120">-Id</span></span>
<span data-ttu-id="35681-121">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="35681-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="35681-122">-Oferta</span><span class="sxs-lookup"><span data-stu-id="35681-122">-Offer</span></span>
<span data-ttu-id="35681-123">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="35681-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="35681-124">Para obter uma oferta de imagem, use o cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="35681-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="35681-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="35681-125">-PublisherName</span></span>
<span data-ttu-id="35681-126">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="35681-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="35681-127">Para obter um fornecedor, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="35681-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="35681-128">-SKUs</span><span class="sxs-lookup"><span data-stu-id="35681-128">-Skus</span></span>
<span data-ttu-id="35681-129">Especifica uma SKU de VMImage.</span><span class="sxs-lookup"><span data-stu-id="35681-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="35681-130">Para obter os SKUs, use o cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="35681-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="35681-131">-Versão</span><span class="sxs-lookup"><span data-stu-id="35681-131">-Version</span></span>
<span data-ttu-id="35681-132">Especifica uma versão de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="35681-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="35681-133">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="35681-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="35681-134">-VM</span><span class="sxs-lookup"><span data-stu-id="35681-134">-VM</span></span>
<span data-ttu-id="35681-135">Especifica o objeto da máquina virtual local a ser configurado.</span><span class="sxs-lookup"><span data-stu-id="35681-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="35681-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35681-136">CommonParameters</span></span>
<span data-ttu-id="35681-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35681-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35681-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35681-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35681-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35681-139">INPUTS</span></span>

### <span data-ttu-id="35681-140">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="35681-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="35681-141">System. String</span><span class="sxs-lookup"><span data-stu-id="35681-141">System.String</span></span>

## <span data-ttu-id="35681-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35681-142">OUTPUTS</span></span>

### <span data-ttu-id="35681-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="35681-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="35681-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35681-144">NOTES</span></span>

## <span data-ttu-id="35681-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35681-145">RELATED LINKS</span></span>

[<span data-ttu-id="35681-146">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="35681-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="35681-147">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="35681-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="35681-148">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="35681-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="35681-149">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="35681-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="35681-150">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="35681-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="35681-151">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="35681-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


