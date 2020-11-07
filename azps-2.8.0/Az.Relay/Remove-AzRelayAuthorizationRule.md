---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: 8523fd6698e2fcdc4212b68a93269d60bc642628
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773394"
---
# <span data-ttu-id="04c49-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="04c49-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="04c49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04c49-102">SYNOPSIS</span></span>
<span data-ttu-id="04c49-103">Remove a regra de autorização de um HybridConnection das entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="04c49-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="04c49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04c49-104">SYNTAX</span></span>

### <span data-ttu-id="04c49-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="04c49-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04c49-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="04c49-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04c49-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="04c49-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04c49-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04c49-108">DESCRIPTION</span></span>
<span data-ttu-id="04c49-109">O cmdlet **Remove-AzRelayAuthorizationRule** remove a regra de autorização das entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="04c49-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="04c49-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04c49-110">EXAMPLES</span></span>

### <span data-ttu-id="04c49-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04c49-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="04c49-112">Remove a regra `AuthoRule1` de autorização do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="04c49-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="04c49-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="04c49-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="04c49-114">Remove a regra `AuthoRule1` de autorização do WcfRelay `TestWcfRelay` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="04c49-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="04c49-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="04c49-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="04c49-116">Remove a regra `AuthoRule1` de autorização do HybridConnection `TestHybridConnection` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="04c49-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="04c49-117">OS</span><span class="sxs-lookup"><span data-stu-id="04c49-117">PARAMETERS</span></span>

### <span data-ttu-id="04c49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c49-118">-DefaultProfile</span></span>
<span data-ttu-id="04c49-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04c49-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04c49-120">-Force</span><span class="sxs-lookup"><span data-stu-id="04c49-120">-Force</span></span>
<span data-ttu-id="04c49-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="04c49-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="04c49-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="04c49-122">-HybridConnection</span></span>
<span data-ttu-id="04c49-123">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="04c49-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="04c49-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="04c49-124">-Name</span></span>
<span data-ttu-id="04c49-125">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="04c49-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="04c49-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="04c49-126">-Namespace</span></span>
<span data-ttu-id="04c49-127">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="04c49-127">Namespace Name.</span></span>

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

### <span data-ttu-id="04c49-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04c49-128">-PassThru</span></span>
<span data-ttu-id="04c49-129">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="04c49-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="04c49-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04c49-130">-ResourceGroupName</span></span>
<span data-ttu-id="04c49-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="04c49-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="04c49-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="04c49-132">-WcfRelay</span></span>
<span data-ttu-id="04c49-133">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="04c49-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="04c49-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04c49-134">-Confirm</span></span>
<span data-ttu-id="04c49-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04c49-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04c49-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04c49-136">-WhatIf</span></span>
<span data-ttu-id="04c49-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04c49-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04c49-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04c49-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04c49-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c49-139">CommonParameters</span></span>
<span data-ttu-id="04c49-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04c49-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c49-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04c49-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c49-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04c49-142">INPUTS</span></span>

### <span data-ttu-id="04c49-143">System. String</span><span class="sxs-lookup"><span data-stu-id="04c49-143">System.String</span></span>

## <span data-ttu-id="04c49-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04c49-144">OUTPUTS</span></span>

### <span data-ttu-id="04c49-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04c49-145">System.Boolean</span></span>

## <span data-ttu-id="04c49-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04c49-146">NOTES</span></span>

## <span data-ttu-id="04c49-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04c49-147">RELATED LINKS</span></span>