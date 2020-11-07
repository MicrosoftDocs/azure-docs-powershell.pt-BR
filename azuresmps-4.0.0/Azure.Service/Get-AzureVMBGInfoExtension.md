---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4CB958B-AC85-4036-A6D6-002FAF40BB66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e74be3310b895ef4c941a59541a64f9c6d1b279
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945532"
---
# <span data-ttu-id="b13eb-101">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="b13eb-101">Get-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="b13eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b13eb-102">SYNOPSIS</span></span>
<span data-ttu-id="b13eb-103">Obtém a extensão BGInfo aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b13eb-103">Gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="b13eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b13eb-104">SYNTAX</span></span>

```
Get-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b13eb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b13eb-105">DESCRIPTION</span></span>
<span data-ttu-id="b13eb-106">O cmdlet **Get-AzureVMBGInfoExtension** Obtém a extensão BGInfo aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b13eb-106">The **Get-AzureVMBGInfoExtension** cmdlet gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="b13eb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b13eb-107">EXAMPLES</span></span>

### <span data-ttu-id="b13eb-108">Exemplo 1: obter a extensão BGInfo aplicada a uma máquina virtual especificada</span><span class="sxs-lookup"><span data-stu-id="b13eb-108">Example 1: Get the BGInfo extension applied on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="b13eb-109">Este comando obtém a extensão BGInfo aplicada a uma máquina virtual especificada</span><span class="sxs-lookup"><span data-stu-id="b13eb-109">This command gets the BGInfo extension applied on a specified virtual machine</span></span>

## <span data-ttu-id="b13eb-110">OS</span><span class="sxs-lookup"><span data-stu-id="b13eb-110">PARAMETERS</span></span>

### <span data-ttu-id="b13eb-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b13eb-111">-InformationAction</span></span>
<span data-ttu-id="b13eb-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="b13eb-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b13eb-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b13eb-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b13eb-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="b13eb-114">Continue</span></span>
- <span data-ttu-id="b13eb-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="b13eb-115">Ignore</span></span>
- <span data-ttu-id="b13eb-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="b13eb-116">Inquire</span></span>
- <span data-ttu-id="b13eb-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b13eb-117">SilentlyContinue</span></span>
- <span data-ttu-id="b13eb-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="b13eb-118">Stop</span></span>
- <span data-ttu-id="b13eb-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="b13eb-119">Suspend</span></span>

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

### <span data-ttu-id="b13eb-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b13eb-120">-InformationVariable</span></span>
<span data-ttu-id="b13eb-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="b13eb-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b13eb-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b13eb-122">-Profile</span></span>
<span data-ttu-id="b13eb-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b13eb-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b13eb-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b13eb-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b13eb-125">-VM</span><span class="sxs-lookup"><span data-stu-id="b13eb-125">-VM</span></span>
<span data-ttu-id="b13eb-126">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="b13eb-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="b13eb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13eb-127">CommonParameters</span></span>
<span data-ttu-id="b13eb-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b13eb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13eb-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b13eb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13eb-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b13eb-130">INPUTS</span></span>

## <span data-ttu-id="b13eb-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b13eb-131">OUTPUTS</span></span>

## <span data-ttu-id="b13eb-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b13eb-132">NOTES</span></span>

## <span data-ttu-id="b13eb-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b13eb-133">RELATED LINKS</span></span>

[<span data-ttu-id="b13eb-134">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="b13eb-134">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)

[<span data-ttu-id="b13eb-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="b13eb-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


