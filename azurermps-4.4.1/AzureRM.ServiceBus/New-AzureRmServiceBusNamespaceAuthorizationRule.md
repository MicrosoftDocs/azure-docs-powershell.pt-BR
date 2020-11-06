---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 6e20ceb2a6809e1e6010263563006468753cd41c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610170"
---
# <span data-ttu-id="1d729-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1d729-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="1d729-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d729-102">SYNOPSIS</span></span>
<span data-ttu-id="1d729-103">Cria uma nova regra de autorização para o namespace especificado do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="1d729-103">Creates a new authorization rule for the specified Service Bus namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d729-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d729-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d729-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d729-105">DESCRIPTION</span></span>
<span data-ttu-id="1d729-106">O cmdlet **New-AzureRmServiceBusNamespaceAuthorizationRule** cria uma nova regra de autorização para o namespace especificado de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="1d729-106">The **New-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1d729-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d729-107">EXAMPLES</span></span>

### <span data-ttu-id="1d729-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1d729-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="1d729-109">Cria `AuthoRule1` com os direitos de **escuta** e **envio** para o namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="1d729-109">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="1d729-110">OS</span><span class="sxs-lookup"><span data-stu-id="1d729-110">PARAMETERS</span></span>

### <span data-ttu-id="1d729-111">-Resource</span><span class="sxs-lookup"><span data-stu-id="1d729-111">-ResourceGroup</span></span>
<span data-ttu-id="1d729-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1d729-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="1d729-113">-Direitos</span><span class="sxs-lookup"><span data-stu-id="1d729-113">-Rights</span></span>
<span data-ttu-id="1d729-114">Os direitos; por exemplo, @ ("Listen", "enviar", "gerenciar")</span><span class="sxs-lookup"><span data-stu-id="1d729-114">The Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d729-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1d729-115">-Confirm</span></span>
<span data-ttu-id="1d729-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d729-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d729-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d729-117">-WhatIf</span></span>
<span data-ttu-id="1d729-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1d729-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d729-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1d729-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d729-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d729-120">-DefaultProfile</span></span>
<span data-ttu-id="1d729-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d729-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d729-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d729-122">-Name</span></span>
<span data-ttu-id="1d729-123">Nome do AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="1d729-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d729-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1d729-124">-Namespace</span></span>
<span data-ttu-id="1d729-125">Nome do namespace do ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="1d729-125">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d729-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d729-126">CommonParameters</span></span>
<span data-ttu-id="1d729-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d729-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d729-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d729-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d729-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d729-129">INPUTS</span></span>

### <span data-ttu-id="1d729-130">-Resource</span><span class="sxs-lookup"><span data-stu-id="1d729-130">-ResourceGroup</span></span>
 <span data-ttu-id="1d729-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1d729-131">System.String</span></span>
 

### <span data-ttu-id="1d729-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="1d729-132">-NamespaceName</span></span>
 <span data-ttu-id="1d729-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1d729-133">System.String</span></span>
 

### <span data-ttu-id="1d729-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="1d729-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="1d729-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1d729-135">System.String</span></span>
 

### <span data-ttu-id="1d729-136">-Direitos</span><span class="sxs-lookup"><span data-stu-id="1d729-136">-Rights</span></span>
 <span data-ttu-id="1d729-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="1d729-137">System.String []</span></span>

## <span data-ttu-id="1d729-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d729-138">OUTPUTS</span></span>

### <span data-ttu-id="1d729-139">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1d729-139">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="1d729-140">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 tipo: Microsoft. ServiceBus/AuthorizationRules Name: AuthoRule1 Location: Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="1d729-140">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="1d729-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d729-141">NOTES</span></span>

## <span data-ttu-id="1d729-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d729-142">RELATED LINKS</span></span>

