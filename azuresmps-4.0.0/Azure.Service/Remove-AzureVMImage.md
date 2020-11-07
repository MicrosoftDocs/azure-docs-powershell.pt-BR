---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946454"
---
# <span data-ttu-id="a22ba-101">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a22ba-101">Remove-AzureVMImage</span></span>

## <span data-ttu-id="a22ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a22ba-102">SYNOPSIS</span></span>
<span data-ttu-id="a22ba-103">Remove uma imagem do sistema operacional do repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="a22ba-103">Removes an operating system image from the image repository.</span></span>

## <span data-ttu-id="a22ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a22ba-104">SYNTAX</span></span>

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a22ba-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a22ba-105">DESCRIPTION</span></span>
<span data-ttu-id="a22ba-106">O cmdlet **Remove-AzureVMImage** remove uma imagem do sistema operacional do repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="a22ba-106">The **Remove-AzureVMImage** cmdlet removes an operating system image from the image repository.</span></span>
<span data-ttu-id="a22ba-107">Por padrão, esse cmdlet não exclui o blob da imagem física associada da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a22ba-107">By default, this cmdlet does not delete the associated physical image blob from the storage account.</span></span>
<span data-ttu-id="a22ba-108">Para excluir o VHD (disco rígido virtual) associado, use o parâmetro **DeleteVHD** .</span><span class="sxs-lookup"><span data-stu-id="a22ba-108">To delete the associated virtual hard drive (VHD), use the **DeleteVHD** parameter.</span></span>

## <span data-ttu-id="a22ba-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a22ba-109">EXAMPLES</span></span>

### <span data-ttu-id="a22ba-110">Exemplo 1: remover uma imagem do repositório de imagens</span><span class="sxs-lookup"><span data-stu-id="a22ba-110">Example 1: Remove an image from the image repository</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

<span data-ttu-id="a22ba-111">Esse comando Remove a imagem chamada Image001 do repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="a22ba-111">This command removes the image named Image001 from the image repository.</span></span>

### <span data-ttu-id="a22ba-112">Exemplo 2: remover uma imagem do repositório de imagens e também o VHD</span><span class="sxs-lookup"><span data-stu-id="a22ba-112">Example 2: Remove an image from the image repository and also the VHD</span></span>
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

<span data-ttu-id="a22ba-113">Esse comando Remove a imagem chamada Image001 do repositório de imagens e também exclui a imagem VHD física da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a22ba-113">This command removes the image named Image001 from the image repository and also deletes the physical VHD image from the storage account.</span></span>

### <span data-ttu-id="a22ba-114">Exemplo 3: definir um contexto de assinatura e remover todas as imagens</span><span class="sxs-lookup"><span data-stu-id="a22ba-114">Example 3: Set a subscription context and then remove all the images</span></span>
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

<span data-ttu-id="a22ba-115">Esse comando define o contexto de assinatura e remove todas as imagens do repositório de imagens cujo rótulo inclui o nome beta.</span><span class="sxs-lookup"><span data-stu-id="a22ba-115">This command sets the subscription context and then removes all the images from the image repository whose Label includes the name Beta.</span></span>

## <span data-ttu-id="a22ba-116">OS</span><span class="sxs-lookup"><span data-stu-id="a22ba-116">PARAMETERS</span></span>

### <span data-ttu-id="a22ba-117">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="a22ba-117">-DeleteVHD</span></span>
<span data-ttu-id="a22ba-118">Indica que esse cmdlet exclui o blob da imagem VHD física da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a22ba-118">Indicates that this cmdlet deletes the physical VHD image blob from the storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a22ba-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a22ba-119">-ImageName</span></span>
<span data-ttu-id="a22ba-120">Especifica a imagem do sistema operacional ou da máquina virtual a ser removida do repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="a22ba-120">Specifies the operating system or virtual machine image to remove from the image repository.</span></span>

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

### <span data-ttu-id="a22ba-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a22ba-121">-InformationAction</span></span>
<span data-ttu-id="a22ba-122">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="a22ba-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a22ba-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a22ba-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a22ba-124">Contínuo</span><span class="sxs-lookup"><span data-stu-id="a22ba-124">Continue</span></span>
- <span data-ttu-id="a22ba-125">Ignorar</span><span class="sxs-lookup"><span data-stu-id="a22ba-125">Ignore</span></span>
- <span data-ttu-id="a22ba-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="a22ba-126">Inquire</span></span>
- <span data-ttu-id="a22ba-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a22ba-127">SilentlyContinue</span></span>
- <span data-ttu-id="a22ba-128">Finaliza</span><span class="sxs-lookup"><span data-stu-id="a22ba-128">Stop</span></span>
- <span data-ttu-id="a22ba-129">Suspensão</span><span class="sxs-lookup"><span data-stu-id="a22ba-129">Suspend</span></span>

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

### <span data-ttu-id="a22ba-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a22ba-130">-InformationVariable</span></span>
<span data-ttu-id="a22ba-131">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="a22ba-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a22ba-132">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a22ba-132">-Profile</span></span>
<span data-ttu-id="a22ba-133">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a22ba-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a22ba-134">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a22ba-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a22ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a22ba-135">CommonParameters</span></span>
<span data-ttu-id="a22ba-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a22ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a22ba-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a22ba-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a22ba-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a22ba-138">INPUTS</span></span>

## <span data-ttu-id="a22ba-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a22ba-139">OUTPUTS</span></span>

## <span data-ttu-id="a22ba-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a22ba-140">NOTES</span></span>

## <span data-ttu-id="a22ba-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a22ba-141">RELATED LINKS</span></span>

[<span data-ttu-id="a22ba-142">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a22ba-142">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="a22ba-143">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a22ba-143">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="a22ba-144">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a22ba-144">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="a22ba-145">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a22ba-145">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


