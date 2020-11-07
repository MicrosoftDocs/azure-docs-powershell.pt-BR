---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A4E9C9A7-7FD2-4FD5-AB35-CFF717607B44
online version: ''
schema: 2.0.0
ms.openlocfilehash: c6da222e6cbfe02e181e4a863d8ce8d585215bdd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946147"
---
# <span data-ttu-id="7be23-101">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="7be23-101">Remove-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="7be23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7be23-102">SYNOPSIS</span></span>
<span data-ttu-id="7be23-103">Remove o disco de usuário de um usuário de uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7be23-103">Removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="7be23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7be23-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUserDisk [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7be23-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7be23-105">DESCRIPTION</span></span>
<span data-ttu-id="7be23-106">O cmdlet **Remove-AzureRemoteAppUserDisk** remove o disco de usuário de um usuário de uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7be23-106">The **Remove-AzureRemoteAppUserDisk** cmdlet removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="7be23-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7be23-107">EXAMPLES</span></span>

### <span data-ttu-id="7be23-108">Exemplo 1: remover um disco de usuário</span><span class="sxs-lookup"><span data-stu-id="7be23-108">Example 1: Remove a user disk</span></span>
```
PS C:\> Remove-AzureRemoteAppUserDisk -CollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="7be23-109">Esse comando Remove o disco de usuário de um usuário do Azure Active Directory que tem o UPN PattiFuller@contoso.com da coleção Contoso01.</span><span class="sxs-lookup"><span data-stu-id="7be23-109">This command removes the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01.</span></span>

## <span data-ttu-id="7be23-110">OS</span><span class="sxs-lookup"><span data-stu-id="7be23-110">PARAMETERS</span></span>

### <span data-ttu-id="7be23-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="7be23-111">-CollectionName</span></span>
<span data-ttu-id="7be23-112">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7be23-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="7be23-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7be23-113">-Profile</span></span>
<span data-ttu-id="7be23-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7be23-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7be23-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7be23-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7be23-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="7be23-116">-UserUpn</span></span>
<span data-ttu-id="7be23-117">Especifica o nome principal do usuário (UPN) do usuário para o qual esse cmdlet Remove o disco.</span><span class="sxs-lookup"><span data-stu-id="7be23-117">Specifies the user principal name (UPN) of the user for whom this cmdlet removes the disk.</span></span>

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

### <span data-ttu-id="7be23-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7be23-118">-Confirm</span></span>
<span data-ttu-id="7be23-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7be23-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7be23-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7be23-120">-WhatIf</span></span>
<span data-ttu-id="7be23-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7be23-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7be23-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7be23-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7be23-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be23-123">CommonParameters</span></span>
<span data-ttu-id="7be23-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7be23-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be23-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7be23-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be23-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7be23-126">INPUTS</span></span>

## <span data-ttu-id="7be23-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7be23-127">OUTPUTS</span></span>

## <span data-ttu-id="7be23-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7be23-128">NOTES</span></span>

## <span data-ttu-id="7be23-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7be23-129">RELATED LINKS</span></span>

[<span data-ttu-id="7be23-130">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="7be23-130">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)


