---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118720"
---
# <span data-ttu-id="1067a-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="1067a-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="1067a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1067a-102">SYNOPSIS</span></span>
<span data-ttu-id="1067a-103">Obtém uma lista de recursos adaptáveis de Desarmamentos de Rede no escopo de um recurso estendido.</span><span class="sxs-lookup"><span data-stu-id="1067a-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="1067a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1067a-104">SYNTAX</span></span>

### <span data-ttu-id="1067a-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="1067a-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="1067a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="1067a-106">DESCRIPTION</span></span>
<span data-ttu-id="1067a-107">As Reticência adaptáveis de rede são calculadas automaticamente pelo Centro de Segurança do Azure, use este cmdlet para obter uma lista de recursos adaptáveis de rede com escopo de um recurso estendido.</span><span class="sxs-lookup"><span data-stu-id="1067a-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="1067a-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1067a-108">EXAMPLES</span></span>

### <span data-ttu-id="1067a-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1067a-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="1067a-110">Obtém uma lista de recursos adaptáveis de Desarmamentos de Rede no escopo de um recurso estendido.</span><span class="sxs-lookup"><span data-stu-id="1067a-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="1067a-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1067a-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="1067a-112">Obter um único recurso Adaptive Network Desarmandos</span><span class="sxs-lookup"><span data-stu-id="1067a-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="1067a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1067a-113">PARAMETERS</span></span>

### <span data-ttu-id="1067a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1067a-114">-DefaultProfile</span></span>
<span data-ttu-id="1067a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1067a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1067a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1067a-116">-ResourceGroupName</span></span>
<span data-ttu-id="1067a-117">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1067a-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1067a-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1067a-118">-ResourceName</span></span>
<span data-ttu-id="1067a-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1067a-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1067a-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="1067a-120">-ResourceNamespace</span></span>
<span data-ttu-id="1067a-121">O Namespace do recurso.</span><span class="sxs-lookup"><span data-stu-id="1067a-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1067a-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1067a-122">-ResourceType</span></span>
<span data-ttu-id="1067a-123">O tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="1067a-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1067a-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="1067a-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="1067a-125">O nome do recurso Desarmamento de Rede Adaptável.</span><span class="sxs-lookup"><span data-stu-id="1067a-125">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1067a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1067a-126">-SubscriptionId</span></span>
<span data-ttu-id="1067a-127">ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="1067a-127">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="1067a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1067a-128">CommonParameters</span></span>
<span data-ttu-id="1067a-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1067a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1067a-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1067a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1067a-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="1067a-131">INPUTS</span></span>

### <span data-ttu-id="1067a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1067a-132">System.String</span></span>

## <span data-ttu-id="1067a-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="1067a-133">OUTPUTS</span></span>

### <span data-ttu-id="1067a-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="1067a-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="1067a-135">Notas</span><span class="sxs-lookup"><span data-stu-id="1067a-135">NOTES</span></span>

## <span data-ttu-id="1067a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1067a-136">RELATED LINKS</span></span>