---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: eb4415f4c61fd97543bd0e50de6a0a3737f435f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771810"
---
# <span data-ttu-id="5383a-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="5383a-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="5383a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5383a-102">SYNOPSIS</span></span>
<span data-ttu-id="5383a-103">Obtém a integridade do backend do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5383a-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="5383a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5383a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5383a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5383a-105">DESCRIPTION</span></span>
<span data-ttu-id="5383a-106">O cmdlet Get-AzApplicationGatewayBackendHealth Obtém a integridade do backend do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5383a-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="5383a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5383a-107">EXAMPLES</span></span>

### <span data-ttu-id="5383a-108">Exemplo 1: Obtém integridade de back-end sem recursos expandidos.</span><span class="sxs-lookup"><span data-stu-id="5383a-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="5383a-109">Esse comando obtém a integridade de back-end do gateway do aplicativo chamada ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="5383a-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="5383a-110">Exemplo 2: Obtém a integridade do back-end com recursos expandidos.</span><span class="sxs-lookup"><span data-stu-id="5383a-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="5383a-111">Esse comando obtém a integridade back-end (com recursos expandidos) do Application Gateway chamada ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="5383a-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="5383a-112">OS</span><span class="sxs-lookup"><span data-stu-id="5383a-112">PARAMETERS</span></span>

### <span data-ttu-id="5383a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5383a-113">-AsJob</span></span>
<span data-ttu-id="5383a-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5383a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5383a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5383a-115">-DefaultProfile</span></span>
<span data-ttu-id="5383a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5383a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5383a-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="5383a-117">-ExpandResource</span></span>
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

### <span data-ttu-id="5383a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5383a-118">-Name</span></span>
<span data-ttu-id="5383a-119">Especifica o nome do aplicativo do gateway que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="5383a-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5383a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5383a-120">-ResourceGroupName</span></span>
<span data-ttu-id="5383a-121">Especifica o nome do grupo de recursos que contém o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5383a-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="5383a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5383a-122">CommonParameters</span></span>
<span data-ttu-id="5383a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5383a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5383a-124">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5383a-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5383a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5383a-125">INPUTS</span></span>

### <span data-ttu-id="5383a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5383a-126">System.String</span></span>

## <span data-ttu-id="5383a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5383a-127">OUTPUTS</span></span>

### <span data-ttu-id="5383a-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="5383a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="5383a-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5383a-129">NOTES</span></span>
<span data-ttu-id="5383a-130">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="5383a-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5383a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5383a-131">RELATED LINKS</span></span>

[<span data-ttu-id="5383a-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5383a-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

