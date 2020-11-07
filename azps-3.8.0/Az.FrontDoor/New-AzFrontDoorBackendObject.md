---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: fe9e846b08a7e56951390b8364f617b1493b8aca
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777483"
---
# <span data-ttu-id="8f7af-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="8f7af-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="8f7af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f7af-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7af-103">Criar um objeto PSBackend</span><span class="sxs-lookup"><span data-stu-id="8f7af-103">Create a PSBackend object</span></span>

## <span data-ttu-id="8f7af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f7af-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f7af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f7af-105">DESCRIPTION</span></span>
<span data-ttu-id="8f7af-106">Criar um objeto PSBackend para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="8f7af-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="8f7af-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f7af-107">EXAMPLES</span></span>

### <span data-ttu-id="8f7af-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f7af-108">Example 1</span></span>
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

<span data-ttu-id="8f7af-109">Criar um objeto PSBackend para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="8f7af-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="8f7af-110">OS</span><span class="sxs-lookup"><span data-stu-id="8f7af-110">PARAMETERS</span></span>

### <span data-ttu-id="8f7af-111">-Endereço</span><span class="sxs-lookup"><span data-stu-id="8f7af-111">-Address</span></span>
<span data-ttu-id="8f7af-112">Localização do back-end (endereço IP ou FQDN)</span><span class="sxs-lookup"><span data-stu-id="8f7af-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="8f7af-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="8f7af-113">-BackendHostHeader</span></span>
<span data-ttu-id="8f7af-114">O valor a ser usado como o cabeçalho do host enviado ao back-end.</span><span class="sxs-lookup"><span data-stu-id="8f7af-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="8f7af-115">O valor padrão é o endereço de back-end.</span><span class="sxs-lookup"><span data-stu-id="8f7af-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="8f7af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7af-116">-DefaultProfile</span></span>
<span data-ttu-id="8f7af-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f7af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f7af-118">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="8f7af-118">-EnabledState</span></span>
<span data-ttu-id="8f7af-119">Se o uso deste back-end deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="8f7af-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="8f7af-120">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="8f7af-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="8f7af-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="8f7af-121">-HttpPort</span></span>
<span data-ttu-id="8f7af-122">O número da porta TCP HTTP.</span><span class="sxs-lookup"><span data-stu-id="8f7af-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="8f7af-123">Deve estar entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="8f7af-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="8f7af-124">O valor padrão é 80.</span><span class="sxs-lookup"><span data-stu-id="8f7af-124">Default value is 80.</span></span>

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

### <span data-ttu-id="8f7af-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="8f7af-125">-HttpsPort</span></span>
<span data-ttu-id="8f7af-126">O número da porta TCP HTTPS.</span><span class="sxs-lookup"><span data-stu-id="8f7af-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="8f7af-127">Deve estar entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="8f7af-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="8f7af-128">O valor padrão é 443</span><span class="sxs-lookup"><span data-stu-id="8f7af-128">Default value is 443</span></span>

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

### <span data-ttu-id="8f7af-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="8f7af-129">-Priority</span></span>
<span data-ttu-id="8f7af-130">Prioridade a ser usada para balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="8f7af-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="8f7af-131">Deve estar entre 1 e 5.</span><span class="sxs-lookup"><span data-stu-id="8f7af-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="8f7af-132">O valor padrão é 1</span><span class="sxs-lookup"><span data-stu-id="8f7af-132">Default value is 1</span></span>

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

### <span data-ttu-id="8f7af-133">-Weight</span><span class="sxs-lookup"><span data-stu-id="8f7af-133">-Weight</span></span>
<span data-ttu-id="8f7af-134">Peso desse ponto de extremidade para fins de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="8f7af-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="8f7af-135">Deve estar entre 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="8f7af-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="8f7af-136">O valor padrão é 50</span><span class="sxs-lookup"><span data-stu-id="8f7af-136">Default value is 50</span></span>

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

### <span data-ttu-id="8f7af-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7af-137">CommonParameters</span></span>
<span data-ttu-id="8f7af-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7af-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7af-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f7af-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7af-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f7af-140">INPUTS</span></span>

### <span data-ttu-id="8f7af-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8f7af-141">None</span></span>

## <span data-ttu-id="8f7af-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f7af-142">OUTPUTS</span></span>

### <span data-ttu-id="8f7af-143">Microsoft. Azure. Commands. FrontDoor. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="8f7af-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="8f7af-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f7af-144">NOTES</span></span>

## <span data-ttu-id="8f7af-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f7af-145">RELATED LINKS</span></span>

[<span data-ttu-id="8f7af-146">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="8f7af-146">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
