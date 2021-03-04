---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: d5b7a2d0713fec7c11f33d778cf9708c253f153a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887125"
---
# <span data-ttu-id="1d9db-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="1d9db-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="1d9db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d9db-102">SYNOPSIS</span></span>
<span data-ttu-id="1d9db-103">Criar um objeto PSBackend</span><span class="sxs-lookup"><span data-stu-id="1d9db-103">Create a PSBackend object</span></span>

## <span data-ttu-id="1d9db-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1d9db-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d9db-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1d9db-105">DESCRIPTION</span></span>
<span data-ttu-id="1d9db-106">Criar um objeto PSBackend para criação da Porta Da Frente</span><span class="sxs-lookup"><span data-stu-id="1d9db-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="1d9db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d9db-107">EXAMPLES</span></span>

### <span data-ttu-id="1d9db-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1d9db-108">Example 1</span></span>
```powershell
PS C:\>New-AzFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="1d9db-109">Criar um objeto PSBackend para criação da Porta Da Frente</span><span class="sxs-lookup"><span data-stu-id="1d9db-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="1d9db-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1d9db-110">PARAMETERS</span></span>

### <span data-ttu-id="1d9db-111">-Address</span><span class="sxs-lookup"><span data-stu-id="1d9db-111">-Address</span></span>
<span data-ttu-id="1d9db-112">Local do back-end (endereço IP ou FQDN)</span><span class="sxs-lookup"><span data-stu-id="1d9db-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="1d9db-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="1d9db-113">-BackendHostHeader</span></span>
<span data-ttu-id="1d9db-114">O valor a ser usado como o header do host enviado para o back-end.</span><span class="sxs-lookup"><span data-stu-id="1d9db-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="1d9db-115">O valor padrão é o endereço back-end.</span><span class="sxs-lookup"><span data-stu-id="1d9db-115">Default value is the backend address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d9db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d9db-116">-DefaultProfile</span></span>
<span data-ttu-id="1d9db-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d9db-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d9db-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="1d9db-118">-EnabledState</span></span>
<span data-ttu-id="1d9db-119">Se deve habilitar o uso desse back-end.</span><span class="sxs-lookup"><span data-stu-id="1d9db-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="1d9db-120">O valor padrão é Habilitado</span><span class="sxs-lookup"><span data-stu-id="1d9db-120">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d9db-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="1d9db-121">-HttpPort</span></span>
<span data-ttu-id="1d9db-122">O número da porta TCP HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d9db-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="1d9db-123">Deve estar entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="1d9db-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="1d9db-124">O valor padrão é 80.</span><span class="sxs-lookup"><span data-stu-id="1d9db-124">Default value is 80.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d9db-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="1d9db-125">-HttpsPort</span></span>
<span data-ttu-id="1d9db-126">O número da porta TCP HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1d9db-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="1d9db-127">Deve estar entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="1d9db-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="1d9db-128">O valor padrão é 443</span><span class="sxs-lookup"><span data-stu-id="1d9db-128">Default value is 443</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d9db-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="1d9db-129">-Priority</span></span>
<span data-ttu-id="1d9db-130">Prioridade a ser usada para balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="1d9db-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="1d9db-131">Deve estar entre 1 e 5.</span><span class="sxs-lookup"><span data-stu-id="1d9db-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="1d9db-132">O valor padrão é 1</span><span class="sxs-lookup"><span data-stu-id="1d9db-132">Default value is 1</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d9db-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="1d9db-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="1d9db-134">Alias do recurso Private Link.</span><span class="sxs-lookup"><span data-stu-id="1d9db-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="1d9db-135">Preencher esse campo opcional indica que esse back-end é 'Private'</span><span class="sxs-lookup"><span data-stu-id="1d9db-135">Populating this optional field indicates that this backend is 'Private'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d9db-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="1d9db-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="1d9db-137">Uma mensagem personalizada a ser incluída na solicitação de aprovação para se conectar ao Link Particular</span><span class="sxs-lookup"><span data-stu-id="1d9db-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d9db-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="1d9db-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="1d9db-139">O local do recurso Private Link.</span><span class="sxs-lookup"><span data-stu-id="1d9db-139">The Location of Private Link resource.</span></span> <span data-ttu-id="1d9db-140">O local é necessário quando PrivateLinkResourceId é definido</span><span class="sxs-lookup"><span data-stu-id="1d9db-140">Location is required when PrivateLinkResourceId is set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d9db-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="1d9db-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="1d9db-142">A ID de Recurso do Link Particular.</span><span class="sxs-lookup"><span data-stu-id="1d9db-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="1d9db-143">Preencher esse campo opcional indica que esse back-end é 'Private'</span><span class="sxs-lookup"><span data-stu-id="1d9db-143">Populating this optional field indicates that this backend is 'Private'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d9db-144">-Weight</span><span class="sxs-lookup"><span data-stu-id="1d9db-144">-Weight</span></span>
<span data-ttu-id="1d9db-145">Peso desse ponto de extremidade para fins de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="1d9db-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="1d9db-146">Deve estar entre 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="1d9db-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="1d9db-147">O valor padrão é 50</span><span class="sxs-lookup"><span data-stu-id="1d9db-147">Default value is 50</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d9db-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d9db-148">CommonParameters</span></span>
<span data-ttu-id="1d9db-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d9db-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d9db-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d9db-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d9db-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d9db-151">INPUTS</span></span>

### <span data-ttu-id="1d9db-152">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1d9db-152">None</span></span>

## <span data-ttu-id="1d9db-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1d9db-153">OUTPUTS</span></span>

### <span data-ttu-id="1d9db-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span><span class="sxs-lookup"><span data-stu-id="1d9db-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="1d9db-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="1d9db-155">NOTES</span></span>

## <span data-ttu-id="1d9db-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d9db-156">RELATED LINKS</span></span>

[<span data-ttu-id="1d9db-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="1d9db-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
