---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116542"
---
# <span data-ttu-id="9bef4-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9bef4-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="9bef4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bef4-102">SYNOPSIS</span></span>
<span data-ttu-id="9bef4-103">Obtém tipos de oferta do VMImage.</span><span class="sxs-lookup"><span data-stu-id="9bef4-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="9bef4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bef4-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bef4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bef4-105">DESCRIPTION</span></span>
<span data-ttu-id="9bef4-106">O **cmdlet Get-AzVMImageOffer** obtém os tipos de oferta VMImage.</span><span class="sxs-lookup"><span data-stu-id="9bef4-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="9bef4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9bef4-107">EXAMPLES</span></span>

### <span data-ttu-id="9bef4-108">Exemplo 1: Obter tipos de oferta para um editor</span><span class="sxs-lookup"><span data-stu-id="9bef4-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="9bef4-109">Esse comando obtém os tipos de oferta para o editor especificado na região central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="9bef4-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="9bef4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bef4-110">PARAMETERS</span></span>

### <span data-ttu-id="9bef4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bef4-111">-DefaultProfile</span></span>
<span data-ttu-id="9bef4-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9bef4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bef4-113">-Local</span><span class="sxs-lookup"><span data-stu-id="9bef4-113">-Location</span></span>
<span data-ttu-id="9bef4-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="9bef4-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="9bef4-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9bef4-115">-PublisherName</span></span>
<span data-ttu-id="9bef4-116">Especifica o nome de um editor de uma VMImage.</span><span class="sxs-lookup"><span data-stu-id="9bef4-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="9bef4-117">Para obter um editor, use o Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bef4-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9bef4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bef4-118">CommonParameters</span></span>
<span data-ttu-id="9bef4-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bef4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bef4-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bef4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bef4-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="9bef4-121">INPUTS</span></span>

### <span data-ttu-id="9bef4-122">System.String</span><span class="sxs-lookup"><span data-stu-id="9bef4-122">System.String</span></span>

## <span data-ttu-id="9bef4-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="9bef4-123">OUTPUTS</span></span>

### <span data-ttu-id="9bef4-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="9bef4-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="9bef4-125">Notas</span><span class="sxs-lookup"><span data-stu-id="9bef4-125">NOTES</span></span>

## <span data-ttu-id="9bef4-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bef4-126">RELATED LINKS</span></span>

[<span data-ttu-id="9bef4-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9bef4-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="9bef4-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9bef4-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9bef4-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9bef4-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="9bef4-130">Salvar-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9bef4-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


