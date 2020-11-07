---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3DCA1502-9528-458D-A9EA-762A4BD2726B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284fcf4bd31eeb9437b8cc7669fff0824155180f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946448"
---
# <span data-ttu-id="a0d79-101">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a0d79-101">Remove-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="a0d79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0d79-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d79-103">Remove a extensão de script personalizada de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0d79-103">Removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="a0d79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0d79-104">SYNTAX</span></span>

```
Remove-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a0d79-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0d79-105">DESCRIPTION</span></span>
<span data-ttu-id="a0d79-106">O cmdlet **Remove-AzureVMCustomScriptExtension** remove a extensão de script personalizada de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a0d79-106">The **Remove-AzureVMCustomScriptExtension** cmdlet removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="a0d79-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0d79-107">EXAMPLES</span></span>

### <span data-ttu-id="a0d79-108">Exemplo 1: remover uma extensão de script personalizado da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="a0d79-108">Example 1: Remove a virtual machine custom script extension</span></span>
```
PS C:\> Remove-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="a0d79-109">Esse comando Remove a extensão de script personalizada da máquina virtual do Azure da máquina virtual especificada, conforme armazenada na variável $VM.</span><span class="sxs-lookup"><span data-stu-id="a0d79-109">This command removes the Azure virtual machine custom script extension from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="a0d79-110">OS</span><span class="sxs-lookup"><span data-stu-id="a0d79-110">PARAMETERS</span></span>

### <span data-ttu-id="a0d79-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a0d79-111">-InformationAction</span></span>
<span data-ttu-id="a0d79-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="a0d79-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a0d79-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a0d79-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0d79-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="a0d79-114">Continue</span></span>
- <span data-ttu-id="a0d79-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="a0d79-115">Ignore</span></span>
- <span data-ttu-id="a0d79-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="a0d79-116">Inquire</span></span>
- <span data-ttu-id="a0d79-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a0d79-117">SilentlyContinue</span></span>
- <span data-ttu-id="a0d79-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="a0d79-118">Stop</span></span>
- <span data-ttu-id="a0d79-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="a0d79-119">Suspend</span></span>

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

### <span data-ttu-id="a0d79-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a0d79-120">-InformationVariable</span></span>
<span data-ttu-id="a0d79-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="a0d79-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a0d79-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a0d79-122">-Profile</span></span>
<span data-ttu-id="a0d79-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a0d79-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a0d79-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a0d79-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a0d79-125">-VM</span><span class="sxs-lookup"><span data-stu-id="a0d79-125">-VM</span></span>
<span data-ttu-id="a0d79-126">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="a0d79-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="a0d79-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d79-127">CommonParameters</span></span>
<span data-ttu-id="a0d79-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d79-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d79-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d79-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d79-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0d79-130">INPUTS</span></span>

## <span data-ttu-id="a0d79-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0d79-131">OUTPUTS</span></span>

## <span data-ttu-id="a0d79-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0d79-132">NOTES</span></span>

## <span data-ttu-id="a0d79-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0d79-133">RELATED LINKS</span></span>

[<span data-ttu-id="a0d79-134">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a0d79-134">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="a0d79-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a0d79-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


