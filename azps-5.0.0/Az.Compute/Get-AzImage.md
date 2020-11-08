---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 4d1de6553a07cf58fdc109dc5703e37392a27a02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125024"
---
# <span data-ttu-id="7a7b1-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="7a7b1-101">Get-AzImage</span></span>

## <span data-ttu-id="7a7b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a7b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7b1-103">Obtém as propriedades de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="7a7b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a7b1-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a7b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a7b1-105">DESCRIPTION</span></span>
<span data-ttu-id="7a7b1-106">O cmdlet **Get-AzImage** Obtém as propriedades de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="7a7b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a7b1-107">EXAMPLES</span></span>

### <span data-ttu-id="7a7b1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a7b1-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="7a7b1-109">Este comando obtém as propriedades da imagem chamada "Image01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="7a7b1-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="7a7b1-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7a7b1-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="7a7b1-111">Esse comando obtém as propriedades de todas as imagens no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="7a7b1-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="7a7b1-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7a7b1-112">Example 3</span></span>
```
PS C:\> Get-AzImage

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="7a7b1-113">Este comando obtém as propriedades de todas as imagens sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="7a7b1-114">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="7a7b1-114">Example 4</span></span>
```
PS C:\> Get-AzImage -Name "Image*"

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="7a7b1-115">Esse comando obtém as propriedades de todas as imagens na assinatura que começa com "Image".</span><span class="sxs-lookup"><span data-stu-id="7a7b1-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="7a7b1-116">OS</span><span class="sxs-lookup"><span data-stu-id="7a7b1-116">PARAMETERS</span></span>

### <span data-ttu-id="7a7b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7b1-117">-DefaultProfile</span></span>
<span data-ttu-id="7a7b1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a7b1-119">-Expandir</span><span class="sxs-lookup"><span data-stu-id="7a7b1-119">-Expand</span></span>
<span data-ttu-id="7a7b1-120">Especifica a consulta de expandir expressão.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-120">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7b1-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="7a7b1-121">-ImageName</span></span>
<span data-ttu-id="7a7b1-122">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7a7b1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a7b1-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a7b1-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7a7b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7b1-125">CommonParameters</span></span>
<span data-ttu-id="7a7b1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a7b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a7b1-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a7b1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7b1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a7b1-128">INPUTS</span></span>

### <span data-ttu-id="7a7b1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7a7b1-129">System.String</span></span>

## <span data-ttu-id="7a7b1-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a7b1-130">OUTPUTS</span></span>

### <span data-ttu-id="7a7b1-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="7a7b1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="7a7b1-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a7b1-132">NOTES</span></span>

## <span data-ttu-id="7a7b1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a7b1-133">RELATED LINKS</span></span>
