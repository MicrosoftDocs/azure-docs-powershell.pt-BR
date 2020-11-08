---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125441"
---
# <span data-ttu-id="da452-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="da452-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="da452-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da452-102">SYNOPSIS</span></span>
<span data-ttu-id="da452-103">Obtém os locais em que os recursos do ExpressRoutePort estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="da452-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="da452-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da452-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da452-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da452-105">DESCRIPTION</span></span>
<span data-ttu-id="da452-106">O cmdlet **Get-AzExpressRoutePortsLocation** é usado para recuperar os locais nos quais os recursos do ExpressRoutePort estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="da452-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="da452-107">Considerando um local específico como entrada, o cmdlet exibe os detalhes desse local, ou seja, lista de larguras de banda disponíveis nesse local.</span><span class="sxs-lookup"><span data-stu-id="da452-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="da452-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da452-108">EXAMPLES</span></span>

### <span data-ttu-id="da452-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="da452-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="da452-110">Lista os locais em que os recursos do ExpressRoutePort estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="da452-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="da452-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="da452-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="da452-112">Lista as larguras de banda do ExpressRoutePort disponíveis no local $loc.</span><span class="sxs-lookup"><span data-stu-id="da452-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="da452-113">OS</span><span class="sxs-lookup"><span data-stu-id="da452-113">PARAMETERS</span></span>

### <span data-ttu-id="da452-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da452-114">-DefaultProfile</span></span>
<span data-ttu-id="da452-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da452-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da452-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="da452-116">-LocationName</span></span>
<span data-ttu-id="da452-117">O nome do local.</span><span class="sxs-lookup"><span data-stu-id="da452-117">The name of the location.</span></span>

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

### <span data-ttu-id="da452-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da452-118">CommonParameters</span></span>
<span data-ttu-id="da452-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da452-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da452-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da452-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da452-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da452-121">INPUTS</span></span>

### <span data-ttu-id="da452-122">System. String</span><span class="sxs-lookup"><span data-stu-id="da452-122">System.String</span></span>

## <span data-ttu-id="da452-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da452-123">OUTPUTS</span></span>

### <span data-ttu-id="da452-124">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="da452-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="da452-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da452-125">NOTES</span></span>

## <span data-ttu-id="da452-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da452-126">RELATED LINKS</span></span>
