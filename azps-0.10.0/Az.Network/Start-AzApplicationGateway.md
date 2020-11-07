---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 8c37ed72659c8b5ab00d54a7ecbe9622cb9f553b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776490"
---
# <span data-ttu-id="e4fdf-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4fdf-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="e4fdf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="e4fdf-103">Inicia um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-103">Starts an application gateway.</span></span>

## <span data-ttu-id="e4fdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4fdf-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4fdf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4fdf-105">DESCRIPTION</span></span>
<span data-ttu-id="e4fdf-106">O cmdlet **Start-AzApplicationGateway** inicia um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="e4fdf-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="e4fdf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4fdf-107">EXAMPLES</span></span>

### <span data-ttu-id="e4fdf-108">Example1: iniciar um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="e4fdf-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="e4fdf-109">Esse comando inicia o aplicativo gateway armazenado na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="e4fdf-110">OS</span><span class="sxs-lookup"><span data-stu-id="e4fdf-110">PARAMETERS</span></span>

### <span data-ttu-id="e4fdf-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4fdf-111">-ApplicationGateway</span></span>
<span data-ttu-id="e4fdf-112">Especifica o gateway do aplicativo em que este cmdlet é iniciado.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="e4fdf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4fdf-113">-DefaultProfile</span></span>
<span data-ttu-id="e4fdf-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4fdf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4fdf-115">CommonParameters</span></span>
<span data-ttu-id="e4fdf-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4fdf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4fdf-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4fdf-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4fdf-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4fdf-118">INPUTS</span></span>

### <span data-ttu-id="e4fdf-119">System. String</span><span class="sxs-lookup"><span data-stu-id="e4fdf-119">System.String</span></span>

## <span data-ttu-id="e4fdf-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4fdf-120">OUTPUTS</span></span>

### <span data-ttu-id="e4fdf-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4fdf-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e4fdf-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4fdf-122">NOTES</span></span>

## <span data-ttu-id="e4fdf-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4fdf-123">RELATED LINKS</span></span>

[<span data-ttu-id="e4fdf-124">Parar-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4fdf-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)

