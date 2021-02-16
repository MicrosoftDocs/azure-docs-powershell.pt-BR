---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 4d1de6553a07cf58fdc109dc5703e37392a27a02
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117868"
---
# <span data-ttu-id="f8cd0-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="f8cd0-101">Get-AzImage</span></span>

## <span data-ttu-id="f8cd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f8cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="f8cd0-103">Obtém as propriedades de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="f8cd0-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="f8cd0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8cd0-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8cd0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8cd0-105">DESCRIPTION</span></span>
<span data-ttu-id="f8cd0-106">O **cmdlet Get-AzImage** obtém as propriedades de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="f8cd0-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="f8cd0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f8cd0-107">EXAMPLES</span></span>

### <span data-ttu-id="f8cd0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f8cd0-108">Example 1</span></span>
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

<span data-ttu-id="f8cd0-109">Esse comando obtém as propriedades da imagem chamada "Imagem01" no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="f8cd0-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f8cd0-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f8cd0-110">Example 2</span></span>
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

<span data-ttu-id="f8cd0-111">Esse comando obtém as propriedades de todas as imagens no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="f8cd0-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f8cd0-112">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f8cd0-112">Example 3</span></span>
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

<span data-ttu-id="f8cd0-113">Esse comando obtém as propriedades de todas as imagens sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="f8cd0-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="f8cd0-114">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="f8cd0-114">Example 4</span></span>
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

<span data-ttu-id="f8cd0-115">Esse comando obtém as propriedades de todas as imagens sob a assinatura que começam com "Imagem".</span><span class="sxs-lookup"><span data-stu-id="f8cd0-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="f8cd0-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8cd0-116">PARAMETERS</span></span>

### <span data-ttu-id="f8cd0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8cd0-117">-DefaultProfile</span></span>
<span data-ttu-id="f8cd0-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f8cd0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8cd0-119">-Expandir</span><span class="sxs-lookup"><span data-stu-id="f8cd0-119">-Expand</span></span>
<span data-ttu-id="f8cd0-120">Especifica a consulta expandir expressão.</span><span class="sxs-lookup"><span data-stu-id="f8cd0-120">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="f8cd0-121">-NomedaImagem</span><span class="sxs-lookup"><span data-stu-id="f8cd0-121">-ImageName</span></span>
<span data-ttu-id="f8cd0-122">Especifica o nome de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="f8cd0-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="f8cd0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8cd0-123">-ResourceGroupName</span></span>
<span data-ttu-id="f8cd0-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f8cd0-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f8cd0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8cd0-125">CommonParameters</span></span>
<span data-ttu-id="f8cd0-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8cd0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8cd0-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8cd0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8cd0-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="f8cd0-128">INPUTS</span></span>

### <span data-ttu-id="f8cd0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f8cd0-129">System.String</span></span>

## <span data-ttu-id="f8cd0-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="f8cd0-130">OUTPUTS</span></span>

### <span data-ttu-id="f8cd0-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="f8cd0-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f8cd0-132">Notas</span><span class="sxs-lookup"><span data-stu-id="f8cd0-132">NOTES</span></span>

## <span data-ttu-id="f8cd0-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f8cd0-133">RELATED LINKS</span></span>
