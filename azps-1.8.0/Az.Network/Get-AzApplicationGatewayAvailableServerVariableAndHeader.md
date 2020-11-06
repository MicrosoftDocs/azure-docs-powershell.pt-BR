---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8f0fc8caba03251ede507fc383ef99c10a06eeb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600669"
---
# <span data-ttu-id="596d7-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="596d7-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="596d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="596d7-102">SYNOPSIS</span></span>
<span data-ttu-id="596d7-103">Obter as variáveis de servidor com suporte e os cabeçalhos de solicitação e resposta disponíveis.</span><span class="sxs-lookup"><span data-stu-id="596d7-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="596d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="596d7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="596d7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="596d7-105">DESCRIPTION</span></span>
<span data-ttu-id="596d7-106">O cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** Obtém as variáveis de servidor com suporte e os cabeçalhos de solicitação e resposta disponíveis.</span><span class="sxs-lookup"><span data-stu-id="596d7-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="596d7-107">Os parâmetros podem ser usados para obter as listas de variáveis ou de cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="596d7-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="596d7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="596d7-108">EXAMPLES</span></span>

### <span data-ttu-id="596d7-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="596d7-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="596d7-110">Esses comandos retornam todas as variáveis de servidor disponíveis.</span><span class="sxs-lookup"><span data-stu-id="596d7-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="596d7-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="596d7-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="596d7-112">Esses comandos retornam todos os cabeçalhos de solicitação disponíveis.</span><span class="sxs-lookup"><span data-stu-id="596d7-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="596d7-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="596d7-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="596d7-114">Esses comandos retornam todos os cabeçalhos de resposta disponíveis.</span><span class="sxs-lookup"><span data-stu-id="596d7-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="596d7-115">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="596d7-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="596d7-116">Esses comandos retornam todas as variáveis de servidor disponíveis, cabeçalhos de solicitação e resposta.</span><span class="sxs-lookup"><span data-stu-id="596d7-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="596d7-117">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="596d7-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="596d7-118">Esses comandos retornam todas as variáveis de servidor disponíveis, cabeçalhos de solicitação e resposta.</span><span class="sxs-lookup"><span data-stu-id="596d7-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="596d7-119">OS</span><span class="sxs-lookup"><span data-stu-id="596d7-119">PARAMETERS</span></span>

### <span data-ttu-id="596d7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="596d7-120">-DefaultProfile</span></span>
<span data-ttu-id="596d7-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="596d7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="596d7-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="596d7-122">-RequestHeader</span></span>
<span data-ttu-id="596d7-123">O Application Gateway disponibilizou cabeçalhos de solicitação.</span><span class="sxs-lookup"><span data-stu-id="596d7-123">Application Gateway available request headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="596d7-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="596d7-124">-ResponseHeader</span></span>
<span data-ttu-id="596d7-125">Cabeçalhos de resposta do Application Gateway disponíveis.</span><span class="sxs-lookup"><span data-stu-id="596d7-125">Application Gateway available response headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="596d7-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="596d7-126">-ServerVariable</span></span>
<span data-ttu-id="596d7-127">Variáveis de servidor disponíveis do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="596d7-127">Application Gateway available server variables.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="596d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="596d7-128">CommonParameters</span></span>
<span data-ttu-id="596d7-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="596d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="596d7-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="596d7-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="596d7-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="596d7-131">INPUTS</span></span>

### <span data-ttu-id="596d7-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="596d7-132">None</span></span>

## <span data-ttu-id="596d7-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="596d7-133">OUTPUTS</span></span>

### <span data-ttu-id="596d7-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="596d7-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="596d7-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="596d7-135">NOTES</span></span>
<span data-ttu-id="596d7-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** é um alias para o cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** .</span><span class="sxs-lookup"><span data-stu-id="596d7-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="596d7-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="596d7-137">RELATED LINKS</span></span>
