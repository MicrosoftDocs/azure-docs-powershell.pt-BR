---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259377"
---
# <span data-ttu-id="f0d91-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f0d91-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f0d91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0d91-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d91-103">Cria uma nova configuração de descarga da configuração para as configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="f0d91-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="f0d91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0d91-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0d91-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0d91-105">DESCRIPTION</span></span>
<span data-ttu-id="f0d91-106">O cmdlet **New-AzApplicationGatewayConnectionDraining** cria uma nova conexão para descarregar a configuração de http back-end.</span><span class="sxs-lookup"><span data-stu-id="f0d91-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="f0d91-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0d91-107">EXAMPLES</span></span>

### <span data-ttu-id="f0d91-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f0d91-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="f0d91-109">O comando cria uma nova configuração de descarregamento de conexão com enabled definido como true e DrainTimeoutInSec definido como 42 segundos e a armazena em $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="f0d91-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="f0d91-110">OS</span><span class="sxs-lookup"><span data-stu-id="f0d91-110">PARAMETERS</span></span>

### <span data-ttu-id="f0d91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d91-111">-DefaultProfile</span></span>
<span data-ttu-id="f0d91-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d91-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0d91-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="f0d91-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="f0d91-114">O número de segundos que a conexão drenada está ativa.</span><span class="sxs-lookup"><span data-stu-id="f0d91-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="f0d91-115">Os valores aceitáveis variam de 1 segundo a 3600 segundos.</span><span class="sxs-lookup"><span data-stu-id="f0d91-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d91-116">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="f0d91-116">-Enabled</span></span>
<span data-ttu-id="f0d91-117">Se a descarga de conexão está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="f0d91-117">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d91-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d91-118">CommonParameters</span></span>
<span data-ttu-id="f0d91-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d91-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d91-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d91-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d91-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0d91-121">INPUTS</span></span>

### <span data-ttu-id="f0d91-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f0d91-122">None</span></span>

## <span data-ttu-id="f0d91-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0d91-123">OUTPUTS</span></span>

### <span data-ttu-id="f0d91-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f0d91-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="f0d91-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0d91-125">NOTES</span></span>

## <span data-ttu-id="f0d91-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0d91-126">RELATED LINKS</span></span>

[<span data-ttu-id="f0d91-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f0d91-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f0d91-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f0d91-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="f0d91-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f0d91-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

