---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 7f3834e13ce6fb6c3e9a661fead09ffcfab78933
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439914"
---
# <span data-ttu-id="70d65-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="70d65-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="70d65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70d65-102">SYNOPSIS</span></span>
<span data-ttu-id="70d65-103">Cria uma configuração de redirecionamento para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="70d65-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70d65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70d65-104">SYNTAX</span></span>

### <span data-ttu-id="70d65-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="70d65-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70d65-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="70d65-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70d65-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="70d65-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70d65-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70d65-108">DESCRIPTION</span></span>
<span data-ttu-id="70d65-109">**O cmdlet New-AzureRmApplicationGatewayRedirectConfiguration** cria uma configuração de redirecionamento para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="70d65-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="70d65-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70d65-110">EXAMPLES</span></span>

### <span data-ttu-id="70d65-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="70d65-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="70d65-112">Esse comando cria uma configuração de redirecionamento chamada Redirect01 e armazena o resultado na variável chamada $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="70d65-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="70d65-113">OS</span><span class="sxs-lookup"><span data-stu-id="70d65-113">PARAMETERS</span></span>

### <span data-ttu-id="70d65-114">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="70d65-114">-IncludePath</span></span>
<span data-ttu-id="70d65-115">Inclua o caminho na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="70d65-115">Include path in the redirected url.</span></span>
<span data-ttu-id="70d65-116">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="70d65-116">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d65-117">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="70d65-117">-IncludeQueryString</span></span>
<span data-ttu-id="70d65-118">Inclua a cadeia de caracteres de consulta na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="70d65-118">Include query string in the redirected url.</span></span>
<span data-ttu-id="70d65-119">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="70d65-119">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d65-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="70d65-120">-Name</span></span>
<span data-ttu-id="70d65-121">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="70d65-121">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="70d65-122">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="70d65-122">-RedirectType</span></span>
<span data-ttu-id="70d65-123">O tipo de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="70d65-123">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d65-124">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="70d65-124">-TargetListener</span></span>
<span data-ttu-id="70d65-125">HTTPListener para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="70d65-125">HTTPListener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d65-126">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="70d65-126">-TargetListenerID</span></span>
<span data-ttu-id="70d65-127">ID da escuta para a qual redirecionar a solicitação</span><span class="sxs-lookup"><span data-stu-id="70d65-127">ID of  listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d65-128">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="70d65-128">-TargetUrl</span></span>
<span data-ttu-id="70d65-129">URL de destino fo redirecionamento</span><span class="sxs-lookup"><span data-stu-id="70d65-129">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d65-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d65-130">-DefaultProfile</span></span>
<span data-ttu-id="70d65-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70d65-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70d65-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d65-132">CommonParameters</span></span>
<span data-ttu-id="70d65-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70d65-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d65-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70d65-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d65-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70d65-135">INPUTS</span></span>

### <span data-ttu-id="70d65-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="70d65-136">None</span></span>

## <span data-ttu-id="70d65-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70d65-137">OUTPUTS</span></span>

### <span data-ttu-id="70d65-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="70d65-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="70d65-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70d65-139">NOTES</span></span>

## <span data-ttu-id="70d65-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70d65-140">RELATED LINKS</span></span>

