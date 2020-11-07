---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-help.xml
ms.assetid: 02F429EA-FE9A-427F-86B5-C9C4275FD3EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 289cc21b6edd2a841b8121672d838aaa056db4f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945698"
---
# <span data-ttu-id="22ab8-101">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="22ab8-101">Copy-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="22ab8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="22ab8-103">Copia o disco de usuário de um usuário de uma coleção do Azure RemoteApp para outra.</span><span class="sxs-lookup"><span data-stu-id="22ab8-103">Copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="22ab8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22ab8-104">SYNTAX</span></span>

```
Copy-AzureRemoteAppUserDisk [-SourceCollectionName] <String> [-DestinationCollectionName] <String>
 [-UserUpn] <String> [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="22ab8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="22ab8-106">O cmdlet **Copy-AzureRemoteAppUserDisk** copia o disco de usuário de um usuário de uma coleção do Azure RemoteApp para outra.</span><span class="sxs-lookup"><span data-stu-id="22ab8-106">The **Copy-AzureRemoteAppUserDisk** cmdlet copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="22ab8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22ab8-107">EXAMPLES</span></span>

### <span data-ttu-id="22ab8-108">Exemplo 1: copiar um disco de usuário</span><span class="sxs-lookup"><span data-stu-id="22ab8-108">Example 1: Copy a user disk</span></span>
```
PS C:\> Copy-AzureRemoteAppUserDisk -DestinationCollectionName "Contoso02" -SourceCollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com" -OverwriteExistingUserDisk
```

<span data-ttu-id="22ab8-109">Esse comando copia o disco do usuário de um usuário do Azure Active Directory que tem o UPN PattiFuller@contoso.com da coleção Contoso01 para a coleção Contoso02.</span><span class="sxs-lookup"><span data-stu-id="22ab8-109">This command copies the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01 to the collection Contoso02.</span></span>
<span data-ttu-id="22ab8-110">Se um disco do usuário PattiFuller@contoso.com já existir no Contoso02, esse comando o substituirá.</span><span class="sxs-lookup"><span data-stu-id="22ab8-110">If a user disk for PattiFuller@contoso.com already exists on Contoso02, this command overwrites it.</span></span>

## <span data-ttu-id="22ab8-111">OS</span><span class="sxs-lookup"><span data-stu-id="22ab8-111">PARAMETERS</span></span>

### <span data-ttu-id="22ab8-112">-DestinationCollectionName</span><span class="sxs-lookup"><span data-stu-id="22ab8-112">-DestinationCollectionName</span></span>
<span data-ttu-id="22ab8-113">Especifica o nome da coleção de destino do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="22ab8-113">Specifies the name of the destination Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="22ab8-114">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="22ab8-114">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="22ab8-115">Indica que esse cmdlet substitui um disco do usuário existente.</span><span class="sxs-lookup"><span data-stu-id="22ab8-115">Indicates that this cmdlet overwrites an existing user disk.</span></span>

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

### <span data-ttu-id="22ab8-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="22ab8-116">-Profile</span></span>
<span data-ttu-id="22ab8-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="22ab8-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="22ab8-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="22ab8-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="22ab8-119">-SourceCollectionName</span><span class="sxs-lookup"><span data-stu-id="22ab8-119">-SourceCollectionName</span></span>
<span data-ttu-id="22ab8-120">Especifica o nome da coleção do Azure RemoteApp de origem.</span><span class="sxs-lookup"><span data-stu-id="22ab8-120">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="22ab8-121">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="22ab8-121">-UserUpn</span></span>
<span data-ttu-id="22ab8-122">Especifica o nome principal do usuário (UPN) do usuário para o qual esse cmdlet copia o disco.</span><span class="sxs-lookup"><span data-stu-id="22ab8-122">Specifies the user principal name (UPN) of the user for whom this cmdlet copies the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ab8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ab8-123">CommonParameters</span></span>
<span data-ttu-id="22ab8-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ab8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ab8-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22ab8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ab8-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22ab8-126">INPUTS</span></span>

## <span data-ttu-id="22ab8-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22ab8-127">OUTPUTS</span></span>

## <span data-ttu-id="22ab8-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22ab8-128">NOTES</span></span>

## <span data-ttu-id="22ab8-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22ab8-129">RELATED LINKS</span></span>

[<span data-ttu-id="22ab8-130">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="22ab8-130">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


