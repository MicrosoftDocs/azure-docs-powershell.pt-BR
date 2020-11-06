---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 08f7f33138ddf9d5226cfc93f263fdec65de3388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429108"
---
# <span data-ttu-id="50873-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="50873-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="50873-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50873-102">SYNOPSIS</span></span>
<span data-ttu-id="50873-103">Remove a regra de autorização de um namespace de barramento de serviço do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="50873-103">Removes the authorization rule of a Service Bus namespace from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50873-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50873-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroupName <String> -Namespace <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50873-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50873-105">DESCRIPTION</span></span>
<span data-ttu-id="50873-106">O cmdlet **Remove-AzureRmServiceBusNamespaceAuthorizationRule** remove a regra de autorização de um namespace de barramento de serviço para o grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="50873-106">The **Remove-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace for the specified resource group.</span></span>

## <span data-ttu-id="50873-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50873-107">EXAMPLES</span></span>

### <span data-ttu-id="50873-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="50873-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="50873-109">Remove a regra `SBAuthoRule1` de autorização do namespace `SB-Example1` do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="50873-109">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

## <span data-ttu-id="50873-110">OS</span><span class="sxs-lookup"><span data-stu-id="50873-110">PARAMETERS</span></span>

### <span data-ttu-id="50873-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="50873-111">-Confirm</span></span>
<span data-ttu-id="50873-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50873-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50873-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50873-113">-WhatIf</span></span>
<span data-ttu-id="50873-114">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="50873-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50873-115">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="50873-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50873-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50873-116">-DefaultProfile</span></span>
<span data-ttu-id="50873-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50873-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50873-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="50873-118">-Name</span></span>
<span data-ttu-id="50873-119">Nome do namespace AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="50873-119">Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="50873-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="50873-120">-Namespace</span></span>
<span data-ttu-id="50873-121">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="50873-121">Namespace Name.</span></span>

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

### <span data-ttu-id="50873-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50873-122">-ResourceGroupName</span></span>
<span data-ttu-id="50873-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="50873-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50873-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50873-124">CommonParameters</span></span>
<span data-ttu-id="50873-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50873-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50873-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50873-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50873-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50873-127">INPUTS</span></span>

### <span data-ttu-id="50873-128">-Resource</span><span class="sxs-lookup"><span data-stu-id="50873-128">-ResourceGroup</span></span>
 <span data-ttu-id="50873-129">System. String</span><span class="sxs-lookup"><span data-stu-id="50873-129">System.String</span></span>

### <span data-ttu-id="50873-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="50873-130">-NamespaceName</span></span>
 <span data-ttu-id="50873-131">System. String</span><span class="sxs-lookup"><span data-stu-id="50873-131">System.String</span></span>

### <span data-ttu-id="50873-132">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="50873-132">-AuthorizationRuleName</span></span>
 <span data-ttu-id="50873-133">System. String</span><span class="sxs-lookup"><span data-stu-id="50873-133">System.String</span></span>

## <span data-ttu-id="50873-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50873-134">OUTPUTS</span></span>

### <span data-ttu-id="50873-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50873-135">System.Boolean</span></span>

## <span data-ttu-id="50873-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50873-136">NOTES</span></span>

## <span data-ttu-id="50873-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50873-137">RELATED LINKS</span></span>

