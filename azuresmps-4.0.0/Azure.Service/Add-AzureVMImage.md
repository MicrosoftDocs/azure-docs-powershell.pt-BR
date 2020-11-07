---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DECCEE-86C8-4662-9ED0-D1BDB4E687C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68efd1c750646abffa90eb8318d0df189a4c9eb9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945715"
---
# <span data-ttu-id="9b46e-101">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="9b46e-101">Add-AzureVMImage</span></span>

## <span data-ttu-id="9b46e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b46e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b46e-103">Adiciona uma nova imagem do sistema operacional ou uma nova imagem de máquina virtual ao repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="9b46e-103">Adds a new operating system image or a new virtual machine image to the image repository.</span></span>

## <span data-ttu-id="9b46e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b46e-104">SYNTAX</span></span>

### <span data-ttu-id="9b46e-105">OSImage (padrão)</span><span class="sxs-lookup"><span data-stu-id="9b46e-105">OSImage (Default)</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-MediaLocation] <String> [-OS] <String> [[-Label] <String>]
 [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>]
 [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>] [[-SmallIconName] <String>]
 [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9b46e-106">VMImage</span><span class="sxs-lookup"><span data-stu-id="9b46e-106">VMImage</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-OS] <String>]
 [[-Label] <String>] [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>]
 [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9b46e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b46e-107">DESCRIPTION</span></span>
<span data-ttu-id="9b46e-108">O cmdlet **Add-AzureVMImage** adiciona uma nova imagem do sistema operacional ou uma nova imagem de máquina virtual ao repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="9b46e-108">The **Add-AzureVMImage** cmdlet adds a new operating system image or a new virtual machine image to the image repository.</span></span>
<span data-ttu-id="9b46e-109">A imagem é uma imagem do sistema operacional generalizada, usando Sysprep para Windows ou para Linux, usando a ferramenta apropriada para a distribuição.</span><span class="sxs-lookup"><span data-stu-id="9b46e-109">The image is a generalized operating system image, using either Sysprep for Windows or, for Linux, using the appropriate tool for the distribution.</span></span>

## <span data-ttu-id="9b46e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b46e-110">EXAMPLES</span></span>

### <span data-ttu-id="9b46e-111">Exemplo 1: adicionar uma imagem do sistema operacional ao repositório</span><span class="sxs-lookup"><span data-stu-id="9b46e-111">Example 1: Add an operating system image to the repository</span></span>
```
PS C:\> $S = New-AzureVMImageDiskConfigSet
PS C:\> Set-AzureVMImageOSDiskConfig -DiskConfig $S -HostCaching ReadWrite -OSState "Generalized" -OS "Windows" -MediaLink $Link
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test1" -HostCaching ReadWrite -Lun 0 -MediaLink $Link1
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4" -HostCaching ReadWrite -Lun 0 -MediaLink $Link
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4"
PS C:\> $IMGName = "TestCREATEvmimage2";
PS C:\> Add-AzureVMImage -ImageName $IMGName -Label "Test1" -Description "Test1" -DiskConfig $S -Eula "http://www.contoso.com" -ImageFamily Windows -PublishedDate (Get-Date) -PrivacyUri "http://www.test.com" -RecommendedVMSize Small -IconName "Icon01" -SmallIconName "SmallIcon01" -ShowInGui
```

<span data-ttu-id="9b46e-112">Este exemplo adiciona uma imagem do sistema operacional ao repositório.</span><span class="sxs-lookup"><span data-stu-id="9b46e-112">This example adds an operating system image to the repository.</span></span>

## <span data-ttu-id="9b46e-113">OS</span><span class="sxs-lookup"><span data-stu-id="9b46e-113">PARAMETERS</span></span>

### <span data-ttu-id="9b46e-114">-Descrição</span><span class="sxs-lookup"><span data-stu-id="9b46e-114">-Description</span></span>
<span data-ttu-id="9b46e-115">Especifica a descrição da imagem do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9b46e-115">Specifies the description of the operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="9b46e-116">-DiskConfig</span></span>
<span data-ttu-id="9b46e-117">Especifica a configuração de disco do sistema operacional para a imagem da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b46e-117">Specifies the operating system disk configuration for the virtual machine image.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: VMImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-118">-EULA</span><span class="sxs-lookup"><span data-stu-id="9b46e-118">-Eula</span></span>
<span data-ttu-id="9b46e-119">Especifica o contrato de licença de usuário final.</span><span class="sxs-lookup"><span data-stu-id="9b46e-119">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="9b46e-120">É recomendável usar uma URL para esse valor.</span><span class="sxs-lookup"><span data-stu-id="9b46e-120">It is recommended that you use an URL for this value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-121">-Iconname</span><span class="sxs-lookup"><span data-stu-id="9b46e-121">-IconName</span></span>
<span data-ttu-id="9b46e-122">Especifica o nome do ícone que é usado quando a imagem é adicionada ao repositório.</span><span class="sxs-lookup"><span data-stu-id="9b46e-122">Specifies the name of the icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-123">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="9b46e-123">-ImageFamily</span></span>
<span data-ttu-id="9b46e-124">Especifica um valor que é usado para agrupar imagens do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9b46e-124">Specifies a value that is used to group operating system images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-125">-ImageName</span><span class="sxs-lookup"><span data-stu-id="9b46e-125">-ImageName</span></span>
<span data-ttu-id="9b46e-126">Especifica o nome da imagem que está sendo adicionada ao repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="9b46e-126">Specifies the name of the image being added to the image repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9b46e-127">-InformationAction</span></span>
<span data-ttu-id="9b46e-128">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="9b46e-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9b46e-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9b46e-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b46e-130">Contínuo</span><span class="sxs-lookup"><span data-stu-id="9b46e-130">Continue</span></span>
- <span data-ttu-id="9b46e-131">Ignorar</span><span class="sxs-lookup"><span data-stu-id="9b46e-131">Ignore</span></span>
- <span data-ttu-id="9b46e-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="9b46e-132">Inquire</span></span>
- <span data-ttu-id="9b46e-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9b46e-133">SilentlyContinue</span></span>
- <span data-ttu-id="9b46e-134">Finaliza</span><span class="sxs-lookup"><span data-stu-id="9b46e-134">Stop</span></span>
- <span data-ttu-id="9b46e-135">Suspensão</span><span class="sxs-lookup"><span data-stu-id="9b46e-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9b46e-136">-InformationVariable</span></span>
<span data-ttu-id="9b46e-137">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="9b46e-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-138">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="9b46e-138">-Label</span></span>
<span data-ttu-id="9b46e-139">Especifica um rótulo para dar a imagem.</span><span class="sxs-lookup"><span data-stu-id="9b46e-139">Specifies a label to give the image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-140">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="9b46e-140">-MediaLocation</span></span>
<span data-ttu-id="9b46e-141">Especifica o local da página blob físico em que a imagem reside.</span><span class="sxs-lookup"><span data-stu-id="9b46e-141">Specifies the location of the physical blob page where the image resides.</span></span>
<span data-ttu-id="9b46e-142">Este é um link para uma página blob no armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9b46e-142">This is a link to a blob page in the current subscription's storage.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-143">-OS</span><span class="sxs-lookup"><span data-stu-id="9b46e-143">-OS</span></span>
<span data-ttu-id="9b46e-144">Especifica a versão do sistema operacional da imagem.</span><span class="sxs-lookup"><span data-stu-id="9b46e-144">Specifies the operating system version of the image.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: VMImage
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-145">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="9b46e-145">-PrivacyUri</span></span>
<span data-ttu-id="9b46e-146">Especifica a URL que aponta para um documento que contém a política de privacidade relacionada à imagem do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9b46e-146">Specifies the URL that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-147">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9b46e-147">-Profile</span></span>
<span data-ttu-id="9b46e-148">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9b46e-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b46e-149">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9b46e-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9b46e-150">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="9b46e-150">-PublishedDate</span></span>
<span data-ttu-id="9b46e-151">Especifica a data em que a imagem do sistema operacional foi adicionada ao repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="9b46e-151">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-152">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="9b46e-152">-RecommendedVMSize</span></span>
<span data-ttu-id="9b46e-153">Especifica o tamanho a ser usado para a máquina virtual que é criada a partir da imagem do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9b46e-153">Specifies the size to use for the virtual machine that is created from the operating system image.</span></span>

<span data-ttu-id="9b46e-154">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9b46e-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b46e-155">Port</span><span class="sxs-lookup"><span data-stu-id="9b46e-155">Medium</span></span>
- <span data-ttu-id="9b46e-156">Muita</span><span class="sxs-lookup"><span data-stu-id="9b46e-156">Large</span></span>
- <span data-ttu-id="9b46e-157">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="9b46e-157">ExtraLarge</span></span>
- <span data-ttu-id="9b46e-158">A5</span><span class="sxs-lookup"><span data-stu-id="9b46e-158">A5</span></span>
- <span data-ttu-id="9b46e-159">A6</span><span class="sxs-lookup"><span data-stu-id="9b46e-159">A6</span></span>
- <span data-ttu-id="9b46e-160">A7</span><span class="sxs-lookup"><span data-stu-id="9b46e-160">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-161">-ShowInGui</span><span class="sxs-lookup"><span data-stu-id="9b46e-161">-ShowInGui</span></span>
<span data-ttu-id="9b46e-162">Indica que esse cmdlet mostra a imagem na GUI.</span><span class="sxs-lookup"><span data-stu-id="9b46e-162">Indicates that this cmdlet shows the image in the GUI.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-163">-SmallIconname</span><span class="sxs-lookup"><span data-stu-id="9b46e-163">-SmallIconName</span></span>
<span data-ttu-id="9b46e-164">Especifica o nome do pequeno ícone que é usado quando a imagem é adicionada ao repositório.</span><span class="sxs-lookup"><span data-stu-id="9b46e-164">Specifies the name of the small icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b46e-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b46e-165">CommonParameters</span></span>
<span data-ttu-id="9b46e-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b46e-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b46e-167">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b46e-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b46e-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b46e-168">INPUTS</span></span>

## <span data-ttu-id="9b46e-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b46e-169">OUTPUTS</span></span>

### <span data-ttu-id="9b46e-170">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="9b46e-170">OSImageContext</span></span>

## <span data-ttu-id="9b46e-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b46e-171">NOTES</span></span>

## <span data-ttu-id="9b46e-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b46e-172">RELATED LINKS</span></span>

[<span data-ttu-id="9b46e-173">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="9b46e-173">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="9b46e-174">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="9b46e-174">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="9b46e-175">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="9b46e-175">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="9b46e-176">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="9b46e-176">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


