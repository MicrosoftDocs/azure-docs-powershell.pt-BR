---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 0b7d1f72b25da91e85a578a88eded7a511d6d1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891106"
---
# <span data-ttu-id="eb9a1-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eb9a1-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="eb9a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="eb9a1-103">Testa a existência de uma instância da Capacidade Incorporada do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="eb9a1-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="eb9a1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eb9a1-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb9a1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eb9a1-105">DESCRIPTION</span></span>
<span data-ttu-id="eb9a1-106">O Test-AzPowerBIEmbeddedCapacity cmdlet testa a existência de uma instância da Capacidade Incorporada do PowerBI</span><span class="sxs-lookup"><span data-stu-id="eb9a1-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="eb9a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb9a1-107">EXAMPLES</span></span>

### <span data-ttu-id="eb9a1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eb9a1-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="eb9a1-109">Este comando testará se há uma capacidade chamada testcapacity</span><span class="sxs-lookup"><span data-stu-id="eb9a1-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="eb9a1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eb9a1-110">PARAMETERS</span></span>

### <span data-ttu-id="eb9a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb9a1-111">-DefaultProfile</span></span>
<span data-ttu-id="eb9a1-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb9a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb9a1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="eb9a1-113">-Name</span></span>
<span data-ttu-id="eb9a1-114">Nome da Capacidade Incorporada do PowerBI</span><span class="sxs-lookup"><span data-stu-id="eb9a1-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="eb9a1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb9a1-115">CommonParameters</span></span>
<span data-ttu-id="eb9a1-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb9a1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb9a1-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb9a1-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb9a1-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb9a1-118">INPUTS</span></span>

### <span data-ttu-id="eb9a1-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="eb9a1-119">None</span></span>

## <span data-ttu-id="eb9a1-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eb9a1-120">OUTPUTS</span></span>

### <span data-ttu-id="eb9a1-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eb9a1-121">System.Boolean</span></span>

## <span data-ttu-id="eb9a1-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="eb9a1-122">NOTES</span></span>

## <span data-ttu-id="eb9a1-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb9a1-123">RELATED LINKS</span></span>

[<span data-ttu-id="eb9a1-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eb9a1-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="eb9a1-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="eb9a1-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
