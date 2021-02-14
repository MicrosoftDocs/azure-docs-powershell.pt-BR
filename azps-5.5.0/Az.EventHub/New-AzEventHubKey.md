---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: 477884e676118f461578be500715fd3698957003
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115798"
---
# <span data-ttu-id="e50f4-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="e50f4-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="e50f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e50f4-102">SYNOPSIS</span></span>
<span data-ttu-id="e50f4-103">Cria uma nova chave primária ou secundária para a regra de autorização de Hubs de Eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="e50f4-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="e50f4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e50f4-104">SYNTAX</span></span>

### <span data-ttu-id="e50f4-105">NamespaceAuthorizationRuleSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e50f4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e50f4-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e50f4-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e50f4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e50f4-107">DESCRIPTION</span></span>
<span data-ttu-id="e50f4-108">O New-AzEventHubKey cmdlet regenera a chave SAS primária ou secundária para a regra de autorização de Hubs de Eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="e50f4-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="e50f4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e50f4-109">EXAMPLES</span></span>

### <span data-ttu-id="e50f4-110">Exemplo 1: Namespace - AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e50f4-110">Example 1: Namespace - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="e50f4-111">Regenera a chave primária da regra de autorização \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="e50f4-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="e50f4-112">Exemplo 2: EventHub - AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e50f4-112">Example 2: EventHub - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="e50f4-113">Regenera a chave primária da regra de autorização \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="e50f4-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="e50f4-114">Exemplo 3: - Namespace - AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="e50f4-114">Example 3: - Namespace - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="e50f4-115">Exemplo 4: EventHub - AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="e50f4-115">Example 4: EventHub - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="e50f4-116">Regenera a chave secundária da regra de autorização \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="e50f4-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="e50f4-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e50f4-117">PARAMETERS</span></span>

### <span data-ttu-id="e50f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50f4-118">-DefaultProfile</span></span>
<span data-ttu-id="e50f4-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e50f4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e50f4-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e50f4-120">-EventHub</span></span>
<span data-ttu-id="e50f4-121">Nome do EventHub</span><span class="sxs-lookup"><span data-stu-id="e50f4-121">EventHub Name</span></span>

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

### <span data-ttu-id="e50f4-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="e50f4-122">-KeyValue</span></span>
<span data-ttu-id="e50f4-123">Uma chave de 256 bits codificada com base64 para assinar e validar o token SAS.</span><span class="sxs-lookup"><span data-stu-id="e50f4-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="e50f4-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e50f4-124">-Name</span></span>
<span data-ttu-id="e50f4-125">Nome de AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e50f4-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="e50f4-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e50f4-126">-Namespace</span></span>
<span data-ttu-id="e50f4-127">Nome do namespace</span><span class="sxs-lookup"><span data-stu-id="e50f4-127">Namespace Name</span></span>

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

### <span data-ttu-id="e50f4-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="e50f4-128">-RegenerateKey</span></span>
<span data-ttu-id="e50f4-129">Chaves de Regeneração - 'PrimaryKey'/'SecondaryKey'</span><span class="sxs-lookup"><span data-stu-id="e50f4-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="e50f4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e50f4-130">-ResourceGroupName</span></span>
<span data-ttu-id="e50f4-131">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e50f4-131">Resource Group Name</span></span>

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

### <span data-ttu-id="e50f4-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e50f4-132">-Confirm</span></span>
<span data-ttu-id="e50f4-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e50f4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e50f4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e50f4-134">-WhatIf</span></span>
<span data-ttu-id="e50f4-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e50f4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e50f4-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e50f4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e50f4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50f4-137">CommonParameters</span></span>
<span data-ttu-id="e50f4-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e50f4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50f4-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e50f4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50f4-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="e50f4-140">INPUTS</span></span>

### <span data-ttu-id="e50f4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e50f4-141">System.String</span></span>

## <span data-ttu-id="e50f4-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="e50f4-142">OUTPUTS</span></span>

### <span data-ttu-id="e50f4-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="e50f4-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="e50f4-144">Notas</span><span class="sxs-lookup"><span data-stu-id="e50f4-144">NOTES</span></span>

## <span data-ttu-id="e50f4-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e50f4-145">RELATED LINKS</span></span>
