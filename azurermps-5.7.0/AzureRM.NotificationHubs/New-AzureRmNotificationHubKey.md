---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
ms.openlocfilehash: 66d947cc9d5765fdbfeb815019bbd739f7c3d819
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440834"
---
# <span data-ttu-id="22978-101">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="22978-101">New-AzureRmNotificationHubKey</span></span>

## <span data-ttu-id="22978-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22978-102">SYNOPSIS</span></span>
<span data-ttu-id="22978-103">Regenerar a chave de regra de autorização para um NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="22978-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22978-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22978-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22978-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22978-105">DESCRIPTION</span></span>
<span data-ttu-id="22978-106">New-AzureRmNotificationHubKey cmdlet regenera a chave primária/chave secundária para a regra de autorização NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="22978-106">New-AzureRmNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="22978-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22978-107">EXAMPLES</span></span>

### <span data-ttu-id="22978-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="22978-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="22978-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="22978-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="22978-110">OS</span><span class="sxs-lookup"><span data-stu-id="22978-110">PARAMETERS</span></span>

### <span data-ttu-id="22978-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="22978-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22978-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22978-112">-DefaultProfile</span></span>
<span data-ttu-id="22978-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="22978-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22978-114">-Force</span><span class="sxs-lookup"><span data-stu-id="22978-114">-Force</span></span>
<span data-ttu-id="22978-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="22978-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="22978-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="22978-116">-Namespace</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22978-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="22978-117">-NotificationHub</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22978-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="22978-118">-PolicyKey</span></span>
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

### <span data-ttu-id="22978-119">-Resource</span><span class="sxs-lookup"><span data-stu-id="22978-119">-ResourceGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22978-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="22978-120">-Confirm</span></span>
<span data-ttu-id="22978-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22978-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22978-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22978-122">-WhatIf</span></span>
<span data-ttu-id="22978-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="22978-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22978-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22978-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22978-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22978-125">CommonParameters</span></span>
<span data-ttu-id="22978-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22978-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22978-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22978-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22978-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22978-128">INPUTS</span></span>

### <span data-ttu-id="22978-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="22978-129">None</span></span>
<span data-ttu-id="22978-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="22978-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22978-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22978-131">OUTPUTS</span></span>

### <span data-ttu-id="22978-132">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="22978-132">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="22978-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22978-133">NOTES</span></span>

## <span data-ttu-id="22978-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22978-134">RELATED LINKS</span></span>

