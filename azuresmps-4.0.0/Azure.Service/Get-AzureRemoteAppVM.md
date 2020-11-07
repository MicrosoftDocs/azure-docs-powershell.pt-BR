---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946571"
---
# <span data-ttu-id="e80a5-101">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="e80a5-101">Get-AzureRemoteAppVM</span></span>

## <span data-ttu-id="e80a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e80a5-102">SYNOPSIS</span></span>
<span data-ttu-id="e80a5-103">Obtém as máquinas virtuais em uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e80a5-103">Gets the virtual machines in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="e80a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e80a5-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e80a5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e80a5-105">DESCRIPTION</span></span>
<span data-ttu-id="e80a5-106">O cmdlet **Get-AzureRemoteAppVM** Obtém as máquinas virtuais criadas em uma coleção do Azure RemoteApp para hospedagem de sessão.</span><span class="sxs-lookup"><span data-stu-id="e80a5-106">The **Get-AzureRemoteAppVM** cmdlet gets the virtual machines created under an Azure RemoteApp collection for session hosting.</span></span>

## <span data-ttu-id="e80a5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e80a5-107">EXAMPLES</span></span>

### <span data-ttu-id="e80a5-108">Exemplo 1: exibir as máquinas virtuais em uma coleção</span><span class="sxs-lookup"><span data-stu-id="e80a5-108">Example 1: Display the virtual machines in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

<span data-ttu-id="e80a5-109">Esse comando exibe as máquinas virtuais usadas para hospedagem de sessão em uma coleção do Azure RemoteApp chamada contoso.</span><span class="sxs-lookup"><span data-stu-id="e80a5-109">This command displays the virtual machines used for session hosting in an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="e80a5-110">OS</span><span class="sxs-lookup"><span data-stu-id="e80a5-110">PARAMETERS</span></span>

### <span data-ttu-id="e80a5-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="e80a5-111">-CollectionName</span></span>
<span data-ttu-id="e80a5-112">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e80a5-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e80a5-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e80a5-113">-Profile</span></span>
<span data-ttu-id="e80a5-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e80a5-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e80a5-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e80a5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e80a5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e80a5-116">CommonParameters</span></span>
<span data-ttu-id="e80a5-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e80a5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e80a5-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e80a5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e80a5-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e80a5-119">INPUTS</span></span>

## <span data-ttu-id="e80a5-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e80a5-120">OUTPUTS</span></span>

## <span data-ttu-id="e80a5-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e80a5-121">NOTES</span></span>

## <span data-ttu-id="e80a5-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e80a5-122">RELATED LINKS</span></span>

[<span data-ttu-id="e80a5-123">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="e80a5-123">Restart-AzureRemoteAppVM</span></span>](./Restart-AzureRemoteAppVM.md)


