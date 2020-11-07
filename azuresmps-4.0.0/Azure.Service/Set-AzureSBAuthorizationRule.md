---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 17065902-97EA-4F5F-926B-B7CBEE3EAF84
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab76cf3052f28b0ff89e3e41aaa08127cc33411e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945820"
---
# <span data-ttu-id="c7bea-101">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c7bea-101">Set-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="c7bea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7bea-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bea-103">Atualiza a regra de autorização de barramento de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="c7bea-103">Updates existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="c7bea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7bea-104">SYNTAX</span></span>

### <span data-ttu-id="c7bea-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="c7bea-105">EntitySAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c7bea-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="c7bea-106">NamespaceSAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c7bea-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7bea-107">DESCRIPTION</span></span>
<span data-ttu-id="c7bea-108">Atualiza a regra de autorização de barramento de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="c7bea-108">Updates existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="c7bea-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7bea-109">EXAMPLES</span></span>

### <span data-ttu-id="c7bea-110">Exemplo 1: renovar chave primária para a regra de autorização no nível de namespace</span><span class="sxs-lookup"><span data-stu-id="c7bea-110">Example 1: Renew primary key for authorization rule at namespace level</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="c7bea-111">A chave primária é renovada.</span><span class="sxs-lookup"><span data-stu-id="c7bea-111">The primary key is renewed.</span></span>

### <span data-ttu-id="c7bea-112">Exemplo 2: permissão de atualização de regra de autorização</span><span class="sxs-lookup"><span data-stu-id="c7bea-112">Example 2: Update authorization rule permission</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Listen", "Send") -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="c7bea-113">Atualiza as permissões.</span><span class="sxs-lookup"><span data-stu-id="c7bea-113">Updates the permissions.</span></span>

## <span data-ttu-id="c7bea-114">OS</span><span class="sxs-lookup"><span data-stu-id="c7bea-114">PARAMETERS</span></span>

### <span data-ttu-id="c7bea-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="c7bea-115">-EntityName</span></span>
<span data-ttu-id="c7bea-116">O nome da entidade à qual aplicar a regra.</span><span class="sxs-lookup"><span data-stu-id="c7bea-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="c7bea-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="c7bea-117">-EntityType</span></span>
<span data-ttu-id="c7bea-118">O tipo de entidade (fila, tópico, retransmissor, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="c7bea-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="c7bea-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7bea-119">-Name</span></span>
<span data-ttu-id="c7bea-120">O nome exclusivo da regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="c7bea-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="c7bea-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c7bea-121">-Namespace</span></span>
<span data-ttu-id="c7bea-122">O nome do namespace para aplicar a regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="c7bea-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="c7bea-123">Se nenhuma EntityName fornecer a regra estará no nível de namespace.</span><span class="sxs-lookup"><span data-stu-id="c7bea-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="c7bea-124">-Permissão</span><span class="sxs-lookup"><span data-stu-id="c7bea-124">-Permission</span></span>
<span data-ttu-id="c7bea-125">As permissões de autorização (enviar, gerenciar, escutar).</span><span class="sxs-lookup"><span data-stu-id="c7bea-125">The authorization permissions (Send, Manage, Listen).</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bea-126">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c7bea-126">-PrimaryKey</span></span>
<span data-ttu-id="c7bea-127">A chave primária de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="c7bea-127">The Shared Access Signature primary key.</span></span>
<span data-ttu-id="c7bea-128">Será gerado se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="c7bea-128">Will be generated if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bea-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c7bea-129">-Profile</span></span>
<span data-ttu-id="c7bea-130">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c7bea-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7bea-131">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c7bea-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7bea-132">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="c7bea-132">-SecondaryKey</span></span>
<span data-ttu-id="c7bea-133">A chave secundária de assinatura do acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="c7bea-133">The Shared Access Signature secondary key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bea-134">CommonParameters</span></span>
<span data-ttu-id="c7bea-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7bea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bea-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7bea-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bea-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7bea-137">INPUTS</span></span>

## <span data-ttu-id="c7bea-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7bea-138">OUTPUTS</span></span>

## <span data-ttu-id="c7bea-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7bea-139">NOTES</span></span>

## <span data-ttu-id="c7bea-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7bea-140">RELATED LINKS</span></span>

[<span data-ttu-id="c7bea-141">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c7bea-141">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="c7bea-142">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c7bea-142">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="c7bea-143">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c7bea-143">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)


