---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: c15528befc90a0249101602fef9b178e7a63c0ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430498"
---
# <span data-ttu-id="af01b-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="af01b-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="af01b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af01b-102">SYNOPSIS</span></span>
<span data-ttu-id="af01b-103">Remove a regra de autorização do hub de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="af01b-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af01b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af01b-104">SYNTAX</span></span>

### <span data-ttu-id="af01b-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="af01b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af01b-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="af01b-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af01b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af01b-107">DESCRIPTION</span></span>
<span data-ttu-id="af01b-108">O cmdlet Remove-AzureRmEventHubAuthorizationRule remove e exclui a regra de autorização especificada do hub de eventos fornecido.</span><span class="sxs-lookup"><span data-stu-id="af01b-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="af01b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af01b-109">EXAMPLES</span></span>

### <span data-ttu-id="af01b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af01b-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="af01b-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="af01b-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="af01b-112">Remove a regra de autorização \` MyAuthRuleName \` da MyEventHubName do hub de eventos \` \` .</span><span class="sxs-lookup"><span data-stu-id="af01b-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="af01b-113">OS</span><span class="sxs-lookup"><span data-stu-id="af01b-113">PARAMETERS</span></span>

### <span data-ttu-id="af01b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af01b-114">-DefaultProfile</span></span>
<span data-ttu-id="af01b-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af01b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af01b-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="af01b-116">-EventHub</span></span>
<span data-ttu-id="af01b-117">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="af01b-117">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af01b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="af01b-118">-Force</span></span>
<span data-ttu-id="af01b-119">Não pedir confirmação</span><span class="sxs-lookup"><span data-stu-id="af01b-119">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="af01b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="af01b-120">-Name</span></span>
<span data-ttu-id="af01b-121">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="af01b-121">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af01b-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="af01b-122">-Namespace</span></span>
<span data-ttu-id="af01b-123">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="af01b-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af01b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af01b-124">-PassThru</span></span>
<span data-ttu-id="af01b-125">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="af01b-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="af01b-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="af01b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="af01b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af01b-127">-ResourceGroupName</span></span>
<span data-ttu-id="af01b-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="af01b-128">Resource Group Name</span></span>

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

### <span data-ttu-id="af01b-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af01b-129">-Confirm</span></span>
<span data-ttu-id="af01b-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af01b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af01b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af01b-131">-WhatIf</span></span>
<span data-ttu-id="af01b-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af01b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af01b-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af01b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af01b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af01b-134">CommonParameters</span></span>
<span data-ttu-id="af01b-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af01b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="af01b-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af01b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af01b-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af01b-137">INPUTS</span></span>

### <span data-ttu-id="af01b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="af01b-138">System.String</span></span>


## <span data-ttu-id="af01b-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af01b-139">OUTPUTS</span></span>

### <span data-ttu-id="af01b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af01b-140">System.Boolean</span></span>


## <span data-ttu-id="af01b-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af01b-141">NOTES</span></span>

## <span data-ttu-id="af01b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af01b-142">RELATED LINKS</span></span>
