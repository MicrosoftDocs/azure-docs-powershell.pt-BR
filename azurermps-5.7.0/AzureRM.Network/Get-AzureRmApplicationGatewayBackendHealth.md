---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: 6e6a2bef9ea6bc237db97139bcc7e9e7a0624fd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427539"
---
# <span data-ttu-id="9f5e1-101">Get-AzureRmApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="9f5e1-101">Get-AzureRmApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="9f5e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5e1-103">Obtém a integridade do backend do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9f5e1-103">Gets application gateway backend health.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f5e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f5e1-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f5e1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f5e1-105">DESCRIPTION</span></span>
<span data-ttu-id="9f5e1-106">O cmdlet Get-AzureRmApplicationGatewayBackendHealth Obtém a integridade do backend do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9f5e1-106">The Get-AzureRmApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="9f5e1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f5e1-107">EXAMPLES</span></span>

### <span data-ttu-id="9f5e1-108">--------------------------Exemplo 1: Obtém a integridade do back-end sem recursos expandidos.</span><span class="sxs-lookup"><span data-stu-id="9f5e1-108">--------------------------  Example 1: Gets backend health without expanded resources.</span></span>  --------------------------
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="9f5e1-109">Esse comando obtém a integridade de back-end do gateway do aplicativo chamada ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="9f5e1-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="9f5e1-110">--------------------------Exemplo 1: Obtém a integridade do back-end com recursos expandidos.</span><span class="sxs-lookup"><span data-stu-id="9f5e1-110">--------------------------  Example 1: Gets backend health with expanded resources.</span></span>  --------------------------
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="9f5e1-111">Esse comando obtém a integridade back-end (com recursos expandidos) do Application Gateway chamada ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="9f5e1-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="9f5e1-112">OS</span><span class="sxs-lookup"><span data-stu-id="9f5e1-112">PARAMETERS</span></span>

### <span data-ttu-id="9f5e1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f5e1-113">-AsJob</span></span>
<span data-ttu-id="9f5e1-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9f5e1-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5e1-115">-DefaultProfile</span></span>
<span data-ttu-id="9f5e1-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f5e1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f5e1-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="9f5e1-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5e1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f5e1-118">-Name</span></span>
<span data-ttu-id="9f5e1-119">Especifica o nome do aplicativo do gateway que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9f5e1-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5e1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f5e1-120">-ResourceGroupName</span></span>
<span data-ttu-id="9f5e1-121">Especifica o nome do grupo de recursos que contém o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9f5e1-121">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5e1-122">CommonParameters</span></span>
<span data-ttu-id="9f5e1-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f5e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5e1-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f5e1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5e1-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f5e1-125">INPUTS</span></span>

### <span data-ttu-id="9f5e1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9f5e1-126">System.String</span></span>

## <span data-ttu-id="9f5e1-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f5e1-127">OUTPUTS</span></span>

### <span data-ttu-id="9f5e1-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="9f5e1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="9f5e1-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f5e1-129">NOTES</span></span>
<span data-ttu-id="9f5e1-130">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="9f5e1-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9f5e1-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f5e1-131">RELATED LINKS</span></span>

[<span data-ttu-id="9f5e1-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9f5e1-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

