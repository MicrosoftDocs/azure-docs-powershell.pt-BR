---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: eb2c92b0efcbcd5333c600fe481e21752a96be9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127102"
---
# <span data-ttu-id="eba59-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="eba59-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="eba59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eba59-102">SYNOPSIS</span></span>
<span data-ttu-id="eba59-103">Obtém o tipo de extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="eba59-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="eba59-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eba59-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eba59-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="eba59-105">DESCRIPTION</span></span>
<span data-ttu-id="eba59-106">O cmdlet **Get-AzVMExtensionImageType** obtém o tipo de extensão do Azure.</span><span class="sxs-lookup"><span data-stu-id="eba59-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="eba59-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eba59-107">EXAMPLES</span></span>

### <span data-ttu-id="eba59-108">Exemplo 1: Obter um tipo de imagem de extensão</span><span class="sxs-lookup"><span data-stu-id="eba59-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="eba59-109">Esse comando obtém o tipo de imagem de extensão para o editor e o local especificados.</span><span class="sxs-lookup"><span data-stu-id="eba59-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="eba59-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eba59-110">PARAMETERS</span></span>

### <span data-ttu-id="eba59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba59-111">-DefaultProfile</span></span>
<span data-ttu-id="eba59-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="eba59-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eba59-113">-Local</span><span class="sxs-lookup"><span data-stu-id="eba59-113">-Location</span></span>
<span data-ttu-id="eba59-114">Especifica o local de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="eba59-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="eba59-115">Esse cmdlet obtém o tipo de extensão no local especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eba59-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="eba59-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="eba59-116">-PublisherName</span></span>
<span data-ttu-id="eba59-117">Especifica o nome de um editor de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="eba59-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="eba59-118">Para obter um editor de extensões, use Get-AzVMImagePublisher cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eba59-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="eba59-119">Este cmdlet obtém o tipo de extensão do editor especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eba59-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="eba59-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba59-120">CommonParameters</span></span>
<span data-ttu-id="eba59-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba59-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba59-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eba59-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba59-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="eba59-123">INPUTS</span></span>

### <span data-ttu-id="eba59-124">System.String</span><span class="sxs-lookup"><span data-stu-id="eba59-124">System.String</span></span>

## <span data-ttu-id="eba59-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="eba59-125">OUTPUTS</span></span>

### <span data-ttu-id="eba59-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="eba59-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="eba59-127">Notas</span><span class="sxs-lookup"><span data-stu-id="eba59-127">NOTES</span></span>

## <span data-ttu-id="eba59-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eba59-128">RELATED LINKS</span></span>

[<span data-ttu-id="eba59-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="eba59-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="eba59-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="eba59-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


