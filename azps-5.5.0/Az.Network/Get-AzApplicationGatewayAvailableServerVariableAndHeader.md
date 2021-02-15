---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114191"
---
# <span data-ttu-id="35466-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="35466-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="35466-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35466-102">SYNOPSIS</span></span>
<span data-ttu-id="35466-103">Obter as variáveis de servidor com suporte e os headers de solicitação e resposta disponíveis.</span><span class="sxs-lookup"><span data-stu-id="35466-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="35466-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35466-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="35466-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="35466-105">DESCRIPTION</span></span>
<span data-ttu-id="35466-106">O cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** obtém as variáveis de servidor com suporte e os headers de solicitação e resposta disponíveis.</span><span class="sxs-lookup"><span data-stu-id="35466-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="35466-107">Os parâmetros podem ser usados para obter as variáveis ou listas de headers.</span><span class="sxs-lookup"><span data-stu-id="35466-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="35466-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="35466-108">EXAMPLES</span></span>

### <span data-ttu-id="35466-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="35466-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="35466-110">Esses comandos retornam todas as variáveis de servidor disponíveis.</span><span class="sxs-lookup"><span data-stu-id="35466-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="35466-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="35466-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="35466-112">Esses comandos retornam todos os headers de solicitação disponíveis.</span><span class="sxs-lookup"><span data-stu-id="35466-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="35466-113">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="35466-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="35466-114">Esses comandos retornam todos os headers de resposta disponíveis.</span><span class="sxs-lookup"><span data-stu-id="35466-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="35466-115">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="35466-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="35466-116">Esses comandos retornam todas as variáveis de servidor disponíveis, os headers de solicitação e resposta.</span><span class="sxs-lookup"><span data-stu-id="35466-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="35466-117">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="35466-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="35466-118">Esses comandos retornam todas as variáveis de servidor disponíveis, os headers de solicitação e resposta.</span><span class="sxs-lookup"><span data-stu-id="35466-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="35466-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35466-119">PARAMETERS</span></span>

### <span data-ttu-id="35466-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35466-120">-DefaultProfile</span></span>
<span data-ttu-id="35466-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35466-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35466-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="35466-122">-RequestHeader</span></span>
<span data-ttu-id="35466-123">Headers de solicitação disponíveis do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35466-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="35466-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="35466-124">-ResponseHeader</span></span>
<span data-ttu-id="35466-125">Headers de resposta disponíveis do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35466-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="35466-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="35466-126">-ServerVariable</span></span>
<span data-ttu-id="35466-127">Variáveis de servidor disponíveis do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35466-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="35466-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35466-128">CommonParameters</span></span>
<span data-ttu-id="35466-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35466-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35466-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35466-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35466-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="35466-131">INPUTS</span></span>

### <span data-ttu-id="35466-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="35466-132">None</span></span>

## <span data-ttu-id="35466-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="35466-133">OUTPUTS</span></span>

### <span data-ttu-id="35466-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="35466-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="35466-135">Notas</span><span class="sxs-lookup"><span data-stu-id="35466-135">NOTES</span></span>
<span data-ttu-id="35466-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** é um alias para o cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader.**</span><span class="sxs-lookup"><span data-stu-id="35466-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="35466-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35466-137">RELATED LINKS</span></span>
