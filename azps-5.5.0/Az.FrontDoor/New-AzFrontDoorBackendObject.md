---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113823"
---
# <span data-ttu-id="d2b9b-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="d2b9b-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="d2b9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="d2b9b-103">Criar um objeto PSBackend</span><span class="sxs-lookup"><span data-stu-id="d2b9b-103">Create a PSBackend object</span></span>

## <span data-ttu-id="d2b9b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2b9b-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2b9b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2b9b-105">DESCRIPTION</span></span>
<span data-ttu-id="d2b9b-106">Criar um objeto PSBackend para criação da Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="d2b9b-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="d2b9b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d2b9b-107">EXAMPLES</span></span>

### <span data-ttu-id="d2b9b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2b9b-108">Example 1</span></span>
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

<span data-ttu-id="d2b9b-109">Criar um objeto PSBackend para criação da Porta da Frente</span><span class="sxs-lookup"><span data-stu-id="d2b9b-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="d2b9b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2b9b-110">PARAMETERS</span></span>

### <span data-ttu-id="d2b9b-111">-Endereço</span><span class="sxs-lookup"><span data-stu-id="d2b9b-111">-Address</span></span>
<span data-ttu-id="d2b9b-112">Local do back-end (endereço IP ou FQDN)</span><span class="sxs-lookup"><span data-stu-id="d2b9b-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="d2b9b-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="d2b9b-113">-BackendHostHeader</span></span>
<span data-ttu-id="d2b9b-114">O valor a ser usado como o header do host enviado para o back-end.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="d2b9b-115">O valor padrão é o endereço de back-end.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="d2b9b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2b9b-116">-DefaultProfile</span></span>
<span data-ttu-id="d2b9b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2b9b-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d2b9b-118">-EnabledState</span></span>
<span data-ttu-id="d2b9b-119">Se você quer habilitar o uso desse back-end.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="d2b9b-120">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="d2b9b-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="d2b9b-121">-httpPort</span><span class="sxs-lookup"><span data-stu-id="d2b9b-121">-HttpPort</span></span>
<span data-ttu-id="d2b9b-122">O número da porta HTTP TCP.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="d2b9b-123">Deve estar entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="d2b9b-124">O valor padrão é 80.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-124">Default value is 80.</span></span>

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

### <span data-ttu-id="d2b9b-125">-httpsPort</span><span class="sxs-lookup"><span data-stu-id="d2b9b-125">-HttpsPort</span></span>
<span data-ttu-id="d2b9b-126">O número da porta HTTPS TCP.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="d2b9b-127">Deve estar entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="d2b9b-128">O valor padrão é 443</span><span class="sxs-lookup"><span data-stu-id="d2b9b-128">Default value is 443</span></span>

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

### <span data-ttu-id="d2b9b-129">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="d2b9b-129">-Priority</span></span>
<span data-ttu-id="d2b9b-130">Prioridade a ser usada para balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="d2b9b-131">Deve estar entre 1 e 5.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="d2b9b-132">O valor padrão é 1</span><span class="sxs-lookup"><span data-stu-id="d2b9b-132">Default value is 1</span></span>

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

### <span data-ttu-id="d2b9b-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="d2b9b-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="d2b9b-134">O Alias do recurso Link Particular.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="d2b9b-135">Preencher este campo opcional indica que esse back-end é "Particular"</span><span class="sxs-lookup"><span data-stu-id="d2b9b-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="d2b9b-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="d2b9b-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="d2b9b-137">Uma mensagem personalizada a ser incluída na solicitação de aprovação para se conectar ao Link Particular</span><span class="sxs-lookup"><span data-stu-id="d2b9b-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="d2b9b-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="d2b9b-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="d2b9b-139">O local do recurso Link Particular.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-139">The Location of Private Link resource.</span></span> <span data-ttu-id="d2b9b-140">O local é necessário quando PrivateLinkResourceId é definido</span><span class="sxs-lookup"><span data-stu-id="d2b9b-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="d2b9b-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="d2b9b-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="d2b9b-142">A ID do Recurso do Link Particular.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="d2b9b-143">Preencher este campo opcional indica que esse back-end é "Particular"</span><span class="sxs-lookup"><span data-stu-id="d2b9b-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="d2b9b-144">-Peso</span><span class="sxs-lookup"><span data-stu-id="d2b9b-144">-Weight</span></span>
<span data-ttu-id="d2b9b-145">Peso deste ponto de extremidade para fins de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="d2b9b-146">Deve estar entre 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="d2b9b-147">O valor padrão é 50</span><span class="sxs-lookup"><span data-stu-id="d2b9b-147">Default value is 50</span></span>

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

### <span data-ttu-id="d2b9b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2b9b-148">CommonParameters</span></span>
<span data-ttu-id="d2b9b-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2b9b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2b9b-150">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2b9b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2b9b-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="d2b9b-151">INPUTS</span></span>

### <span data-ttu-id="d2b9b-152">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d2b9b-152">None</span></span>

## <span data-ttu-id="d2b9b-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="d2b9b-153">OUTPUTS</span></span>

### <span data-ttu-id="d2b9b-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span><span class="sxs-lookup"><span data-stu-id="d2b9b-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="d2b9b-155">Notas</span><span class="sxs-lookup"><span data-stu-id="d2b9b-155">NOTES</span></span>

## <span data-ttu-id="d2b9b-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2b9b-156">RELATED LINKS</span></span>

[<span data-ttu-id="d2b9b-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="d2b9b-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
