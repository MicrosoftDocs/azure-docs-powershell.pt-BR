---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 6236AD2C-D54D-4013-9977-AD1E6EAC2F21
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac0283f6c9de9a1cd5f17abd6e27ebb2c8629505
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946433"
---
# <span data-ttu-id="dc00b-101">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="dc00b-101">Send-AzureRemoteAppSessionMessage</span></span>

## <span data-ttu-id="dc00b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc00b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc00b-103">Envia uma mensagem para um usuário.</span><span class="sxs-lookup"><span data-stu-id="dc00b-103">Sends a message to a user.</span></span>

## <span data-ttu-id="dc00b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc00b-104">SYNTAX</span></span>

```
Send-AzureRemoteAppSessionMessage [-CollectionName] <String> [-UserUpn] <String> [-Message] <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dc00b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc00b-105">DESCRIPTION</span></span>
<span data-ttu-id="dc00b-106">O cmdlet **Send-AzureRemoteAppSessionMessage** envia uma mensagem para um usuário que está conectado a uma sessão do RemoteApp do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc00b-106">The **Send-AzureRemoteAppSessionMessage** cmdlet sends a message to a user who is connected to an Azure RemoteApp session.</span></span>

## <span data-ttu-id="dc00b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc00b-107">EXAMPLES</span></span>

### <span data-ttu-id="dc00b-108">Exemplo 1: Enviar uma mensagem para um usuário</span><span class="sxs-lookup"><span data-stu-id="dc00b-108">Example 1: Send a message to a user</span></span>
```
PS C:\> Send-AzureRemoteAppSessionMessage -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com" -Message "The system will be going down for maintenance soon.  Please save your work and close your RemoteApps."
```

<span data-ttu-id="dc00b-109">Esse comando envia uma mensagem para o usuário cujo UPN é PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="dc00b-109">This command sends a message to the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="dc00b-110">OS</span><span class="sxs-lookup"><span data-stu-id="dc00b-110">PARAMETERS</span></span>

### <span data-ttu-id="dc00b-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="dc00b-111">-CollectionName</span></span>
<span data-ttu-id="dc00b-112">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="dc00b-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="dc00b-113">-Mensagem</span><span class="sxs-lookup"><span data-stu-id="dc00b-113">-Message</span></span>
<span data-ttu-id="dc00b-114">Especifica a mensagem a ser enviada.</span><span class="sxs-lookup"><span data-stu-id="dc00b-114">Specifies the message to send.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc00b-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="dc00b-115">-Profile</span></span>
<span data-ttu-id="dc00b-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="dc00b-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dc00b-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="dc00b-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc00b-118">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="dc00b-118">-UserUpn</span></span>
<span data-ttu-id="dc00b-119">Especifica o nome principal do usuário (UPN) de um usuário, por exemplo, PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="dc00b-119">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="dc00b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc00b-120">CommonParameters</span></span>
<span data-ttu-id="dc00b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc00b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc00b-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc00b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc00b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc00b-123">INPUTS</span></span>

## <span data-ttu-id="dc00b-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc00b-124">OUTPUTS</span></span>

## <span data-ttu-id="dc00b-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc00b-125">NOTES</span></span>

## <span data-ttu-id="dc00b-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc00b-126">RELATED LINKS</span></span>

[<span data-ttu-id="dc00b-127">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="dc00b-127">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="dc00b-128">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="dc00b-128">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="dc00b-129">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="dc00b-129">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


