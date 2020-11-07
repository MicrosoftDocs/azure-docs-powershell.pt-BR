---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946583"
---
# <span data-ttu-id="9e657-101">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="9e657-101">Update-AzureVMImage</span></span>

## <span data-ttu-id="9e657-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e657-102">SYNOPSIS</span></span>
<span data-ttu-id="9e657-103">Atualiza o rótulo de uma imagem do sistema operacional no repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="9e657-103">Updates the label of an operating system image in the image repository.</span></span>

## <span data-ttu-id="9e657-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e657-104">SYNTAX</span></span>

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9e657-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e657-105">DESCRIPTION</span></span>
<span data-ttu-id="9e657-106">O cmdlet **Update-AzureVMImage** atualiza o rótulo em uma imagem do sistema operacional no repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="9e657-106">The **Update-AzureVMImage** cmdlet updates the label on an operating system image in the image repository.</span></span>
<span data-ttu-id="9e657-107">Ele retorna um objeto Image com informações sobre a imagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="9e657-107">It returns an image object with information about the updated image.</span></span>

## <span data-ttu-id="9e657-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e657-108">EXAMPLES</span></span>

### <span data-ttu-id="9e657-109">Exemplo 1: atualizar uma imagem alterando o rótulo da imagem</span><span class="sxs-lookup"><span data-stu-id="9e657-109">Example 1: Update an image by changing the image label</span></span>
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

<span data-ttu-id="9e657-110">Esse comando atualiza a imagem chamada Windows-Server-2008-SP2 alterando o rótulo de imagem para DoNotUse.</span><span class="sxs-lookup"><span data-stu-id="9e657-110">This command updates the image named Windows-Server-2008-SP2 by changing the image label to DoNotUse.</span></span>

### <span data-ttu-id="9e657-111">Exemplo 2: obter todos os sistemas operacionais por rótulo e atualizar a etiqueta</span><span class="sxs-lookup"><span data-stu-id="9e657-111">Example 2: Get all operating systems by label and then update the label</span></span>
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

<span data-ttu-id="9e657-112">Esse comando obtém todas as imagens do sistema operacional rotuladas DoNotUse e altera o rótulo para atualizado.</span><span class="sxs-lookup"><span data-stu-id="9e657-112">This command gets all the operating system images labeled DoNotUse and changes the label to Updated.</span></span>

## <span data-ttu-id="9e657-113">OS</span><span class="sxs-lookup"><span data-stu-id="9e657-113">PARAMETERS</span></span>

### <span data-ttu-id="9e657-114">-Descrição</span><span class="sxs-lookup"><span data-stu-id="9e657-114">-Description</span></span>
<span data-ttu-id="9e657-115">Especifica a descrição da imagem do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9e657-115">Specifies the description of the operating system image.</span></span>

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

### <span data-ttu-id="9e657-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="9e657-116">-DiskConfig</span></span>
<span data-ttu-id="9e657-117">Especifica o disco do sistema operacional e a configuração do disco de dados para a imagem da máquina virtual criada usando cmdlets **New-AzureVMImageDiskConfigSet** , **set-AzureVMImageOSDiskConfig** e **set-AzureVMImageDataDiskConfig** .</span><span class="sxs-lookup"><span data-stu-id="9e657-117">Specifies the operating system disk and data disk configuration for the virtual machine image created by using the **New-AzureVMImageDiskConfigSet** , **Set-AzureVMImageOSDiskConfig** , and **Set-AzureVMImageDataDiskConfig** cmdlets.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e657-118">-DontShowInGui</span><span class="sxs-lookup"><span data-stu-id="9e657-118">-DontShowInGui</span></span>
<span data-ttu-id="9e657-119">Indica que esse cmdlet não mostra a imagem na GUI.</span><span class="sxs-lookup"><span data-stu-id="9e657-119">Indicates that this cmdlet does not show the image in the GUI.</span></span>

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

### <span data-ttu-id="9e657-120">-EULA</span><span class="sxs-lookup"><span data-stu-id="9e657-120">-Eula</span></span>
<span data-ttu-id="9e657-121">Especifica o contrato de licença de usuário final.</span><span class="sxs-lookup"><span data-stu-id="9e657-121">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="9e657-122">Recomendamos que o valor seja uma URL.</span><span class="sxs-lookup"><span data-stu-id="9e657-122">We recommend that the value is a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e657-123">-Iconname</span><span class="sxs-lookup"><span data-stu-id="9e657-123">-IconName</span></span>
<span data-ttu-id="9e657-124">Especifica o nome do ícone padrão para a imagem do sistema operacional ou da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9e657-124">Specifies the standard icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="9e657-125">-ImageFamily</span><span class="sxs-lookup"><span data-stu-id="9e657-125">-ImageFamily</span></span>
<span data-ttu-id="9e657-126">Especifica um valor que pode ser usado para agrupar imagens do sistema operacional ou da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9e657-126">Specifies a value that can be used to group operating system or virtual machine images.</span></span>

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

