---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: d16b5d916f3a807de818c58de94f7f0841e04d17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886008"
---
# <span data-ttu-id="c77cc-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="c77cc-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="c77cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c77cc-102">SYNOPSIS</span></span>
<span data-ttu-id="c77cc-103">Obtém os locais nos quais os recursos expressRoutePort estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c77cc-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="c77cc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c77cc-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c77cc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c77cc-105">DESCRIPTION</span></span>
<span data-ttu-id="c77cc-106">O cmdlet **Get-AzExpressRoutePortsLocation** é usado para recuperar os locais nos quais os recursos do ExpressRoutePort estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c77cc-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="c77cc-107">Dado um local específico como entrada, o cmdlet exibe os detalhes desse local, ou seja, lista de larguras de banda disponíveis nesse local.</span><span class="sxs-lookup"><span data-stu-id="c77cc-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="c77cc-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c77cc-108">EXAMPLES</span></span>

### <span data-ttu-id="c77cc-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c77cc-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="c77cc-110">Lista os locais nos quais os recursos do ExpressRoutePort estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c77cc-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="c77cc-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c77cc-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="c77cc-112">Lista as larguras de banda do ExpressRoutePort disponíveis no local $loc.</span><span class="sxs-lookup"><span data-stu-id="c77cc-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="c77cc-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c77cc-113">PARAMETERS</span></span>

### <span data-ttu-id="c77cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c77cc-114">-DefaultProfile</span></span>
<span data-ttu-id="c77cc-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c77cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c77cc-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="c77cc-116">-LocationName</span></span>
<span data-ttu-id="c77cc-117">O nome do local.</span><span class="sxs-lookup"><span data-stu-id="c77cc-117">The name of the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c77cc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c77cc-118">CommonParameters</span></span>
<span data-ttu-id="c77cc-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c77cc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c77cc-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c77cc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c77cc-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c77cc-121">INPUTS</span></span>

### <span data-ttu-id="c77cc-122">System.String</span><span class="sxs-lookup"><span data-stu-id="c77cc-122">System.String</span></span>

## <span data-ttu-id="c77cc-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c77cc-123">OUTPUTS</span></span>

### <span data-ttu-id="c77cc-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="c77cc-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="c77cc-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="c77cc-125">NOTES</span></span>

## <span data-ttu-id="c77cc-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c77cc-126">RELATED LINKS</span></span>
