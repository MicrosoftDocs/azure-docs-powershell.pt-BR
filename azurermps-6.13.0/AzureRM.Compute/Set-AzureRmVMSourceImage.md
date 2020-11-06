---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: c164d352256f84ea18c09b775c9a9639dbde7866
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430346"
---
# <span data-ttu-id="a4aa2-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="a4aa2-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="a4aa2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="a4aa2-103">Especifica a imagem de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4aa2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4aa2-104">SYNTAX</span></span>

### <span data-ttu-id="a4aa2-105">ImageReferenceSkuParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a4aa2-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4aa2-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4aa2-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4aa2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4aa2-107">DESCRIPTION</span></span>
<span data-ttu-id="a4aa2-108">O cmdlet **set-AzureRmVMSourceImage** especifica a imagem da plataforma a ser usada para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="a4aa2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4aa2-109">EXAMPLES</span></span>

### <span data-ttu-id="a4aa2-110">Exemplo 1: definir valores para uma imagem</span><span class="sxs-lookup"><span data-stu-id="a4aa2-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="a4aa2-111">O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a4aa2-112">O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a4aa2-113">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a4aa2-114">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a4aa2-115">O comando final define valores para nome, oferta, SKU e versão do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="a4aa2-116">Os cmdlets **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** e **Get-AzureRmVMImage** podem descobrir essas configurações.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="a4aa2-117">OS</span><span class="sxs-lookup"><span data-stu-id="a4aa2-117">PARAMETERS</span></span>

### <span data-ttu-id="a4aa2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4aa2-118">-DefaultProfile</span></span>
<span data-ttu-id="a4aa2-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4aa2-120">-ID</span><span class="sxs-lookup"><span data-stu-id="a4aa2-120">-Id</span></span>
<span data-ttu-id="a4aa2-121">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-121">Specifies the ID.</span></span>

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

### <span data-ttu-id="a4aa2-122">-Oferta</span><span class="sxs-lookup"><span data-stu-id="a4aa2-122">-Offer</span></span>
<span data-ttu-id="a4aa2-123">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="a4aa2-124">Para obter uma oferta de imagem, use o cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="a4aa2-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a4aa2-125">-PublisherName</span></span>
<span data-ttu-id="a4aa2-126">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="a4aa2-127">Para obter um fornecedor, use o cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="a4aa2-128">-SKUs</span><span class="sxs-lookup"><span data-stu-id="a4aa2-128">-Skus</span></span>
<span data-ttu-id="a4aa2-129">Especifica uma SKU de VMImage.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="a4aa2-130">Para obter os SKUs, use o cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="a4aa2-131">-Versão</span><span class="sxs-lookup"><span data-stu-id="a4aa2-131">-Version</span></span>
<span data-ttu-id="a4aa2-132">Especifica uma versão de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="a4aa2-133">Para usar a versão mais recente, especifique um valor mais recente em vez de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="a4aa2-134">-VM</span><span class="sxs-lookup"><span data-stu-id="a4aa2-134">-VM</span></span>
<span data-ttu-id="a4aa2-135">Especifica o objeto da máquina virtual local a ser configurado.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-135">Specifies the local virtual machine object to configure.</span></span>

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

### <span data-ttu-id="a4aa2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4aa2-136">CommonParameters</span></span>
<span data-ttu-id="a4aa2-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4aa2-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4aa2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4aa2-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4aa2-139">INPUTS</span></span>

### <span data-ttu-id="a4aa2-140">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a4aa2-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a4aa2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a4aa2-141">System.String</span></span>

## <span data-ttu-id="a4aa2-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4aa2-142">OUTPUTS</span></span>

### <span data-ttu-id="a4aa2-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a4aa2-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a4aa2-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4aa2-144">NOTES</span></span>

## <span data-ttu-id="a4aa2-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4aa2-145">RELATED LINKS</span></span>

[<span data-ttu-id="a4aa2-146">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a4aa2-146">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="a4aa2-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a4aa2-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="a4aa2-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a4aa2-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="a4aa2-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a4aa2-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="a4aa2-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a4aa2-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="a4aa2-151">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="a4aa2-151">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


