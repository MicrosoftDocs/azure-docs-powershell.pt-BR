---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: 0e3c1a9113bf3872ca86227272e36abd67781b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601343"
---
# <span data-ttu-id="41110-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="41110-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="41110-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41110-102">SYNOPSIS</span></span>
<span data-ttu-id="41110-103">Obtém o tipo de uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="41110-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="41110-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41110-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41110-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41110-105">DESCRIPTION</span></span>
<span data-ttu-id="41110-106">O cmdlet **Get-AzVMExtensionImageType** Obtém o tipo de uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="41110-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="41110-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41110-107">EXAMPLES</span></span>

### <span data-ttu-id="41110-108">Exemplo 1: obter um tipo de imagem de extensão</span><span class="sxs-lookup"><span data-stu-id="41110-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="41110-109">Esse comando obtém o tipo de imagem de extensão do Publicador e local especificados.</span><span class="sxs-lookup"><span data-stu-id="41110-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="41110-110">OS</span><span class="sxs-lookup"><span data-stu-id="41110-110">PARAMETERS</span></span>

### <span data-ttu-id="41110-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41110-111">-DefaultProfile</span></span>
<span data-ttu-id="41110-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41110-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41110-113">-Local</span><span class="sxs-lookup"><span data-stu-id="41110-113">-Location</span></span>
<span data-ttu-id="41110-114">Especifica o local de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="41110-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="41110-115">Esse cmdlet obtém o tipo de uma extensão no local que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="41110-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="41110-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="41110-116">-PublisherName</span></span>
<span data-ttu-id="41110-117">Especifica o nome de um fornecedor de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="41110-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="41110-118">Para obter um fornecedor de extensão, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="41110-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="41110-119">Esse cmdlet obtém o tipo de uma extensão do Publicador que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="41110-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="41110-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41110-120">CommonParameters</span></span>
<span data-ttu-id="41110-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41110-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41110-122">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41110-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41110-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41110-123">INPUTS</span></span>

### <span data-ttu-id="41110-124">System. String</span><span class="sxs-lookup"><span data-stu-id="41110-124">System.String</span></span>

## <span data-ttu-id="41110-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41110-125">OUTPUTS</span></span>

### <span data-ttu-id="41110-126">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="41110-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="41110-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41110-127">NOTES</span></span>

## <span data-ttu-id="41110-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41110-128">RELATED LINKS</span></span>

[<span data-ttu-id="41110-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="41110-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="41110-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="41110-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


