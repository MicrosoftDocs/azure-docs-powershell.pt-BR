---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: 4756402ab46deb0260db19474a26e2c568055187
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440430"
---
# <span data-ttu-id="53138-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="53138-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="53138-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53138-102">SYNOPSIS</span></span>
<span data-ttu-id="53138-103">Regenerar a chave de regra de autorização para um namespace.</span><span class="sxs-lookup"><span data-stu-id="53138-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53138-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53138-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53138-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53138-105">DESCRIPTION</span></span>
<span data-ttu-id="53138-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenera a chave primária/chave secundária para a regra de autorização de namespace.</span><span class="sxs-lookup"><span data-stu-id="53138-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="53138-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53138-107">EXAMPLES</span></span>

### <span data-ttu-id="53138-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="53138-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="53138-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="53138-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="53138-110">OS</span><span class="sxs-lookup"><span data-stu-id="53138-110">PARAMETERS</span></span>

### <span data-ttu-id="53138-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="53138-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53138-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53138-112">-DefaultProfile</span></span>
<span data-ttu-id="53138-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="53138-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53138-114">-Force</span><span class="sxs-lookup"><span data-stu-id="53138-114">-Force</span></span>
<span data-ttu-id="53138-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="53138-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="53138-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="53138-116">-Namespace</span></span>
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

### <span data-ttu-id="53138-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="53138-117">-PolicyKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53138-118">-Resource</span><span class="sxs-lookup"><span data-stu-id="53138-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="53138-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53138-119">-Confirm</span></span>
<span data-ttu-id="53138-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53138-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53138-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53138-121">-WhatIf</span></span>
<span data-ttu-id="53138-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53138-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53138-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53138-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53138-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53138-124">CommonParameters</span></span>
<span data-ttu-id="53138-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53138-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53138-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53138-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53138-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53138-127">INPUTS</span></span>

### <span data-ttu-id="53138-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="53138-128">None</span></span>
<span data-ttu-id="53138-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="53138-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="53138-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53138-130">OUTPUTS</span></span>

### <span data-ttu-id="53138-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="53138-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="53138-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53138-132">NOTES</span></span>

## <span data-ttu-id="53138-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53138-133">RELATED LINKS</span></span>

