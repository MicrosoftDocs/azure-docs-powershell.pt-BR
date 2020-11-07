---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7ED074F0-1E9E-40C2-A543-D19A49831DD3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f0b8ca9acfe5a62b002944bd44e11acfcd38ec1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946533"
---
# <span data-ttu-id="98726-101">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="98726-101">Get-AzureVMExtension</span></span>

## <span data-ttu-id="98726-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98726-102">SYNOPSIS</span></span>
<span data-ttu-id="98726-103">Obtém extensões de recurso aplicadas a máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="98726-103">Gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="98726-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98726-104">SYNTAX</span></span>

### <span data-ttu-id="98726-105">ListByReferenceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="98726-105">ListByReferenceName (Default)</span></span>
```
Get-AzureVMExtension [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="98726-106">ListByExtensionName</span><span class="sxs-lookup"><span data-stu-id="98726-106">ListByExtensionName</span></span>
```
Get-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="98726-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98726-107">DESCRIPTION</span></span>
<span data-ttu-id="98726-108">O cmdlet **Get-AzureVMExtension** Obtém extensões de recursos aplicadas a máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="98726-108">The **Get-AzureVMExtension** cmdlet gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="98726-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98726-109">EXAMPLES</span></span>

### <span data-ttu-id="98726-110">Exemplo 1: obter as extensões de recursos aplicadas a uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="98726-110">Example 1: Get the resource extensions applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName $SVC -Name $VM | Get-AzureVMExtension;
```

<span data-ttu-id="98726-111">Esse comando obtém as extensões de recursos aplicadas à máquina virtual especificada, conforme armazenadas na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="98726-111">This command gets the resource extensions applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="98726-112">OS</span><span class="sxs-lookup"><span data-stu-id="98726-112">PARAMETERS</span></span>

### <span data-ttu-id="98726-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="98726-113">-ExtensionName</span></span>
<span data-ttu-id="98726-114">Especifica o nome da extensão da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="98726-114">Specifies the virtual machine extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98726-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="98726-115">-InformationAction</span></span>
<span data-ttu-id="98726-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="98726-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="98726-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="98726-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="98726-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="98726-118">Continue</span></span>
- <span data-ttu-id="98726-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="98726-119">Ignore</span></span>
- <span data-ttu-id="98726-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="98726-120">Inquire</span></span>
- <span data-ttu-id="98726-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="98726-121">SilentlyContinue</span></span>
- <span data-ttu-id="98726-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="98726-122">Stop</span></span>
- <span data-ttu-id="98726-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="98726-123">Suspend</span></span>

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

### <span data-ttu-id="98726-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="98726-124">-InformationVariable</span></span>
<span data-ttu-id="98726-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="98726-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="98726-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="98726-126">-Profile</span></span>
<span data-ttu-id="98726-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="98726-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="98726-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="98726-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="98726-129">-Publisher</span><span class="sxs-lookup"><span data-stu-id="98726-129">-Publisher</span></span>
<span data-ttu-id="98726-130">Especifica o fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="98726-130">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98726-131">-Referencename</span><span class="sxs-lookup"><span data-stu-id="98726-131">-ReferenceName</span></span>
<span data-ttu-id="98726-132">Especifica o nome de referência da extensão.</span><span class="sxs-lookup"><span data-stu-id="98726-132">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByReferenceName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98726-133">-Versão</span><span class="sxs-lookup"><span data-stu-id="98726-133">-Version</span></span>
<span data-ttu-id="98726-134">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="98726-134">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98726-135">-VM</span><span class="sxs-lookup"><span data-stu-id="98726-135">-VM</span></span>
<span data-ttu-id="98726-136">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="98726-136">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98726-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98726-137">CommonParameters</span></span>
<span data-ttu-id="98726-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98726-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98726-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98726-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98726-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98726-140">INPUTS</span></span>

## <span data-ttu-id="98726-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98726-141">OUTPUTS</span></span>

## <span data-ttu-id="98726-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98726-142">NOTES</span></span>

## <span data-ttu-id="98726-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98726-143">RELATED LINKS</span></span>

[<span data-ttu-id="98726-144">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="98726-144">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="98726-145">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="98726-145">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


