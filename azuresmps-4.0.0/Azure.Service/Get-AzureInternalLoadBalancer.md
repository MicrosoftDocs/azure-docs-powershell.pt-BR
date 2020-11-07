---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A439ADC4-991E-4860-82AA-7BED315991B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9f28659835fef4778eac729ccd020eb82f563bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946340"
---
# <span data-ttu-id="80bf4-101">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80bf4-101">Get-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="80bf4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="80bf4-103">Obtém os detalhes da configuração interna do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="80bf4-103">Gets the details of the internal load balancer configuration.</span></span>

## <span data-ttu-id="80bf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80bf4-104">SYNTAX</span></span>

```
Get-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="80bf4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="80bf4-106">O cmdlet **Get-AzureInternalLoadBalancer** Obtém os detalhes da configuração interna do balanceador de carga para um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="80bf4-106">The **Get-AzureInternalLoadBalancer** cmdlet gets the details of the internal load balancer configuration for an Azure service.</span></span>

## <span data-ttu-id="80bf4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80bf4-107">EXAMPLES</span></span>

### <span data-ttu-id="80bf4-108">Exemplo 1: obter detalhes para um balanceador de carga interno</span><span class="sxs-lookup"><span data-stu-id="80bf4-108">Example 1: Get details for an internal load balancer</span></span>
```
PS C:\> Get-AzureService -ServiceName "ContosoService" | Get-AzureInternalLoadBalancer
```

<span data-ttu-id="80bf4-109">Esse comando obtém o serviço denominado ContosoService usando o cmdlet **Get-AzureService** .</span><span class="sxs-lookup"><span data-stu-id="80bf4-109">This command gets the service named ContosoService by using the **Get-AzureService** cmdlet.</span></span>
<span data-ttu-id="80bf4-110">O comando passa esse serviço para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="80bf4-110">The command passes that service to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="80bf4-111">O cmdlet atual Obtém detalhes para o balanceador de carga interno desse serviço.</span><span class="sxs-lookup"><span data-stu-id="80bf4-111">The current cmdlet gets details for the internal load balancer for that service.</span></span>

## <span data-ttu-id="80bf4-112">OS</span><span class="sxs-lookup"><span data-stu-id="80bf4-112">PARAMETERS</span></span>

### <span data-ttu-id="80bf4-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="80bf4-113">-InformationAction</span></span>
<span data-ttu-id="80bf4-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="80bf4-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="80bf4-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="80bf4-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80bf4-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="80bf4-116">Continue</span></span>
- <span data-ttu-id="80bf4-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="80bf4-117">Ignore</span></span>
- <span data-ttu-id="80bf4-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="80bf4-118">Inquire</span></span>
- <span data-ttu-id="80bf4-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="80bf4-119">SilentlyContinue</span></span>
- <span data-ttu-id="80bf4-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="80bf4-120">Stop</span></span>
- <span data-ttu-id="80bf4-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="80bf4-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80bf4-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="80bf4-122">-InformationVariable</span></span>
<span data-ttu-id="80bf4-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="80bf4-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80bf4-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="80bf4-124">-Profile</span></span>
<span data-ttu-id="80bf4-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="80bf4-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80bf4-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="80bf4-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80bf4-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="80bf4-127">-ServiceName</span></span>
<span data-ttu-id="80bf4-128">Especifica o nome do serviço para o qual esse cmdlet obtém detalhes para um balanceador de carga interno.</span><span class="sxs-lookup"><span data-stu-id="80bf4-128">Specifies the name of the service for which this cmdlet gets details for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80bf4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80bf4-129">CommonParameters</span></span>
<span data-ttu-id="80bf4-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80bf4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80bf4-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80bf4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80bf4-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80bf4-132">INPUTS</span></span>

## <span data-ttu-id="80bf4-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80bf4-133">OUTPUTS</span></span>

### <span data-ttu-id="80bf4-134">Microsoft. WindowsAzure. Commands. onmanagement. Model. InternalLoadBalancerContext</span><span class="sxs-lookup"><span data-stu-id="80bf4-134">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerContext</span></span>

## <span data-ttu-id="80bf4-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80bf4-135">NOTES</span></span>

## <span data-ttu-id="80bf4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80bf4-136">RELATED LINKS</span></span>

[<span data-ttu-id="80bf4-137">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80bf4-137">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="80bf4-138">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="80bf4-138">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="80bf4-139">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="80bf4-139">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="80bf4-140">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80bf4-140">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="80bf4-141">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80bf4-141">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


