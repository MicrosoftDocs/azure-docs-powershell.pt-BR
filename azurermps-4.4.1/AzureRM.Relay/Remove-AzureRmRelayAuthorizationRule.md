---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 8eaf2ff99fe7f3ea49d73af95eb4482c645be59f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609576"
---
# <span data-ttu-id="23978-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="23978-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="23978-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23978-102">SYNOPSIS</span></span>
<span data-ttu-id="23978-103">Remove a regra de autorização de um HybridConnection das entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="23978-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23978-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23978-104">SYNTAX</span></span>

### <span data-ttu-id="23978-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="23978-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23978-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="23978-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23978-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="23978-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23978-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23978-108">DESCRIPTION</span></span>
<span data-ttu-id="23978-109">O cmdlet **Remove-AzureRmRelayAuthorizationRule** remove a regra de autorização das entidades de retransmissão fornecidas (namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="23978-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="23978-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23978-110">EXAMPLES</span></span>

### <span data-ttu-id="23978-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23978-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="23978-112">Remove a regra `AuthoRule1` de autorização do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="23978-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="23978-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="23978-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="23978-114">Remove a regra `AuthoRule1` de autorização do WcfRelay `TestWcfRelay` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="23978-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="23978-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="23978-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="23978-116">Remove a regra `AuthoRule1` de autorização do HybridConnection `TestHybridConnection` do namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="23978-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="23978-117">OS</span><span class="sxs-lookup"><span data-stu-id="23978-117">PARAMETERS</span></span>

### <span data-ttu-id="23978-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23978-118">-Confirm</span></span>
<span data-ttu-id="23978-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23978-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23978-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="23978-120">-HybridConnection</span></span>
<span data-ttu-id="23978-121">Nome do HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="23978-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="23978-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="23978-122">-Name</span></span>
<span data-ttu-id="23978-123">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="23978-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="23978-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="23978-124">-Namespace</span></span>
<span data-ttu-id="23978-125">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="23978-125">Namespace Name.</span></span>

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

### <span data-ttu-id="23978-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23978-126">-ResourceGroupName</span></span>
<span data-ttu-id="23978-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23978-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="23978-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="23978-128">-WcfRelay</span></span>
<span data-ttu-id="23978-129">Nome do WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="23978-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="23978-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23978-130">-WhatIf</span></span>
<span data-ttu-id="23978-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23978-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23978-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23978-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23978-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23978-133">-DefaultProfile</span></span>
<span data-ttu-id="23978-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23978-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23978-135">-Force</span><span class="sxs-lookup"><span data-stu-id="23978-135">-Force</span></span>
<span data-ttu-id="23978-136">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="23978-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="23978-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23978-137">-PassThru</span></span>
<span data-ttu-id="23978-138">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="23978-138">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="23978-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23978-139">CommonParameters</span></span>
<span data-ttu-id="23978-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23978-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23978-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23978-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23978-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23978-142">INPUTS</span></span>

### <span data-ttu-id="23978-143">System. String</span><span class="sxs-lookup"><span data-stu-id="23978-143">System.String</span></span>

## <span data-ttu-id="23978-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23978-144">OUTPUTS</span></span>

### <span data-ttu-id="23978-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23978-145">System.Boolean</span></span>

## <span data-ttu-id="23978-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23978-146">NOTES</span></span>

## <span data-ttu-id="23978-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23978-147">RELATED LINKS</span></span>

