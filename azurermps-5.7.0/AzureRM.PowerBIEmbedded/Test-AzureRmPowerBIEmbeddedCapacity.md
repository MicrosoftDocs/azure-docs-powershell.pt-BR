---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426664"
---
# <span data-ttu-id="9a7d7-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9a7d7-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="9a7d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="9a7d7-103">Testa a existência de uma instância da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a7d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a7d7-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="9a7d7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a7d7-105">DESCRIPTION</span></span>
<span data-ttu-id="9a7d7-106">O cmdlet Test-AzureRmPowerBIEmbeddedCapacity testa a existência de uma instância da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="9a7d7-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="9a7d7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a7d7-107">EXAMPLES</span></span>

### <span data-ttu-id="9a7d7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9a7d7-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="9a7d7-109">Esse comando testará se há uma capacidade chamada testcapacity</span><span class="sxs-lookup"><span data-stu-id="9a7d7-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="9a7d7-110">OS</span><span class="sxs-lookup"><span data-stu-id="9a7d7-110">PARAMETERS</span></span>

### <span data-ttu-id="9a7d7-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a7d7-111">-Name</span></span>
<span data-ttu-id="9a7d7-112">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="9a7d7-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="9a7d7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a7d7-113">CommonParameters</span></span>
<span data-ttu-id="9a7d7-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a7d7-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a7d7-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a7d7-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a7d7-116">INPUTS</span></span>

### <span data-ttu-id="9a7d7-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9a7d7-117">None</span></span>
<span data-ttu-id="9a7d7-118">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a7d7-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a7d7-119">OUTPUTS</span></span>

### <span data-ttu-id="9a7d7-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a7d7-120">System.Boolean</span></span>

## <span data-ttu-id="9a7d7-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a7d7-121">NOTES</span></span>

## <span data-ttu-id="9a7d7-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a7d7-122">RELATED LINKS</span></span>

[<span data-ttu-id="9a7d7-123">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9a7d7-123">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="9a7d7-124">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="9a7d7-124">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
