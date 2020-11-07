---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 41693da553178bdd45d19da498a5774ef8d2fa60
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775425"
---
# <span data-ttu-id="1d46a-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="1d46a-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="1d46a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d46a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d46a-103">Cria uma correspondência de resposta de investigação de integridade usada pela investigação de integridade para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1d46a-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="1d46a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d46a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d46a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d46a-105">DESCRIPTION</span></span>
<span data-ttu-id="1d46a-106">**O cmdlet Add-AzApplicationGatewayProbeHealthResponseMatch** cria uma correspondência de resposta de investigação de integridade usada pela investigação de integridade para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1d46a-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="1d46a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d46a-107">EXAMPLES</span></span>

### <span data-ttu-id="1d46a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1d46a-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="1d46a-109">Esse comando cria uma correspondência de resposta de integridade que pode ser transmitida para ProbeConfig como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1d46a-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="1d46a-110">OS</span><span class="sxs-lookup"><span data-stu-id="1d46a-110">PARAMETERS</span></span>

### <span data-ttu-id="1d46a-111">-Corpo</span><span class="sxs-lookup"><span data-stu-id="1d46a-111">-Body</span></span>
<span data-ttu-id="1d46a-112">Corpo que deve estar contido na resposta de integridade.</span><span class="sxs-lookup"><span data-stu-id="1d46a-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="1d46a-113">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="1d46a-113">Default value is empty</span></span>

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

### <span data-ttu-id="1d46a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d46a-114">-DefaultProfile</span></span>
<span data-ttu-id="1d46a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d46a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d46a-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1d46a-116">-StatusCode</span></span>
<span data-ttu-id="1d46a-117">Intervalos permitidos de códigos de status íntegros. O intervalo padrão de códigos de status Íntegro é 200-399</span><span class="sxs-lookup"><span data-stu-id="1d46a-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="1d46a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d46a-118">CommonParameters</span></span>
<span data-ttu-id="1d46a-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d46a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d46a-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d46a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d46a-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d46a-121">INPUTS</span></span>

### <span data-ttu-id="1d46a-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1d46a-122">None</span></span>

## <span data-ttu-id="1d46a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d46a-123">OUTPUTS</span></span>

### <span data-ttu-id="1d46a-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="1d46a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="1d46a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d46a-125">NOTES</span></span>

## <span data-ttu-id="1d46a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d46a-126">RELATED LINKS</span></span>

