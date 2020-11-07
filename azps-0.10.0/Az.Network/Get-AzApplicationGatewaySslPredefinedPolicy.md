---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 2c55da6b7193d02de51e273df4626152d6d088fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775567"
---
# <span data-ttu-id="eebbc-101">Get-AzApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="eebbc-101">Get-AzApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="eebbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eebbc-102">SYNOPSIS</span></span>
<span data-ttu-id="eebbc-103">Obtém políticas SSL predefinidas fornecidas pelo Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="eebbc-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="eebbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eebbc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eebbc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eebbc-105">DESCRIPTION</span></span>
<span data-ttu-id="eebbc-106">O cmdlet **Get-AzApplicationGatewaySslPredefinedPolicy** tem diretivas SSL predefinidas fornecidas pelo Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="eebbc-106">The **Get-AzApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="eebbc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eebbc-107">EXAMPLES</span></span>

### <span data-ttu-id="eebbc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eebbc-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="eebbc-109">Esses comandos retornam todas as políticas de SSL predefinidas.</span><span class="sxs-lookup"><span data-stu-id="eebbc-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="eebbc-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="eebbc-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="eebbc-111">Esses comandos retornam uma política predefinida com o nome AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="eebbc-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="eebbc-112">OS</span><span class="sxs-lookup"><span data-stu-id="eebbc-112">PARAMETERS</span></span>

### <span data-ttu-id="eebbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebbc-113">-DefaultProfile</span></span>
<span data-ttu-id="eebbc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eebbc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eebbc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="eebbc-115">-Name</span></span>
<span data-ttu-id="eebbc-116">Nome da política predefinida SSL</span><span class="sxs-lookup"><span data-stu-id="eebbc-116">Name of the ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eebbc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebbc-117">CommonParameters</span></span>
<span data-ttu-id="eebbc-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eebbc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebbc-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eebbc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebbc-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eebbc-120">INPUTS</span></span>

### <span data-ttu-id="eebbc-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="eebbc-121">None</span></span>

## <span data-ttu-id="eebbc-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eebbc-122">OUTPUTS</span></span>

### <span data-ttu-id="eebbc-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="eebbc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="eebbc-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eebbc-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="eebbc-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eebbc-125">NOTES</span></span>

## <span data-ttu-id="eebbc-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eebbc-126">RELATED LINKS</span></span>

