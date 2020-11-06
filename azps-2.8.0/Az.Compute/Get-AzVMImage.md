---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 13871100efbe2fe62de769adcc40ee434e86eb21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597433"
---
# <span data-ttu-id="54a08-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="54a08-101">Get-AzVMImage</span></span>

## <span data-ttu-id="54a08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54a08-102">SYNOPSIS</span></span>
<span data-ttu-id="54a08-103">Obtém todas as versões de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="54a08-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="54a08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54a08-104">SYNTAX</span></span>

### <span data-ttu-id="54a08-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="54a08-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54a08-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="54a08-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54a08-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54a08-107">DESCRIPTION</span></span>
<span data-ttu-id="54a08-108">O cmdlet **Get-AzVMImage** obtém todas as versões de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="54a08-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="54a08-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54a08-109">EXAMPLES</span></span>

### <span data-ttu-id="54a08-110">Exemplo 1: obter objetos VMImage</span><span class="sxs-lookup"><span data-stu-id="54a08-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="54a08-111">Esse comando obtém todas as versões de VMImage correspondentes aos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="54a08-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="54a08-112">Exemplo 2: obter objeto de VMImage</span><span class="sxs-lookup"><span data-stu-id="54a08-112">Example 2: Get VMImage object</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.20180315

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/centralus/
                   Publishers/MicrosoftWindowsServer/ArtifactTypes/VMImage/Offers/windowsserver/Skus/2012-R2-Datacenter
                   /Versions/4.127.20180315
Location         : centralus
PublisherName    : MicrosoftWindowsServer
Offer            : windowsserver
Skus             : 2012-R2-Datacenter
Version          : 4.127.20180315
FilterExpression :
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="54a08-113">Esse comando obtém uma versão específica da VMImage que corresponde aos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="54a08-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="54a08-114">Exemplo 3: obter objetos VMImage</span><span class="sxs-lookup"><span data-stu-id="54a08-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="54a08-115">Esse comando obtém todas as versões de VMImage correspondentes aos valores especificados com filtragem sobre a versão.</span><span class="sxs-lookup"><span data-stu-id="54a08-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="54a08-116">OS</span><span class="sxs-lookup"><span data-stu-id="54a08-116">PARAMETERS</span></span>

### <span data-ttu-id="54a08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a08-117">-DefaultProfile</span></span>
<span data-ttu-id="54a08-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54a08-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54a08-119">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="54a08-119">-FilterExpression</span></span>
<span data-ttu-id="54a08-120">Especifica uma expressão de filtro.</span><span class="sxs-lookup"><span data-stu-id="54a08-120">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a08-121">-Local</span><span class="sxs-lookup"><span data-stu-id="54a08-121">-Location</span></span>
<span data-ttu-id="54a08-122">Especifica a localização de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="54a08-122">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54a08-123">-Oferta</span><span class="sxs-lookup"><span data-stu-id="54a08-123">-Offer</span></span>
<span data-ttu-id="54a08-124">Especifica o tipo de oferta da VMImage.</span><span class="sxs-lookup"><span data-stu-id="54a08-124">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="54a08-125">Para obter uma oferta de imagem, use o cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="54a08-125">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54a08-126">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="54a08-126">-PublisherName</span></span>
<span data-ttu-id="54a08-127">Especifica o fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="54a08-127">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="54a08-128">Para obter um editor de imagens, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="54a08-128">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54a08-129">-SKUs</span><span class="sxs-lookup"><span data-stu-id="54a08-129">-Skus</span></span>
<span data-ttu-id="54a08-130">Especifica uma SKU de VMImage.</span><span class="sxs-lookup"><span data-stu-id="54a08-130">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="54a08-131">Para obter uma SKU, use o cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="54a08-131">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54a08-132">-Versão</span><span class="sxs-lookup"><span data-stu-id="54a08-132">-Version</span></span>
<span data-ttu-id="54a08-133">Especifica a versão da VMImage.</span><span class="sxs-lookup"><span data-stu-id="54a08-133">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="54a08-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a08-134">CommonParameters</span></span>
<span data-ttu-id="54a08-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54a08-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a08-136">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54a08-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a08-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54a08-137">INPUTS</span></span>

### <span data-ttu-id="54a08-138">System. String</span><span class="sxs-lookup"><span data-stu-id="54a08-138">System.String</span></span>

## <span data-ttu-id="54a08-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54a08-139">OUTPUTS</span></span>

### <span data-ttu-id="54a08-140">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="54a08-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="54a08-141">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="54a08-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="54a08-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54a08-142">NOTES</span></span>

## <span data-ttu-id="54a08-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54a08-143">RELATED LINKS</span></span>

[<span data-ttu-id="54a08-144">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="54a08-144">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="54a08-145">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="54a08-145">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="54a08-146">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="54a08-146">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="54a08-147">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="54a08-147">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


