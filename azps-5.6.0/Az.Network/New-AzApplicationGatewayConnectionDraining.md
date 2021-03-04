---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b5bfedea118aa3770bac3141d05db379a4655906
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892429"
---
# <span data-ttu-id="32b7b-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="32b7b-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="32b7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="32b7b-103">Cria uma nova configuração de esvaziamento de conexão para configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="32b7b-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="32b7b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="32b7b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32b7b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="32b7b-105">DESCRIPTION</span></span>
<span data-ttu-id="32b7b-106">O cmdlet **New-AzApplicationGatewayConnectionDraining** cria uma nova configuração de esvaziamento de conexão para configurações http back-end.</span><span class="sxs-lookup"><span data-stu-id="32b7b-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="32b7b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32b7b-107">EXAMPLES</span></span>

### <span data-ttu-id="32b7b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="32b7b-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="32b7b-109">O comando cria uma nova configuração de esvaziamento de conexão com o conjunto Habilitado como True e DrainTimeoutInSec definido como 42 segundos e armazena-a em $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="32b7b-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="32b7b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="32b7b-110">PARAMETERS</span></span>

### <span data-ttu-id="32b7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b7b-111">-DefaultProfile</span></span>
<span data-ttu-id="32b7b-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="32b7b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32b7b-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="32b7b-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="32b7b-114">O número de segundos de drenagem de conexão está ativo.</span><span class="sxs-lookup"><span data-stu-id="32b7b-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="32b7b-115">Os valores aceitáveis são de 1 segundo a 3600 segundos.</span><span class="sxs-lookup"><span data-stu-id="32b7b-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="32b7b-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="32b7b-116">-Enabled</span></span>
<span data-ttu-id="32b7b-117">Se o esvaziamento de conexão está habilitado ou não.</span><span class="sxs-lookup"><span data-stu-id="32b7b-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="32b7b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b7b-118">CommonParameters</span></span>
<span data-ttu-id="32b7b-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b7b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b7b-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32b7b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b7b-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32b7b-121">INPUTS</span></span>

### <span data-ttu-id="32b7b-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="32b7b-122">None</span></span>

## <span data-ttu-id="32b7b-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="32b7b-123">OUTPUTS</span></span>

### <span data-ttu-id="32b7b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="32b7b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="32b7b-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="32b7b-125">NOTES</span></span>

## <span data-ttu-id="32b7b-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32b7b-126">RELATED LINKS</span></span>

[<span data-ttu-id="32b7b-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="32b7b-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="32b7b-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="32b7b-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="32b7b-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="32b7b-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

