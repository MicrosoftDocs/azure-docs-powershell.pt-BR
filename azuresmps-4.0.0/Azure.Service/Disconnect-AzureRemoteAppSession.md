---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 514C33F8-F0B8-4F37-AB2D-BB54DD754931
online version: ''
schema: 2.0.0
ms.openlocfilehash: c256ce8ba720eb08ffec2ab56ecca40ab74f4948
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945686"
---
# <span data-ttu-id="52d07-101">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="52d07-101">Disconnect-AzureRemoteAppSession</span></span>

## <span data-ttu-id="52d07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52d07-102">SYNOPSIS</span></span>
<span data-ttu-id="52d07-103">Desconecta uma sessão do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="52d07-103">Disconnects an Azure RemoteApp session.</span></span>

## <span data-ttu-id="52d07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52d07-104">SYNTAX</span></span>

```
Disconnect-AzureRemoteAppSession [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="52d07-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52d07-105">DESCRIPTION</span></span>
<span data-ttu-id="52d07-106">O cmdlet **Disconnect-AzureRemoteAppSession** desconecta a sessão do Azure RemoteApp de um usuário.</span><span class="sxs-lookup"><span data-stu-id="52d07-106">The **Disconnect-AzureRemoteAppSession** cmdlet disconnects a user's Azure RemoteApp session.</span></span>
<span data-ttu-id="52d07-107">O cliente do usuário se desconecta da sessão do Azure RemoteApp, mas os programas do usuário continuam sendo executados.</span><span class="sxs-lookup"><span data-stu-id="52d07-107">The user's client disconnects from their Azure RemoteApp session, but the user's programs continue to run.</span></span>

## <span data-ttu-id="52d07-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52d07-108">EXAMPLES</span></span>

### <span data-ttu-id="52d07-109">Exemplo 1: desconectar a sessão de um usuário</span><span class="sxs-lookup"><span data-stu-id="52d07-109">Example 1: Disconnect a user's session</span></span>
```
PS C:\> Disconnect-AzureRemoteAppSession -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="52d07-110">Esse comando desconecta a sessão do Azure RemoteApp na coleção ContosoApps para o usuário cujo UPN é PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="52d07-110">This command disconnects the Azure RemoteApp session in the ContosoApps collection for the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="52d07-111">OS</span><span class="sxs-lookup"><span data-stu-id="52d07-111">PARAMETERS</span></span>

### <span data-ttu-id="52d07-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="52d07-112">-CollectionName</span></span>
<span data-ttu-id="52d07-113">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="52d07-113">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="52d07-114">-Perfil</span><span class="sxs-lookup"><span data-stu-id="52d07-114">-Profile</span></span>
<span data-ttu-id="52d07-115">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="52d07-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52d07-116">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="52d07-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52d07-117">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="52d07-117">-UserUpn</span></span>
<span data-ttu-id="52d07-118">Especifica o nome principal do usuário (UPN) de um usuário, por exemplo PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="52d07-118">Specifies the User Principal Name (UPN) of a user, for example PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="52d07-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d07-119">CommonParameters</span></span>
<span data-ttu-id="52d07-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52d07-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d07-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d07-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d07-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52d07-122">INPUTS</span></span>

## <span data-ttu-id="52d07-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52d07-123">OUTPUTS</span></span>

## <span data-ttu-id="52d07-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52d07-124">NOTES</span></span>

## <span data-ttu-id="52d07-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52d07-125">RELATED LINKS</span></span>

[<span data-ttu-id="52d07-126">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="52d07-126">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="52d07-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="52d07-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="52d07-128">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="52d07-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


