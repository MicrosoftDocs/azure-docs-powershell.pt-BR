---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 67890A2A-7922-4E4A-96B4-B58CF532D2DE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a949128309e2777984be0dac33f27b0bc53aab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945737"
---
# <span data-ttu-id="e9be8-101">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="e9be8-101">Update-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="e9be8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9be8-102">SYNOPSIS</span></span>
<span data-ttu-id="e9be8-103">Atualiza uma coleção do Azure RemoteApp com uma nova imagem de modelo.</span><span class="sxs-lookup"><span data-stu-id="e9be8-103">Updates an Azure RemoteApp collection with a new template image.</span></span>

## <span data-ttu-id="e9be8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9be8-104">SYNTAX</span></span>

```
Update-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [[-SubnetName] <String>]
 [-ForceLogoffWhenUpdateComplete] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9be8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9be8-105">DESCRIPTION</span></span>
<span data-ttu-id="e9be8-106">O cmdlet **Update-AzureRemoteAppCollection** atualiza uma coleção do Azure RemoteApp com uma nova imagem de modelo.</span><span class="sxs-lookup"><span data-stu-id="e9be8-106">The **Update-AzureRemoteAppCollection** cmdlet updates an Azure RemoteApp collection with a new template image.</span></span>
<span data-ttu-id="e9be8-107">Após a conclusão da atualização, os usuários com sessões existentes têm uma hora para se desconectarem antes de serem desconectadas automaticamente. Quando eles entram novamente, eles se conectam à coleção recém atualizada.</span><span class="sxs-lookup"><span data-stu-id="e9be8-107">After the update completes, users with existing sessions have one hour to sign out before they are automatically signed out. When they sign in again, they connect to the newly updated collection.</span></span>
<span data-ttu-id="e9be8-108">Para forçar os usuários a se desconectarem imediatamente assim que a coleção for atualizada, especifique o parâmetro *ForceLogoffWhenUpdateComplete* .</span><span class="sxs-lookup"><span data-stu-id="e9be8-108">To force users to be immediately signed out as soon as the collection is updated, specify the *ForceLogoffWhenUpdateComplete* parameter.</span></span>

## <span data-ttu-id="e9be8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9be8-109">EXAMPLES</span></span>

## <span data-ttu-id="e9be8-110">OS</span><span class="sxs-lookup"><span data-stu-id="e9be8-110">PARAMETERS</span></span>

### <span data-ttu-id="e9be8-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="e9be8-111">-CollectionName</span></span>
<span data-ttu-id="e9be8-112">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e9be8-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="e9be8-113">-ForceLogoffWhenUpdateComplete</span><span class="sxs-lookup"><span data-stu-id="e9be8-113">-ForceLogoffWhenUpdateComplete</span></span>
<span data-ttu-id="e9be8-114">Indica que esse cmdlet assina usuários de suas sessões existentes assim que a atualização é concluída.</span><span class="sxs-lookup"><span data-stu-id="e9be8-114">Indicates that this cmdlet signs users out of their existing sessions as soon as the update is complete.</span></span>
<span data-ttu-id="e9be8-115">Quando os usuários entram novamente, eles se conectam à coleção recém atualizada.</span><span class="sxs-lookup"><span data-stu-id="e9be8-115">When users sign in again, they connect to the newly updated collection.</span></span>

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

### <span data-ttu-id="e9be8-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e9be8-116">-ImageName</span></span>
<span data-ttu-id="e9be8-117">Especifica o nome de uma imagem de modelo do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e9be8-117">Specifies the name of an Azure RemoteApp template image.</span></span>

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

### <span data-ttu-id="e9be8-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e9be8-118">-Profile</span></span>
<span data-ttu-id="e9be8-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e9be8-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9be8-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e9be8-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e9be8-121">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e9be8-121">-SubnetName</span></span>
<span data-ttu-id="e9be8-122">Especifica o nome da sub-rede na qual a coleção será movida.</span><span class="sxs-lookup"><span data-stu-id="e9be8-122">Specifies the name of the subnet into which to move the collection.</span></span>

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

### <span data-ttu-id="e9be8-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e9be8-123">-Confirm</span></span>
<span data-ttu-id="e9be8-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9be8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9be8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9be8-125">-WhatIf</span></span>
<span data-ttu-id="e9be8-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e9be8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9be8-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e9be8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9be8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9be8-128">CommonParameters</span></span>
<span data-ttu-id="e9be8-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9be8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9be8-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9be8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9be8-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9be8-131">INPUTS</span></span>

## <span data-ttu-id="e9be8-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9be8-132">OUTPUTS</span></span>

## <span data-ttu-id="e9be8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9be8-133">NOTES</span></span>

## <span data-ttu-id="e9be8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9be8-134">RELATED LINKS</span></span>

[<span data-ttu-id="e9be8-135">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="e9be8-135">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="e9be8-136">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="e9be8-136">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="e9be8-137">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="e9be8-137">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)


