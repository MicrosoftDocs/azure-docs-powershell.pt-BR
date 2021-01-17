---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 38a9d9d36d4abdf85149fe9d7da5387468985daf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428880"
---
# <span data-ttu-id="0b6bd-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b6bd-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="0b6bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="0b6bd-103">Atualiza um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0b6bd-103">Updates an application gateway.</span></span>

## <span data-ttu-id="0b6bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b6bd-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b6bd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b6bd-105">DESCRIPTION</span></span>
<span data-ttu-id="0b6bd-106">O cmdlet **set-AzApplicationGateway** atualiza um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b6bd-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="0b6bd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b6bd-107">EXAMPLES</span></span>

### <span data-ttu-id="0b6bd-108">Exemplo 1: atualizar um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="0b6bd-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="0b6bd-109">Esses comandos atualizam o gateway do aplicativo com configurações na variável $AppGw e armazena o gateway atualizado na variável $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="0b6bd-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="0b6bd-110">OS</span><span class="sxs-lookup"><span data-stu-id="0b6bd-110">PARAMETERS</span></span>

### <span data-ttu-id="0b6bd-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b6bd-111">-ApplicationGateway</span></span>
<span data-ttu-id="0b6bd-112">Especifica um objeto do aplicativo gateway que representa o estado para o qual o gateway do aplicativo deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="0b6bd-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="0b6bd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b6bd-113">-AsJob</span></span>
<span data-ttu-id="0b6bd-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0b6bd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b6bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b6bd-115">-DefaultProfile</span></span>
<span data-ttu-id="0b6bd-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b6bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b6bd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b6bd-117">CommonParameters</span></span>
<span data-ttu-id="0b6bd-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b6bd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b6bd-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b6bd-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b6bd-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b6bd-120">INPUTS</span></span>

### <span data-ttu-id="0b6bd-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b6bd-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0b6bd-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b6bd-122">OUTPUTS</span></span>

### <span data-ttu-id="0b6bd-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b6bd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0b6bd-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b6bd-124">NOTES</span></span>

## <span data-ttu-id="0b6bd-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b6bd-125">RELATED LINKS</span></span>

[<span data-ttu-id="0b6bd-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b6bd-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


