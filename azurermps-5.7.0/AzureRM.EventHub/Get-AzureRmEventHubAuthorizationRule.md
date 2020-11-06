---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d162122b82f592472fb31f1087db29faedf08cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439877"
---
# <span data-ttu-id="46b3f-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="46b3f-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="46b3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="46b3f-103">Obtém os detalhes de uma regra de autorização ou obtém uma lista de regras de autorização.</span><span class="sxs-lookup"><span data-stu-id="46b3f-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46b3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46b3f-104">SYNTAX</span></span>

### <span data-ttu-id="46b3f-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="46b3f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46b3f-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="46b3f-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46b3f-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="46b3f-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46b3f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46b3f-108">DESCRIPTION</span></span>
<span data-ttu-id="46b3f-109">O cmdlet Get-AzureRmEventHubAuthorizationRule Obtém os detalhes de uma regra de autorização ou uma lista de todas as regras de autorização para um hub de eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="46b3f-109">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="46b3f-110">Se o nome de uma regra de autorização for fornecido, os detalhes dessa única regra de autorização serão retornados.</span><span class="sxs-lookup"><span data-stu-id="46b3f-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="46b3f-111">Se o nome de uma regra de autorização não for fornecido, uma lista de todas as regras de autorização para o Hub de eventos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="46b3f-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="46b3f-112">Se o nome do alias fornecido (recuperação de desastre) fornecido, os detalhes da regra de autorização do namespace para alias configurado serão retornados.</span><span class="sxs-lookup"><span data-stu-id="46b3f-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span> 

## <span data-ttu-id="46b3f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46b3f-113">EXAMPLES</span></span>

### <span data-ttu-id="46b3f-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46b3f-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="46b3f-115">Obtém a regra de autorização \` MyAuthRuleName \` no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="46b3f-115">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="46b3f-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="46b3f-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="46b3f-117">Obtém uma lista de todas as regras de autorização no Hub de eventos \` MyEventHubName \` , cujo escopo é o namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="46b3f-117">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="46b3f-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="46b3f-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="46b3f-119">Obtém a regra de autorização \` MyAuthRuleName \` no namespace \` mynamespacename \` .</span><span class="sxs-lookup"><span data-stu-id="46b3f-119">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="46b3f-120">OS</span><span class="sxs-lookup"><span data-stu-id="46b3f-120">PARAMETERS</span></span>

### <span data-ttu-id="46b3f-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="46b3f-121">-AliasName</span></span>
<span data-ttu-id="46b3f-122">Nome do alias</span><span class="sxs-lookup"><span data-stu-id="46b3f-122">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b3f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b3f-123">-DefaultProfile</span></span>
<span data-ttu-id="46b3f-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46b3f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46b3f-125">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="46b3f-125">-Eventhub</span></span>
<span data-ttu-id="46b3f-126">Nome do Eventhub</span><span class="sxs-lookup"><span data-stu-id="46b3f-126">Eventhub Name</span></span>

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

### <span data-ttu-id="46b3f-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="46b3f-127">-Name</span></span>
<span data-ttu-id="46b3f-128">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="46b3f-128">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b3f-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="46b3f-129">-Namespace</span></span>
<span data-ttu-id="46b3f-130">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="46b3f-130">Namespace Name</span></span>

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

### <span data-ttu-id="46b3f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46b3f-131">-ResourceGroupName</span></span>
<span data-ttu-id="46b3f-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="46b3f-132">Resource Group Name</span></span>

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

### <span data-ttu-id="46b3f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b3f-133">CommonParameters</span></span>
<span data-ttu-id="46b3f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b3f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="46b3f-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46b3f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b3f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46b3f-136">INPUTS</span></span>

### <span data-ttu-id="46b3f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="46b3f-137">System.String</span></span>


## <span data-ttu-id="46b3f-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46b3f-138">OUTPUTS</span></span>

### <span data-ttu-id="46b3f-139">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="46b3f-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="46b3f-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46b3f-140">NOTES</span></span>

## <span data-ttu-id="46b3f-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46b3f-141">RELATED LINKS</span></span>
