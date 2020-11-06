---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610564"
---
# <span data-ttu-id="67992-101">Get-AzureRmExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="67992-101">Get-AzureRmExpressRoutePortsLocation</span></span>

## <span data-ttu-id="67992-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67992-102">SYNOPSIS</span></span>
<span data-ttu-id="67992-103">Obtém os locais em que os recursos do ExpressRoutePort estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="67992-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67992-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67992-104">SYNTAX</span></span>

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67992-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67992-105">DESCRIPTION</span></span>
<span data-ttu-id="67992-106">O cmdlet **Get-AzureRmExpressRoutePortsLocation** é usado para recuperar os locais nos quais os recursos do ExpressRoutePort estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="67992-106">The **Get-AzureRmExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="67992-107">Considerando um local específico como entrada, o cmdlet exibe os detalhes desse local, ou seja, lista de larguras de banda disponíveis nesse local.</span><span class="sxs-lookup"><span data-stu-id="67992-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>


## <span data-ttu-id="67992-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67992-108">EXAMPLES</span></span>

### <span data-ttu-id="67992-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67992-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

<span data-ttu-id="67992-110">Lista os locais em que os recursos do ExpressRoutePort estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="67992-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="67992-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="67992-111">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="67992-112">Lista as larguras de banda do ExpressRoutePort disponíveis no local $loc.</span><span class="sxs-lookup"><span data-stu-id="67992-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="67992-113">OS</span><span class="sxs-lookup"><span data-stu-id="67992-113">PARAMETERS</span></span>

### <span data-ttu-id="67992-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67992-114">-DefaultProfile</span></span>
<span data-ttu-id="67992-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67992-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67992-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="67992-116">-LocationName</span></span>
<span data-ttu-id="67992-117">O nome do local.</span><span class="sxs-lookup"><span data-stu-id="67992-117">The name of the location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67992-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67992-118">CommonParameters</span></span>
<span data-ttu-id="67992-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67992-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67992-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67992-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67992-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67992-121">INPUTS</span></span>

### <span data-ttu-id="67992-122">System. String</span><span class="sxs-lookup"><span data-stu-id="67992-122">System.String</span></span>

## <span data-ttu-id="67992-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67992-123">OUTPUTS</span></span>

### <span data-ttu-id="67992-124">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="67992-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="67992-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67992-125">NOTES</span></span>

## <span data-ttu-id="67992-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67992-126">RELATED LINKS</span></span>
