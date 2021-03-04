---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: f9f4eb7f60683524eccec8b3d35926b86fa52bbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886041"
---
# <span data-ttu-id="463a1-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="463a1-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="463a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="463a1-102">SYNOPSIS</span></span>
<span data-ttu-id="463a1-103">Obtém os principais detalhes principais da regra de autorização de Hubs de Eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="463a1-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="463a1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="463a1-104">SYNTAX</span></span>

### <span data-ttu-id="463a1-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="463a1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="463a1-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="463a1-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="463a1-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="463a1-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="463a1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="463a1-108">DESCRIPTION</span></span>
<span data-ttu-id="463a1-109">O Get-AzEventHubKey cmdlet retorna as conexões primárias e secundárias e os detalhes das chaves da regra de autorização NameSpace/Event Hubs/Alias especificada.</span><span class="sxs-lookup"><span data-stu-id="463a1-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="463a1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="463a1-110">EXAMPLES</span></span>

### <span data-ttu-id="463a1-111">Exemplo 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="463a1-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="463a1-112">Exemplo 2: EventHub</span><span class="sxs-lookup"><span data-stu-id="463a1-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="463a1-113">Obtém detalhes de conexões primárias e secundárias e chaves para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="463a1-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="463a1-114">Exemplo 3: Alias (Configuração de Recuperação Geográfica)</span><span class="sxs-lookup"><span data-stu-id="463a1-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="463a1-115">Obtém detalhes de Chaves e conexões Primárias, Secundárias, AliasPrimary e AliasSecondary para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="463a1-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="463a1-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="463a1-116">PARAMETERS</span></span>

### <span data-ttu-id="463a1-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="463a1-117">-AliasName</span></span>
<span data-ttu-id="463a1-118">Nome do alias</span><span class="sxs-lookup"><span data-stu-id="463a1-118">Alias Name</span></span>

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

### <span data-ttu-id="463a1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463a1-119">-DefaultProfile</span></span>
<span data-ttu-id="463a1-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="463a1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="463a1-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="463a1-121">-EventHub</span></span>
<span data-ttu-id="463a1-122">Nome eventHub</span><span class="sxs-lookup"><span data-stu-id="463a1-122">EventHub Name</span></span>

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

### <span data-ttu-id="463a1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="463a1-123">-Name</span></span>
<span data-ttu-id="463a1-124">Nome authorizationRule</span><span class="sxs-lookup"><span data-stu-id="463a1-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="463a1-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="463a1-125">-Namespace</span></span>
<span data-ttu-id="463a1-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="463a1-126">Namespace Name</span></span>

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

### <span data-ttu-id="463a1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="463a1-127">-ResourceGroupName</span></span>
<span data-ttu-id="463a1-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="463a1-128">Resource Group Name</span></span>

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

### <span data-ttu-id="463a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463a1-129">CommonParameters</span></span>
<span data-ttu-id="463a1-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463a1-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="463a1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463a1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="463a1-132">INPUTS</span></span>

### <span data-ttu-id="463a1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="463a1-133">System.String</span></span>

## <span data-ttu-id="463a1-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="463a1-134">OUTPUTS</span></span>

### <span data-ttu-id="463a1-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="463a1-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="463a1-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="463a1-136">NOTES</span></span>

## <span data-ttu-id="463a1-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="463a1-137">RELATED LINKS</span></span>
