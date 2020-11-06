---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 306bb6e4e12adcb4a4eda65b2517ddf0648a81fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602910"
---
# <span data-ttu-id="d89f4-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d89f4-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d89f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d89f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d89f4-103">Testa a existência de uma instância da capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="d89f4-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d89f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d89f4-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d89f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d89f4-105">DESCRIPTION</span></span>
<span data-ttu-id="d89f4-106">O cmdlet Test-AzureRmPowerBIEmbeddedCapacity testa a existência de uma instância da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="d89f4-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="d89f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d89f4-107">EXAMPLES</span></span>

### <span data-ttu-id="d89f4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d89f4-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="d89f4-109">Esse comando testará se há uma capacidade chamada testcapacity</span><span class="sxs-lookup"><span data-stu-id="d89f4-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="d89f4-110">OS</span><span class="sxs-lookup"><span data-stu-id="d89f4-110">PARAMETERS</span></span>

### <span data-ttu-id="d89f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d89f4-111">-DefaultProfile</span></span>
<span data-ttu-id="d89f4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d89f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d89f4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d89f4-113">-Name</span></span>
<span data-ttu-id="d89f4-114">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="d89f4-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d89f4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89f4-115">CommonParameters</span></span>
<span data-ttu-id="d89f4-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d89f4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89f4-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d89f4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89f4-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d89f4-118">INPUTS</span></span>

### <span data-ttu-id="d89f4-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d89f4-119">None</span></span>

## <span data-ttu-id="d89f4-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d89f4-120">OUTPUTS</span></span>

### <span data-ttu-id="d89f4-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d89f4-121">System.Boolean</span></span>

## <span data-ttu-id="d89f4-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d89f4-122">NOTES</span></span>

## <span data-ttu-id="d89f4-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d89f4-123">RELATED LINKS</span></span>

[<span data-ttu-id="d89f4-124">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d89f4-124">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d89f4-125">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d89f4-125">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
