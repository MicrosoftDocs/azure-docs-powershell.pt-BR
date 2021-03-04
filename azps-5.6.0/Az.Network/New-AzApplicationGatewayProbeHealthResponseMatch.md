---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 04da18bcd50fa547f1a59142682c93b4e3e5ab62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888234"
---
# <span data-ttu-id="835c0-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="835c0-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="835c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="835c0-102">SYNOPSIS</span></span>
<span data-ttu-id="835c0-103">Cria uma resposta de sonda de saúde usada pela Sonda de Saúde para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="835c0-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="835c0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="835c0-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="835c0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="835c0-105">DESCRIPTION</span></span>
<span data-ttu-id="835c0-106">O cmdlet **Add-AzApplicationGatewayProbeHealthResponseMatch** cria uma resposta de sonda de saúde usada pela Sonda de Saúde para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="835c0-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="835c0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="835c0-107">EXAMPLES</span></span>

### <span data-ttu-id="835c0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="835c0-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="835c0-109">Este comando cria uma resposta de saúde que pode ser passada para ProbeConfig como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="835c0-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="835c0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="835c0-110">PARAMETERS</span></span>

### <span data-ttu-id="835c0-111">-Body</span><span class="sxs-lookup"><span data-stu-id="835c0-111">-Body</span></span>
<span data-ttu-id="835c0-112">Corpo que deve estar contido na resposta de saúde.</span><span class="sxs-lookup"><span data-stu-id="835c0-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="835c0-113">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="835c0-113">Default value is empty</span></span>

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

### <span data-ttu-id="835c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="835c0-114">-DefaultProfile</span></span>
<span data-ttu-id="835c0-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="835c0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="835c0-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="835c0-116">-StatusCode</span></span>
<span data-ttu-id="835c0-117">Intervalos permitidos de códigos de status saudáveis. O intervalo padrão de códigos de status saudáveis é de 200 a 399</span><span class="sxs-lookup"><span data-stu-id="835c0-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="835c0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="835c0-118">CommonParameters</span></span>
<span data-ttu-id="835c0-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="835c0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="835c0-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="835c0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="835c0-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="835c0-121">INPUTS</span></span>

### <span data-ttu-id="835c0-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="835c0-122">None</span></span>

## <span data-ttu-id="835c0-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="835c0-123">OUTPUTS</span></span>

### <span data-ttu-id="835c0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="835c0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="835c0-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="835c0-125">NOTES</span></span>

## <span data-ttu-id="835c0-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="835c0-126">RELATED LINKS</span></span>
