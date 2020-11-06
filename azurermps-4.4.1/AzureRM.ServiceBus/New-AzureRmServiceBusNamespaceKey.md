---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 5b366a3be8ca715a42c1c1f916d8ebf327dff8fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432548"
---
# <span data-ttu-id="69bae-101">New-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="69bae-101">New-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="69bae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69bae-102">SYNOPSIS</span></span>
<span data-ttu-id="69bae-103">Regenera a cadeia de caracteres de conexão primária ou secundária para o namespace do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="69bae-103">Regenerates the primary or secondary connection strings for the Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69bae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69bae-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69bae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69bae-105">DESCRIPTION</span></span>
<span data-ttu-id="69bae-106">O cmdlet **New-AzureRmServiceBusNamespace** gera novas cadeias de conexão primária ou secundária para o namespace especificado e a regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="69bae-106">The **New-AzureRmServiceBusNamespace** cmdlet generates new primary or secondary connection strings for the specified namespace and authorization rule.</span></span>

## <span data-ttu-id="69bae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69bae-107">EXAMPLES</span></span>

### <span data-ttu-id="69bae-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69bae-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="69bae-109">Regenera as cadeias de conexão primária ou secundária para o namespace.</span><span class="sxs-lookup"><span data-stu-id="69bae-109">Regenerates the primary or secondary connection strings for the namespace.</span></span>

## <span data-ttu-id="69bae-110">OS</span><span class="sxs-lookup"><span data-stu-id="69bae-110">PARAMETERS</span></span>

### <span data-ttu-id="69bae-111">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="69bae-111">-RegenerateKeys</span></span>
<span data-ttu-id="69bae-112">Regenerar chaves: PrimaryKey/SecondaryKey.</span><span class="sxs-lookup"><span data-stu-id="69bae-112">Regenerate Keys: PrimaryKey/SecondaryKey.</span></span>

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

### <span data-ttu-id="69bae-113">-Resource</span><span class="sxs-lookup"><span data-stu-id="69bae-113">-ResourceGroup</span></span>
<span data-ttu-id="69bae-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69bae-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69bae-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="69bae-115">-Confirm</span></span>
<span data-ttu-id="69bae-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69bae-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69bae-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69bae-117">-WhatIf</span></span>
<span data-ttu-id="69bae-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69bae-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69bae-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69bae-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69bae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69bae-120">-DefaultProfile</span></span>
<span data-ttu-id="69bae-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69bae-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69bae-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="69bae-122">-Name</span></span>
<span data-ttu-id="69bae-123">Nome da regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="69bae-123">Authorization Rule Name.</span></span>

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

### <span data-ttu-id="69bae-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="69bae-124">-Namespace</span></span>
<span data-ttu-id="69bae-125">Nome do namespace.</span><span class="sxs-lookup"><span data-stu-id="69bae-125">Namespace Name.</span></span>

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

### <span data-ttu-id="69bae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69bae-126">CommonParameters</span></span>
<span data-ttu-id="69bae-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69bae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69bae-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69bae-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69bae-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69bae-129">INPUTS</span></span>

### <span data-ttu-id="69bae-130">-Resource</span><span class="sxs-lookup"><span data-stu-id="69bae-130">-ResourceGroup</span></span>
 <span data-ttu-id="69bae-131">System. String</span><span class="sxs-lookup"><span data-stu-id="69bae-131">System.String</span></span>
 

### <span data-ttu-id="69bae-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="69bae-132">-NamespaceName</span></span>
 <span data-ttu-id="69bae-133">System. String</span><span class="sxs-lookup"><span data-stu-id="69bae-133">System.String</span></span>
 

### <span data-ttu-id="69bae-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="69bae-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="69bae-135">System. String</span><span class="sxs-lookup"><span data-stu-id="69bae-135">System.String</span></span>
 

### <span data-ttu-id="69bae-136">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="69bae-136">-RegenerateKeys</span></span>
 <span data-ttu-id="69bae-137">System. String</span><span class="sxs-lookup"><span data-stu-id="69bae-137">System.String</span></span>

## <span data-ttu-id="69bae-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69bae-138">OUTPUTS</span></span>

### <span data-ttu-id="69bae-139">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="69bae-139">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="69bae-140">PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-Value} SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-valor} PrimaryKey: {PrimaryKey valor} SecondaryKey: {SecondaryKey valor} KeyName: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="69bae-140">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="69bae-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69bae-141">NOTES</span></span>

## <span data-ttu-id="69bae-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69bae-142">RELATED LINKS</span></span>

