---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimageoffer
schema: 2.0.0
ms.openlocfilehash: 00169d833244ece2f697d2429f5e5db5ee0bf901
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785792"
---
# <span data-ttu-id="2957f-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="2957f-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="2957f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2957f-102">SYNOPSIS</span></span>
<span data-ttu-id="2957f-103">Obtém tipos de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="2957f-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2957f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2957f-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2957f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2957f-105">DESCRIPTION</span></span>
<span data-ttu-id="2957f-106">O cmdlet **Get-AzureRmVMImageOffer** Obtém os tipos de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="2957f-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="2957f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2957f-107">EXAMPLES</span></span>

### <span data-ttu-id="2957f-108">Exemplo 1: obter tipos de oferta para um fornecedor</span><span class="sxs-lookup"><span data-stu-id="2957f-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="2957f-109">Esse comando obtém os tipos de oferta do fornecedor especificado na região central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="2957f-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="2957f-110">OS</span><span class="sxs-lookup"><span data-stu-id="2957f-110">PARAMETERS</span></span>

### <span data-ttu-id="2957f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2957f-111">-DefaultProfile</span></span>
<span data-ttu-id="2957f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2957f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2957f-113">-Local</span><span class="sxs-lookup"><span data-stu-id="2957f-113">-Location</span></span>
<span data-ttu-id="2957f-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="2957f-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="2957f-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="2957f-115">-PublisherName</span></span>
<span data-ttu-id="2957f-116">Especifica o nome de um fornecedor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="2957f-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="2957f-117">Para obter um fornecedor, use o cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="2957f-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="2957f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2957f-118">CommonParameters</span></span>
<span data-ttu-id="2957f-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2957f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2957f-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2957f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2957f-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2957f-121">INPUTS</span></span>

### <span data-ttu-id="2957f-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2957f-122">None</span></span>
<span data-ttu-id="2957f-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2957f-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2957f-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2957f-124">OUTPUTS</span></span>

### <span data-ttu-id="2957f-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="2957f-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="2957f-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2957f-126">NOTES</span></span>

## <span data-ttu-id="2957f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2957f-127">RELATED LINKS</span></span>

[<span data-ttu-id="2957f-128">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2957f-128">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="2957f-129">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2957f-129">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="2957f-130">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2957f-130">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="2957f-131">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2957f-131">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


