---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 40AE50AA-6807-4481-8B77-A038914D462E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a4c6997a7ae70a72a21800cce1d4f5f32475a85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946447"
---
# <span data-ttu-id="35784-101">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="35784-101">Remove-AzureVMDscExtension</span></span>

## <span data-ttu-id="35784-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35784-102">SYNOPSIS</span></span>
<span data-ttu-id="35784-103">Remove uma extensão DSC do Azure de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35784-103">Removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="35784-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35784-104">SYNTAX</span></span>

```
Remove-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35784-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35784-105">DESCRIPTION</span></span>
<span data-ttu-id="35784-106">O cmdlet **Remove-AzureVMDscExtension** remove uma extensão DSC do Azure de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35784-106">The **Remove-AzureVMDscExtension** cmdlet removes an Azure DSC extension from a virtual machine.</span></span>
<span data-ttu-id="35784-107">A saída desse cmdlet precisa ser canalizada para o cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="35784-107">The output of this cmdlet needs to be piped to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="35784-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35784-108">EXAMPLES</span></span>

### <span data-ttu-id="35784-109">Exemplo 1: remover uma extensão DSC de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="35784-109">Example 1: Remove a DSC extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDscExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="35784-110">Esse comando Remove uma extensão DSC do Azure de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="35784-110">This command removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="35784-111">OS</span><span class="sxs-lookup"><span data-stu-id="35784-111">PARAMETERS</span></span>

### <span data-ttu-id="35784-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="35784-112">-InformationAction</span></span>
<span data-ttu-id="35784-113">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="35784-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="35784-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="35784-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35784-115">Contínuo</span><span class="sxs-lookup"><span data-stu-id="35784-115">Continue</span></span>
- <span data-ttu-id="35784-116">Ignorar</span><span class="sxs-lookup"><span data-stu-id="35784-116">Ignore</span></span>
- <span data-ttu-id="35784-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="35784-117">Inquire</span></span>
- <span data-ttu-id="35784-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="35784-118">SilentlyContinue</span></span>
- <span data-ttu-id="35784-119">Finaliza</span><span class="sxs-lookup"><span data-stu-id="35784-119">Stop</span></span>
- <span data-ttu-id="35784-120">Suspensão</span><span class="sxs-lookup"><span data-stu-id="35784-120">Suspend</span></span>

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

### <span data-ttu-id="35784-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="35784-121">-InformationVariable</span></span>
<span data-ttu-id="35784-122">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="35784-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="35784-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="35784-123">-Profile</span></span>
<span data-ttu-id="35784-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="35784-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="35784-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="35784-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="35784-126">-VM</span><span class="sxs-lookup"><span data-stu-id="35784-126">-VM</span></span>
<span data-ttu-id="35784-127">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="35784-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="35784-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35784-128">-Confirm</span></span>
<span data-ttu-id="35784-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35784-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35784-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35784-130">-WhatIf</span></span>
<span data-ttu-id="35784-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35784-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35784-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35784-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35784-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35784-133">CommonParameters</span></span>
<span data-ttu-id="35784-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35784-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35784-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35784-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35784-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35784-136">INPUTS</span></span>

## <span data-ttu-id="35784-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35784-137">OUTPUTS</span></span>

## <span data-ttu-id="35784-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35784-138">NOTES</span></span>

## <span data-ttu-id="35784-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35784-139">RELATED LINKS</span></span>

[<span data-ttu-id="35784-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="35784-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="35784-141">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="35784-141">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="35784-142">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="35784-142">Update-AzureVM</span></span>](./Update-AzureVM.md)


