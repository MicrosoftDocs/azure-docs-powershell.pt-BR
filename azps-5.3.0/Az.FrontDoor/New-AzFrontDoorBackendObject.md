---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429369"
---
# <span data-ttu-id="bc922-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="bc922-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="bc922-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc922-102">SYNOPSIS</span></span>
<span data-ttu-id="bc922-103">Criar um objeto PSBackend</span><span class="sxs-lookup"><span data-stu-id="bc922-103">Create a PSBackend object</span></span>

## <span data-ttu-id="bc922-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc922-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc922-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc922-105">DESCRIPTION</span></span>
<span data-ttu-id="bc922-106">Criar um objeto PSBackend para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="bc922-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="bc922-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc922-107">EXAMPLES</span></span>

### <span data-ttu-id="bc922-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc922-108">Example 1</span></span>
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

<span data-ttu-id="bc922-109">Criar um objeto PSBackend para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="bc922-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="bc922-110">OS</span><span class="sxs-lookup"><span data-stu-id="bc922-110">PARAMETERS</span></span>

### <span data-ttu-id="bc922-111">-Endereço</span><span class="sxs-lookup"><span data-stu-id="bc922-111">-Address</span></span>
<span data-ttu-id="bc922-112">Localização do back-end (endereço IP ou FQDN)</span><span class="sxs-lookup"><span data-stu-id="bc922-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="bc922-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="bc922-113">-BackendHostHeader</span></span>
<span data-ttu-id="bc922-114">O valor a ser usado como o cabeçalho do host enviado ao back-end.</span><span class="sxs-lookup"><span data-stu-id="bc922-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="bc922-115">O valor padrão é o endereço de back-end.</span><span class="sxs-lookup"><span data-stu-id="bc922-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="bc922-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc922-116">-DefaultProfile</span></span>
<span data-ttu-id="bc922-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc922-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc922-118">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="bc922-118">-EnabledState</span></span>
<span data-ttu-id="bc922-119">Se o uso deste back-end deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="bc922-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="bc922-120">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="bc922-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="bc922-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="bc922-121">-HttpPort</span></span>
<span data-ttu-id="bc922-122">O número da porta TCP HTTP.</span><span class="sxs-lookup"><span data-stu-id="bc922-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="bc922-123">Deve estar entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="bc922-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="bc922-124">O valor padrão é 80.</span><span class="sxs-lookup"><span data-stu-id="bc922-124">Default value is 80.</span></span>

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

### <span data-ttu-id="bc922-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="bc922-125">-HttpsPort</span></span>
<span data-ttu-id="bc922-126">O número da porta TCP HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bc922-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="bc922-127">Deve estar entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="bc922-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="bc922-128">O valor padrão é 443</span><span class="sxs-lookup"><span data-stu-id="bc922-128">Default value is 443</span></span>

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

### <span data-ttu-id="bc922-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="bc922-129">-Priority</span></span>
<span data-ttu-id="bc922-130">Prioridade a ser usada para balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="bc922-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="bc922-131">Deve estar entre 1 e 5.</span><span class="sxs-lookup"><span data-stu-id="bc922-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="bc922-132">O valor padrão é 1</span><span class="sxs-lookup"><span data-stu-id="bc922-132">Default value is 1</span></span>

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

### <span data-ttu-id="bc922-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="bc922-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="bc922-134">O alias do recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="bc922-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="bc922-135">O preenchimento desse campo opcional indica que esse back-end é ' privado '</span><span class="sxs-lookup"><span data-stu-id="bc922-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="bc922-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="bc922-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="bc922-137">Uma mensagem personalizada a ser incluída na solicitação de aprovação para se conectar ao link privado</span><span class="sxs-lookup"><span data-stu-id="bc922-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="bc922-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="bc922-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="bc922-139">A localização do recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="bc922-139">The Location of Private Link resource.</span></span> <span data-ttu-id="bc922-140">A localização é necessária quando o PrivateLinkResourceId está definido</span><span class="sxs-lookup"><span data-stu-id="bc922-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="bc922-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="bc922-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="bc922-142">A ID do recurso do link particular.</span><span class="sxs-lookup"><span data-stu-id="bc922-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="bc922-143">O preenchimento desse campo opcional indica que esse back-end é ' privado '</span><span class="sxs-lookup"><span data-stu-id="bc922-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="bc922-144">-Weight</span><span class="sxs-lookup"><span data-stu-id="bc922-144">-Weight</span></span>
<span data-ttu-id="bc922-145">Peso desse ponto de extremidade para fins de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="bc922-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="bc922-146">Deve estar entre 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="bc922-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="bc922-147">O valor padrão é 50</span><span class="sxs-lookup"><span data-stu-id="bc922-147">Default value is 50</span></span>

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

### <span data-ttu-id="bc922-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc922-148">CommonParameters</span></span>
<span data-ttu-id="bc922-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc922-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc922-150">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc922-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc922-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc922-151">INPUTS</span></span>

### <span data-ttu-id="bc922-152">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bc922-152">None</span></span>

## <span data-ttu-id="bc922-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc922-153">OUTPUTS</span></span>

### <span data-ttu-id="bc922-154">Microsoft. Azure. Commands. FrontDoor. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="bc922-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="bc922-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc922-155">NOTES</span></span>

## <span data-ttu-id="bc922-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc922-156">RELATED LINKS</span></span>

[<span data-ttu-id="bc922-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="bc922-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
