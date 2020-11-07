---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946532"
---
# <span data-ttu-id="2311b-101">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="2311b-101">Get-AzureVMImage</span></span>

## <span data-ttu-id="2311b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2311b-102">SYNOPSIS</span></span>
<span data-ttu-id="2311b-103">Obtém as propriedades em um ou em uma lista de sistemas operacionais ou em uma imagem de máquina virtual no repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="2311b-103">Gets the properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>

## <span data-ttu-id="2311b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2311b-104">SYNTAX</span></span>

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2311b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2311b-105">DESCRIPTION</span></span>
<span data-ttu-id="2311b-106">O cmdlet **Get-AzureVMImage** Obtém Propriedades em um ou uma lista de sistemas operacionais ou uma imagem de máquina virtual no repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="2311b-106">The **Get-AzureVMImage** cmdlet gets properties on one or a list of operating systems or a virtual machine image in the image repository.</span></span>
<span data-ttu-id="2311b-107">O cmdlet retorna informações de todas as imagens no repositório ou de uma imagem específica se o nome da imagem for fornecido.</span><span class="sxs-lookup"><span data-stu-id="2311b-107">The cmdlet returns information for all images in the repository, or about a specific image if its image name is provided.</span></span>

## <span data-ttu-id="2311b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2311b-108">EXAMPLES</span></span>

### <span data-ttu-id="2311b-109">Exemplo 1: obter um objeto de imagem específico do repositório de imagens atual.</span><span class="sxs-lookup"><span data-stu-id="2311b-109">Example 1: Get a specific image object from the current image repository.</span></span>
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

<span data-ttu-id="2311b-110">Esse comando obtém o objeto Image chamado Image001 do repositório de imagens atual.</span><span class="sxs-lookup"><span data-stu-id="2311b-110">This command gets the image object named Image001 from the current image repository.</span></span>

### <span data-ttu-id="2311b-111">Exemplo 2: obter todas as imagens do repositório de imagens atual</span><span class="sxs-lookup"><span data-stu-id="2311b-111">Example 2: Get all images from the current image repository</span></span>
```
PS C:\> Get-AzureVMImage
```

<span data-ttu-id="2311b-112">Esse comando recupera todas as imagens do repositório de imagens atual.</span><span class="sxs-lookup"><span data-stu-id="2311b-112">This command retrieves all the images from the current image repository.</span></span>

### <span data-ttu-id="2311b-113">Exemplo 3: definir o contexto de assinatura e obter todas as imagens</span><span class="sxs-lookup"><span data-stu-id="2311b-113">Example 3: Set the subscription context and then get all the images</span></span>
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

<span data-ttu-id="2311b-114">Esse comando define o contexto da assinatura e recupera todas as imagens do repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="2311b-114">This command sets the subscription context and then retrieves all the images from the image repository.</span></span>

## <span data-ttu-id="2311b-115">OS</span><span class="sxs-lookup"><span data-stu-id="2311b-115">PARAMETERS</span></span>

### <span data-ttu-id="2311b-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="2311b-116">-ImageName</span></span>
<span data-ttu-id="2311b-117">Especifica o nome da imagem do sistema operacional ou da máquina virtual no repositório de imagens.</span><span class="sxs-lookup"><span data-stu-id="2311b-117">Specifies the name of the operating system or virtual machine image in the image repository.</span></span>
<span data-ttu-id="2311b-118">Se você não especificar esse parâmetro, todas as imagens serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="2311b-118">If you do not specify this parameter, all the images are returned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2311b-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="2311b-119">-InformationAction</span></span>
<span data-ttu-id="2311b-120">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="2311b-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2311b-121">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2311b-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2311b-122">Contínuo</span><span class="sxs-lookup"><span data-stu-id="2311b-122">Continue</span></span>
- <span data-ttu-id="2311b-123">Ignorar</span><span class="sxs-lookup"><span data-stu-id="2311b-123">Ignore</span></span>
- <span data-ttu-id="2311b-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="2311b-124">Inquire</span></span>
- <span data-ttu-id="2311b-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2311b-125">SilentlyContinue</span></span>
- <span data-ttu-id="2311b-126">Finaliza</span><span class="sxs-lookup"><span data-stu-id="2311b-126">Stop</span></span>
- <span data-ttu-id="2311b-127">Suspensão</span><span class="sxs-lookup"><span data-stu-id="2311b-127">Suspend</span></span>

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

### <span data-ttu-id="2311b-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2311b-128">-InformationVariable</span></span>
<span data-ttu-id="2311b-129">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="2311b-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2311b-130">-Perfil</span><span class="sxs-lookup"><span data-stu-id="2311b-130">-Profile</span></span>
<span data-ttu-id="2311b-131">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="2311b-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2311b-132">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="2311b-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2311b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2311b-133">CommonParameters</span></span>
<span data-ttu-id="2311b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2311b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2311b-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2311b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2311b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2311b-136">INPUTS</span></span>

## <span data-ttu-id="2311b-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2311b-137">OUTPUTS</span></span>

## <span data-ttu-id="2311b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2311b-138">NOTES</span></span>

## <span data-ttu-id="2311b-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2311b-139">RELATED LINKS</span></span>

[<span data-ttu-id="2311b-140">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="2311b-140">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="2311b-141">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="2311b-141">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="2311b-142">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="2311b-142">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="2311b-143">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="2311b-143">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


