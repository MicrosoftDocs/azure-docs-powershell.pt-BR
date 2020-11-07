---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: 378c6ee91c438bfa70ab8e89e069ad81d3515e33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955443"
---
# <span data-ttu-id="8c89b-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="8c89b-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="8c89b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c89b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c89b-103">Obtém a integridade do backend do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8c89b-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="8c89b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c89b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c89b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c89b-105">DESCRIPTION</span></span>
<span data-ttu-id="8c89b-106">O cmdlet Get-AzApplicationGatewayBackendHealth Obtém a integridade do backend do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8c89b-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="8c89b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c89b-107">EXAMPLES</span></span>

### <span data-ttu-id="8c89b-108">Exemplo 1: Obtém integridade de back-end sem recursos expandidos.</span><span class="sxs-lookup"><span data-stu-id="8c89b-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="8c89b-109">Esse comando obtém a integridade de back-end do gateway do aplicativo chamada ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="8c89b-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="8c89b-110">Exemplo 2: Obtém a integridade do back-end com recursos expandidos.</span><span class="sxs-lookup"><span data-stu-id="8c89b-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="8c89b-111">Esse comando obtém a integridade back-end (com recursos expandidos) do Application Gateway chamada ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="8c89b-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="8c89b-112">OS</span><span class="sxs-lookup"><span data-stu-id="8c89b-112">PARAMETERS</span></span>

### <span data-ttu-id="8c89b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c89b-113">-AsJob</span></span>
<span data-ttu-id="8c89b-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8c89b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c89b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c89b-115">-DefaultProfile</span></span>
<span data-ttu-id="8c89b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c89b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c89b-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="8c89b-117">-ExpandResource</span></span>
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

### <span data-ttu-id="8c89b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c89b-118">-Name</span></span>
<span data-ttu-id="8c89b-119">Especifica o nome do aplicativo do gateway que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8c89b-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8c89b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c89b-120">-ResourceGroupName</span></span>
<span data-ttu-id="8c89b-121">Especifica o nome do grupo de recursos que contém o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8c89b-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="8c89b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c89b-122">CommonParameters</span></span>
<span data-ttu-id="8c89b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c89b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c89b-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c89b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c89b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c89b-125">INPUTS</span></span>

### <span data-ttu-id="8c89b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8c89b-126">System.String</span></span>

## <span data-ttu-id="8c89b-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c89b-127">OUTPUTS</span></span>

### <span data-ttu-id="8c89b-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="8c89b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="8c89b-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c89b-129">NOTES</span></span>
<span data-ttu-id="8c89b-130">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="8c89b-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8c89b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c89b-131">RELATED LINKS</span></span>

[<span data-ttu-id="8c89b-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8c89b-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

