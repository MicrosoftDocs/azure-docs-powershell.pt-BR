---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobehealthresponsematch
schema: 2.0.0
ms.openlocfilehash: 8781b52c3ed50a2a533b90815f1637ebcfe6df52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785171"
---
# <span data-ttu-id="7a586-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="7a586-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="7a586-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a586-102">SYNOPSIS</span></span>
<span data-ttu-id="7a586-103">Cria uma correspondência de resposta de investigação de integridade usada pela investigação de integridade para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7a586-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a586-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a586-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a586-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a586-105">DESCRIPTION</span></span>
<span data-ttu-id="7a586-106">**O cmdlet Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cria uma correspondência de resposta de investigação de integridade usada pela investigação de integridade para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7a586-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="7a586-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a586-107">EXAMPLES</span></span>

### <span data-ttu-id="7a586-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a586-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="7a586-109">Esse comando cria uma correspondência de resposta de integridade que pode ser transmitida para ProbeConfig como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7a586-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="7a586-110">OS</span><span class="sxs-lookup"><span data-stu-id="7a586-110">PARAMETERS</span></span>

### <span data-ttu-id="7a586-111">-Corpo</span><span class="sxs-lookup"><span data-stu-id="7a586-111">-Body</span></span>
<span data-ttu-id="7a586-112">Corpo que deve estar contido na resposta de integridade.</span><span class="sxs-lookup"><span data-stu-id="7a586-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="7a586-113">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="7a586-113">Default value is empty</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a586-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a586-114">-DefaultProfile</span></span>
<span data-ttu-id="7a586-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a586-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a586-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7a586-116">-StatusCode</span></span>
<span data-ttu-id="7a586-117">Intervalos permitidos de códigos de status íntegros. O intervalo padrão de códigos de status Íntegro é 200-399</span><span class="sxs-lookup"><span data-stu-id="7a586-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a586-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a586-118">CommonParameters</span></span>
<span data-ttu-id="7a586-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a586-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a586-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a586-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a586-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a586-121">INPUTS</span></span>

### <span data-ttu-id="7a586-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7a586-122">None</span></span>

## <span data-ttu-id="7a586-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a586-123">OUTPUTS</span></span>

### <span data-ttu-id="7a586-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="7a586-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="7a586-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a586-125">NOTES</span></span>

## <span data-ttu-id="7a586-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a586-126">RELATED LINKS</span></span>

