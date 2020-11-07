---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945614"
---
# <span data-ttu-id="690e2-101">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="690e2-101">Get-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="690e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="690e2-102">SYNOPSIS</span></span>
<span data-ttu-id="690e2-103">Obtém regras de autorização de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="690e2-103">Gets Service bus authorization rules.</span></span>


## <span data-ttu-id="690e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="690e2-104">SYNTAX</span></span>

### <span data-ttu-id="690e2-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="690e2-105">EntitySAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="690e2-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="690e2-106">NamespaceSAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="690e2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="690e2-107">DESCRIPTION</span></span>
<span data-ttu-id="690e2-108">Obtém regras de autorização de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="690e2-108">Gets Service bus authorization rules.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="690e2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="690e2-109">EXAMPLES</span></span>

### <span data-ttu-id="690e2-110">Exemplo 1: obter regra de autorização no nível de namespace</span><span class="sxs-lookup"><span data-stu-id="690e2-110">Example 1: Get authorization rule at namespace level</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

<span data-ttu-id="690e2-111">Obtém todas as regras de autorização disponíveis em MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="690e2-111">Gets all available authorization rules at MyNamespace.</span></span>

### <span data-ttu-id="690e2-112">Exemplo 2: obter regra de autorização para uma fila</span><span class="sxs-lookup"><span data-stu-id="690e2-112">Example 2: Get authorization rule for a Queue</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="690e2-113">Obtém todas as regras de autorização disponíveis uma fila myentity no MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="690e2-113">Gets all available authorization rules a MyEntity Queue on MyNamespace.</span></span>

### <span data-ttu-id="690e2-114">Exemplo 3: obter regra de autorização por nome</span><span class="sxs-lookup"><span data-stu-id="690e2-114">Example 3: Get authorization rule by name</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="690e2-115">Obtém uma regra de autorização chamada myrule no nível MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="690e2-115">Gets an authorization rule called MyRule on MyNamespace level.</span></span>

### <span data-ttu-id="690e2-116">Exemplo 4: obter regra de autorização por permissão</span><span class="sxs-lookup"><span data-stu-id="690e2-116">Example 4: Get authorization rule by permission</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="690e2-117">Obtém todas as regras de autorização que têm permissão de envio no nível de namespace.</span><span class="sxs-lookup"><span data-stu-id="690e2-117">Gets all authorization rules that have send permission on namespace level.</span></span>

## <span data-ttu-id="690e2-118">OS</span><span class="sxs-lookup"><span data-stu-id="690e2-118">PARAMETERS</span></span>

### <span data-ttu-id="690e2-119">-EntityName</span><span class="sxs-lookup"><span data-stu-id="690e2-119">-EntityName</span></span>
<span data-ttu-id="690e2-120">O nome da entidade à qual aplicar a regra.</span><span class="sxs-lookup"><span data-stu-id="690e2-120">The entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690e2-121">-EntityType</span><span class="sxs-lookup"><span data-stu-id="690e2-121">-EntityType</span></span>
<span data-ttu-id="690e2-122">O tipo de entidade (fila, tópico, retransmissor, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="690e2-122">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690e2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="690e2-123">-Name</span></span>
<span data-ttu-id="690e2-124">O nome exclusivo da regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="690e2-124">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690e2-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="690e2-125">-Namespace</span></span>
<span data-ttu-id="690e2-126">O nome do namespace para aplicar a regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="690e2-126">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="690e2-127">Se nenhuma EntityName fornecer a regra estará no nível de namespace.</span><span class="sxs-lookup"><span data-stu-id="690e2-127">If no EntityName provided the rule will be on the namespace level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690e2-128">-Permissão</span><span class="sxs-lookup"><span data-stu-id="690e2-128">-Permission</span></span>
<span data-ttu-id="690e2-129">As permissões de autorização para filtrar (enviar, gerenciar, escutar).</span><span class="sxs-lookup"><span data-stu-id="690e2-129">The authorization permissions to filter (Send, Manage, Listen).</span></span>
<span data-ttu-id="690e2-130">Usa correspondência exata.</span><span class="sxs-lookup"><span data-stu-id="690e2-130">This uses exact match.</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690e2-131">-Perfil</span><span class="sxs-lookup"><span data-stu-id="690e2-131">-Profile</span></span>
<span data-ttu-id="690e2-132">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="690e2-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="690e2-133">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="690e2-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690e2-134">CommonParameters</span></span>
<span data-ttu-id="690e2-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="690e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690e2-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="690e2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690e2-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="690e2-137">INPUTS</span></span>

## <span data-ttu-id="690e2-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="690e2-138">OUTPUTS</span></span>

## <span data-ttu-id="690e2-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="690e2-139">NOTES</span></span>

## <span data-ttu-id="690e2-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="690e2-140">RELATED LINKS</span></span>

[<span data-ttu-id="690e2-141">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="690e2-141">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="690e2-142">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="690e2-142">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="690e2-143">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="690e2-143">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


