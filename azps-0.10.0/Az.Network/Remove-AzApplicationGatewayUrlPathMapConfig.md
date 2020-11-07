---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 51428d44c2fc5ce29259924f71617317b163ac29
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775311"
---
# <span data-ttu-id="d153c-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d153c-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d153c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d153c-102">SYNOPSIS</span></span>
<span data-ttu-id="d153c-103">Remove os mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="d153c-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d153c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d153c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d153c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d153c-105">DESCRIPTION</span></span>
<span data-ttu-id="d153c-106">O cmdlet **Remove-AzApplicationGatewayUrlPathMapConfig** remove mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="d153c-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d153c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d153c-107">EXAMPLES</span></span>

### <span data-ttu-id="d153c-108">1:</span><span class="sxs-lookup"><span data-stu-id="d153c-108">1:</span></span>
```

```

## <span data-ttu-id="d153c-109">OS</span><span class="sxs-lookup"><span data-stu-id="d153c-109">PARAMETERS</span></span>

### <span data-ttu-id="d153c-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d153c-110">-ApplicationGateway</span></span>
<span data-ttu-id="d153c-111">Especifica o gateway do aplicativo para o qual esse cmdlet Remove a configuração do mapa de caminho da URL.</span><span class="sxs-lookup"><span data-stu-id="d153c-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d153c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d153c-112">-DefaultProfile</span></span>
<span data-ttu-id="d153c-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d153c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d153c-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d153c-114">-Name</span></span>
<span data-ttu-id="d153c-115">Especifica o nome do mapa de caminho de URL que este cmdlet Remove do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="d153c-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d153c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d153c-116">CommonParameters</span></span>
<span data-ttu-id="d153c-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d153c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d153c-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d153c-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d153c-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d153c-119">INPUTS</span></span>

### <span data-ttu-id="d153c-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d153c-120">PSApplicationGateway</span></span>
<span data-ttu-id="d153c-121">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d153c-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="d153c-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d153c-122">OUTPUTS</span></span>

### <span data-ttu-id="d153c-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d153c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d153c-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d153c-124">NOTES</span></span>

## <span data-ttu-id="d153c-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d153c-125">RELATED LINKS</span></span>

[<span data-ttu-id="d153c-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d153c-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d153c-127">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d153c-127">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d153c-128">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d153c-128">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d153c-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d153c-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


