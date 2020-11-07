---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 87163619-DEA4-4183-BB11-2D7B16F4BE8A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee4e094c1e38c54b1f9ad4e78723ec49fff1f75b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946247"
---
# <span data-ttu-id="1bbf3-101">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="1bbf3-101">Invoke-AzureRemoteAppSessionLogoff</span></span>

## <span data-ttu-id="1bbf3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1bbf3-102">SYNOPSIS</span></span>
<span data-ttu-id="1bbf3-103">Desconecta uma sessão do Azure RemoteApp imediatamente.</span><span class="sxs-lookup"><span data-stu-id="1bbf3-103">Logs off an Azure RemoteApp session immediately.</span></span>

## <span data-ttu-id="1bbf3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bbf3-104">SYNTAX</span></span>

```
Invoke-AzureRemoteAppSessionLogoff [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bbf3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1bbf3-105">DESCRIPTION</span></span>
<span data-ttu-id="1bbf3-106">O cmdlet **Invoke-AzureRemoteAppSessionLogoff** desconecta imediatamente um usuário de uma sessão remota em execução no Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="1bbf3-106">The **Invoke-AzureRemoteAppSessionLogoff** cmdlet immediately logs off a user from a remote session running in Azure RemoteApp.</span></span>

## <span data-ttu-id="1bbf3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1bbf3-107">EXAMPLES</span></span>

### <span data-ttu-id="1bbf3-108">Exemplo 1: fazer logoff de um usuário</span><span class="sxs-lookup"><span data-stu-id="1bbf3-108">Example 1: Log off a user</span></span>
```
PS C:\> Invoke-AzureRemoteAppSessionLogoff -CollectionName ContosoApps -UserUpn PattiFuller@contoso.com
```

<span data-ttu-id="1bbf3-109">Esse comando desconecta o usuário cujo UPN está PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="1bbf3-109">This command logs off the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="1bbf3-110">OS</span><span class="sxs-lookup"><span data-stu-id="1bbf3-110">PARAMETERS</span></span>

### <span data-ttu-id="1bbf3-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="1bbf3-111">-CollectionName</span></span>
<span data-ttu-id="1bbf3-112">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="1bbf3-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bbf3-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1bbf3-113">-Profile</span></span>
<span data-ttu-id="1bbf3-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1bbf3-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1bbf3-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1bbf3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1bbf3-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="1bbf3-116">-UserUpn</span></span>
<span data-ttu-id="1bbf3-117">Especifica o nome principal do usuário (UPN) de um usuário, por exemplo, PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="1bbf3-117">Specifes the user Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bbf3-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1bbf3-118">-Confirm</span></span>
<span data-ttu-id="1bbf3-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bbf3-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bbf3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bbf3-120">-WhatIf</span></span>
<span data-ttu-id="1bbf3-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1bbf3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bbf3-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1bbf3-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bbf3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bbf3-123">CommonParameters</span></span>
<span data-ttu-id="1bbf3-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bbf3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bbf3-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bbf3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bbf3-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1bbf3-126">INPUTS</span></span>

## <span data-ttu-id="1bbf3-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1bbf3-127">OUTPUTS</span></span>

## <span data-ttu-id="1bbf3-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1bbf3-128">NOTES</span></span>

## <span data-ttu-id="1bbf3-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bbf3-129">RELATED LINKS</span></span>

[<span data-ttu-id="1bbf3-130">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="1bbf3-130">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="1bbf3-131">Desconectar-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="1bbf3-131">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="1bbf3-132">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="1bbf3-132">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)


