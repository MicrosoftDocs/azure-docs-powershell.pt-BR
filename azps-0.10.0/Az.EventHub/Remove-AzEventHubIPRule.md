---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: ee52da845460def78e241d34f25aa9a997e4b7db
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775866"
---
# <span data-ttu-id="3fd95-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="3fd95-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="3fd95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3fd95-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd95-103">Remover uma única regra de IP para o NetworkRuleSet do namespace especificado</span><span class="sxs-lookup"><span data-stu-id="3fd95-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="3fd95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3fd95-104">SYNTAX</span></span>

### <span data-ttu-id="3fd95-105">IPRulePropertiesParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3fd95-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fd95-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fd95-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3fd95-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3fd95-107">DESCRIPTION</span></span>
<span data-ttu-id="3fd95-108">Remover uma única regra de IP para o NetworkRuleSet do namespace especificado</span><span class="sxs-lookup"><span data-stu-id="3fd95-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="3fd95-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3fd95-109">EXAMPLES</span></span>

### <span data-ttu-id="3fd95-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3fd95-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="3fd95-111">Remove IpMask do NetworkRuleSet do namespace especificado</span><span class="sxs-lookup"><span data-stu-id="3fd95-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="3fd95-112">OS</span><span class="sxs-lookup"><span data-stu-id="3fd95-112">PARAMETERS</span></span>

### <span data-ttu-id="3fd95-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fd95-113">-AsJob</span></span>
<span data-ttu-id="3fd95-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3fd95-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fd95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd95-115">-DefaultProfile</span></span>
<span data-ttu-id="3fd95-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd95-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fd95-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="3fd95-117">-IpMask</span></span>
<span data-ttu-id="3fd95-118">ID do recurso de sub-rede</span><span class="sxs-lookup"><span data-stu-id="3fd95-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd95-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="3fd95-119">-IpRuleObject</span></span>
<span data-ttu-id="3fd95-120">Objeto de configuração IPRule</span><span class="sxs-lookup"><span data-stu-id="3fd95-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd95-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3fd95-121">-Name</span></span>
<span data-ttu-id="3fd95-122">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="3fd95-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd95-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fd95-123">-PassThru</span></span>
<span data-ttu-id="3fd95-124">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="3fd95-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3fd95-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fd95-125">-ResourceGroupName</span></span>
<span data-ttu-id="3fd95-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3fd95-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd95-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3fd95-127">-Confirm</span></span>
<span data-ttu-id="3fd95-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fd95-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd95-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fd95-129">-WhatIf</span></span>
<span data-ttu-id="3fd95-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3fd95-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fd95-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3fd95-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd95-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd95-132">CommonParameters</span></span>
<span data-ttu-id="3fd95-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd95-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3fd95-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fd95-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd95-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3fd95-135">INPUTS</span></span>

### <span data-ttu-id="3fd95-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3fd95-136">System.String</span></span>

### <span data-ttu-id="3fd95-137">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="3fd95-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="3fd95-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3fd95-138">OUTPUTS</span></span>

### <span data-ttu-id="3fd95-139">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="3fd95-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="3fd95-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3fd95-140">NOTES</span></span>

## <span data-ttu-id="3fd95-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fd95-141">RELATED LINKS</span></span>