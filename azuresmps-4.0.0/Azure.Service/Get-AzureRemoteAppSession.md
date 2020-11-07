---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946577"
---
# <span data-ttu-id="928df-101">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="928df-101">Get-AzureRemoteAppSession</span></span>

## <span data-ttu-id="928df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="928df-102">SYNOPSIS</span></span>
<span data-ttu-id="928df-103">Lista todas as sessões ativas e desconectadas do RemoteApp do Azure para uma coleção.</span><span class="sxs-lookup"><span data-stu-id="928df-103">Lists all active and disconnected Azure RemoteApp sessions for a collection.</span></span>

## <span data-ttu-id="928df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="928df-104">SYNTAX</span></span>

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="928df-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="928df-105">DESCRIPTION</span></span>
<span data-ttu-id="928df-106">O cmdlet **Get-AzureRemoteAppSession** lista todas as sessões do Azure RemoteApp ativas e desconectadas para uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="928df-106">The **Get-AzureRemoteAppSession** cmdlet lists all active and disconnected Azure RemoteApp sessions for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="928df-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="928df-107">EXAMPLES</span></span>

### <span data-ttu-id="928df-108">Exemplo 1: listar todas as sessões em uma coleção</span><span class="sxs-lookup"><span data-stu-id="928df-108">Example 1: List all the sessions in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

<span data-ttu-id="928df-109">Esse comando lista todas as sessões do Azure RemoteApp Collection chamadas ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="928df-109">This command lists all sessions in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="928df-110">OS</span><span class="sxs-lookup"><span data-stu-id="928df-110">PARAMETERS</span></span>

### <span data-ttu-id="928df-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="928df-111">-CollectionName</span></span>
<span data-ttu-id="928df-112">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="928df-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="928df-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="928df-113">-Profile</span></span>
<span data-ttu-id="928df-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="928df-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="928df-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="928df-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="928df-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="928df-116">-UserUpn</span></span>
<span data-ttu-id="928df-117">Especifica o nome de usuário principal (UPN) de um usuário para o qual obter sessões do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="928df-117">Specifies the user Principal Name (UPN) of a user for which to get Azure RemoteApp sessions.</span></span>
<span data-ttu-id="928df-118">Por exemplo, o UPN pode estar no seguinte formato: PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="928df-118">For example, the UPN can be in the following format: PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="928df-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928df-119">CommonParameters</span></span>
<span data-ttu-id="928df-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="928df-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928df-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="928df-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928df-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="928df-122">INPUTS</span></span>

## <span data-ttu-id="928df-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="928df-123">OUTPUTS</span></span>

## <span data-ttu-id="928df-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="928df-124">NOTES</span></span>

## <span data-ttu-id="928df-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="928df-125">RELATED LINKS</span></span>

[<span data-ttu-id="928df-126">Desconectar-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="928df-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="928df-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="928df-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="928df-128">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="928df-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


