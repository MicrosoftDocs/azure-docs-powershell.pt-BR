---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 62d37b30f20cf6d0738cfc927c266d6869be5586
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603240"
---
# <span data-ttu-id="115d6-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="115d6-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="115d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="115d6-102">SYNOPSIS</span></span>
<span data-ttu-id="115d6-103">Remove a regra de autorização de um HybridConnection das entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="115d6-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="115d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="115d6-104">SYNTAX</span></span>

### <span data-ttu-id="115d6-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="115d6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="115d6-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="115d6-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="115d6-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="115d6-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="115d6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="115d6-108">DESCRIPTION</span></span>
<span data-ttu-id="115d6-109">O cmdlet **Remove-AzureRmRelayAuthorizationRule** remove a regra de autorização das entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="115d6-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="115d6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="115d6-110">EXAMPLES</span></span>

### <span data-ttu-id="115d6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="115d6-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="115d6-112">Remove a regra `AuthoRule1` de autorização do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="115d6-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="115d6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="115d6-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="115d6-114">Remove a regra `AuthoRule1` de autorização do WcfRelay `TestWcfRelay` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="115d6-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="115d6-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="115d6-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="115d6-116">Remove a regra `AuthoRule1` de autorização do HybridConnection `TestHybridConnection` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="115d6-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="115d6-117">OS</span><span class="sxs-lookup"><span data-stu-id="115d6-117">PARAMETERS</span></span>

### <span data-ttu-id="115d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="115d6-118">-DefaultProfile</span></span>
<span data-ttu-id="115d6-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="115d6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115d6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="115d6-120">-Force</span></span>
<span data-ttu-id="115d6-121">Não pedir confirmação</span><span class="sxs-lookup"><span data-stu-id="115d6-121">Do not ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115d6-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="115d6-122">-HybridConnection</span></span>
<span data-ttu-id="115d6-123">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="115d6-123">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115d6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="115d6-124">-Name</span></span>
<span data-ttu-id="115d6-125">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="115d6-125">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115d6-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="115d6-126">-Namespace</span></span>
<span data-ttu-id="115d6-127">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="115d6-127">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115d6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="115d6-128">-PassThru</span></span>
<span data-ttu-id="115d6-129">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="115d6-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115d6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="115d6-130">-ResourceGroupName</span></span>
<span data-ttu-id="115d6-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="115d6-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="115d6-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="115d6-132">-WcfRelay</span></span>
<span data-ttu-id="115d6-133">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="115d6-133">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115d6-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="115d6-134">-Confirm</span></span>
<span data-ttu-id="115d6-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="115d6-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115d6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="115d6-136">-WhatIf</span></span>
<span data-ttu-id="115d6-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="115d6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="115d6-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="115d6-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115d6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="115d6-139">CommonParameters</span></span>
<span data-ttu-id="115d6-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="115d6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="115d6-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="115d6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="115d6-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="115d6-142">INPUTS</span></span>

### <span data-ttu-id="115d6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="115d6-143">System.String</span></span>

## <span data-ttu-id="115d6-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="115d6-144">OUTPUTS</span></span>

### <span data-ttu-id="115d6-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="115d6-145">System.Boolean</span></span>

## <span data-ttu-id="115d6-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="115d6-146">NOTES</span></span>

## <span data-ttu-id="115d6-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="115d6-147">RELATED LINKS</span></span>

