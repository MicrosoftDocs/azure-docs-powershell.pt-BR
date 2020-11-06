---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: f8a9f074398df5ce9d8464adf3c22a65d14784b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439873"
---
# <span data-ttu-id="b9fdd-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="b9fdd-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="b9fdd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fdd-103">Obtém os detalhes da chave primária da regra de autorização dos hubs de eventos especificados.</span><span class="sxs-lookup"><span data-stu-id="b9fdd-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9fdd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9fdd-104">SYNTAX</span></span>

### <span data-ttu-id="b9fdd-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9fdd-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9fdd-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9fdd-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9fdd-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9fdd-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9fdd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9fdd-108">DESCRIPTION</span></span>
<span data-ttu-id="b9fdd-109">O cmdlet Get-AzureRmEventHubKey retorna connectionStrings primária e secundária e detalhes de chaves do NameSpace especificado/hubs de evento/regra de autorização de alias.</span><span class="sxs-lookup"><span data-stu-id="b9fdd-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="b9fdd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9fdd-110">EXAMPLES</span></span>

### <span data-ttu-id="b9fdd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9fdd-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="b9fdd-112">Obtém detalhes de connectionStrings primárias e secundárias e chaves para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="b9fdd-112">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="b9fdd-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9fdd-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="b9fdd-114">Obtém detalhes das teclas e connectionStrings primária, secundária, AliasPrimary e AliasSecondary para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="b9fdd-114">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="b9fdd-115">OS</span><span class="sxs-lookup"><span data-stu-id="b9fdd-115">PARAMETERS</span></span>

### <span data-ttu-id="b9fdd-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="b9fdd-116">-AliasName</span></span>
<span data-ttu-id="b9fdd-117">Nome do alias</span><span class="sxs-lookup"><span data-stu-id="b9fdd-117">Alias Name</span></span>

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

### <span data-ttu-id="b9fdd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fdd-118">-DefaultProfile</span></span>
<span data-ttu-id="b9fdd-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9fdd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9fdd-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b9fdd-120">-EventHub</span></span>
<span data-ttu-id="b9fdd-121">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="b9fdd-121">EventHub Name</span></span>

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

### <span data-ttu-id="b9fdd-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9fdd-122">-Name</span></span>
<span data-ttu-id="b9fdd-123">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b9fdd-123">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="b9fdd-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b9fdd-124">-Namespace</span></span>
<span data-ttu-id="b9fdd-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="b9fdd-125">Namespace Name</span></span>

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

### <span data-ttu-id="b9fdd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9fdd-126">-ResourceGroupName</span></span>
<span data-ttu-id="b9fdd-127">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b9fdd-127">Resource Group Name</span></span>

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

### <span data-ttu-id="b9fdd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fdd-128">CommonParameters</span></span>
<span data-ttu-id="b9fdd-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9fdd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b9fdd-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9fdd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9fdd-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9fdd-131">INPUTS</span></span>

### <span data-ttu-id="b9fdd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b9fdd-132">System.String</span></span>


## <span data-ttu-id="b9fdd-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9fdd-133">OUTPUTS</span></span>

### <span data-ttu-id="b9fdd-134">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="b9fdd-134">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="b9fdd-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9fdd-135">NOTES</span></span>

## <span data-ttu-id="b9fdd-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9fdd-136">RELATED LINKS</span></span>
