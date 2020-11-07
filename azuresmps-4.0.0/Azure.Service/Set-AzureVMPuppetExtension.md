---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 268D3E91-AB0F-451F-93B2-9226985910B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41648470b76d889c1ee9d47e4200f843e9f11522
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945849"
---
# <span data-ttu-id="27a37-101">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="27a37-101">Set-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="27a37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27a37-102">SYNOPSIS</span></span>
<span data-ttu-id="27a37-103">Define a extensão Puppet para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="27a37-103">Sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="27a37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27a37-104">SYNTAX</span></span>

```
Set-AzureVMPuppetExtension [-PuppetMasterServer] <String> [[-Version] <String>] [-Disable]
 [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="27a37-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27a37-105">DESCRIPTION</span></span>
<span data-ttu-id="27a37-106">O cmdlet **set-AzureVMPuppetExtension** define a extensão Puppet para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="27a37-106">The **Set-AzureVMPuppetExtension** cmdlet sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="27a37-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27a37-107">EXAMPLES</span></span>

### <span data-ttu-id="27a37-108">Exemplo 1: definir a extensão Puppet para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="27a37-108">Example 1: Set the Puppet extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="27a37-109">Este exemplo define a extensão Puppet para a máquina virtual especificada, conforme armazenada na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="27a37-109">This example sets the Puppet extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="27a37-110">OS</span><span class="sxs-lookup"><span data-stu-id="27a37-110">PARAMETERS</span></span>

### <span data-ttu-id="27a37-111">-Disable</span><span class="sxs-lookup"><span data-stu-id="27a37-111">-Disable</span></span>
<span data-ttu-id="27a37-112">Indica que esse cmdlet desabilita o estado da extensão.</span><span class="sxs-lookup"><span data-stu-id="27a37-112">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a37-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="27a37-113">-InformationAction</span></span>
<span data-ttu-id="27a37-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="27a37-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="27a37-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="27a37-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="27a37-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="27a37-116">Continue</span></span>
- <span data-ttu-id="27a37-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="27a37-117">Ignore</span></span>
- <span data-ttu-id="27a37-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="27a37-118">Inquire</span></span>
- <span data-ttu-id="27a37-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="27a37-119">SilentlyContinue</span></span>
- <span data-ttu-id="27a37-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="27a37-120">Stop</span></span>
- <span data-ttu-id="27a37-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="27a37-121">Suspend</span></span>

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

### <span data-ttu-id="27a37-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="27a37-122">-InformationVariable</span></span>
<span data-ttu-id="27a37-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="27a37-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="27a37-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="27a37-124">-Profile</span></span>
<span data-ttu-id="27a37-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="27a37-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="27a37-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="27a37-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="27a37-127">-PuppetMasterServer</span><span class="sxs-lookup"><span data-stu-id="27a37-127">-PuppetMasterServer</span></span>
<span data-ttu-id="27a37-128">Especifica o nome de domínio totalmente qualificado (FQDN) do Puppet Master Server.</span><span class="sxs-lookup"><span data-stu-id="27a37-128">Specifies the fully qualified domain name (FQDN) of puppet master server.</span></span>

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

### <span data-ttu-id="27a37-129">-Referencename</span><span class="sxs-lookup"><span data-stu-id="27a37-129">-ReferenceName</span></span>
<span data-ttu-id="27a37-130">Especifica o nome de referência da extensão.</span><span class="sxs-lookup"><span data-stu-id="27a37-130">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="27a37-131">Esta é uma cadeia de caracteres definida pelo usuário que é usada para fazer referência a uma extensão.</span><span class="sxs-lookup"><span data-stu-id="27a37-131">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="27a37-132">Ele é especificado quando a extensão é adicionada à máquina virtual pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="27a37-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="27a37-133">Para atualizações subsequentes, você precisa especificar o nome de referência usado anteriormente ao atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="27a37-133">For subsequent updates, you need to specify the previously used reference name when you update the extension.</span></span>
<span data-ttu-id="27a37-134">O Referencename atribuído a uma extensão é retornado usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="27a37-134">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="27a37-135">-Versão</span><span class="sxs-lookup"><span data-stu-id="27a37-135">-Version</span></span>
<span data-ttu-id="27a37-136">Especifica a versão de extensão.</span><span class="sxs-lookup"><span data-stu-id="27a37-136">Specifies the extension version.</span></span>

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

### <span data-ttu-id="27a37-137">-VM</span><span class="sxs-lookup"><span data-stu-id="27a37-137">-VM</span></span>
<span data-ttu-id="27a37-138">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="27a37-138">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="27a37-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a37-139">CommonParameters</span></span>
<span data-ttu-id="27a37-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27a37-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a37-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27a37-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a37-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27a37-142">INPUTS</span></span>

## <span data-ttu-id="27a37-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27a37-143">OUTPUTS</span></span>

## <span data-ttu-id="27a37-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27a37-144">NOTES</span></span>

## <span data-ttu-id="27a37-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27a37-145">RELATED LINKS</span></span>

[<span data-ttu-id="27a37-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="27a37-146">Get-AzureVM</span></span>](./Get-AzureVM.md)


