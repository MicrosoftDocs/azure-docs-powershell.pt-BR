---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 75320133-E7B1-40D4-B16D-567686D5AE99
online version: ''
schema: 2.0.0
ms.openlocfilehash: 40d3bdc73ce6bcbb199cf99bb0586de52f05e132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945987"
---
# <span data-ttu-id="512db-101">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="512db-101">New-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="512db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="512db-102">SYNOPSIS</span></span>
<span data-ttu-id="512db-103">Cria uma nova regra de autorização de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="512db-103">Creates new Service Bus authorization rule.</span></span>

## <span data-ttu-id="512db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="512db-104">SYNTAX</span></span>

### <span data-ttu-id="512db-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="512db-105">EntitySAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="512db-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="512db-106">NamespaceSAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="512db-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="512db-107">DESCRIPTION</span></span>
<span data-ttu-id="512db-108">O cmdlet **New-AzureSBAuthorizationRule** cria uma regra de autorização de barramento de serviço.</span><span class="sxs-lookup"><span data-stu-id="512db-108">The **New-AzureSBAuthorizationRule** cmdlet creates a Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="512db-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="512db-109">EXAMPLES</span></span>

### <span data-ttu-id="512db-110">Exemplo 1: criar uma regra de autorização com chave primária gerada</span><span class="sxs-lookup"><span data-stu-id="512db-110">Example 1: Create an authorization rule with generated primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="512db-111">Cria uma nova regra de autorização no namespace nível com permissão de envio.</span><span class="sxs-lookup"><span data-stu-id="512db-111">Creates new authorization rule on namespace level with Send permission.</span></span>

### <span data-ttu-id="512db-112">Exemplo 2: cria uma regra de autorização fornecendo a chave primária</span><span class="sxs-lookup"><span data-stu-id="512db-112">Example 2: Creates an authorization rule by providing the primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Manage", "Listen", "Send") -EntityName MyEntity -EntityType Queue -PrimaryKey P+lL/Mnd2Z9sj5hwMrRyAxQDdX8RHfbdqU2eIAqs1rc=
```

<span data-ttu-id="512db-113">Cria uma nova regra de autorização no nível de fila myentity com todas as permissões.</span><span class="sxs-lookup"><span data-stu-id="512db-113">Creates new authorization rule on MyEntity Queue level with all permissions.</span></span>

## <span data-ttu-id="512db-114">OS</span><span class="sxs-lookup"><span data-stu-id="512db-114">PARAMETERS</span></span>

### <span data-ttu-id="512db-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="512db-115">-EntityName</span></span>
<span data-ttu-id="512db-116">Especifica o nome da entidade à qual aplicar a regra.</span><span class="sxs-lookup"><span data-stu-id="512db-116">Specifies the entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512db-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="512db-117">-EntityType</span></span>
<span data-ttu-id="512db-118">Especifica o tipo de entidade.</span><span class="sxs-lookup"><span data-stu-id="512db-118">Specifies the entity type.</span></span>
<span data-ttu-id="512db-119">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="512db-119">Valid values are:</span></span>
  
- <span data-ttu-id="512db-120">Coloca</span><span class="sxs-lookup"><span data-stu-id="512db-120">Queue</span></span>
- <span data-ttu-id="512db-121">Tópico</span><span class="sxs-lookup"><span data-stu-id="512db-121">Topic</span></span>
- <span data-ttu-id="512db-122">Haja</span><span class="sxs-lookup"><span data-stu-id="512db-122">Relay</span></span>
- <span data-ttu-id="512db-123">NotificationHub</span><span class="sxs-lookup"><span data-stu-id="512db-123">NotificationHub</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512db-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="512db-124">-Name</span></span>
<span data-ttu-id="512db-125">Especifica o nome da regra de autorização exclusiva.</span><span class="sxs-lookup"><span data-stu-id="512db-125">Specifies the unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512db-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="512db-126">-Namespace</span></span>
<span data-ttu-id="512db-127">Especifica o nome do namespace para aplicar a regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="512db-127">Specifies the namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="512db-128">Se nenhuma *EntityName* fornecer a regra estará no nível de namespace.</span><span class="sxs-lookup"><span data-stu-id="512db-128">If no *EntityName* provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="512db-129">-Permissão</span><span class="sxs-lookup"><span data-stu-id="512db-129">-Permission</span></span>
<span data-ttu-id="512db-130">As permissões de autorização (enviar, gerenciar, escutar).</span><span class="sxs-lookup"><span data-stu-id="512db-130">The authorization permissions (Send, Manage, Listen).</span></span>

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

### <span data-ttu-id="512db-131">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="512db-131">-PrimaryKey</span></span>
<span data-ttu-id="512db-132">Especifica a chave primária de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="512db-132">Specifies the Shared Access Signature primary key.</span></span>
<span data-ttu-id="512db-133">Será gerado se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="512db-133">Will be generated if not provided.</span></span>

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

### <span data-ttu-id="512db-134">-Perfil</span><span class="sxs-lookup"><span data-stu-id="512db-134">-Profile</span></span>
<span data-ttu-id="512db-135">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="512db-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="512db-136">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="512db-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="512db-137">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="512db-137">-SecondaryKey</span></span>
<span data-ttu-id="512db-138">Especifica a chave secundária de assinatura de acesso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="512db-138">Specifies the Shared Access Signature secondary key.</span></span>

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

### <span data-ttu-id="512db-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512db-139">CommonParameters</span></span>
<span data-ttu-id="512db-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="512db-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512db-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="512db-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512db-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="512db-142">INPUTS</span></span>

## <span data-ttu-id="512db-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="512db-143">OUTPUTS</span></span>

## <span data-ttu-id="512db-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="512db-144">NOTES</span></span>

## <span data-ttu-id="512db-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="512db-145">RELATED LINKS</span></span>

[<span data-ttu-id="512db-146">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="512db-146">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="512db-147">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="512db-147">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="512db-148">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="512db-148">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


