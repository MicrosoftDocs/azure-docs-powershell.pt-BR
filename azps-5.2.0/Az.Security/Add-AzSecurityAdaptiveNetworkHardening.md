---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258966"
---
# <span data-ttu-id="a621a-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="a621a-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="a621a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a621a-102">SYNOPSIS</span></span>
<span data-ttu-id="a621a-103">Impõe as regras fornecidas na (s) NSG (s) listadas na solicitação</span><span class="sxs-lookup"><span data-stu-id="a621a-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="a621a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a621a-104">SYNTAX</span></span>

### <span data-ttu-id="a621a-105">ResourceGroupLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="a621a-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a621a-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a621a-106">DESCRIPTION</span></span>
<span data-ttu-id="a621a-107">As otimizações de rede adaptáveis são calculadas automaticamente pela central de segurança do Azure, use esse cmdlet para impor as regras dadas nas NSG (s) listadas na solicitação.</span><span class="sxs-lookup"><span data-stu-id="a621a-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="a621a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a621a-108">EXAMPLES</span></span>

### <span data-ttu-id="a621a-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a621a-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="a621a-110">Impõe as regras fornecidas na (s) NSG (s) listadas na solicitação</span><span class="sxs-lookup"><span data-stu-id="a621a-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="a621a-111">OS</span><span class="sxs-lookup"><span data-stu-id="a621a-111">PARAMETERS</span></span>

### <span data-ttu-id="a621a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a621a-112">-DefaultProfile</span></span>
<span data-ttu-id="a621a-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a621a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a621a-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="a621a-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="a621a-115">O nome do recurso de proteção de rede adaptável.</span><span class="sxs-lookup"><span data-stu-id="a621a-115">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a621a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a621a-116">-ResourceGroupName</span></span>
<span data-ttu-id="a621a-117">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a621a-117">Resource group name.</span></span>

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

### <span data-ttu-id="a621a-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a621a-118">-ResourceName</span></span>
<span data-ttu-id="a621a-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a621a-119">Resource name.</span></span>

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

### <span data-ttu-id="a621a-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="a621a-120">-ResourceNamespace</span></span>
<span data-ttu-id="a621a-121">O namespace do recurso.</span><span class="sxs-lookup"><span data-stu-id="a621a-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="a621a-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a621a-122">-ResourceType</span></span>
<span data-ttu-id="a621a-123">O tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="a621a-123">The type of the resource.</span></span>

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

### <span data-ttu-id="a621a-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a621a-124">-SubscriptionId</span></span>
<span data-ttu-id="a621a-125">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a621a-125">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a621a-126">-Regras</span><span class="sxs-lookup"><span data-stu-id="a621a-126">-Rules</span></span>
<span data-ttu-id="a621a-127">As regras a serem imposição.</span><span class="sxs-lookup"><span data-stu-id="a621a-127">The rules to enforce.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule
Parameter Sets: Rules
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a621a-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="a621a-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="a621a-129">As identificações de recursos do Azure dos grupos de segurança de rede efetivos que serão atualizadas com as regras de segurança criadas das regras de proteção de rede adaptável.</span><span class="sxs-lookup"><span data-stu-id="a621a-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

```yaml
Type: System.Collections.Generic.List<System.String>
Parameter Sets: NetworkSecurityGroups
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a621a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a621a-130">-PassThru</span></span>
<span data-ttu-id="a621a-131">Retornar um valor que indica êxito ou falha</span><span class="sxs-lookup"><span data-stu-id="a621a-131">Return a value indicating success or failure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a621a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a621a-132">CommonParameters</span></span>
<span data-ttu-id="a621a-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a621a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a621a-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a621a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a621a-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a621a-135">INPUTS</span></span>

### <span data-ttu-id="a621a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a621a-136">System.String</span></span>

### <span data-ttu-id="a621a-137">Microsoft. Azure. Commands. SecurityCenter. Models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="a621a-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="a621a-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a621a-138">OUTPUTS</span></span>

### <span data-ttu-id="a621a-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a621a-139">System.Boolean</span></span>

## <span data-ttu-id="a621a-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a621a-140">NOTES</span></span>

## <span data-ttu-id="a621a-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a621a-141">RELATED LINKS</span></span>