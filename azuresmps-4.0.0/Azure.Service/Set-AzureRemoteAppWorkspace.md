---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946051"
---
# <span data-ttu-id="81db2-101">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="81db2-101">Set-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="81db2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81db2-102">SYNOPSIS</span></span>
<span data-ttu-id="81db2-103">Define as propriedades de um espaço de trabalho do RemoteApp do Azure.</span><span class="sxs-lookup"><span data-stu-id="81db2-103">Sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="81db2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81db2-104">SYNTAX</span></span>

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="81db2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81db2-105">DESCRIPTION</span></span>
<span data-ttu-id="81db2-106">O cmdlet **set-AzureRemoteAppWorkspace** define as propriedades de um espaço de trabalho do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="81db2-106">The **Set-AzureRemoteAppWorkspace** cmdlet sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="81db2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81db2-107">EXAMPLES</span></span>

### <span data-ttu-id="81db2-108">Exemplo 1: definir o nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="81db2-108">Example 1: Set the workspace name</span></span>
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

<span data-ttu-id="81db2-109">Esse comando define o nome do espaço de trabalho do RemoteApp do Azure para aplicativos de trabalho da contoso.</span><span class="sxs-lookup"><span data-stu-id="81db2-109">This command sets the Azure RemoteApp workspace name to Contoso Work Applications.</span></span>

## <span data-ttu-id="81db2-110">OS</span><span class="sxs-lookup"><span data-stu-id="81db2-110">PARAMETERS</span></span>

### <span data-ttu-id="81db2-111">-Perfil</span><span class="sxs-lookup"><span data-stu-id="81db2-111">-Profile</span></span>
<span data-ttu-id="81db2-112">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="81db2-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="81db2-113">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="81db2-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="81db2-114">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="81db2-114">-WorkspaceName</span></span>
<span data-ttu-id="81db2-115">Especifica o nome do espaço de trabalho do RemoteApp do Azure.</span><span class="sxs-lookup"><span data-stu-id="81db2-115">Specifies the name of the Azure RemoteApp workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81db2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81db2-116">CommonParameters</span></span>
<span data-ttu-id="81db2-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81db2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81db2-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81db2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81db2-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81db2-119">INPUTS</span></span>

## <span data-ttu-id="81db2-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81db2-120">OUTPUTS</span></span>

## <span data-ttu-id="81db2-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81db2-121">NOTES</span></span>
* <span data-ttu-id="81db2-122">Todas as coleções do RemoteApp do Azure para uma assinatura especificada existem dentro de um espaço de trabalho compartilhado.</span><span class="sxs-lookup"><span data-stu-id="81db2-122">All Azure RemoteApp collections for a specified subscription exist within a shared workspace.</span></span>

## <span data-ttu-id="81db2-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81db2-123">RELATED LINKS</span></span>

[<span data-ttu-id="81db2-124">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="81db2-124">Get-AzureRemoteAppWorkspace</span></span>](./Get-AzureRemoteAppWorkspace.md)


