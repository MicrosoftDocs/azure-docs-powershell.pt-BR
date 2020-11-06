---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: ca03b95748203546fb8d9235cb7822a4dde359a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440612"
---
# <span data-ttu-id="7f1a8-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7f1a8-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="7f1a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f1a8-102">SYNOPSIS</span></span>
<span data-ttu-id="7f1a8-103">Cria uma nova configuração de descarga da configuração para as configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="7f1a8-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f1a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f1a8-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f1a8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f1a8-105">DESCRIPTION</span></span>
<span data-ttu-id="7f1a8-106">O cmdlet **New-AzureRmApplicationGatewayConnectionDraining** cria uma nova conexão para descarregar a configuração de http back-end.</span><span class="sxs-lookup"><span data-stu-id="7f1a8-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="7f1a8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f1a8-107">EXAMPLES</span></span>

### <span data-ttu-id="7f1a8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7f1a8-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="7f1a8-109">O comando cria uma nova configuração de descarregamento de conexão com enabled definido como true e DrainTimeoutInSec definido como 42 segundos e a armazena em $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="7f1a8-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="7f1a8-110">OS</span><span class="sxs-lookup"><span data-stu-id="7f1a8-110">PARAMETERS</span></span>

### <span data-ttu-id="7f1a8-111">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="7f1a8-111">-DrainTimeoutInSec</span></span>
<span data-ttu-id="7f1a8-112">O número de segundos que a conexão drenada está ativa.</span><span class="sxs-lookup"><span data-stu-id="7f1a8-112">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="7f1a8-113">Os valores aceitáveis variam de 1 segundo a 3600 segundos.</span><span class="sxs-lookup"><span data-stu-id="7f1a8-113">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="7f1a8-114">Habilitado para o</span><span class="sxs-lookup"><span data-stu-id="7f1a8-114">-Enabled</span></span>
<span data-ttu-id="7f1a8-115">Se a descarga de conexão está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="7f1a8-115">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="7f1a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f1a8-116">-DefaultProfile</span></span>
<span data-ttu-id="7f1a8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f1a8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f1a8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f1a8-118">CommonParameters</span></span>
<span data-ttu-id="7f1a8-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f1a8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f1a8-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f1a8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f1a8-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f1a8-121">INPUTS</span></span>

### <span data-ttu-id="7f1a8-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7f1a8-122">None</span></span>

## <span data-ttu-id="7f1a8-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f1a8-123">OUTPUTS</span></span>

### <span data-ttu-id="7f1a8-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7f1a8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="7f1a8-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f1a8-125">NOTES</span></span>

## <span data-ttu-id="7f1a8-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f1a8-126">RELATED LINKS</span></span>

[<span data-ttu-id="7f1a8-127">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7f1a8-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="7f1a8-128">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7f1a8-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="7f1a8-129">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7f1a8-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

