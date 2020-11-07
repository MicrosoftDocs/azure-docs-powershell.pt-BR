---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B98FCF46-A5D6-4CC9-B82A-60B429A21A8B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8079844a931debee5b9338e98d405697cc4336f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945501"
---
# <span data-ttu-id="f350d-101">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="f350d-101">Remove-AzureVMExtension</span></span>

## <span data-ttu-id="f350d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f350d-102">SYNOPSIS</span></span>
<span data-ttu-id="f350d-103">Remove extensões de recursos de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f350d-103">Removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="f350d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f350d-104">SYNTAX</span></span>

### <span data-ttu-id="f350d-105">RemoveByExtensionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f350d-105">RemoveByExtensionName (Default)</span></span>
```
Remove-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f350d-106">RemoveByReferenceName</span><span class="sxs-lookup"><span data-stu-id="f350d-106">RemoveByReferenceName</span></span>
```
Remove-AzureVMExtension [-ReferenceName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f350d-107">RemoveAll</span><span class="sxs-lookup"><span data-stu-id="f350d-107">RemoveAll</span></span>
```
Remove-AzureVMExtension [-RemoveAll] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f350d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f350d-108">DESCRIPTION</span></span>
<span data-ttu-id="f350d-109">O cmdlet **Remove-AzureVMExtension** remove extensões de recursos de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f350d-109">The **Remove-AzureVMExtension** cmdlet removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="f350d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f350d-110">EXAMPLES</span></span>

### <span data-ttu-id="f350d-111">Exemplo 1: remover uma extensão usando um nome específico e o Publisher</span><span class="sxs-lookup"><span data-stu-id="f350d-111">Example 1: Remove an extension using a specific name and publisher</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -ExtensionName $EXT -Publisher $PUB;
```

<span data-ttu-id="f350d-112">Este comando Remove uma extensão com o nome e o fornecedor especificados.</span><span class="sxs-lookup"><span data-stu-id="f350d-112">This command removes an extension with the specified name and publisher.</span></span>

### <span data-ttu-id="f350d-113">Exemplo 2: remover todas as extensões de uma determinada máquina virtual</span><span class="sxs-lookup"><span data-stu-id="f350d-113">Example 2: Remove all extensions from a specific virtual machine</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -RemoveAll;
```

<span data-ttu-id="f350d-114">Esse comando Remove todas as extensões da máquina virtual especificada, conforme armazenadas na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="f350d-114">This command removes all extensions from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="f350d-115">OS</span><span class="sxs-lookup"><span data-stu-id="f350d-115">PARAMETERS</span></span>

### <span data-ttu-id="f350d-116">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="f350d-116">-ExtensionName</span></span>
<span data-ttu-id="f350d-117">Especifica o nome da extensão que esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f350d-117">Specifies the extension name that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f350d-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f350d-118">-InformationAction</span></span>
<span data-ttu-id="f350d-119">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="f350d-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f350d-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f350d-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f350d-121">Contínuo</span><span class="sxs-lookup"><span data-stu-id="f350d-121">Continue</span></span>
- <span data-ttu-id="f350d-122">Ignorar</span><span class="sxs-lookup"><span data-stu-id="f350d-122">Ignore</span></span>
- <span data-ttu-id="f350d-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="f350d-123">Inquire</span></span>
- <span data-ttu-id="f350d-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f350d-124">SilentlyContinue</span></span>
- <span data-ttu-id="f350d-125">Finaliza</span><span class="sxs-lookup"><span data-stu-id="f350d-125">Stop</span></span>
- <span data-ttu-id="f350d-126">Suspensão</span><span class="sxs-lookup"><span data-stu-id="f350d-126">Suspend</span></span>

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

### <span data-ttu-id="f350d-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f350d-127">-InformationVariable</span></span>
<span data-ttu-id="f350d-128">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="f350d-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f350d-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f350d-129">-Profile</span></span>
<span data-ttu-id="f350d-130">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f350d-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f350d-131">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f350d-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f350d-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f350d-132">-Publisher</span></span>
<span data-ttu-id="f350d-133">Especifica o fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="f350d-133">Specifies the extension publisher.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f350d-134">-Referencename</span><span class="sxs-lookup"><span data-stu-id="f350d-134">-ReferenceName</span></span>
<span data-ttu-id="f350d-135">Especifica o nome de referência da extensão.</span><span class="sxs-lookup"><span data-stu-id="f350d-135">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByReferenceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f350d-136">-RemoveAll</span><span class="sxs-lookup"><span data-stu-id="f350d-136">-RemoveAll</span></span>
<span data-ttu-id="f350d-137">Indica que esse cmdlet Remove todas as extensões de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f350d-137">Indicates that this cmdlet removes all resource extensions from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAll
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f350d-138">-VM</span><span class="sxs-lookup"><span data-stu-id="f350d-138">-VM</span></span>
<span data-ttu-id="f350d-139">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="f350d-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="f350d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f350d-140">CommonParameters</span></span>
<span data-ttu-id="f350d-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f350d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f350d-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f350d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f350d-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f350d-143">INPUTS</span></span>

## <span data-ttu-id="f350d-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f350d-144">OUTPUTS</span></span>

## <span data-ttu-id="f350d-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f350d-145">NOTES</span></span>

## <span data-ttu-id="f350d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f350d-146">RELATED LINKS</span></span>

[<span data-ttu-id="f350d-147">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="f350d-147">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="f350d-148">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="f350d-148">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


