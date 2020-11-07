---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E246C177-EAEE-4D7A-A544-664F47862FC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92d450a10628ea7e85a49962ac262d4dece8e4c8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946131"
---
# <span data-ttu-id="6c40f-101">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6c40f-101">Remove-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="6c40f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c40f-102">SYNOPSIS</span></span>
<span data-ttu-id="6c40f-103">Remove a regra de autorização de barramento de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="6c40f-103">Removes existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="6c40f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c40f-104">SYNTAX</span></span>

### <span data-ttu-id="6c40f-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="6c40f-105">EntitySAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> -EntityName <String>
 -EntityType <ServiceBusEntityType> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6c40f-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="6c40f-106">NamespaceSAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c40f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c40f-107">DESCRIPTION</span></span>
<span data-ttu-id="6c40f-108">Remove a regra de autorização de barramento de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="6c40f-108">Removes existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="6c40f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c40f-109">EXAMPLES</span></span>

### <span data-ttu-id="6c40f-110">Exemplo 1: Remover regra de autorização no nível de namespace</span><span class="sxs-lookup"><span data-stu-id="6c40f-110">Example 1: Remove authorization rule at namespace level</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="6c40f-111">Remove a regra de autorização myrule da MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="6c40f-111">Removes authorization rule MyRule from MyNamespace.</span></span>

### <span data-ttu-id="6c40f-112">Exemplo 2: remover a regra de autorização de uma fila</span><span class="sxs-lookup"><span data-stu-id="6c40f-112">Example 2: Remove authorization rule for a Queue</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="6c40f-113">Remove a regra de autorização chamada myrule para uma fila myentity no MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="6c40f-113">Removes authorization rule called MyRule for a MyEntity Queue on MyNamespace.</span></span>

## <span data-ttu-id="6c40f-114">OS</span><span class="sxs-lookup"><span data-stu-id="6c40f-114">PARAMETERS</span></span>

### <span data-ttu-id="6c40f-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="6c40f-115">-EntityName</span></span>
<span data-ttu-id="6c40f-116">O nome da entidade à qual aplicar a regra.</span><span class="sxs-lookup"><span data-stu-id="6c40f-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="6c40f-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="6c40f-117">-EntityType</span></span>
<span data-ttu-id="6c40f-118">O tipo de entidade (fila, tópico, retransmissor, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="6c40f-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="6c40f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c40f-119">-Name</span></span>
<span data-ttu-id="6c40f-120">O nome exclusivo da regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="6c40f-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="6c40f-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6c40f-121">-Namespace</span></span>
<span data-ttu-id="6c40f-122">O nome do namespace para aplicar a regra de autorização.</span><span class="sxs-lookup"><span data-stu-id="6c40f-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="6c40f-123">Se nenhuma EntityName fornecer a regra estará no nível de namespace.</span><span class="sxs-lookup"><span data-stu-id="6c40f-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="6c40f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c40f-124">-PassThru</span></span>
<span data-ttu-id="6c40f-125">Indica que esse cmdlet retorna um objeto que representa o item no qual ele funciona.</span><span class="sxs-lookup"><span data-stu-id="6c40f-125">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="6c40f-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="6c40f-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c40f-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6c40f-127">-Profile</span></span>
<span data-ttu-id="6c40f-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6c40f-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c40f-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6c40f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c40f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c40f-130">CommonParameters</span></span>
<span data-ttu-id="6c40f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c40f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c40f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c40f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c40f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c40f-133">INPUTS</span></span>

## <span data-ttu-id="6c40f-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c40f-134">OUTPUTS</span></span>

## <span data-ttu-id="6c40f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c40f-135">NOTES</span></span>

## <span data-ttu-id="6c40f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c40f-136">RELATED LINKS</span></span>

[<span data-ttu-id="6c40f-137">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6c40f-137">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="6c40f-138">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6c40f-138">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="6c40f-139">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6c40f-139">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


