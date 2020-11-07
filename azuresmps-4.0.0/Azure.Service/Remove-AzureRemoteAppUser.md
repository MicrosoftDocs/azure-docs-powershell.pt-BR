---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DE89F1C4-8441-4438-B235-F5E0F726EFF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc3bad916830cb638d13f39964e12dc874f7d9f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945866"
---
# <span data-ttu-id="dce65-101">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="dce65-101">Remove-AzureRemoteAppUser</span></span>

## <span data-ttu-id="dce65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dce65-102">SYNOPSIS</span></span>
<span data-ttu-id="dce65-103">Remove um usuário de uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="dce65-103">Removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="dce65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dce65-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dce65-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dce65-105">DESCRIPTION</span></span>
<span data-ttu-id="dce65-106">O cmdlet **Remove-AzureRemoteAppUser** remove um usuário de uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="dce65-106">The **Remove-AzureRemoteAppUser** cmdlet removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="dce65-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dce65-107">EXAMPLES</span></span>

### <span data-ttu-id="dce65-108">Example1: remover um usuário de uma coleção</span><span class="sxs-lookup"><span data-stu-id="dce65-108">Example1: Remove a user from a collection</span></span>
```
PS C:\> Remove-AzureRemoteAppUser -CollectionName "Contoso" -Type OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="dce65-109">Esse comando Remove o usuário do Azure ActiveDirectory PattiFuller@contoso.com da coleção da contoso.</span><span class="sxs-lookup"><span data-stu-id="dce65-109">This command removes the Azure ActiveDirectory user PattiFuller@contoso.com from the Contoso collection.</span></span>

## <span data-ttu-id="dce65-110">OS</span><span class="sxs-lookup"><span data-stu-id="dce65-110">PARAMETERS</span></span>

### <span data-ttu-id="dce65-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="dce65-111">-Alias</span></span>
<span data-ttu-id="dce65-112">Especifica um alias do programa publicado.</span><span class="sxs-lookup"><span data-stu-id="dce65-112">Specifies a published program alias.</span></span>
<span data-ttu-id="dce65-113">Você pode usar esse parâmetro somente no modo de publicação por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dce65-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="dce65-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="dce65-114">-CollectionName</span></span>
<span data-ttu-id="dce65-115">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="dce65-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="dce65-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="dce65-116">-Profile</span></span>
<span data-ttu-id="dce65-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="dce65-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dce65-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="dce65-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dce65-119">-Digite</span><span class="sxs-lookup"><span data-stu-id="dce65-119">-Type</span></span>
<span data-ttu-id="dce65-120">Especifica um tipo de usuário.</span><span class="sxs-lookup"><span data-stu-id="dce65-120">Specifies a user type.</span></span>
<span data-ttu-id="dce65-121">Os valores aceitáveis para esse parâmetro são: OrgId ou MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="dce65-121">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

```yaml
Type: PrincipalProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: OrgId, MicrosoftAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce65-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="dce65-122">-UserUpn</span></span>
<span data-ttu-id="dce65-123">Especifica o nome principal do usuário (UPN) de um usuário, por exemplo, user@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="dce65-123">Specifies the User Principal Name (UPN) of a user, for example, user@contoso.com.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce65-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce65-124">CommonParameters</span></span>
<span data-ttu-id="dce65-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce65-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce65-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce65-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce65-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dce65-127">INPUTS</span></span>

## <span data-ttu-id="dce65-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dce65-128">OUTPUTS</span></span>

## <span data-ttu-id="dce65-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dce65-129">NOTES</span></span>

## <span data-ttu-id="dce65-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dce65-130">RELATED LINKS</span></span>

[<span data-ttu-id="dce65-131">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="dce65-131">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="dce65-132">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="dce65-132">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


