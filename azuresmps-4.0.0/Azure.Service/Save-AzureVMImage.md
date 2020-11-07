---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A1CE31E-0158-441E-BC2D-B5D21C9D9421
online version: ''
schema: 2.0.0
ms.openlocfilehash: a956aa7eaf383b0cf5cdb20b39d2f6b54e292f92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945451"
---
# <span data-ttu-id="4c913-101">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="4c913-101">Save-AzureVMImage</span></span>

## <span data-ttu-id="4c913-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c913-102">SYNOPSIS</span></span>
<span data-ttu-id="4c913-103">Captura e salva a imagem de uma máquina virtual do Azure interrompida.</span><span class="sxs-lookup"><span data-stu-id="4c913-103">Captures and saves the image of a stopped Azure virtual machine.</span></span>

## <span data-ttu-id="4c913-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c913-104">SYNTAX</span></span>

```
Save-AzureVMImage [-ServiceName] <String> [-Name] <String> [-ImageName] <String> [[-ImageLabel] <String>]
 [[-OSState] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4c913-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c913-105">DESCRIPTION</span></span>
<span data-ttu-id="4c913-106">O cmdlet **Save-AzureVMImage** captura e salva a imagem de uma máquina virtual do Azure interrompida.</span><span class="sxs-lookup"><span data-stu-id="4c913-106">The **Save-AzureVMImage** cmdlet captures and saves the image of a stopped Azure virtual machine.</span></span>
<span data-ttu-id="4c913-107">Para máquinas virtuais do Windows, execute a ferramenta Sysprep para preparar a imagem antes que ela seja capturada.</span><span class="sxs-lookup"><span data-stu-id="4c913-107">For Windows virtual machines, run the Sysprep tool to prepare the image before it is captured.</span></span>
<span data-ttu-id="4c913-108">Depois que a imagem é capturada, a máquina virtual é excluída.</span><span class="sxs-lookup"><span data-stu-id="4c913-108">After the image is captured, the virtual machine is deleted.</span></span>

## <span data-ttu-id="4c913-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c913-109">EXAMPLES</span></span>

### <span data-ttu-id="4c913-110">Exemplo 1: salvar uma máquina virtual existente e, em seguida, excluí-la de uma implantação</span><span class="sxs-lookup"><span data-stu-id="4c913-110">Example 1: Save an existing virtual machine and then delete it from a deployment</span></span>
```
PS C:\> Save-AzureVMImage -ServiceName "MyService" -Name "MyVM" -NewImageName "MyBaseImage" -NewImageLabel "MyBaseVM"
```

<span data-ttu-id="4c913-111">Esse comando captura uma máquina virtual existente e a exclui da implantação.</span><span class="sxs-lookup"><span data-stu-id="4c913-111">This command captures an existing virtual machine and deletes it from the deployment.</span></span>

## <span data-ttu-id="4c913-112">OS</span><span class="sxs-lookup"><span data-stu-id="4c913-112">PARAMETERS</span></span>

### <span data-ttu-id="4c913-113">-ImageLabel</span><span class="sxs-lookup"><span data-stu-id="4c913-113">-ImageLabel</span></span>
<span data-ttu-id="4c913-114">Especifica o rótulo da imagem da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4c913-114">Specifies the label of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageLabel

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c913-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="4c913-115">-ImageName</span></span>
<span data-ttu-id="4c913-116">Especifica o nome da imagem da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4c913-116">Specifies the name of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c913-117">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="4c913-117">-InformationAction</span></span>
<span data-ttu-id="4c913-118">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="4c913-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4c913-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4c913-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4c913-120">Contínuo</span><span class="sxs-lookup"><span data-stu-id="4c913-120">Continue</span></span>
- <span data-ttu-id="4c913-121">Ignorar</span><span class="sxs-lookup"><span data-stu-id="4c913-121">Ignore</span></span>
- <span data-ttu-id="4c913-122">Inquire</span><span class="sxs-lookup"><span data-stu-id="4c913-122">Inquire</span></span>
- <span data-ttu-id="4c913-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4c913-123">SilentlyContinue</span></span>
- <span data-ttu-id="4c913-124">Finaliza</span><span class="sxs-lookup"><span data-stu-id="4c913-124">Stop</span></span>
- <span data-ttu-id="4c913-125">Suspensão</span><span class="sxs-lookup"><span data-stu-id="4c913-125">Suspend</span></span>

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

### <span data-ttu-id="4c913-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4c913-126">-InformationVariable</span></span>
<span data-ttu-id="4c913-127">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="4c913-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4c913-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c913-128">-Name</span></span>
<span data-ttu-id="4c913-129">Especifica o nome da máquina virtual de origem.</span><span class="sxs-lookup"><span data-stu-id="4c913-129">Specifies the name of the source virtual machine.</span></span>

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

### <span data-ttu-id="4c913-130">-OSState</span><span class="sxs-lookup"><span data-stu-id="4c913-130">-OSState</span></span>
<span data-ttu-id="4c913-131">Especifica o estado do sistema de operação para a imagem da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4c913-131">Specifies the operation system state for the virtual machine image.</span></span>
<span data-ttu-id="4c913-132">Use esse parâmetro se você pretende capturar uma imagem de máquina virtual para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c913-132">Use this parameter if you intend to capture a virtual machine image to Azure.</span></span>

<span data-ttu-id="4c913-133">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="4c913-133">Valid values are:</span></span>

- <span data-ttu-id="4c913-134">Generalizado</span><span class="sxs-lookup"><span data-stu-id="4c913-134">Generalized</span></span>
- <span data-ttu-id="4c913-135">Especialistas</span><span class="sxs-lookup"><span data-stu-id="4c913-135">Specialized</span></span>

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

### <span data-ttu-id="4c913-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4c913-136">-Profile</span></span>
<span data-ttu-id="4c913-137">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4c913-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c913-138">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4c913-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4c913-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4c913-139">-ServiceName</span></span>
<span data-ttu-id="4c913-140">Especifica o nome do serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c913-140">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="4c913-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c913-141">CommonParameters</span></span>
<span data-ttu-id="4c913-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c913-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c913-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c913-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c913-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c913-144">INPUTS</span></span>

## <span data-ttu-id="4c913-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c913-145">OUTPUTS</span></span>

## <span data-ttu-id="4c913-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c913-146">NOTES</span></span>

## <span data-ttu-id="4c913-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c913-147">RELATED LINKS</span></span>

[<span data-ttu-id="4c913-148">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="4c913-148">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="4c913-149">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="4c913-149">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="4c913-150">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="4c913-150">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="4c913-151">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="4c913-151">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