### <span data-ttu-id="9e657-127">-ImageName</span><span class="sxs-lookup"><span data-stu-id="9e657-127">-ImageName</span></span>
<span data-ttu-id="9e657-128">Especifica o nome da imagem a ser atualizada no repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="9e657-128">Specifies the name of the image to update in the image repository.</span></span>

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

### <span data-ttu-id="9e657-129">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9e657-129">-InformationAction</span></span>
<span data-ttu-id="9e657-130">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="9e657-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9e657-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9e657-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e657-132">Contínuo</span><span class="sxs-lookup"><span data-stu-id="9e657-132">Continue</span></span>
- <span data-ttu-id="9e657-133">Ignorar</span><span class="sxs-lookup"><span data-stu-id="9e657-133">Ignore</span></span>
- <span data-ttu-id="9e657-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="9e657-134">Inquire</span></span>
- <span data-ttu-id="9e657-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9e657-135">SilentlyContinue</span></span>
- <span data-ttu-id="9e657-136">Finaliza</span><span class="sxs-lookup"><span data-stu-id="9e657-136">Stop</span></span>
- <span data-ttu-id="9e657-137">Suspensão</span><span class="sxs-lookup"><span data-stu-id="9e657-137">Suspend</span></span>

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

### <span data-ttu-id="9e657-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9e657-138">-InformationVariable</span></span>
<span data-ttu-id="9e657-139">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="9e657-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9e657-140">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="9e657-140">-Label</span></span>
<span data-ttu-id="9e657-141">Especifica o novo rótulo da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e657-141">Specifies the new label of the image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e657-142">-Idioma</span><span class="sxs-lookup"><span data-stu-id="9e657-142">-Language</span></span>
<span data-ttu-id="9e657-143">Especifica o idioma para o sistema operacional na máquina virtual ou na imagem do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9e657-143">Specifies the language for the operating system in the virtual machine or operating system image.</span></span>

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

### <span data-ttu-id="9e657-144">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="9e657-144">-PrivacyUri</span></span>
<span data-ttu-id="9e657-145">Especifica o URI que aponta para um documento que contém a política de privacidade relacionada à imagem do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9e657-145">Specifies the URI that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e657-146">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9e657-146">-Profile</span></span>
<span data-ttu-id="9e657-147">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9e657-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9e657-148">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9e657-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9e657-149">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="9e657-149">-PublishedDate</span></span>
<span data-ttu-id="9e657-150">Especifica a data em que a imagem do sistema operacional foi adicionada ao repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="9e657-150">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e657-151">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="9e657-151">-RecommendedVMSize</span></span>
<span data-ttu-id="9e657-152">Especifica o tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9e657-152">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="9e657-153">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9e657-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e657-154">Port</span><span class="sxs-lookup"><span data-stu-id="9e657-154">Medium</span></span>
- <span data-ttu-id="9e657-155">Muita</span><span class="sxs-lookup"><span data-stu-id="9e657-155">Large</span></span>
- <span data-ttu-id="9e657-156">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="9e657-156">ExtraLarge</span></span>
- <span data-ttu-id="9e657-157">A5</span><span class="sxs-lookup"><span data-stu-id="9e657-157">A5</span></span>
- <span data-ttu-id="9e657-158">A6</span><span class="sxs-lookup"><span data-stu-id="9e657-158">A6</span></span>
- <span data-ttu-id="9e657-159">A7</span><span class="sxs-lookup"><span data-stu-id="9e657-159">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e657-160">-SmallIconname</span><span class="sxs-lookup"><span data-stu-id="9e657-160">-SmallIconName</span></span>
<span data-ttu-id="9e657-161">Especifica o nome do ícone pequeno para a imagem do sistema operacional ou da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9e657-161">Specifies the small icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="9e657-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e657-162">CommonParameters</span></span>
<span data-ttu-id="9e657-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e657-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e657-164">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e657-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e657-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e657-165">INPUTS</span></span>

## <span data-ttu-id="9e657-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e657-166">OUTPUTS</span></span>

### <span data-ttu-id="9e657-167">OSImageContext</span><span class="sxs-lookup"><span data-stu-id="9e657-167">OSImageContext</span></span>

## <span data-ttu-id="9e657-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e657-168">NOTES</span></span>

## <span data-ttu-id="9e657-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e657-169">RELATED LINKS</span></span>

[<span data-ttu-id="9e657-170">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="9e657-170">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="9e657-171">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="9e657-171">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="9e657-172">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="9e657-172">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="9e657-173">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="9e657-173">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="9e657-174">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="9e657-174">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="9e657-175">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="9e657-175">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="9e657-176">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="9e657-176">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


