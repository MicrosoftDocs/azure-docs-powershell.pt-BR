---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 8be39cb4b4b173d3b87efbf0b7ecea72ae233061
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603056"
---
# <span data-ttu-id="60871-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="60871-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="60871-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60871-102">SYNOPSIS</span></span>
<span data-ttu-id="60871-103">Cria uma nova chave primária ou secundária para a regra de autorização de hubs de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="60871-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60871-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60871-104">SYNTAX</span></span>

### <span data-ttu-id="60871-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="60871-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60871-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="60871-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60871-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60871-107">DESCRIPTION</span></span>
<span data-ttu-id="60871-108">O cmdlet New-AzureRmEventHubKey regenera a chave SAS primária ou secundária para a regra de autorização de hubs de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="60871-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="60871-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60871-109">EXAMPLES</span></span>

### <span data-ttu-id="60871-110">Exemplo 1,1</span><span class="sxs-lookup"><span data-stu-id="60871-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="60871-111">Regenera a chave primária para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="60871-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="60871-112">Exemplo 1,2</span><span class="sxs-lookup"><span data-stu-id="60871-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="60871-113">Regenera a chave primária para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="60871-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="60871-114">Exemplo 2,1</span><span class="sxs-lookup"><span data-stu-id="60871-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="60871-115">Exemplo 2,2</span><span class="sxs-lookup"><span data-stu-id="60871-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="60871-116">Regenera a chave secundária para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="60871-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="60871-117">OS</span><span class="sxs-lookup"><span data-stu-id="60871-117">PARAMETERS</span></span>

### <span data-ttu-id="60871-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60871-118">-DefaultProfile</span></span>
<span data-ttu-id="60871-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60871-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60871-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="60871-120">-EventHub</span></span>
<span data-ttu-id="60871-121">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="60871-121">EventHub Name</span></span>

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

### <span data-ttu-id="60871-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="60871-122">-Name</span></span>
<span data-ttu-id="60871-123">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="60871-123">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="60871-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="60871-124">-Namespace</span></span>
<span data-ttu-id="60871-125">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="60871-125">Namespace Name</span></span>

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

### <span data-ttu-id="60871-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="60871-126">-RegenerateKey</span></span>
<span data-ttu-id="60871-127">Regenerar chaves-' PrimaryKey '/' SecondaryKey '</span><span class="sxs-lookup"><span data-stu-id="60871-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60871-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60871-128">-ResourceGroupName</span></span>
<span data-ttu-id="60871-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="60871-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60871-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60871-130">-Confirm</span></span>
<span data-ttu-id="60871-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60871-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60871-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60871-132">-WhatIf</span></span>
<span data-ttu-id="60871-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60871-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60871-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60871-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60871-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60871-135">CommonParameters</span></span>
<span data-ttu-id="60871-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60871-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="60871-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60871-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60871-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60871-138">INPUTS</span></span>

### <span data-ttu-id="60871-139">System. String</span><span class="sxs-lookup"><span data-stu-id="60871-139">System.String</span></span>


## <span data-ttu-id="60871-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60871-140">OUTPUTS</span></span>

### <span data-ttu-id="60871-141">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="60871-141">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="60871-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60871-142">NOTES</span></span>

## <span data-ttu-id="60871-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60871-143">RELATED LINKS</span></span>
