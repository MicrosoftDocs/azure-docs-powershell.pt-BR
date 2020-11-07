---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A121B341-091D-42AD-B56A-3C75E25A1BF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8383240f9c1db58a6a22f6754f98211580d31a73
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946381"
---
# <span data-ttu-id="838f5-101">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="838f5-101">Add-AzureRemoteAppUser</span></span>

## <span data-ttu-id="838f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="838f5-102">SYNOPSIS</span></span>
<span data-ttu-id="838f5-103">Adiciona um usuário a uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="838f5-103">Adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="838f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="838f5-104">SYNTAX</span></span>

```
Add-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="838f5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="838f5-105">DESCRIPTION</span></span>
<span data-ttu-id="838f5-106">O cmdlet **Add-AzureRemoteAppUser** adiciona um usuário a uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="838f5-106">The **Add-AzureRemoteAppUser** cmdlet adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="838f5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="838f5-107">EXAMPLES</span></span>

### <span data-ttu-id="838f5-108">Exemplo 1: adicionar um usuário usando uma conta da Microsoft</span><span class="sxs-lookup"><span data-stu-id="838f5-108">Example 1: Add a user using a Microsoft Account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType MicrosoftAccount -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="838f5-109">Esse comando adiciona a conta da Microsoft PattiFuller@contoso.com à coleção chamada contoso.</span><span class="sxs-lookup"><span data-stu-id="838f5-109">This command adds the Microsoft Account PattiFuller@contoso.com to the collection named Contoso.</span></span>

### <span data-ttu-id="838f5-110">Exemplo 2: adicionar um usuário usando uma conta do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="838f5-110">Example 2: Add a user using an Azure Active Directory account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="838f5-111">Esse comando adiciona a conta do Azure Active Directory PattiFuller@contoso.com à coleção chamada contoso.</span><span class="sxs-lookup"><span data-stu-id="838f5-111">This command adds the Azure Active Directory account PattiFuller@contoso.com to the collection named Contoso.</span></span>

## <span data-ttu-id="838f5-112">OS</span><span class="sxs-lookup"><span data-stu-id="838f5-112">PARAMETERS</span></span>

### <span data-ttu-id="838f5-113">-Alias</span><span class="sxs-lookup"><span data-stu-id="838f5-113">-Alias</span></span>
<span data-ttu-id="838f5-114">Especifica um alias do programa publicado.</span><span class="sxs-lookup"><span data-stu-id="838f5-114">Specifies a published program alias.</span></span>
<span data-ttu-id="838f5-115">Você pode usar esse parâmetro somente no modo de publicação por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="838f5-115">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="838f5-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="838f5-116">-CollectionName</span></span>
<span data-ttu-id="838f5-117">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="838f5-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="838f5-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="838f5-118">-Profile</span></span>
<span data-ttu-id="838f5-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="838f5-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="838f5-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="838f5-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="838f5-121">-Digite</span><span class="sxs-lookup"><span data-stu-id="838f5-121">-Type</span></span>
<span data-ttu-id="838f5-122">Especifica um tipo de usuário.</span><span class="sxs-lookup"><span data-stu-id="838f5-122">Specifies a user type.</span></span>
<span data-ttu-id="838f5-123">Os valores aceitáveis para esse parâmetro são: OrgId ou MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="838f5-123">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

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

### <span data-ttu-id="838f5-124">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="838f5-124">-UserUpn</span></span>
<span data-ttu-id="838f5-125">Especifica o nome principal do usuário (UPN) de um usuário, por exemplo, PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="838f5-125">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="838f5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838f5-126">CommonParameters</span></span>
<span data-ttu-id="838f5-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="838f5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838f5-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="838f5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838f5-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="838f5-129">INPUTS</span></span>

## <span data-ttu-id="838f5-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="838f5-130">OUTPUTS</span></span>

## <span data-ttu-id="838f5-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="838f5-131">NOTES</span></span>

## <span data-ttu-id="838f5-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="838f5-132">RELATED LINKS</span></span>

[<span data-ttu-id="838f5-133">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="838f5-133">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)

[<span data-ttu-id="838f5-134">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="838f5-134">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


