---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6F2CC9F-8C95-484D-8676-7DAA5E0AA617
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf2a5cc1390db2a6ae5eb49894a47d1ccf0aca4c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946316"
---
# <span data-ttu-id="d7875-101">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="d7875-101">Get-AzureRemoteAppUser</span></span>

## <span data-ttu-id="d7875-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7875-102">SYNOPSIS</span></span>
<span data-ttu-id="d7875-103">Lista os usuários em uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d7875-103">Lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="d7875-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7875-104">SYNTAX</span></span>

```
Get-AzureRemoteAppUser [-CollectionName] <String> [[-UserUpn] <String>] [-Alias <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d7875-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7875-105">DESCRIPTION</span></span>
<span data-ttu-id="d7875-106">O cmdlet **Get-AzureRemoteAppUser** lista os usuários em uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d7875-106">The **Get-AzureRemoteAppUser** cmdlet lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="d7875-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7875-107">EXAMPLES</span></span>

### <span data-ttu-id="d7875-108">Exemplo 1: listar os usuários de uma coleção</span><span class="sxs-lookup"><span data-stu-id="d7875-108">Example 1: List the users of a collection</span></span>
```
PS C:\> Get-AzureRemoteAppUser -CollectionName "Contoso"
```

<span data-ttu-id="d7875-109">Esse comando lista os usuários que têm acesso à coleção do Azure RemoteApp chamada contoso.</span><span class="sxs-lookup"><span data-stu-id="d7875-109">This command lists the users who have access to the Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="d7875-110">OS</span><span class="sxs-lookup"><span data-stu-id="d7875-110">PARAMETERS</span></span>

### <span data-ttu-id="d7875-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="d7875-111">-Alias</span></span>
<span data-ttu-id="d7875-112">Especifica um alias do programa publicado.</span><span class="sxs-lookup"><span data-stu-id="d7875-112">Specifies a published program alias.</span></span>
<span data-ttu-id="d7875-113">Você pode usar esse parâmetro somente no modo de publicação por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d7875-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="d7875-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="d7875-114">-CollectionName</span></span>
<span data-ttu-id="d7875-115">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d7875-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="d7875-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d7875-116">-Profile</span></span>
<span data-ttu-id="d7875-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d7875-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d7875-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d7875-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d7875-119">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="d7875-119">-UserUpn</span></span>
<span data-ttu-id="d7875-120">Especifica o nome de usuário principal (UPN) de um usuário para o qual as informações são listadas.</span><span class="sxs-lookup"><span data-stu-id="d7875-120">Specifies the User Principal Name (UPN) of a user for which to list information.</span></span>
<span data-ttu-id="d7875-121">Por exemplo, PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="d7875-121">For example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d7875-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7875-122">CommonParameters</span></span>
<span data-ttu-id="d7875-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7875-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7875-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7875-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7875-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7875-125">INPUTS</span></span>

## <span data-ttu-id="d7875-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7875-126">OUTPUTS</span></span>

## <span data-ttu-id="d7875-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7875-127">NOTES</span></span>

## <span data-ttu-id="d7875-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7875-128">RELATED LINKS</span></span>

[<span data-ttu-id="d7875-129">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="d7875-129">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="d7875-130">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="d7875-130">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="d7875-131">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="d7875-131">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


