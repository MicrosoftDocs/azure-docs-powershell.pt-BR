---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DBC4A0B8-A34A-47AC-930B-EFE23A95A216
online version: ''
schema: 2.0.0
ms.openlocfilehash: 178349299767eefb1d89c31a0199f53373bd2ae2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945995"
---
# <span data-ttu-id="b6cab-101">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b6cab-101">New-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="b6cab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6cab-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cab-103">Carrega ou importa uma imagem de modelo do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b6cab-103">Uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="b6cab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6cab-104">SYNTAX</span></span>

### <span data-ttu-id="b6cab-105">UploadLocalVhd (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6cab-105">UploadLocalVhd (Default)</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> [-Path] <String> [-Resume]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b6cab-106">AzureVmUpload</span><span class="sxs-lookup"><span data-stu-id="b6cab-106">AzureVmUpload</span></span>
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> -AzureVmImageName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b6cab-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6cab-107">DESCRIPTION</span></span>
<span data-ttu-id="b6cab-108">O cmdlet **New-AzureRemoteAppTemplateImage** carrega ou importa uma imagem de modelo do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b6cab-108">The **New-AzureRemoteAppTemplateImage** cmdlet uploads or imports an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="b6cab-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6cab-109">EXAMPLES</span></span>

### <span data-ttu-id="b6cab-110">Exemplo 1: carregar um arquivo VHD para criar uma imagem de modelo</span><span class="sxs-lookup"><span data-stu-id="b6cab-110">Example 1: Upload a VHD file to create a template image</span></span>
```
PS C:\> New-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -Location "North Europe" -Path "C:\RemoteAppImages\ContosoApps.vhd"
```

<span data-ttu-id="b6cab-111">Esse comando carrega C:\RemoteAppImages\ContosoApps.vhd para criar uma imagem de modelo chamada ContosoApps no centro de dados da Europa norte.</span><span class="sxs-lookup"><span data-stu-id="b6cab-111">This command uploads C:\RemoteAppImages\ContosoApps.vhd to create a template image named ContosoApps in the North Europe data center.</span></span>

## <span data-ttu-id="b6cab-112">OS</span><span class="sxs-lookup"><span data-stu-id="b6cab-112">PARAMETERS</span></span>

### <span data-ttu-id="b6cab-113">-AzureVmImageName</span><span class="sxs-lookup"><span data-stu-id="b6cab-113">-AzureVmImageName</span></span>
<span data-ttu-id="b6cab-114">Especifica o nome de uma máquina virtual do Azure a ser usada como uma imagem de modelo.</span><span class="sxs-lookup"><span data-stu-id="b6cab-114">Specifies the name of an Azure virtual machine to use as a template image.</span></span>

```yaml
Type: String
Parameter Sets: AzureVmUpload
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cab-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b6cab-115">-ImageName</span></span>
<span data-ttu-id="b6cab-116">Especifica o nome de uma imagem de modelo do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b6cab-116">Specifies the name of an Azure RemoteApp template image.</span></span>

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

### <span data-ttu-id="b6cab-117">-Local</span><span class="sxs-lookup"><span data-stu-id="b6cab-117">-Location</span></span>
<span data-ttu-id="b6cab-118">Especifica a região do Azure da imagem do modelo.</span><span class="sxs-lookup"><span data-stu-id="b6cab-118">Specifies the Azure region of the template image.</span></span>

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

### <span data-ttu-id="b6cab-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="b6cab-119">-Path</span></span>
<span data-ttu-id="b6cab-120">Especifica o caminho do arquivo da imagem do modelo.</span><span class="sxs-lookup"><span data-stu-id="b6cab-120">Specifies the file path of the template image.</span></span>

```yaml
Type: String
Parameter Sets: UploadLocalVhd
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cab-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b6cab-121">-Profile</span></span>
<span data-ttu-id="b6cab-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b6cab-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6cab-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b6cab-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6cab-124">-Retomar</span><span class="sxs-lookup"><span data-stu-id="b6cab-124">-Resume</span></span>
<span data-ttu-id="b6cab-125">Indica que esse cmdlet retomará se o upload de uma imagem de modelo for interrompido.</span><span class="sxs-lookup"><span data-stu-id="b6cab-125">Indicates that this cmdlet resumes if the upload of a template image is interrupted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UploadLocalVhd
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6cab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cab-126">CommonParameters</span></span>
<span data-ttu-id="b6cab-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6cab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cab-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6cab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cab-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6cab-129">INPUTS</span></span>

## <span data-ttu-id="b6cab-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6cab-130">OUTPUTS</span></span>

## <span data-ttu-id="b6cab-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6cab-131">NOTES</span></span>

## <span data-ttu-id="b6cab-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6cab-132">RELATED LINKS</span></span>

[<span data-ttu-id="b6cab-133">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b6cab-133">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="b6cab-134">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b6cab-134">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="b6cab-135">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b6cab-135">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


