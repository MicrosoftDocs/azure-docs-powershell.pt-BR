---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: 378c6ee91c438bfa70ab8e89e069ad81d3515e33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114183"
---
# <span data-ttu-id="b65f8-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="b65f8-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="b65f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b65f8-102">SYNOPSIS</span></span>
<span data-ttu-id="b65f8-103">Obtém a saúde do back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b65f8-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="b65f8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b65f8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b65f8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b65f8-105">DESCRIPTION</span></span>
<span data-ttu-id="b65f8-106">O cmdlet Get-AzApplicationGatewayBackendHealth obtém a saúde do back-end do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b65f8-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="b65f8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b65f8-107">EXAMPLES</span></span>

### <span data-ttu-id="b65f8-108">Exemplo 1: obtém a saúde de back-end sem recursos expandidos.</span><span class="sxs-lookup"><span data-stu-id="b65f8-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="b65f8-109">Esse comando obtém a saúde de back-end do gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="b65f8-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="b65f8-110">Exemplo 2: obtém a saúde de back-end com recursos expandidos.</span><span class="sxs-lookup"><span data-stu-id="b65f8-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="b65f8-111">Esse comando obtém a saúde de back-end (com recursos expandidos) do gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="b65f8-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="b65f8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b65f8-112">PARAMETERS</span></span>

### <span data-ttu-id="b65f8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b65f8-113">-AsJob</span></span>
<span data-ttu-id="b65f8-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b65f8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b65f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65f8-115">-DefaultProfile</span></span>
<span data-ttu-id="b65f8-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b65f8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b65f8-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b65f8-117">-ExpandResource</span></span>
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

### <span data-ttu-id="b65f8-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b65f8-118">-Name</span></span>
<span data-ttu-id="b65f8-119">Especifica o nome do gateway de aplicativo que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b65f8-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b65f8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b65f8-120">-ResourceGroupName</span></span>
<span data-ttu-id="b65f8-121">Especifica o nome do grupo de recursos que contém o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b65f8-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="b65f8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65f8-122">CommonParameters</span></span>
<span data-ttu-id="b65f8-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b65f8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65f8-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b65f8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65f8-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="b65f8-125">INPUTS</span></span>

### <span data-ttu-id="b65f8-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b65f8-126">System.String</span></span>

## <span data-ttu-id="b65f8-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="b65f8-127">OUTPUTS</span></span>

### <span data-ttu-id="b65f8-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="b65f8-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="b65f8-129">Notas</span><span class="sxs-lookup"><span data-stu-id="b65f8-129">NOTES</span></span>
<span data-ttu-id="b65f8-130">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="b65f8-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b65f8-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b65f8-131">RELATED LINKS</span></span>

[<span data-ttu-id="b65f8-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b65f8-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

