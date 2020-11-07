---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 34f3de9e2dafe3cfb9b15aad1dda7d75bab67c20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772236"
---
# <span data-ttu-id="e651a-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e651a-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="e651a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e651a-102">SYNOPSIS</span></span>
<span data-ttu-id="e651a-103">Atualiza um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e651a-103">Updates an application gateway.</span></span>

## <span data-ttu-id="e651a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e651a-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e651a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e651a-105">DESCRIPTION</span></span>
<span data-ttu-id="e651a-106">O cmdlet **set-AzApplicationGateway** atualiza um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="e651a-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="e651a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e651a-107">EXAMPLES</span></span>

### <span data-ttu-id="e651a-108">Exemplo 1: atualizar um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="e651a-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="e651a-109">Esse comando atualiza o gateway do aplicativo com configurações na variável $AppGw e armazena o gateway atualizado na variável $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="e651a-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="e651a-110">OS</span><span class="sxs-lookup"><span data-stu-id="e651a-110">PARAMETERS</span></span>

### <span data-ttu-id="e651a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e651a-111">-ApplicationGateway</span></span>
<span data-ttu-id="e651a-112">Especifica um objeto do aplicativo gateway que representa o estado para o qual o gateway do aplicativo deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="e651a-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="e651a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e651a-113">-AsJob</span></span>
<span data-ttu-id="e651a-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e651a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e651a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e651a-115">-DefaultProfile</span></span>
<span data-ttu-id="e651a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e651a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e651a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e651a-117">CommonParameters</span></span>
<span data-ttu-id="e651a-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e651a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e651a-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e651a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e651a-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e651a-120">INPUTS</span></span>

### <span data-ttu-id="e651a-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e651a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e651a-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e651a-122">OUTPUTS</span></span>

### <span data-ttu-id="e651a-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e651a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e651a-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e651a-124">NOTES</span></span>

## <span data-ttu-id="e651a-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e651a-125">RELATED LINKS</span></span>

[<span data-ttu-id="e651a-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e651a-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


