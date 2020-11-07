---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 035B294E-6A1B-41E9-ACFF-D66F9C1A0B11
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9218862bb1e61abe548a94ed5297a6ce69237d54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945619"
---
# <span data-ttu-id="2c501-101">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="2c501-101">Get-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="2c501-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c501-102">SYNOPSIS</span></span>
<span data-ttu-id="2c501-103">Recupera informações sobre um espaço de trabalho do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2c501-103">Retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="2c501-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c501-104">SYNTAX</span></span>

```
Get-AzureRemoteAppWorkspace [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2c501-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c501-105">DESCRIPTION</span></span>
<span data-ttu-id="2c501-106">O cmdlet **Get-AzureRemoteAppWorkspace** recupera informações sobre um espaço de trabalho do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2c501-106">The **Get-AzureRemoteAppWorkspace** cmdlet retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="2c501-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c501-107">EXAMPLES</span></span>

### <span data-ttu-id="2c501-108">Exemplo 1: recuperar informações sobre um espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="2c501-108">Example 1: Retrieve information about a workspace</span></span>
```
PS C:\> Get-AzureRemoteAppWorkspace
ClientUrl                               EndUserFeedName
---------                               ---------------
https://www.remoteapp.windowsazure.com/ Contoso Work Applications
```

<span data-ttu-id="2c501-109">Esse comando recupera informações sobre o espaço de trabalho do RemoteApp do Azure.</span><span class="sxs-lookup"><span data-stu-id="2c501-109">This command retrieves information about the Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="2c501-110">OS</span><span class="sxs-lookup"><span data-stu-id="2c501-110">PARAMETERS</span></span>

### <span data-ttu-id="2c501-111">-Perfil</span><span class="sxs-lookup"><span data-stu-id="2c501-111">-Profile</span></span>
<span data-ttu-id="2c501-112">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="2c501-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2c501-113">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="2c501-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2c501-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c501-114">CommonParameters</span></span>
<span data-ttu-id="2c501-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c501-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c501-116">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c501-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c501-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c501-117">INPUTS</span></span>

## <span data-ttu-id="2c501-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c501-118">OUTPUTS</span></span>

## <span data-ttu-id="2c501-119">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c501-119">NOTES</span></span>

## <span data-ttu-id="2c501-120">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c501-120">RELATED LINKS</span></span>

[<span data-ttu-id="2c501-121">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="2c501-121">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)


