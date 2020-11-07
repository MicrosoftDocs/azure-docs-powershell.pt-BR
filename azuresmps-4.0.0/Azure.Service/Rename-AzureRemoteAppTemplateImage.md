---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 22571840-C27C-4208-A755-EF89E6C4B604
online version: ''
schema: 2.0.0
ms.openlocfilehash: 61cfeab9e02968c7b03e694b9913d4cbe4b3c90a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945474"
---
# <span data-ttu-id="75332-101">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="75332-101">Rename-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="75332-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75332-102">SYNOPSIS</span></span>
<span data-ttu-id="75332-103">Renomeia uma imagem de modelo do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="75332-103">Renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="75332-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75332-104">SYNTAX</span></span>

```
Rename-AzureRemoteAppTemplateImage [-ImageName] <String> [-NewName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="75332-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75332-105">DESCRIPTION</span></span>
<span data-ttu-id="75332-106">O cmdlet **Rename-AzureRemoteAppTemplateImage** renomeia uma imagem de modelo do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="75332-106">The **Rename-AzureRemoteAppTemplateImage** cmdlet renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="75332-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75332-107">EXAMPLES</span></span>

### <span data-ttu-id="75332-108">Exemplo 1: renomear uma imagem de modelo</span><span class="sxs-lookup"><span data-stu-id="75332-108">Example 1: Rename a template image</span></span>
```
PS C:\> Rename-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -NewName "ContosoFinanceApps"
```

<span data-ttu-id="75332-109">Esse comando renomeia a imagem de modelo do Azure RemoteApp chamada ContosoApps para ContosoFinanceApps.</span><span class="sxs-lookup"><span data-stu-id="75332-109">This command renames the Azure RemoteApp template image named ContosoApps to ContosoFinanceApps.</span></span>

## <span data-ttu-id="75332-110">OS</span><span class="sxs-lookup"><span data-stu-id="75332-110">PARAMETERS</span></span>

### <span data-ttu-id="75332-111">-ImageName</span><span class="sxs-lookup"><span data-stu-id="75332-111">-ImageName</span></span>
<span data-ttu-id="75332-112">Especifica o nome de uma imagem de modelo do Azure RemoteApp a ser renomeada.</span><span class="sxs-lookup"><span data-stu-id="75332-112">Specifies the name of an Azure RemoteApp template image to rename.</span></span>

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

### <span data-ttu-id="75332-113">-NewName</span><span class="sxs-lookup"><span data-stu-id="75332-113">-NewName</span></span>
<span data-ttu-id="75332-114">Especifica um novo nome para uma imagem de modelo do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="75332-114">Specifies a new name for an Azure RemoteApp template image.</span></span>

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

### <span data-ttu-id="75332-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="75332-115">-Profile</span></span>
<span data-ttu-id="75332-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="75332-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="75332-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="75332-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="75332-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75332-118">CommonParameters</span></span>
<span data-ttu-id="75332-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75332-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75332-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75332-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75332-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75332-121">INPUTS</span></span>

## <span data-ttu-id="75332-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75332-122">OUTPUTS</span></span>

## <span data-ttu-id="75332-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75332-123">NOTES</span></span>

## <span data-ttu-id="75332-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75332-124">RELATED LINKS</span></span>

[<span data-ttu-id="75332-125">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="75332-125">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="75332-126">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="75332-126">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="75332-127">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="75332-127">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)


