---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: d3f5114243828623ba6c55e9694cc4250ae12657
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427872"
---
# <span data-ttu-id="a7f86-101">Get-AzureRmApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="a7f86-101">Get-AzureRmApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="a7f86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7f86-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f86-103">Obtém a integridade do backend do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a7f86-103">Gets application gateway backend health.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7f86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7f86-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7f86-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7f86-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f86-106">O cmdlet Get-AzureRmApplicationGatewayBackendHealth Obtém a integridade do backend do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a7f86-106">The Get-AzureRmApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="a7f86-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7f86-107">EXAMPLES</span></span>

### <span data-ttu-id="a7f86-108">--------------------------Exemplo 1: Obtém a integridade do back-end sem recursos expandidos.</span><span class="sxs-lookup"><span data-stu-id="a7f86-108">--------------------------  Example 1: Gets backend health without expanded resources.</span></span>  --------------------------
<span data-ttu-id="a7f86-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="a7f86-109">@{paragraph=PS C:\\\>}</span></span>



















```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="a7f86-110">Esse comando obtém a integridade de back-end do gateway do aplicativo chamada ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="a7f86-110">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="a7f86-111">--------------------------Exemplo 1: Obtém a integridade do back-end com recursos expandidos.</span><span class="sxs-lookup"><span data-stu-id="a7f86-111">--------------------------  Example 1: Gets backend health with expanded resources.</span></span>  --------------------------
<span data-ttu-id="a7f86-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="a7f86-112">@{paragraph=PS C:\\\>}</span></span>



















```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="a7f86-113">Esse comando obtém a integridade back-end (com recursos expandidos) do Application Gateway chamada ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="a7f86-113">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="a7f86-114">OS</span><span class="sxs-lookup"><span data-stu-id="a7f86-114">PARAMETERS</span></span>

### <span data-ttu-id="a7f86-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a7f86-115">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f86-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7f86-116">-Name</span></span>
<span data-ttu-id="a7f86-117">Especifica o nome do aplicativo do gateway que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a7f86-117">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f86-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f86-118">-ResourceGroupName</span></span>
<span data-ttu-id="a7f86-119">Especifica o nome do grupo de recursos que contém o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a7f86-119">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f86-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f86-120">-DefaultProfile</span></span>
<span data-ttu-id="a7f86-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f86-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7f86-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f86-122">CommonParameters</span></span>
<span data-ttu-id="a7f86-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f86-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f86-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f86-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f86-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7f86-125">INPUTS</span></span>

### <span data-ttu-id="a7f86-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a7f86-126">System.String</span></span>

## <span data-ttu-id="a7f86-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7f86-127">OUTPUTS</span></span>

### <span data-ttu-id="a7f86-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="a7f86-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="a7f86-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7f86-129">NOTES</span></span>
<span data-ttu-id="a7f86-130">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="a7f86-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a7f86-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7f86-131">RELATED LINKS</span></span>

[<span data-ttu-id="a7f86-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7f86-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

