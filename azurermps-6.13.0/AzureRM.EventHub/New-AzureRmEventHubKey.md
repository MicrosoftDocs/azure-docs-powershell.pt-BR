---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 891e72945e3557ad1047b007504572a981449cd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610072"
---
# <span data-ttu-id="18cdf-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="18cdf-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="18cdf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="18cdf-103">Cria uma nova chave primária ou secundária para a regra de autorização de hubs de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="18cdf-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18cdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18cdf-104">SYNTAX</span></span>

### <span data-ttu-id="18cdf-105">NamespaceAuthorizationRuleSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="18cdf-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18cdf-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="18cdf-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18cdf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18cdf-107">DESCRIPTION</span></span>
<span data-ttu-id="18cdf-108">O cmdlet New-AzureRmEventHubKey regenera a chave SAS primária ou secundária para a regra de autorização de hubs de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="18cdf-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="18cdf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18cdf-109">EXAMPLES</span></span>

### <span data-ttu-id="18cdf-110">Exemplo 1,1-namespace-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="18cdf-110">Example 1.1 - Namespace - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="18cdf-111">Regenera a chave primária para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="18cdf-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="18cdf-112">Exemplo 1,2-AuthorizationRule PrimaryKey-EventHub</span><span class="sxs-lookup"><span data-stu-id="18cdf-112">Example 1.2 - EventHub - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="18cdf-113">Regenera a chave primária para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="18cdf-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="18cdf-114">Exemplo 2,1-namespace-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="18cdf-114">Example 2.1  - Namespace - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="18cdf-115">Exemplo 2,2-EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="18cdf-115">Example 2.2 - EventHub - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="18cdf-116">Regenera a chave secundária para a regra de autorização \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="18cdf-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="18cdf-117">OS</span><span class="sxs-lookup"><span data-stu-id="18cdf-117">PARAMETERS</span></span>

### <span data-ttu-id="18cdf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18cdf-118">-DefaultProfile</span></span>
<span data-ttu-id="18cdf-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18cdf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18cdf-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="18cdf-120">-EventHub</span></span>
<span data-ttu-id="18cdf-121">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="18cdf-121">EventHub Name</span></span>

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

### <span data-ttu-id="18cdf-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="18cdf-122">-KeyValue</span></span>
<span data-ttu-id="18cdf-123">Uma chave de 256 bits codificada em base64 para assinar e validar o token SAS.</span><span class="sxs-lookup"><span data-stu-id="18cdf-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18cdf-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="18cdf-124">-Name</span></span>
<span data-ttu-id="18cdf-125">Nome do AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="18cdf-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="18cdf-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="18cdf-126">-Namespace</span></span>
<span data-ttu-id="18cdf-127">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="18cdf-127">Namespace Name</span></span>

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

### <span data-ttu-id="18cdf-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="18cdf-128">-RegenerateKey</span></span>
<span data-ttu-id="18cdf-129">Regenerar chaves-' PrimaryKey '/' SecondaryKey '</span><span class="sxs-lookup"><span data-stu-id="18cdf-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18cdf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18cdf-130">-ResourceGroupName</span></span>
<span data-ttu-id="18cdf-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="18cdf-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18cdf-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18cdf-132">-Confirm</span></span>
<span data-ttu-id="18cdf-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18cdf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18cdf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18cdf-134">-WhatIf</span></span>
<span data-ttu-id="18cdf-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18cdf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18cdf-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18cdf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18cdf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18cdf-137">CommonParameters</span></span>
<span data-ttu-id="18cdf-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18cdf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18cdf-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18cdf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18cdf-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18cdf-140">INPUTS</span></span>

### <span data-ttu-id="18cdf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="18cdf-141">System.String</span></span>

## <span data-ttu-id="18cdf-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18cdf-142">OUTPUTS</span></span>

### <span data-ttu-id="18cdf-143">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="18cdf-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="18cdf-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18cdf-144">NOTES</span></span>

## <span data-ttu-id="18cdf-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18cdf-145">RELATED LINKS</span></span>
