---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: e0e634a4947953f65c3fd68c9cc3e40dfca17fd2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887952"
---
# <span data-ttu-id="03e0c-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="03e0c-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="03e0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="03e0c-103">Impõe as regras fornecidas nos NSG(s) listados na solicitação</span><span class="sxs-lookup"><span data-stu-id="03e0c-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="03e0c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="03e0c-104">SYNTAX</span></span>

### <span data-ttu-id="03e0c-105">ResourceGroupLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="03e0c-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03e0c-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="03e0c-106">DESCRIPTION</span></span>
<span data-ttu-id="03e0c-107">Os Hardenings adaptáveis de rede são calculados automaticamente pelo Centro de Segurança do Azure, use este cmdlet para impor as regras determinadas nos NSG(s) listados na solicitação.</span><span class="sxs-lookup"><span data-stu-id="03e0c-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="03e0c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03e0c-108">EXAMPLES</span></span>

### <span data-ttu-id="03e0c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="03e0c-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="03e0c-110">Impõe as regras fornecidas nos NSG(s) listados na solicitação</span><span class="sxs-lookup"><span data-stu-id="03e0c-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="03e0c-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="03e0c-111">PARAMETERS</span></span>

### <span data-ttu-id="03e0c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e0c-112">-DefaultProfile</span></span>
<span data-ttu-id="03e0c-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03e0c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03e0c-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="03e0c-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="03e0c-115">O nome do recurso de Proteção de Rede Adaptável.</span><span class="sxs-lookup"><span data-stu-id="03e0c-115">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="03e0c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03e0c-116">-ResourceGroupName</span></span>
<span data-ttu-id="03e0c-117">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="03e0c-117">Resource group name.</span></span>

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

### <span data-ttu-id="03e0c-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="03e0c-118">-ResourceName</span></span>
<span data-ttu-id="03e0c-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="03e0c-119">Resource name.</span></span>

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

### <span data-ttu-id="03e0c-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="03e0c-120">-ResourceNamespace</span></span>
<span data-ttu-id="03e0c-121">O Namespace do recurso.</span><span class="sxs-lookup"><span data-stu-id="03e0c-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="03e0c-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="03e0c-122">-ResourceType</span></span>
<span data-ttu-id="03e0c-123">O tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="03e0c-123">The type of the resource.</span></span>

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

### <span data-ttu-id="03e0c-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03e0c-124">-SubscriptionId</span></span>
<span data-ttu-id="03e0c-125">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="03e0c-125">Azure subscription ID.</span></span>

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

### <span data-ttu-id="03e0c-126">-Rules</span><span class="sxs-lookup"><span data-stu-id="03e0c-126">-Rules</span></span>
<span data-ttu-id="03e0c-127">As regras a ser impostas.</span><span class="sxs-lookup"><span data-stu-id="03e0c-127">The rules to enforce.</span></span>

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

### <span data-ttu-id="03e0c-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="03e0c-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="03e0c-129">As IDs de recurso do Azure dos grupos de segurança de rede efetivos que serão atualizados com as regras de segurança criadas a partir das regras de Proteção de Rede Adaptável.</span><span class="sxs-lookup"><span data-stu-id="03e0c-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

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

### <span data-ttu-id="03e0c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03e0c-130">-PassThru</span></span>
<span data-ttu-id="03e0c-131">Retornar um valor que indica sucesso ou falha</span><span class="sxs-lookup"><span data-stu-id="03e0c-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="03e0c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e0c-132">CommonParameters</span></span>
<span data-ttu-id="03e0c-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03e0c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e0c-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03e0c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e0c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03e0c-135">INPUTS</span></span>

### <span data-ttu-id="03e0c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="03e0c-136">System.String</span></span>

### <span data-ttu-id="03e0c-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="03e0c-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="03e0c-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="03e0c-138">OUTPUTS</span></span>

### <span data-ttu-id="03e0c-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03e0c-139">System.Boolean</span></span>

## <span data-ttu-id="03e0c-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="03e0c-140">NOTES</span></span>

## <span data-ttu-id="03e0c-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03e0c-141">RELATED LINKS</span></span>