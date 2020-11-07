---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: 1864b4c2dcbd4b3d9934ffb15c54fae18082c920
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777019"
---
# <span data-ttu-id="c2c92-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="c2c92-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="c2c92-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2c92-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c92-103">Obtém todas as versões para uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="c2c92-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="c2c92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2c92-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2c92-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2c92-105">DESCRIPTION</span></span>
<span data-ttu-id="c2c92-106">O cmdlet **Get-AzVMExtensionImage** obtém todas as versões de uma extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="c2c92-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="c2c92-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2c92-107">EXAMPLES</span></span>

### <span data-ttu-id="c2c92-108">Exemplo 1: obter as versões de uma imagem de extensão</span><span class="sxs-lookup"><span data-stu-id="c2c92-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="c2c92-109">Esse comando obtém todas as versões da imagem de extensão para o local, o editor e o tipo especificados.</span><span class="sxs-lookup"><span data-stu-id="c2c92-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="c2c92-110">OS</span><span class="sxs-lookup"><span data-stu-id="c2c92-110">PARAMETERS</span></span>

### <span data-ttu-id="c2c92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c92-111">-DefaultProfile</span></span>
<span data-ttu-id="c2c92-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2c92-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c92-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="c2c92-113">-FilterExpression</span></span>
<span data-ttu-id="c2c92-114">Especifica uma expressão de filtro.</span><span class="sxs-lookup"><span data-stu-id="c2c92-114">Specifies a filter expression.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c92-115">-Local</span><span class="sxs-lookup"><span data-stu-id="c2c92-115">-Location</span></span>
<span data-ttu-id="c2c92-116">Especifica o local de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="c2c92-116">Specifies the location of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c92-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="c2c92-117">-PublisherName</span></span>
<span data-ttu-id="c2c92-118">Especifica o nome de um fornecedor de extensão.</span><span class="sxs-lookup"><span data-stu-id="c2c92-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="c2c92-119">Para obter um fornecedor de extensão, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="c2c92-119">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c92-120">-Digite</span><span class="sxs-lookup"><span data-stu-id="c2c92-120">-Type</span></span>
<span data-ttu-id="c2c92-121">Especifica o tipo da extensão.</span><span class="sxs-lookup"><span data-stu-id="c2c92-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="c2c92-122">Para obter um tipo de extensão, use o cmdlet Get-AzVMExtensionImageType.</span><span class="sxs-lookup"><span data-stu-id="c2c92-122">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c92-123">-Versão</span><span class="sxs-lookup"><span data-stu-id="c2c92-123">-Version</span></span>
<span data-ttu-id="c2c92-124">Especifica a versão da extensão que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c2c92-124">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2c92-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c92-125">CommonParameters</span></span>
<span data-ttu-id="c2c92-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2c92-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c92-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2c92-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c92-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2c92-128">INPUTS</span></span>

### <span data-ttu-id="c2c92-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c2c92-129">None</span></span>
<span data-ttu-id="c2c92-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c2c92-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c2c92-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2c92-131">OUTPUTS</span></span>

### <span data-ttu-id="c2c92-132">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="c2c92-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="c2c92-133">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="c2c92-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="c2c92-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2c92-134">NOTES</span></span>

## <span data-ttu-id="c2c92-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2c92-135">RELATED LINKS</span></span>

[<span data-ttu-id="c2c92-136">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="c2c92-136">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="c2c92-137">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c2c92-137">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="c2c92-138">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c2c92-138">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


