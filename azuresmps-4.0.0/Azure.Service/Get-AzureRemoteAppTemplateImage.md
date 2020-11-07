---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946579"
---
# <span data-ttu-id="bde95-101">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="bde95-101">Get-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="bde95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bde95-102">SYNOPSIS</span></span>
<span data-ttu-id="bde95-103">Recupera informações sobre as imagens de modelo do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="bde95-103">Retrieves information about Azure RemoteApp template images.</span></span>

## <span data-ttu-id="bde95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bde95-104">SYNTAX</span></span>

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bde95-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bde95-105">DESCRIPTION</span></span>
<span data-ttu-id="bde95-106">O cmdlet **Get-AzureRemoteAppTemplateImage** recupera informações sobre as imagens de modelo do Azure RemoteApp no Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bde95-106">The **Get-AzureRemoteAppTemplateImage** cmdlet retrieves information about Azure RemoteApp template images in Microsoft Azure.</span></span>
<span data-ttu-id="bde95-107">Esse cmdlet retorna um objeto que contém informações sobre uma imagem de modelo especificada.</span><span class="sxs-lookup"><span data-stu-id="bde95-107">This cmdlet returns an object containing information about a specified template image.</span></span>
<span data-ttu-id="bde95-108">Se nenhuma imagem de modelo for especificada, ela recuperará informações sobre todas as imagens de modelo na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="bde95-108">If no template image is specified, it retrieves information about all the template images in the current subscription.</span></span>

## <span data-ttu-id="bde95-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bde95-109">EXAMPLES</span></span>

### <span data-ttu-id="bde95-110">Exemplo 1: obter uma lista de todas as imagens de modelo</span><span class="sxs-lookup"><span data-stu-id="bde95-110">Example 1: Get a list of all template images</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

<span data-ttu-id="bde95-111">Esse comando retorna a lista de todas as imagens de modelo.</span><span class="sxs-lookup"><span data-stu-id="bde95-111">This command returns the list of all template images.</span></span>

### <span data-ttu-id="bde95-112">Exemplo 2: recuperar informações sobre uma imagem de modelo especificada</span><span class="sxs-lookup"><span data-stu-id="bde95-112">Example 2: Retrieve information about a specified template image</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="bde95-113">Esse comando recupera informações sobre a imagem de modelo chamada ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="bde95-113">This command retrieves information about the template image named ContosoApps.</span></span>

## <span data-ttu-id="bde95-114">OS</span><span class="sxs-lookup"><span data-stu-id="bde95-114">PARAMETERS</span></span>

### <span data-ttu-id="bde95-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="bde95-115">-ImageName</span></span>
<span data-ttu-id="bde95-116">Especifica o nome de uma imagem de modelo do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="bde95-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="bde95-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bde95-117">-Profile</span></span>
<span data-ttu-id="bde95-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="bde95-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bde95-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="bde95-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bde95-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde95-120">CommonParameters</span></span>
<span data-ttu-id="bde95-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bde95-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde95-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bde95-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde95-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bde95-123">INPUTS</span></span>

## <span data-ttu-id="bde95-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bde95-124">OUTPUTS</span></span>

## <span data-ttu-id="bde95-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bde95-125">NOTES</span></span>

## <span data-ttu-id="bde95-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bde95-126">RELATED LINKS</span></span>

[<span data-ttu-id="bde95-127">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="bde95-127">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="bde95-128">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="bde95-128">Get-AzureRemoteAppStartMenuProgram</span></span>](./Get-AzureRemoteAppStartMenuProgram.md)


