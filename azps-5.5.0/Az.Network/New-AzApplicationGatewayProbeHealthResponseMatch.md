---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117412"
---
# <span data-ttu-id="4b6b9-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="4b6b9-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="4b6b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6b9-103">Cria uma resposta de resposta de problemas de saúde usada pela Health Conta para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4b6b9-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="4b6b9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b6b9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b6b9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b6b9-105">DESCRIPTION</span></span>
<span data-ttu-id="4b6b9-106">O cmdlet **Add-AzApplicationGatewayProbeHealthResponseMatch** cria uma resposta de teste de saúde usada pela HealthMatch para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4b6b9-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="4b6b9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b6b9-107">EXAMPLES</span></span>

### <span data-ttu-id="4b6b9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b6b9-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="4b6b9-109">Esse comando cria uma match de resposta de saúde que pode ser passada para o ParameterConfig como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4b6b9-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="4b6b9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b6b9-110">PARAMETERS</span></span>

### <span data-ttu-id="4b6b9-111">-Corpo</span><span class="sxs-lookup"><span data-stu-id="4b6b9-111">-Body</span></span>
<span data-ttu-id="4b6b9-112">Corpo que deve estar contido na resposta à saúde.</span><span class="sxs-lookup"><span data-stu-id="4b6b9-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="4b6b9-113">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="4b6b9-113">Default value is empty</span></span>

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

### <span data-ttu-id="4b6b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6b9-114">-DefaultProfile</span></span>
<span data-ttu-id="4b6b9-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4b6b9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b6b9-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="4b6b9-116">-StatusCode</span></span>
<span data-ttu-id="4b6b9-117">Intervalos permitidos de códigos de status saudáveis. O intervalo padrão de códigos de status saudáveis é de 200 a 399</span><span class="sxs-lookup"><span data-stu-id="4b6b9-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="4b6b9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6b9-118">CommonParameters</span></span>
<span data-ttu-id="4b6b9-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b6b9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6b9-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b6b9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6b9-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="4b6b9-121">INPUTS</span></span>

### <span data-ttu-id="4b6b9-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4b6b9-122">None</span></span>

## <span data-ttu-id="4b6b9-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="4b6b9-123">OUTPUTS</span></span>

### <span data-ttu-id="4b6b9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="4b6b9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="4b6b9-125">Notas</span><span class="sxs-lookup"><span data-stu-id="4b6b9-125">NOTES</span></span>

## <span data-ttu-id="4b6b9-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b6b9-126">RELATED LINKS</span></span>
