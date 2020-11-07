---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: ACBE32E5-AA8C-43CA-9FF4-4B59906C6B85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 45d18179fba41d39456a11575fc2041ad4be8557
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946530"
---
# <span data-ttu-id="f5f8a-101">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="f5f8a-101">Get-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="f5f8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f8a-103">Obtém um objeto do conjunto de configuração de disco do contexto de imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="f5f8a-103">Gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="f5f8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5f8a-104">SYNTAX</span></span>

```
Get-AzureVMImageDiskConfigSet [[-ImageContext] <OSImageContext>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f5f8a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5f8a-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f8a-106">O cmdlet **Get-AzureVMImageDiskConfigSet** Obtém um objeto de conjunto de configuração de disco do contexto de imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="f5f8a-106">The **Get-AzureVMImageDiskConfigSet** cmdlet gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="f5f8a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5f8a-107">EXAMPLES</span></span>

### <span data-ttu-id="f5f8a-108">Exemplo 1: obter um objeto do conjunto de configuração de disco de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="f5f8a-108">Example 1: Get a disk configuration set object from a virtual machine</span></span>
```
PS C:\> Get-AzureVMImage -ImageName $Img | Get-AzureVMImageDiskConfigSet
```

<span data-ttu-id="f5f8a-109">Esse comando obtém um objeto do conjunto de configuração de disco de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f5f8a-109">This command gets a disk configuration set object from a virtual machine.</span></span>

## <span data-ttu-id="f5f8a-110">OS</span><span class="sxs-lookup"><span data-stu-id="f5f8a-110">PARAMETERS</span></span>

### <span data-ttu-id="f5f8a-111">-ImageContext</span><span class="sxs-lookup"><span data-stu-id="f5f8a-111">-ImageContext</span></span>
<span data-ttu-id="f5f8a-112">Especifica o contexto da imagem da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f5f8a-112">Specifies the virtual machine image context.</span></span>

```yaml
Type: OSImageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f8a-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f5f8a-113">-InformationAction</span></span>
<span data-ttu-id="f5f8a-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="f5f8a-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f5f8a-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f5f8a-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5f8a-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="f5f8a-116">Continue</span></span>
- <span data-ttu-id="f5f8a-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="f5f8a-117">Ignore</span></span>
- <span data-ttu-id="f5f8a-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="f5f8a-118">Inquire</span></span>
- <span data-ttu-id="f5f8a-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f5f8a-119">SilentlyContinue</span></span>
- <span data-ttu-id="f5f8a-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="f5f8a-120">Stop</span></span>
- <span data-ttu-id="f5f8a-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="f5f8a-121">Suspend</span></span>

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

### <span data-ttu-id="f5f8a-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f5f8a-122">-InformationVariable</span></span>
<span data-ttu-id="f5f8a-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="f5f8a-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f5f8a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f8a-124">CommonParameters</span></span>
<span data-ttu-id="f5f8a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f8a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f8a-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f8a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f8a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5f8a-127">INPUTS</span></span>

## <span data-ttu-id="f5f8a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5f8a-128">OUTPUTS</span></span>

### <span data-ttu-id="f5f8a-129">Microsoft. WindowsAzure. Commands. onmanagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="f5f8a-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="f5f8a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5f8a-130">NOTES</span></span>

## <span data-ttu-id="f5f8a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5f8a-131">RELATED LINKS</span></span>

[<span data-ttu-id="f5f8a-132">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="f5f8a-132">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="f5f8a-133">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="f5f8a-133">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)


