---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 6b54c300eb6e37544246b785fe30b2a3dcb67b9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609990"
---
# <span data-ttu-id="fff22-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="fff22-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="fff22-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fff22-102">SYNOPSIS</span></span>
<span data-ttu-id="fff22-103">Cria uma correspondência de resposta de investigação de integridade usada pela investigação de integridade para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fff22-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fff22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fff22-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fff22-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fff22-105">DESCRIPTION</span></span>
<span data-ttu-id="fff22-106">**O cmdlet Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cria uma correspondência de resposta de investigação de integridade usada pela investigação de integridade para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fff22-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="fff22-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fff22-107">EXAMPLES</span></span>

### <span data-ttu-id="fff22-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fff22-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="fff22-109">Esse comando cria uma correspondência de resposta de integridade que pode ser transmitida para ProbeConfig como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fff22-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="fff22-110">OS</span><span class="sxs-lookup"><span data-stu-id="fff22-110">PARAMETERS</span></span>

### <span data-ttu-id="fff22-111">-Corpo</span><span class="sxs-lookup"><span data-stu-id="fff22-111">-Body</span></span>
<span data-ttu-id="fff22-112">Corpo que deve estar contido na resposta de integridade.</span><span class="sxs-lookup"><span data-stu-id="fff22-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="fff22-113">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="fff22-113">Default value is empty</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff22-114">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="fff22-114">-StatusCode</span></span>
<span data-ttu-id="fff22-115">Intervalos permitidos de códigos de status íntegros. O intervalo padrão de códigos de status Íntegro é 200-399</span><span class="sxs-lookup"><span data-stu-id="fff22-115">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="fff22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff22-116">-DefaultProfile</span></span>
<span data-ttu-id="fff22-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fff22-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fff22-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff22-118">CommonParameters</span></span>
<span data-ttu-id="fff22-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff22-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff22-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fff22-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff22-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fff22-121">INPUTS</span></span>

### <span data-ttu-id="fff22-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fff22-122">None</span></span>

## <span data-ttu-id="fff22-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fff22-123">OUTPUTS</span></span>

### <span data-ttu-id="fff22-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="fff22-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="fff22-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fff22-125">NOTES</span></span>

## <span data-ttu-id="fff22-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fff22-126">RELATED LINKS</span></span>

