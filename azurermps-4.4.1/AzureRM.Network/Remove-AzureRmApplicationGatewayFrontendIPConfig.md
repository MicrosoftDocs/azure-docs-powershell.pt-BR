---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: ffd2d6811aa210aa838c7fb623788e11223c34e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439904"
---
# <span data-ttu-id="a1c24-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a1c24-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="a1c24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1c24-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c24-103">Remove uma configuração de IP de front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1c24-103">Removes a front-end IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1c24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1c24-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1c24-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1c24-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c24-106">O cmdlet **Remove-AzureRmApplicationGatewayFrontendIPConfig** remove o IP de front-end de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c24-106">The **Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="a1c24-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1c24-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c24-108">Exemplo 1: remover uma configuração de IP de front-end</span><span class="sxs-lookup"><span data-stu-id="a1c24-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="a1c24-109">O primeiro comando obtém um gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a1c24-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a1c24-110">O segundo comando Remove a configuração de IP de front-end denominada FrontEndIP02 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a1c24-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a1c24-111">OS</span><span class="sxs-lookup"><span data-stu-id="a1c24-111">PARAMETERS</span></span>

### <span data-ttu-id="a1c24-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1c24-112">-ApplicationGateway</span></span>
<span data-ttu-id="a1c24-113">Especifica um gateway do aplicativo do qual remover uma configuração de IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="a1c24-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="a1c24-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1c24-114">-Name</span></span>
<span data-ttu-id="a1c24-115">Especifica o nome de uma configuração de IP de front-end a ser removida.</span><span class="sxs-lookup"><span data-stu-id="a1c24-115">Specifies the name of a front-end IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c24-116">-DefaultProfile</span></span>
<span data-ttu-id="a1c24-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c24-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c24-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c24-118">CommonParameters</span></span>
<span data-ttu-id="a1c24-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c24-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c24-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c24-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c24-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1c24-121">INPUTS</span></span>

### <span data-ttu-id="a1c24-122">System. String</span><span class="sxs-lookup"><span data-stu-id="a1c24-122">System.String</span></span>

## <span data-ttu-id="a1c24-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1c24-123">OUTPUTS</span></span>

### <span data-ttu-id="a1c24-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1c24-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a1c24-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1c24-125">NOTES</span></span>

## <span data-ttu-id="a1c24-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1c24-126">RELATED LINKS</span></span>

[<span data-ttu-id="a1c24-127">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a1c24-127">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a1c24-128">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a1c24-128">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a1c24-129">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a1c24-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a1c24-130">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a1c24-130">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


