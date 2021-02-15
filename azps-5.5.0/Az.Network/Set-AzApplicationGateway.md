---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 38a9d9d36d4abdf85149fe9d7da5387468985daf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112774"
---
# <span data-ttu-id="9800f-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9800f-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="9800f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9800f-102">SYNOPSIS</span></span>
<span data-ttu-id="9800f-103">Atualiza um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9800f-103">Updates an application gateway.</span></span>

## <span data-ttu-id="9800f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9800f-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9800f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9800f-105">DESCRIPTION</span></span>
<span data-ttu-id="9800f-106">O cmdlet **Set-AzApplicationGateway** atualiza um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="9800f-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="9800f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9800f-107">EXAMPLES</span></span>

### <span data-ttu-id="9800f-108">Exemplo 1: Atualizar um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="9800f-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="9800f-109">Esses comandos atualizam o gateway do aplicativo com configurações na variável $AppGw e armazenam o gateway atualizado na variável $UpdatedAppGw dados.</span><span class="sxs-lookup"><span data-stu-id="9800f-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="9800f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9800f-110">PARAMETERS</span></span>

### <span data-ttu-id="9800f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9800f-111">-ApplicationGateway</span></span>
<span data-ttu-id="9800f-112">Especifica um objeto de gateway de aplicativo que representa o estado ao qual o gateway de aplicativo deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="9800f-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9800f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9800f-113">-AsJob</span></span>
<span data-ttu-id="9800f-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9800f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9800f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9800f-115">-DefaultProfile</span></span>
<span data-ttu-id="9800f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9800f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9800f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9800f-117">CommonParameters</span></span>
<span data-ttu-id="9800f-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9800f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9800f-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9800f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9800f-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="9800f-120">INPUTS</span></span>

### <span data-ttu-id="9800f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9800f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9800f-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="9800f-122">OUTPUTS</span></span>

### <span data-ttu-id="9800f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9800f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9800f-124">Notas</span><span class="sxs-lookup"><span data-stu-id="9800f-124">NOTES</span></span>

## <span data-ttu-id="9800f-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9800f-125">RELATED LINKS</span></span>

[<span data-ttu-id="9800f-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9800f-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


