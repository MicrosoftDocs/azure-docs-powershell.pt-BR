---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AAEDD44-D11E-47A3-BF0F-D8445A018759
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46dbd7ec58cc112e6573fa3d9c6a52fe0ee14b33
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946443"
---
# <span data-ttu-id="bc600-101">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="bc600-101">Remove-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="bc600-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc600-102">SYNOPSIS</span></span>
<span data-ttu-id="bc600-103">Remove a extensão Puppet aplicada em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bc600-103">Removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="bc600-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc600-104">SYNTAX</span></span>

```
Remove-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bc600-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc600-105">DESCRIPTION</span></span>
<span data-ttu-id="bc600-106">O cmdlet **Remove-AzureVMPuppetExtension** remove a extensão Puppet aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bc600-106">The **Remove-AzureVMPuppetExtension** cmdlet removes the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="bc600-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc600-107">EXAMPLES</span></span>

### <span data-ttu-id="bc600-108">Exemplo 1: remover a extensão Puppet aplicada em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="bc600-108">Example 1: Remove the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMPuppetExtension -VM $VM;
```

<span data-ttu-id="bc600-109">Esse comando Remove a extensão Puppet aplicada na máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="bc600-109">This command removes the Puppet extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="bc600-110">OS</span><span class="sxs-lookup"><span data-stu-id="bc600-110">PARAMETERS</span></span>

### <span data-ttu-id="bc600-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="bc600-111">-InformationAction</span></span>
<span data-ttu-id="bc600-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="bc600-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bc600-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bc600-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bc600-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="bc600-114">Continue</span></span>
- <span data-ttu-id="bc600-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="bc600-115">Ignore</span></span>
- <span data-ttu-id="bc600-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="bc600-116">Inquire</span></span>
- <span data-ttu-id="bc600-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bc600-117">SilentlyContinue</span></span>
- <span data-ttu-id="bc600-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="bc600-118">Stop</span></span>
- <span data-ttu-id="bc600-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="bc600-119">Suspend</span></span>

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

### <span data-ttu-id="bc600-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bc600-120">-InformationVariable</span></span>
<span data-ttu-id="bc600-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="bc600-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bc600-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bc600-122">-Profile</span></span>
<span data-ttu-id="bc600-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="bc600-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bc600-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="bc600-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bc600-125">-VM</span><span class="sxs-lookup"><span data-stu-id="bc600-125">-VM</span></span>
<span data-ttu-id="bc600-126">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="bc600-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="bc600-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc600-127">CommonParameters</span></span>
<span data-ttu-id="bc600-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc600-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc600-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc600-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc600-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc600-130">INPUTS</span></span>

## <span data-ttu-id="bc600-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc600-131">OUTPUTS</span></span>

## <span data-ttu-id="bc600-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc600-132">NOTES</span></span>

## <span data-ttu-id="bc600-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc600-133">RELATED LINKS</span></span>

[<span data-ttu-id="bc600-134">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="bc600-134">Get-AzureVMPuppetExtension</span></span>](./Get-AzureVMPuppetExtension.md)

[<span data-ttu-id="bc600-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="bc600-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


