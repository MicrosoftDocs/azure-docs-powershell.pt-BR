---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 377716B6-8B8C-4CAE-A8FA-835DA24F04C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9610c6b8abaf4d59d6a363253d0b90a0dfcecad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946043"
---
# <span data-ttu-id="70f10-101">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="70f10-101">Set-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="70f10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70f10-102">SYNOPSIS</span></span>
<span data-ttu-id="70f10-103">Define a extensão BGInfo para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="70f10-103">Sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="70f10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70f10-104">SYNTAX</span></span>

### <span data-ttu-id="70f10-105">SetBGInfoExtension (padrão)</span><span class="sxs-lookup"><span data-stu-id="70f10-105">SetBGInfoExtension (Default)</span></span>
```
Set-AzureVMBGInfoExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="70f10-106">UninstallBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="70f10-106">UninstallBGInfoExtension</span></span>
```
Set-AzureVMBGInfoExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="70f10-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70f10-107">DESCRIPTION</span></span>
<span data-ttu-id="70f10-108">O cmdlet **set-AzureVMBGInfoExtension** define a extensão BGInfo para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="70f10-108">The **Set-AzureVMBGInfoExtension** cmdlet sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="70f10-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70f10-109">EXAMPLES</span></span>

### <span data-ttu-id="70f10-110">Exemplo 1: definir a extensão do BGInfo para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="70f10-110">Example 1: Set the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -VM $VM
```

<span data-ttu-id="70f10-111">Esse comando define a extensão BGInfo para a máquina virtual especificada como armazenada na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="70f10-111">This command sets the BGInfo extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="70f10-112">OS</span><span class="sxs-lookup"><span data-stu-id="70f10-112">PARAMETERS</span></span>

### <span data-ttu-id="70f10-113">-Disable</span><span class="sxs-lookup"><span data-stu-id="70f10-113">-Disable</span></span>
<span data-ttu-id="70f10-114">Indica que esse cmdlet desabilita o estado da extensão.</span><span class="sxs-lookup"><span data-stu-id="70f10-114">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f10-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="70f10-115">-InformationAction</span></span>
<span data-ttu-id="70f10-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="70f10-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="70f10-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="70f10-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70f10-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="70f10-118">Continue</span></span>
- <span data-ttu-id="70f10-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="70f10-119">Ignore</span></span>
- <span data-ttu-id="70f10-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="70f10-120">Inquire</span></span>
- <span data-ttu-id="70f10-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="70f10-121">SilentlyContinue</span></span>
- <span data-ttu-id="70f10-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="70f10-122">Stop</span></span>
- <span data-ttu-id="70f10-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="70f10-123">Suspend</span></span>

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

### <span data-ttu-id="70f10-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="70f10-124">-InformationVariable</span></span>
<span data-ttu-id="70f10-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="70f10-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="70f10-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="70f10-126">-Profile</span></span>
<span data-ttu-id="70f10-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="70f10-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="70f10-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="70f10-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="70f10-129">-Referencename</span><span class="sxs-lookup"><span data-stu-id="70f10-129">-ReferenceName</span></span>
<span data-ttu-id="70f10-130">Especifica o nome de referência da extensão BGInfo.</span><span class="sxs-lookup"><span data-stu-id="70f10-130">Specifies the reference name of the BGInfo extension.</span></span>

<span data-ttu-id="70f10-131">Esse parâmetro é uma cadeia de caracteres definida pelo usuário que pode ser usada para fazer referência a uma extensão.</span><span class="sxs-lookup"><span data-stu-id="70f10-131">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="70f10-132">Ele é especificado quando a extensão é adicionada à máquina virtual pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="70f10-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="70f10-133">Você pode especificar o nome de referência usado anteriormente ao atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="70f10-133">You can specify the previously used reference name while updating the extension.</span></span>

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

### <span data-ttu-id="70f10-134">-Desinstalar</span><span class="sxs-lookup"><span data-stu-id="70f10-134">-Uninstall</span></span>
<span data-ttu-id="70f10-135">Indica que esse cmdlet desinstala a extensão BGInfo.</span><span class="sxs-lookup"><span data-stu-id="70f10-135">Indicates that this cmdlet uninstalls the BGInfo extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f10-136">-Versão</span><span class="sxs-lookup"><span data-stu-id="70f10-136">-Version</span></span>
<span data-ttu-id="70f10-137">Especifica a versão da extensão do BGInfo.</span><span class="sxs-lookup"><span data-stu-id="70f10-137">Specifies the version of the BGInfo extension.</span></span>

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

### <span data-ttu-id="70f10-138">-VM</span><span class="sxs-lookup"><span data-stu-id="70f10-138">-VM</span></span>
<span data-ttu-id="70f10-139">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="70f10-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="70f10-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f10-140">CommonParameters</span></span>
<span data-ttu-id="70f10-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70f10-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f10-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70f10-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f10-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70f10-143">INPUTS</span></span>

## <span data-ttu-id="70f10-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70f10-144">OUTPUTS</span></span>

## <span data-ttu-id="70f10-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70f10-145">NOTES</span></span>

## <span data-ttu-id="70f10-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70f10-146">RELATED LINKS</span></span>

[<span data-ttu-id="70f10-147">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="70f10-147">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="70f10-148">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="70f10-148">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)


