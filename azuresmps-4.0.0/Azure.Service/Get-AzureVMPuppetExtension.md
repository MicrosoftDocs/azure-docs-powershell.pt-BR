---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AC28E79-0E3F-4AED-8BFE-8D1C4DCB7715
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd7ece4f8f414df7be6e2d38920f516119f4b82a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946526"
---
# <span data-ttu-id="1ae8a-101">Get-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="1ae8a-101">Get-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="1ae8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ae8a-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae8a-103">Obtém a extensão Puppet aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1ae8a-103">Gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="1ae8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ae8a-104">SYNTAX</span></span>

```
Get-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1ae8a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ae8a-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae8a-106">O cmdlet **Get-AzureVMPuppetExtension** Obtém a extensão Puppet aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1ae8a-106">The **Get-AzureVMPuppetExtension** cmdlet gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="1ae8a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ae8a-107">EXAMPLES</span></span>

### <span data-ttu-id="1ae8a-108">Exemplo 1: obter a extensão Puppet aplicada em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="1ae8a-108">Example 1: Get the Puppet extension applied on a virtual machine</span></span>
```
PS C:\> Get-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="1ae8a-109">Esse comando obtém a extensão Puppet aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1ae8a-109">This command gets the Puppet extension applied on a virtual machine.</span></span>

## <span data-ttu-id="1ae8a-110">OS</span><span class="sxs-lookup"><span data-stu-id="1ae8a-110">PARAMETERS</span></span>

### <span data-ttu-id="1ae8a-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="1ae8a-111">-InformationAction</span></span>
<span data-ttu-id="1ae8a-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="1ae8a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1ae8a-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1ae8a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1ae8a-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="1ae8a-114">Continue</span></span>
- <span data-ttu-id="1ae8a-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="1ae8a-115">Ignore</span></span>
- <span data-ttu-id="1ae8a-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="1ae8a-116">Inquire</span></span>
- <span data-ttu-id="1ae8a-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1ae8a-117">SilentlyContinue</span></span>
- <span data-ttu-id="1ae8a-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="1ae8a-118">Stop</span></span>
- <span data-ttu-id="1ae8a-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="1ae8a-119">Suspend</span></span>

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

### <span data-ttu-id="1ae8a-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1ae8a-120">-InformationVariable</span></span>
<span data-ttu-id="1ae8a-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="1ae8a-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1ae8a-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="1ae8a-122">-Profile</span></span>
<span data-ttu-id="1ae8a-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="1ae8a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ae8a-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="1ae8a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ae8a-125">-VM</span><span class="sxs-lookup"><span data-stu-id="1ae8a-125">-VM</span></span>
<span data-ttu-id="1ae8a-126">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="1ae8a-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="1ae8a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae8a-127">CommonParameters</span></span>
<span data-ttu-id="1ae8a-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae8a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae8a-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae8a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae8a-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ae8a-130">INPUTS</span></span>

## <span data-ttu-id="1ae8a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ae8a-131">OUTPUTS</span></span>

## <span data-ttu-id="1ae8a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ae8a-132">NOTES</span></span>

## <span data-ttu-id="1ae8a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ae8a-133">RELATED LINKS</span></span>

[<span data-ttu-id="1ae8a-134">Remove-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="1ae8a-134">Remove-AzureVMPuppetExtension</span></span>](./Remove-AzureVMPuppetExtension.md)

[<span data-ttu-id="1ae8a-135">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="1ae8a-135">Set-AzureVMPuppetExtension</span></span>](./Set-AzureVMPuppetExtension.md)


