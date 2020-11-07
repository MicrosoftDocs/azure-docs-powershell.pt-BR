---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 5cf730c5ba450978730617b7ddb270c0fdec2bf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770868"
---
# <span data-ttu-id="54149-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="54149-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="54149-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54149-102">SYNOPSIS</span></span>
<span data-ttu-id="54149-103">Criar um objeto PSBackend</span><span class="sxs-lookup"><span data-stu-id="54149-103">Create a PSBackend object</span></span>

## <span data-ttu-id="54149-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54149-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54149-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54149-105">DESCRIPTION</span></span>
<span data-ttu-id="54149-106">Criar um objeto PSBackend para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="54149-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="54149-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54149-107">EXAMPLES</span></span>

### <span data-ttu-id="54149-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="54149-108">Example 1</span></span>
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

<span data-ttu-id="54149-109">Criar um objeto PSBackend para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="54149-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="54149-110">OS</span><span class="sxs-lookup"><span data-stu-id="54149-110">PARAMETERS</span></span>

### <span data-ttu-id="54149-111">-Endereço</span><span class="sxs-lookup"><span data-stu-id="54149-111">-Address</span></span>
<span data-ttu-id="54149-112">Localização do back-end (endereço IP ou FQDN)</span><span class="sxs-lookup"><span data-stu-id="54149-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="54149-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="54149-113">-BackendHostHeader</span></span>
<span data-ttu-id="54149-114">O valor a ser usado como o cabeçalho do host enviado ao back-end.</span><span class="sxs-lookup"><span data-stu-id="54149-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="54149-115">O valor padrão é o endereço de back-end.</span><span class="sxs-lookup"><span data-stu-id="54149-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="54149-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54149-116">-DefaultProfile</span></span>
<span data-ttu-id="54149-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54149-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54149-118">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="54149-118">-EnabledState</span></span>
<span data-ttu-id="54149-119">Se o uso deste back-end deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="54149-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="54149-120">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="54149-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="54149-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="54149-121">-HttpPort</span></span>
<span data-ttu-id="54149-122">O número da porta TCP HTTP.</span><span class="sxs-lookup"><span data-stu-id="54149-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="54149-123">Deve estar entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="54149-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="54149-124">O valor padrão é 80.</span><span class="sxs-lookup"><span data-stu-id="54149-124">Default value is 80.</span></span>

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

### <span data-ttu-id="54149-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="54149-125">-HttpsPort</span></span>
<span data-ttu-id="54149-126">O número da porta TCP HTTPS.</span><span class="sxs-lookup"><span data-stu-id="54149-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="54149-127">Deve estar entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="54149-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="54149-128">O valor padrão é 443</span><span class="sxs-lookup"><span data-stu-id="54149-128">Default value is 443</span></span>

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

### <span data-ttu-id="54149-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="54149-129">-Priority</span></span>
<span data-ttu-id="54149-130">Prioridade a ser usada para balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="54149-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="54149-131">Deve estar entre 1 e 5.</span><span class="sxs-lookup"><span data-stu-id="54149-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="54149-132">O valor padrão é 1</span><span class="sxs-lookup"><span data-stu-id="54149-132">Default value is 1</span></span>

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

### <span data-ttu-id="54149-133">-Weight</span><span class="sxs-lookup"><span data-stu-id="54149-133">-Weight</span></span>
<span data-ttu-id="54149-134">Peso desse ponto de extremidade para fins de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="54149-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="54149-135">Deve estar entre 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="54149-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="54149-136">O valor padrão é 50</span><span class="sxs-lookup"><span data-stu-id="54149-136">Default value is 50</span></span>

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

### <span data-ttu-id="54149-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54149-137">CommonParameters</span></span>
<span data-ttu-id="54149-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54149-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54149-139">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54149-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54149-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54149-140">INPUTS</span></span>

### <span data-ttu-id="54149-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="54149-141">None</span></span>

## <span data-ttu-id="54149-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54149-142">OUTPUTS</span></span>

### <span data-ttu-id="54149-143">Microsoft. Azure. Commands. FrontDoor. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="54149-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="54149-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54149-144">NOTES</span></span>

## <span data-ttu-id="54149-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54149-145">RELATED LINKS</span></span>

[<span data-ttu-id="54149-146">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="54149-146">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
