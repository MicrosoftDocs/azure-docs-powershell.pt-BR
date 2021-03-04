---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 0075b057cecb91b618d06ad36788801a672268aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886255"
---
# <span data-ttu-id="7272b-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="7272b-101">Get-AzVMImage</span></span>

## <span data-ttu-id="7272b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7272b-102">SYNOPSIS</span></span>
<span data-ttu-id="7272b-103">Obtém todas as versões de um VMImage.</span><span class="sxs-lookup"><span data-stu-id="7272b-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="7272b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7272b-104">SYNTAX</span></span>

### <span data-ttu-id="7272b-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="7272b-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7272b-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="7272b-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7272b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7272b-107">DESCRIPTION</span></span>
<span data-ttu-id="7272b-108">O cmdlet **Get-AzVMImage** obtém todas as versões de um VMImage.</span><span class="sxs-lookup"><span data-stu-id="7272b-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="7272b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7272b-109">EXAMPLES</span></span>

### <span data-ttu-id="7272b-110">Exemplo 1: Obter objetos VMImage</span><span class="sxs-lookup"><span data-stu-id="7272b-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="7272b-111">Este comando obtém todas as versões do VMImage que corresponderem aos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="7272b-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="7272b-112">Exemplo 2: Obter objeto VMImage</span><span class="sxs-lookup"><span data-stu-id="7272b-112">Example 2: Get VMImage object</span></span>
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
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="7272b-113">Este comando obtém uma versão específica do VMImage que corresponde aos valores especificados.</span><span class="sxs-lookup"><span data-stu-id="7272b-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="7272b-114">Exemplo 3: Obter objetos VMImage</span><span class="sxs-lookup"><span data-stu-id="7272b-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="7272b-115">Este comando obtém todas as versões do VMImage que corresponderem aos valores especificados com a filtragem sobre a versão.</span><span class="sxs-lookup"><span data-stu-id="7272b-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="7272b-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7272b-116">PARAMETERS</span></span>

### <span data-ttu-id="7272b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7272b-117">-DefaultProfile</span></span>
<span data-ttu-id="7272b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7272b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7272b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="7272b-119">-Location</span></span>
<span data-ttu-id="7272b-120">Especifica o local de um VMImage.</span><span class="sxs-lookup"><span data-stu-id="7272b-120">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="7272b-121">-Offer</span><span class="sxs-lookup"><span data-stu-id="7272b-121">-Offer</span></span>
<span data-ttu-id="7272b-122">Especifica o tipo de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="7272b-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="7272b-123">Para obter uma oferta de imagem, use Get-AzVMImageOffer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7272b-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="7272b-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="7272b-124">-OrderBy</span></span>
<span data-ttu-id="7272b-125">Especifica a ordem dos resultados retornados.</span><span class="sxs-lookup"><span data-stu-id="7272b-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="7272b-126">Formatado como uma consulta OData.</span><span class="sxs-lookup"><span data-stu-id="7272b-126">Formatted as an OData query.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7272b-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="7272b-127">-PublisherName</span></span>
<span data-ttu-id="7272b-128">Especifica o editor de um VMImage.</span><span class="sxs-lookup"><span data-stu-id="7272b-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="7272b-129">Para obter um editor de imagens, use o Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7272b-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="7272b-130">-Skus</span><span class="sxs-lookup"><span data-stu-id="7272b-130">-Skus</span></span>
<span data-ttu-id="7272b-131">Especifica um SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="7272b-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="7272b-132">Para obter um SKU, use o Get-AzVMImageSku cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7272b-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="7272b-133">-Top</span><span class="sxs-lookup"><span data-stu-id="7272b-133">-Top</span></span>
<span data-ttu-id="7272b-134">Especifica o número máximo de imagens de máquina virtual retornadas.</span><span class="sxs-lookup"><span data-stu-id="7272b-134">Specifies the maximum number of virtual machine images returned.</span></span> 

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7272b-135">-Version</span><span class="sxs-lookup"><span data-stu-id="7272b-135">-Version</span></span>
<span data-ttu-id="7272b-136">Especifica a versão do VMImage.</span><span class="sxs-lookup"><span data-stu-id="7272b-136">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7272b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7272b-137">CommonParameters</span></span>
<span data-ttu-id="7272b-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7272b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7272b-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7272b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7272b-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7272b-140">INPUTS</span></span>

### <span data-ttu-id="7272b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7272b-141">System.String</span></span>

## <span data-ttu-id="7272b-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7272b-142">OUTPUTS</span></span>

### <span data-ttu-id="7272b-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="7272b-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="7272b-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="7272b-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="7272b-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="7272b-145">NOTES</span></span>

## <span data-ttu-id="7272b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7272b-146">RELATED LINKS</span></span>

[<span data-ttu-id="7272b-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="7272b-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="7272b-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="7272b-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="7272b-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="7272b-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="7272b-150">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="7272b-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


