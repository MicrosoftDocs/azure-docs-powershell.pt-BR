---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271777"
---
# <span data-ttu-id="69311-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="69311-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="69311-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69311-102">SYNOPSIS</span></span>
<span data-ttu-id="69311-103">Cria uma correspondência de resposta de investigação de integridade usada pela investigação de integridade para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69311-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="69311-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69311-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69311-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69311-105">DESCRIPTION</span></span>
<span data-ttu-id="69311-106">**O cmdlet Add-AzApplicationGatewayProbeHealthResponseMatch** cria uma correspondência de resposta de investigação de integridade usada pela investigação de integridade para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69311-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="69311-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69311-107">EXAMPLES</span></span>

### <span data-ttu-id="69311-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69311-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="69311-109">Esse comando cria uma correspondência de resposta de integridade que pode ser transmitida para ProbeConfig como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="69311-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="69311-110">OS</span><span class="sxs-lookup"><span data-stu-id="69311-110">PARAMETERS</span></span>

### <span data-ttu-id="69311-111">-Corpo</span><span class="sxs-lookup"><span data-stu-id="69311-111">-Body</span></span>
<span data-ttu-id="69311-112">Corpo que deve estar contido na resposta de integridade.</span><span class="sxs-lookup"><span data-stu-id="69311-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="69311-113">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="69311-113">Default value is empty</span></span>

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

### <span data-ttu-id="69311-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69311-114">-DefaultProfile</span></span>
<span data-ttu-id="69311-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69311-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69311-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="69311-116">-StatusCode</span></span>
<span data-ttu-id="69311-117">Intervalos permitidos de códigos de status íntegros. O intervalo padrão de códigos de status Íntegro é 200-399</span><span class="sxs-lookup"><span data-stu-id="69311-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69311-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69311-118">CommonParameters</span></span>
<span data-ttu-id="69311-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69311-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69311-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69311-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69311-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69311-121">INPUTS</span></span>

### <span data-ttu-id="69311-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="69311-122">None</span></span>

## <span data-ttu-id="69311-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69311-123">OUTPUTS</span></span>

### <span data-ttu-id="69311-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="69311-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="69311-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69311-125">NOTES</span></span>

## <span data-ttu-id="69311-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69311-126">RELATED LINKS</span></span>
