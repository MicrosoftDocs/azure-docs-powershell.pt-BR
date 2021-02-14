---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: 947c792c68a314fcfbdc81595f2035c1da539966
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116539"
---
# <span data-ttu-id="1a459-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1a459-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="1a459-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a459-102">SYNOPSIS</span></span>
<span data-ttu-id="1a459-103">Obtém os editores do VMImage.</span><span class="sxs-lookup"><span data-stu-id="1a459-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="1a459-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a459-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a459-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a459-105">DESCRIPTION</span></span>
<span data-ttu-id="1a459-106">O cmdlet **Get-AzVMImagePublisher** obtém os editores do VMImage.</span><span class="sxs-lookup"><span data-stu-id="1a459-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="1a459-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a459-107">EXAMPLES</span></span>

### <span data-ttu-id="1a459-108">Exemplo 1: Obter os editores do VMImage para uma região</span><span class="sxs-lookup"><span data-stu-id="1a459-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="1a459-109">Esse comando obtém os editores de instâncias do VMImage para a região central dos EUA em seu perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a459-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="1a459-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a459-110">PARAMETERS</span></span>

### <span data-ttu-id="1a459-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a459-111">-DefaultProfile</span></span>
<span data-ttu-id="1a459-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1a459-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a459-113">-Local</span><span class="sxs-lookup"><span data-stu-id="1a459-113">-Location</span></span>
<span data-ttu-id="1a459-114">Especifica o local da VMImage.</span><span class="sxs-lookup"><span data-stu-id="1a459-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="1a459-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a459-115">CommonParameters</span></span>
<span data-ttu-id="1a459-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a459-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a459-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a459-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a459-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="1a459-118">INPUTS</span></span>

### <span data-ttu-id="1a459-119">System.String</span><span class="sxs-lookup"><span data-stu-id="1a459-119">System.String</span></span>

## <span data-ttu-id="1a459-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="1a459-120">OUTPUTS</span></span>

### <span data-ttu-id="1a459-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1a459-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="1a459-122">Notas</span><span class="sxs-lookup"><span data-stu-id="1a459-122">NOTES</span></span>

## <span data-ttu-id="1a459-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a459-123">RELATED LINKS</span></span>

[<span data-ttu-id="1a459-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="1a459-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="1a459-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="1a459-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="1a459-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="1a459-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="1a459-127">Salvar-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="1a459-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


