---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 0d2d9d9390f60c7d7eb74061a52b9b437acdf772
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428167"
---
# <span data-ttu-id="97b25-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="97b25-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="97b25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97b25-102">SYNOPSIS</span></span>
<span data-ttu-id="97b25-103">Cria uma configuração de redirecionamento para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97b25-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97b25-104">SYNTAX</span></span>

### <span data-ttu-id="97b25-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="97b25-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97b25-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="97b25-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97b25-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="97b25-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97b25-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97b25-108">DESCRIPTION</span></span>
<span data-ttu-id="97b25-109">**O cmdlet New-AzureRmApplicationGatewayRedirectConfiguration** cria uma configuração de redirecionamento para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97b25-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="97b25-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97b25-110">EXAMPLES</span></span>

### <span data-ttu-id="97b25-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="97b25-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="97b25-112">Esse comando cria uma configuração de redirecionamento chamada Redirect01 e armazena o resultado na variável chamada $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="97b25-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="97b25-113">OS</span><span class="sxs-lookup"><span data-stu-id="97b25-113">PARAMETERS</span></span>

### <span data-ttu-id="97b25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b25-114">-DefaultProfile</span></span>
<span data-ttu-id="97b25-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97b25-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97b25-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="97b25-116">-IncludePath</span></span>
<span data-ttu-id="97b25-117">Inclua o caminho na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="97b25-117">Include path in the redirected url.</span></span>
<span data-ttu-id="97b25-118">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="97b25-118">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b25-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="97b25-119">-IncludeQueryString</span></span>
<span data-ttu-id="97b25-120">Inclua a cadeia de caracteres de consulta na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="97b25-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="97b25-121">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="97b25-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b25-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="97b25-122">-Name</span></span>
<span data-ttu-id="97b25-123">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="97b25-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="97b25-124">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="97b25-124">-RedirectType</span></span>
<span data-ttu-id="97b25-125">O tipo de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="97b25-125">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b25-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="97b25-126">-TargetListener</span></span>
<span data-ttu-id="97b25-127">HTTPListener para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="97b25-127">HTTPListener to redirect the request to</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b25-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="97b25-128">-TargetListenerID</span></span>
<span data-ttu-id="97b25-129">ID da escuta para a qual redirecionar a solicitação</span><span class="sxs-lookup"><span data-stu-id="97b25-129">ID of  listener to redirect the request to</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b25-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="97b25-130">-TargetUrl</span></span>
<span data-ttu-id="97b25-131">URL de destino fo redirecionamento</span><span class="sxs-lookup"><span data-stu-id="97b25-131">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b25-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b25-132">CommonParameters</span></span>
<span data-ttu-id="97b25-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b25-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b25-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b25-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b25-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97b25-135">INPUTS</span></span>

### <span data-ttu-id="97b25-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="97b25-136">None</span></span>

## <span data-ttu-id="97b25-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97b25-137">OUTPUTS</span></span>

### <span data-ttu-id="97b25-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="97b25-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="97b25-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97b25-139">NOTES</span></span>

## <span data-ttu-id="97b25-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97b25-140">RELATED LINKS</span></span>

