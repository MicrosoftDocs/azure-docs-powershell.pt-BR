---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: 1284780428fdaacfc255faf2ac640565eec44950
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891712"
---
# <span data-ttu-id="8ae62-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8ae62-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="8ae62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ae62-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae62-103">Remove a regra de autorização de um HybridConnection das entidades Relay determinadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8ae62-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="8ae62-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8ae62-104">SYNTAX</span></span>

### <span data-ttu-id="8ae62-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8ae62-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ae62-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ae62-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ae62-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8ae62-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ae62-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8ae62-108">DESCRIPTION</span></span>
<span data-ttu-id="8ae62-109">O cmdlet **Remove-AzRelayAuthorizationRule** remove a regra de autorização das entidades Relay determinadas (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8ae62-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="8ae62-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ae62-110">EXAMPLES</span></span>

### <span data-ttu-id="8ae62-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8ae62-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="8ae62-112">Remove a regra de `AuthoRule1` autorização do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="8ae62-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="8ae62-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8ae62-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="8ae62-114">Remove a regra de `AuthoRule1` autorização do WcfRelay `TestWcfRelay` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="8ae62-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="8ae62-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8ae62-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="8ae62-116">Remove a regra de `AuthoRule1` autorização do HybridConnection `TestHybridConnection` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="8ae62-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="8ae62-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8ae62-117">PARAMETERS</span></span>

### <span data-ttu-id="8ae62-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae62-118">-DefaultProfile</span></span>
<span data-ttu-id="8ae62-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ae62-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ae62-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8ae62-120">-Force</span></span>
<span data-ttu-id="8ae62-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="8ae62-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8ae62-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="8ae62-122">-HybridConnection</span></span>
<span data-ttu-id="8ae62-123">Nome de HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="8ae62-123">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae62-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8ae62-124">-Name</span></span>
<span data-ttu-id="8ae62-125">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="8ae62-125">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae62-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8ae62-126">-Namespace</span></span>
<span data-ttu-id="8ae62-127">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="8ae62-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae62-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ae62-128">-PassThru</span></span>
<span data-ttu-id="8ae62-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8ae62-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8ae62-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae62-130">-ResourceGroupName</span></span>
<span data-ttu-id="8ae62-131">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="8ae62-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="8ae62-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8ae62-132">-WcfRelay</span></span>
<span data-ttu-id="8ae62-133">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="8ae62-133">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae62-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ae62-134">-Confirm</span></span>
<span data-ttu-id="8ae62-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ae62-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ae62-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ae62-136">-WhatIf</span></span>
<span data-ttu-id="8ae62-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ae62-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ae62-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ae62-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ae62-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae62-139">CommonParameters</span></span>
<span data-ttu-id="8ae62-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ae62-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae62-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ae62-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae62-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ae62-142">INPUTS</span></span>

### <span data-ttu-id="8ae62-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8ae62-143">System.String</span></span>

## <span data-ttu-id="8ae62-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8ae62-144">OUTPUTS</span></span>

### <span data-ttu-id="8ae62-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ae62-145">System.Boolean</span></span>

## <span data-ttu-id="8ae62-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="8ae62-146">NOTES</span></span>

## <span data-ttu-id="8ae62-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ae62-147">RELATED LINKS</span></span>
