---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 2cb7455d5a902882fdd98dd5fea47ae5a28e1dc9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785172"
---
# <span data-ttu-id="c3b66-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3b66-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="c3b66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3b66-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b66-103">Cria uma configuração de redirecionamento para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3b66-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3b66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3b66-104">SYNTAX</span></span>

### <span data-ttu-id="c3b66-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3b66-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3b66-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c3b66-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3b66-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="c3b66-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3b66-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3b66-108">DESCRIPTION</span></span>
<span data-ttu-id="c3b66-109">**O cmdlet New-AzureRmApplicationGatewayRedirectConfiguration** cria uma configuração de redirecionamento para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3b66-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="c3b66-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3b66-110">EXAMPLES</span></span>

### <span data-ttu-id="c3b66-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3b66-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="c3b66-112">Esse comando cria uma configuração de redirecionamento chamada Redirect01 e armazena o resultado na variável chamada $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="c3b66-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="c3b66-113">OS</span><span class="sxs-lookup"><span data-stu-id="c3b66-113">PARAMETERS</span></span>

### <span data-ttu-id="c3b66-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b66-114">-DefaultProfile</span></span>
<span data-ttu-id="c3b66-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3b66-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3b66-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="c3b66-116">-IncludePath</span></span>
<span data-ttu-id="c3b66-117">Inclua o caminho na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="c3b66-117">Include path in the redirected url.</span></span>
<span data-ttu-id="c3b66-118">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="c3b66-118">Default is true.</span></span>

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

### <span data-ttu-id="c3b66-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="c3b66-119">-IncludeQueryString</span></span>
<span data-ttu-id="c3b66-120">Inclua a cadeia de caracteres de consulta na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="c3b66-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="c3b66-121">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="c3b66-121">Default is true.</span></span>

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

### <span data-ttu-id="c3b66-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3b66-122">-Name</span></span>
<span data-ttu-id="c3b66-123">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="c3b66-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="c3b66-124">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="c3b66-124">-RedirectType</span></span>
<span data-ttu-id="c3b66-125">O tipo de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="c3b66-125">The type of redirect</span></span>

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

### <span data-ttu-id="c3b66-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="c3b66-126">-TargetListener</span></span>
<span data-ttu-id="c3b66-127">HTTPListener para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="c3b66-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="c3b66-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="c3b66-128">-TargetListenerID</span></span>
<span data-ttu-id="c3b66-129">ID da escuta para a qual redirecionar a solicitação</span><span class="sxs-lookup"><span data-stu-id="c3b66-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="c3b66-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="c3b66-130">-TargetUrl</span></span>
<span data-ttu-id="c3b66-131">URL de destino fo redirecionamento</span><span class="sxs-lookup"><span data-stu-id="c3b66-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="c3b66-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b66-132">CommonParameters</span></span>
<span data-ttu-id="c3b66-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3b66-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b66-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3b66-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b66-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3b66-135">INPUTS</span></span>

### <span data-ttu-id="c3b66-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c3b66-136">None</span></span>

## <span data-ttu-id="c3b66-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3b66-137">OUTPUTS</span></span>

### <span data-ttu-id="c3b66-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3b66-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="c3b66-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3b66-139">NOTES</span></span>

## <span data-ttu-id="c3b66-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3b66-140">RELATED LINKS</span></span>

