---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F939FE9-5D42-4EA1-90DC-E6D60158CADE
online version: ''
schema: 2.0.0
ms.openlocfilehash: f2eb6fe50566a5de97f00876bdaa7061bbaf0587
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946475"
---
# <span data-ttu-id="983f8-101">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="983f8-101">Remove-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="983f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="983f8-102">SYNOPSIS</span></span>
<span data-ttu-id="983f8-103">Remove uma configuração interna de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="983f8-103">Removes an internal load balancer configuration.</span></span>

## <span data-ttu-id="983f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="983f8-104">SYNTAX</span></span>

```
Remove-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="983f8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="983f8-105">DESCRIPTION</span></span>
<span data-ttu-id="983f8-106">O cmdlet **Remove-AzureInternalLoadBalancer** remove a configuração interna do balanceador de carga de um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="983f8-106">The **Remove-AzureInternalLoadBalancer** cmdlet removes the internal load balancer configuration from an Azure service.</span></span>
<span data-ttu-id="983f8-107">Se um ponto de extremidade refere-se atualmente ao balanceador de carga interno, esse cmdlet não pode remover a configuração.</span><span class="sxs-lookup"><span data-stu-id="983f8-107">If any endpoint currently refers to the internal load balancer, this cmdlet cannot remove the configuration.</span></span>

## <span data-ttu-id="983f8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="983f8-108">EXAMPLES</span></span>

### <span data-ttu-id="983f8-109">Exemplo 1: remover uma configuração interna de balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="983f8-109">Example 1: Remove an internal load balancer configuration</span></span>
```
PS C:\> Remove-AzureInternalLoadBalancer -ServiceName "ContosoService"
```

<span data-ttu-id="983f8-110">Esse comando Remove a configuração interna do balanceador de carga do serviço chamado ContosoService.</span><span class="sxs-lookup"><span data-stu-id="983f8-110">This command removes the internal load balancer configuration for the service named ContosoService.</span></span>

## <span data-ttu-id="983f8-111">OS</span><span class="sxs-lookup"><span data-stu-id="983f8-111">PARAMETERS</span></span>

### <span data-ttu-id="983f8-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="983f8-112">-InformationAction</span></span>
<span data-ttu-id="983f8-113">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="983f8-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="983f8-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="983f8-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="983f8-115">Contínuo</span><span class="sxs-lookup"><span data-stu-id="983f8-115">Continue</span></span>
- <span data-ttu-id="983f8-116">Ignorar</span><span class="sxs-lookup"><span data-stu-id="983f8-116">Ignore</span></span>
- <span data-ttu-id="983f8-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="983f8-117">Inquire</span></span>
- <span data-ttu-id="983f8-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="983f8-118">SilentlyContinue</span></span>
- <span data-ttu-id="983f8-119">Finaliza</span><span class="sxs-lookup"><span data-stu-id="983f8-119">Stop</span></span>
- <span data-ttu-id="983f8-120">Suspensão</span><span class="sxs-lookup"><span data-stu-id="983f8-120">Suspend</span></span>

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

### <span data-ttu-id="983f8-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="983f8-121">-InformationVariable</span></span>
<span data-ttu-id="983f8-122">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="983f8-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="983f8-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="983f8-123">-Profile</span></span>
<span data-ttu-id="983f8-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="983f8-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="983f8-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="983f8-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="983f8-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="983f8-126">-ServiceName</span></span>
<span data-ttu-id="983f8-127">Especifica o nome do serviço do qual esse cmdlet Remove um balanceador de carga interno.</span><span class="sxs-lookup"><span data-stu-id="983f8-127">Specifies the name of the service from which this cmdlet removes an internal load balancer.</span></span>

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

### <span data-ttu-id="983f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="983f8-128">CommonParameters</span></span>
<span data-ttu-id="983f8-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="983f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="983f8-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="983f8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="983f8-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="983f8-131">INPUTS</span></span>

## <span data-ttu-id="983f8-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="983f8-132">OUTPUTS</span></span>

### <span data-ttu-id="983f8-133">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="983f8-133">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="983f8-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="983f8-134">NOTES</span></span>

## <span data-ttu-id="983f8-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="983f8-135">RELATED LINKS</span></span>

[<span data-ttu-id="983f8-136">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="983f8-136">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="983f8-137">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="983f8-137">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="983f8-138">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="983f8-138">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="983f8-139">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="983f8-139">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


