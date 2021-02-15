---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112852"
---
# <span data-ttu-id="638e7-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="638e7-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="638e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="638e7-102">SYNOPSIS</span></span>
<span data-ttu-id="638e7-103">Cria uma nova configuração de esgotamento de conexão para configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="638e7-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="638e7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="638e7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="638e7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="638e7-105">DESCRIPTION</span></span>
<span data-ttu-id="638e7-106">O cmdlet **New-AzApplicationGatewayConnectionConnectionDraining** cria uma nova configuração de esgotamento de conexão para configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="638e7-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="638e7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="638e7-107">EXAMPLES</span></span>

### <span data-ttu-id="638e7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="638e7-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="638e7-109">O comando cria uma nova configuração de esgotamento de conexão com Habilitado definido como True e DrainTimeoutInSec definido como 42 segundos e a armazena em $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="638e7-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="638e7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="638e7-110">PARAMETERS</span></span>

### <span data-ttu-id="638e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="638e7-111">-DefaultProfile</span></span>
<span data-ttu-id="638e7-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="638e7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="638e7-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="638e7-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="638e7-114">O número de segundos de estouros de conexão está ativo.</span><span class="sxs-lookup"><span data-stu-id="638e7-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="638e7-115">Valores aceitáveis variam de 1 segundo a 3600 segundos.</span><span class="sxs-lookup"><span data-stu-id="638e7-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="638e7-116">-Habilitado</span><span class="sxs-lookup"><span data-stu-id="638e7-116">-Enabled</span></span>
<span data-ttu-id="638e7-117">Se a conexão está habilitada ou não.</span><span class="sxs-lookup"><span data-stu-id="638e7-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="638e7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="638e7-118">CommonParameters</span></span>
<span data-ttu-id="638e7-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="638e7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="638e7-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="638e7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="638e7-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="638e7-121">INPUTS</span></span>

### <span data-ttu-id="638e7-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="638e7-122">None</span></span>

## <span data-ttu-id="638e7-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="638e7-123">OUTPUTS</span></span>

### <span data-ttu-id="638e7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="638e7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="638e7-125">Notas</span><span class="sxs-lookup"><span data-stu-id="638e7-125">NOTES</span></span>

## <span data-ttu-id="638e7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="638e7-126">RELATED LINKS</span></span>

[<span data-ttu-id="638e7-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="638e7-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="638e7-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="638e7-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="638e7-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="638e7-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

