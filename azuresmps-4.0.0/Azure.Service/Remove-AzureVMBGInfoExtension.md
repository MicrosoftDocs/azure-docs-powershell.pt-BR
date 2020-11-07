---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C735528-3844-452F-983B-41AC5CD4E414
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ea39b2c06a5daf7540009f480e7c2ec211e7f47
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945508"
---
# <span data-ttu-id="abdea-101">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="abdea-101">Remove-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="abdea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abdea-102">SYNOPSIS</span></span>
<span data-ttu-id="abdea-103">Remove a extensão BGInfo aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="abdea-103">Removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="abdea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abdea-104">SYNTAX</span></span>

```
Remove-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="abdea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abdea-105">DESCRIPTION</span></span>
<span data-ttu-id="abdea-106">O cmdlet **Remove-AzureVMBGInfoExtension** remove a extensão BGInfo aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="abdea-106">The **Remove-AzureVMBGInfoExtension** cmdlet removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="abdea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abdea-107">EXAMPLES</span></span>

### <span data-ttu-id="abdea-108">Exemplo 1: remover a extensão do BGInfo em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="abdea-108">Example 1: Remove the BGInfo extension on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="abdea-109">Esse comando Remove a extensão BGInfo aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="abdea-109">This command removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="abdea-110">OS</span><span class="sxs-lookup"><span data-stu-id="abdea-110">PARAMETERS</span></span>

### <span data-ttu-id="abdea-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="abdea-111">-InformationAction</span></span>
<span data-ttu-id="abdea-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="abdea-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="abdea-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="abdea-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="abdea-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="abdea-114">Continue</span></span>
- <span data-ttu-id="abdea-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="abdea-115">Ignore</span></span>
- <span data-ttu-id="abdea-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="abdea-116">Inquire</span></span>
- <span data-ttu-id="abdea-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="abdea-117">SilentlyContinue</span></span>
- <span data-ttu-id="abdea-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="abdea-118">Stop</span></span>
- <span data-ttu-id="abdea-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="abdea-119">Suspend</span></span>

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

### <span data-ttu-id="abdea-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="abdea-120">-InformationVariable</span></span>
<span data-ttu-id="abdea-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="abdea-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="abdea-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="abdea-122">-Profile</span></span>
<span data-ttu-id="abdea-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="abdea-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="abdea-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="abdea-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="abdea-125">-VM</span><span class="sxs-lookup"><span data-stu-id="abdea-125">-VM</span></span>
<span data-ttu-id="abdea-126">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="abdea-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="abdea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abdea-127">CommonParameters</span></span>
<span data-ttu-id="abdea-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abdea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abdea-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abdea-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abdea-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abdea-130">INPUTS</span></span>

## <span data-ttu-id="abdea-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abdea-131">OUTPUTS</span></span>

## <span data-ttu-id="abdea-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abdea-132">NOTES</span></span>

## <span data-ttu-id="abdea-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abdea-133">RELATED LINKS</span></span>

[<span data-ttu-id="abdea-134">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="abdea-134">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="abdea-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="abdea-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


