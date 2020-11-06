---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
ms.openlocfilehash: 429db1fae2987531911bd4dfbd4c41daf66a5440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602933"
---
# <span data-ttu-id="35fee-101">New-AzureRmFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="35fee-101">New-AzureRmFrontDoorBackendObject</span></span>

## <span data-ttu-id="35fee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35fee-102">SYNOPSIS</span></span>
<span data-ttu-id="35fee-103">Criar um objeto PSBackend</span><span class="sxs-lookup"><span data-stu-id="35fee-103">Create a PSBackend object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35fee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35fee-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-Priority <Int32>] [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35fee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35fee-105">DESCRIPTION</span></span>
<span data-ttu-id="35fee-106">Criar um objeto PSBackend para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="35fee-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="35fee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35fee-107">EXAMPLES</span></span>

### <span data-ttu-id="35fee-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="35fee-108">Example 1</span></span>
```powershell
PS C:\>New-AzureRmFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="35fee-109">Criar um objeto PSBackend para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="35fee-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="35fee-110">OS</span><span class="sxs-lookup"><span data-stu-id="35fee-110">PARAMETERS</span></span>

### <span data-ttu-id="35fee-111">-Endereço</span><span class="sxs-lookup"><span data-stu-id="35fee-111">-Address</span></span>
<span data-ttu-id="35fee-112">Localização do back-end (endereço IP ou FQDN)</span><span class="sxs-lookup"><span data-stu-id="35fee-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="35fee-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="35fee-113">-BackendHostHeader</span></span>
<span data-ttu-id="35fee-114">O valor a ser usado como o cabeçalho do host enviado ao back-end.</span><span class="sxs-lookup"><span data-stu-id="35fee-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="35fee-115">O valor padrão é o endereço de back-end.</span><span class="sxs-lookup"><span data-stu-id="35fee-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="35fee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35fee-116">-DefaultProfile</span></span>
<span data-ttu-id="35fee-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35fee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35fee-118">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="35fee-118">-EnabledState</span></span>
<span data-ttu-id="35fee-119">Se o uso deste back-end deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="35fee-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="35fee-120">O valor padrão está habilitado</span><span class="sxs-lookup"><span data-stu-id="35fee-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="35fee-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="35fee-121">-HttpPort</span></span>
<span data-ttu-id="35fee-122">O número da porta TCP HTTP.</span><span class="sxs-lookup"><span data-stu-id="35fee-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="35fee-123">Deve estar entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="35fee-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="35fee-124">O valor padrão é 80.</span><span class="sxs-lookup"><span data-stu-id="35fee-124">Default value is 80.</span></span>

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

### <span data-ttu-id="35fee-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="35fee-125">-HttpsPort</span></span>
<span data-ttu-id="35fee-126">O número da porta TCP HTTPS.</span><span class="sxs-lookup"><span data-stu-id="35fee-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="35fee-127">Deve estar entre 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="35fee-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="35fee-128">O valor padrão é 443</span><span class="sxs-lookup"><span data-stu-id="35fee-128">Default value is 443</span></span>

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

### <span data-ttu-id="35fee-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="35fee-129">-Priority</span></span>
<span data-ttu-id="35fee-130">Prioridade a ser usada para balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="35fee-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="35fee-131">Deve estar entre 1 e 5.</span><span class="sxs-lookup"><span data-stu-id="35fee-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="35fee-132">O valor padrão é 1</span><span class="sxs-lookup"><span data-stu-id="35fee-132">Default value is 1</span></span>

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

### <span data-ttu-id="35fee-133">-Weight</span><span class="sxs-lookup"><span data-stu-id="35fee-133">-Weight</span></span>
<span data-ttu-id="35fee-134">Peso desse ponto de extremidade para fins de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="35fee-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="35fee-135">Deve estar entre 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="35fee-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="35fee-136">O valor padrão é 50</span><span class="sxs-lookup"><span data-stu-id="35fee-136">Default value is 50</span></span>

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

### <span data-ttu-id="35fee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35fee-137">CommonParameters</span></span>
<span data-ttu-id="35fee-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35fee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35fee-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35fee-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35fee-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35fee-140">INPUTS</span></span>

### <span data-ttu-id="35fee-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="35fee-141">None</span></span>

## <span data-ttu-id="35fee-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35fee-142">OUTPUTS</span></span>

### <span data-ttu-id="35fee-143">Microsoft. Azure. Commands. FrontDoor. Models. PSBackend</span><span class="sxs-lookup"><span data-stu-id="35fee-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="35fee-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35fee-144">NOTES</span></span>

## <span data-ttu-id="35fee-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35fee-145">RELATED LINKS</span></span>

[<span data-ttu-id="35fee-146">New-AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="35fee-146">New-AzureRmFrontDoorBackendPoolObject</span></span>](./New-AzureRmFrontDoorBackendPoolObject.md)
