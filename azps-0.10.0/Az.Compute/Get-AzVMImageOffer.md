---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: eb56542d02498a0d4b8aa4176c77d75ab6ad4da6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777013"
---
# <span data-ttu-id="79da8-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="79da8-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="79da8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79da8-102">SYNOPSIS</span></span>
<span data-ttu-id="79da8-103">Obtém tipos de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="79da8-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="79da8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79da8-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79da8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79da8-105">DESCRIPTION</span></span>
<span data-ttu-id="79da8-106">O cmdlet **Get-AzVMImageOffer** Obtém os tipos de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="79da8-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="79da8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79da8-107">EXAMPLES</span></span>

### <span data-ttu-id="79da8-108">Exemplo 1: obter tipos de oferta para um fornecedor</span><span class="sxs-lookup"><span data-stu-id="79da8-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="79da8-109">Esse comando obtém os tipos de oferta do fornecedor especificado na região central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="79da8-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="79da8-110">OS</span><span class="sxs-lookup"><span data-stu-id="79da8-110">PARAMETERS</span></span>

### <span data-ttu-id="79da8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79da8-111">-DefaultProfile</span></span>
<span data-ttu-id="79da8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79da8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79da8-113">-Local</span><span class="sxs-lookup"><span data-stu-id="79da8-113">-Location</span></span>
<span data-ttu-id="79da8-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="79da8-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="79da8-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="79da8-115">-PublisherName</span></span>
<span data-ttu-id="79da8-116">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="79da8-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="79da8-117">Para obter um fornecedor, use o cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="79da8-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="79da8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79da8-118">CommonParameters</span></span>
<span data-ttu-id="79da8-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79da8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79da8-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79da8-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79da8-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79da8-121">INPUTS</span></span>

### <span data-ttu-id="79da8-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="79da8-122">None</span></span>
<span data-ttu-id="79da8-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="79da8-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79da8-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79da8-124">OUTPUTS</span></span>

### <span data-ttu-id="79da8-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="79da8-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="79da8-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79da8-126">NOTES</span></span>

## <span data-ttu-id="79da8-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79da8-127">RELATED LINKS</span></span>

[<span data-ttu-id="79da8-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="79da8-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="79da8-129">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="79da8-129">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="79da8-130">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="79da8-130">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="79da8-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="79da8-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


