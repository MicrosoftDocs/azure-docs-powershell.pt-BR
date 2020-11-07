---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e768c8f5e557954dd6e932726f38b9844699de9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771927"
---
# <span data-ttu-id="2bc5d-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bc5d-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="2bc5d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bc5d-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc5d-103">Cria uma configuração de redirecionamento para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bc5d-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="2bc5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bc5d-104">SYNTAX</span></span>

### <span data-ttu-id="2bc5d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2bc5d-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bc5d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2bc5d-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bc5d-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="2bc5d-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bc5d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bc5d-108">DESCRIPTION</span></span>
<span data-ttu-id="2bc5d-109">**O cmdlet New-AzApplicationGatewayRedirectConfiguration** cria uma configuração de redirecionamento para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2bc5d-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="2bc5d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bc5d-110">EXAMPLES</span></span>

### <span data-ttu-id="2bc5d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2bc5d-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="2bc5d-112">Esse comando cria uma configuração de redirecionamento chamada Redirect01 e armazena o resultado na variável chamada $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="2bc5d-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="2bc5d-113">OS</span><span class="sxs-lookup"><span data-stu-id="2bc5d-113">PARAMETERS</span></span>

### <span data-ttu-id="2bc5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc5d-114">-DefaultProfile</span></span>
<span data-ttu-id="2bc5d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc5d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bc5d-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="2bc5d-116">-IncludePath</span></span>
<span data-ttu-id="2bc5d-117">Inclua o caminho na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="2bc5d-117">Include path in the redirected url.</span></span>
<span data-ttu-id="2bc5d-118">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="2bc5d-118">Default is true.</span></span>

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

### <span data-ttu-id="2bc5d-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="2bc5d-119">-IncludeQueryString</span></span>
<span data-ttu-id="2bc5d-120">Inclua a cadeia de caracteres de consulta na URL redirecionada.</span><span class="sxs-lookup"><span data-stu-id="2bc5d-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="2bc5d-121">O padrão é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="2bc5d-121">Default is true.</span></span>

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

### <span data-ttu-id="2bc5d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2bc5d-122">-Name</span></span>
<span data-ttu-id="2bc5d-123">O nome da configuração de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="2bc5d-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="2bc5d-124">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="2bc5d-124">-RedirectType</span></span>
<span data-ttu-id="2bc5d-125">O tipo de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="2bc5d-125">The type of redirect</span></span>

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

### <span data-ttu-id="2bc5d-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="2bc5d-126">-TargetListener</span></span>
<span data-ttu-id="2bc5d-127">Escuta HTTP para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="2bc5d-127">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="2bc5d-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="2bc5d-128">-TargetListenerID</span></span>
<span data-ttu-id="2bc5d-129">ID do ouvinte HTTP para redirecionar a solicitação para</span><span class="sxs-lookup"><span data-stu-id="2bc5d-129">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="2bc5d-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="2bc5d-130">-TargetUrl</span></span>
<span data-ttu-id="2bc5d-131">URL de destino fo redirecionamento</span><span class="sxs-lookup"><span data-stu-id="2bc5d-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="2bc5d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc5d-132">CommonParameters</span></span>
<span data-ttu-id="2bc5d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc5d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc5d-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bc5d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc5d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bc5d-135">INPUTS</span></span>

### <span data-ttu-id="2bc5d-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2bc5d-136">None</span></span>

## <span data-ttu-id="2bc5d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bc5d-137">OUTPUTS</span></span>

### <span data-ttu-id="2bc5d-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bc5d-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="2bc5d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bc5d-139">NOTES</span></span>

## <span data-ttu-id="2bc5d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bc5d-140">RELATED LINKS</span></span>

[<span data-ttu-id="2bc5d-141">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bc5d-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="2bc5d-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bc5d-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="2bc5d-143">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bc5d-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="2bc5d-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bc5d-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
