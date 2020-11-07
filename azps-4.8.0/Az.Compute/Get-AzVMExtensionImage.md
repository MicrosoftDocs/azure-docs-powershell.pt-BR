---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 83d54f9c0b47db5dc718d273b1a1760ab319a666
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955758"
---
# <span data-ttu-id="e14dc-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="e14dc-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="e14dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e14dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e14dc-103">Obtém todas as versões para uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="e14dc-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="e14dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e14dc-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e14dc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e14dc-105">DESCRIPTION</span></span>
<span data-ttu-id="e14dc-106">O cmdlet **Get-AzVMExtensionImage** obtém todas as versões de uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="e14dc-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="e14dc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e14dc-107">EXAMPLES</span></span>

### <span data-ttu-id="e14dc-108">Exemplo 1: obter as versões de uma imagem de extensão</span><span class="sxs-lookup"><span data-stu-id="e14dc-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient"

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/11.18.6.2
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 11.18.6.2
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="e14dc-109">Esse comando obtém todas as versões da imagem de extensão para o local, o editor e o tipo especificados.</span><span class="sxs-lookup"><span data-stu-id="e14dc-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="e14dc-110">Exemplo 2: obter as versões de uma imagem de extensão com o filtro sobre a versão</span><span class="sxs-lookup"><span data-stu-id="e14dc-110">Example 2: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 12*

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="e14dc-111">Esse comando obtém todas as versões da imagem de extensão para o local especificado, o Publisher, o tipo e a versão começando com 12.</span><span class="sxs-lookup"><span data-stu-id="e14dc-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="e14dc-112">Exemplo 3: obter as versões de uma imagem de extensão com o filtro sobre a versão</span><span class="sxs-lookup"><span data-stu-id="e14dc-112">Example 3: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 1207.12.3.0

Id                         : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/
                             westus/Publishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/V
                             ersions/1207.12.3.0
Location                   : westus
PublisherName              : Chef.Bootstrap.WindowsAzure
Type                       : ChefClient
Version                    : 1207.12.3.0
FilterExpression           :
Name                       :
HandlerSchema              :
OperatingSystem            : Windows
ComputeRole                : IaaS
SupportsMultipleExtensions : False
VMScaleSetEnabled          : False
```

<span data-ttu-id="e14dc-113">Esse comando obtém todas as versões da imagem de extensão para o local, o tipo e a versão especificados.</span><span class="sxs-lookup"><span data-stu-id="e14dc-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="e14dc-114">OS</span><span class="sxs-lookup"><span data-stu-id="e14dc-114">PARAMETERS</span></span>

### <span data-ttu-id="e14dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e14dc-115">-DefaultProfile</span></span>
<span data-ttu-id="e14dc-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e14dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e14dc-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="e14dc-117">-FilterExpression</span></span>
<span data-ttu-id="e14dc-118">Especifica uma expressão de filtro.</span><span class="sxs-lookup"><span data-stu-id="e14dc-118">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14dc-119">-Local</span><span class="sxs-lookup"><span data-stu-id="e14dc-119">-Location</span></span>
<span data-ttu-id="e14dc-120">Especifica o local de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="e14dc-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="e14dc-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="e14dc-121">-PublisherName</span></span>
<span data-ttu-id="e14dc-122">Especifica o nome de um fornecedor de extensão.</span><span class="sxs-lookup"><span data-stu-id="e14dc-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="e14dc-123">Para obter um fornecedor de extensão, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="e14dc-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="e14dc-124">-Digite</span><span class="sxs-lookup"><span data-stu-id="e14dc-124">-Type</span></span>
<span data-ttu-id="e14dc-125">Especifica o tipo da extensão.</span><span class="sxs-lookup"><span data-stu-id="e14dc-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="e14dc-126">Para obter um tipo de extensão, use o cmdlet Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="e14dc-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="e14dc-127">-Versão</span><span class="sxs-lookup"><span data-stu-id="e14dc-127">-Version</span></span>
<span data-ttu-id="e14dc-128">Especifica a versão da extensão que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e14dc-128">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e14dc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e14dc-129">CommonParameters</span></span>
<span data-ttu-id="e14dc-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e14dc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e14dc-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e14dc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e14dc-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e14dc-132">INPUTS</span></span>

### <span data-ttu-id="e14dc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e14dc-133">System.String</span></span>

## <span data-ttu-id="e14dc-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e14dc-134">OUTPUTS</span></span>

### <span data-ttu-id="e14dc-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="e14dc-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="e14dc-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="e14dc-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="e14dc-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e14dc-137">NOTES</span></span>

## <span data-ttu-id="e14dc-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e14dc-138">RELATED LINKS</span></span>

[<span data-ttu-id="e14dc-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="e14dc-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="e14dc-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e14dc-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="e14dc-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e14dc-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


