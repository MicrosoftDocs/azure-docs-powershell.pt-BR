---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 27be06fb85cc4bd1dc38dd7a123205d3ba7ff4d3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775897"
---
# <span data-ttu-id="11a69-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="11a69-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="11a69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11a69-102">SYNOPSIS</span></span>
<span data-ttu-id="11a69-103">Obtém os detalhes da chave primária da regra de autorização dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="11a69-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="11a69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11a69-104">SYNTAX</span></span>

### <span data-ttu-id="11a69-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="11a69-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11a69-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="11a69-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11a69-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="11a69-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11a69-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11a69-108">DESCRIPTION</span></span>
<span data-ttu-id="11a69-109">O cmdlet Get-AzEventHubKey retorna connectionStrings primária e secundária e detalhes de chaves do NameSpace especificado/hubs de evento/regra de autorização de alias.</span><span class="sxs-lookup"><span data-stu-id="11a69-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="11a69-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11a69-110">EXAMPLES</span></span>

### <span data-ttu-id="11a69-111">Exemplo 1-namespace</span><span class="sxs-lookup"><span data-stu-id="11a69-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="11a69-112">Exemplo 2-EventHub</span><span class="sxs-lookup"><span data-stu-id="11a69-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="11a69-113">Obtém detalhes de connectionStrings primárias e secundárias e chaves para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="11a69-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="11a69-114">Exemplo 3-alias (configuração de georecuperação)</span><span class="sxs-lookup"><span data-stu-id="11a69-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="11a69-115">Obtém detalhes das teclas e connectionStrings primária, secundária, AliasPrimary e AliasSecondary para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="11a69-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="11a69-116">OS</span><span class="sxs-lookup"><span data-stu-id="11a69-116">PARAMETERS</span></span>

### <span data-ttu-id="11a69-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="11a69-117">-AliasName</span></span>
<span data-ttu-id="11a69-118">Nome do alias</span><span class="sxs-lookup"><span data-stu-id="11a69-118">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11a69-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a69-119">-DefaultProfile</span></span>
<span data-ttu-id="11a69-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11a69-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11a69-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="11a69-121">-EventHub</span></span>
<span data-ttu-id="11a69-122">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="11a69-122">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11a69-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="11a69-123">-Name</span></span>
<span data-ttu-id="11a69-124">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="11a69-124">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11a69-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="11a69-125">-Namespace</span></span>
<span data-ttu-id="11a69-126">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="11a69-126">Namespace Name</span></span>

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

### <span data-ttu-id="11a69-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11a69-127">-ResourceGroupName</span></span>
<span data-ttu-id="11a69-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="11a69-128">Resource Group Name</span></span>

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

### <span data-ttu-id="11a69-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a69-129">CommonParameters</span></span>
<span data-ttu-id="11a69-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11a69-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a69-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11a69-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a69-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11a69-132">INPUTS</span></span>

### <span data-ttu-id="11a69-133">System. String</span><span class="sxs-lookup"><span data-stu-id="11a69-133">System.String</span></span>

## <span data-ttu-id="11a69-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11a69-134">OUTPUTS</span></span>

### <span data-ttu-id="11a69-135">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="11a69-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="11a69-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11a69-136">NOTES</span></span>

## <span data-ttu-id="11a69-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11a69-137">RELATED LINKS</span></span>
