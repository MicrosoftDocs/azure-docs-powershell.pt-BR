---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A46832F2-CA94-43A4-AFF9-70D02851713F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1146cee245693c19b333af5a4efd9fcc1bebc725
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945505"
---
# <span data-ttu-id="fe56c-101">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="fe56c-101">Remove-AzureVMChefExtension</span></span>

## <span data-ttu-id="fe56c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe56c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe56c-103">Remove a extensão chefe aplicada na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe56c-103">Removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="fe56c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe56c-104">SYNTAX</span></span>

```
Remove-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fe56c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe56c-105">DESCRIPTION</span></span>
<span data-ttu-id="fe56c-106">O cmdlet **Remove-AzureVMChefExtension** exclui a extensão chefe aplicada na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe56c-106">The **Remove-AzureVMChefExtension** cmdlet deletes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="fe56c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe56c-107">EXAMPLES</span></span>

### <span data-ttu-id="fe56c-108">Exemplo 1: remover a extensão chefe aplicada na máquina virtual especificada</span><span class="sxs-lookup"><span data-stu-id="fe56c-108">Example 1: Remove the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Remove-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="fe56c-109">Esse comando Remove a extensão chefe aplicada na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe56c-109">This command removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="fe56c-110">OS</span><span class="sxs-lookup"><span data-stu-id="fe56c-110">PARAMETERS</span></span>

### <span data-ttu-id="fe56c-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fe56c-111">-InformationAction</span></span>
<span data-ttu-id="fe56c-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="fe56c-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fe56c-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fe56c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe56c-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="fe56c-114">Continue</span></span>
- <span data-ttu-id="fe56c-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="fe56c-115">Ignore</span></span>
- <span data-ttu-id="fe56c-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="fe56c-116">Inquire</span></span>
- <span data-ttu-id="fe56c-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fe56c-117">SilentlyContinue</span></span>
- <span data-ttu-id="fe56c-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="fe56c-118">Stop</span></span>
- <span data-ttu-id="fe56c-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="fe56c-119">Suspend</span></span>

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

### <span data-ttu-id="fe56c-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fe56c-120">-InformationVariable</span></span>
<span data-ttu-id="fe56c-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="fe56c-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fe56c-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="fe56c-122">-Profile</span></span>
<span data-ttu-id="fe56c-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="fe56c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe56c-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="fe56c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fe56c-125">-VM</span><span class="sxs-lookup"><span data-stu-id="fe56c-125">-VM</span></span>
<span data-ttu-id="fe56c-126">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="fe56c-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="fe56c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe56c-127">CommonParameters</span></span>
<span data-ttu-id="fe56c-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe56c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe56c-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe56c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe56c-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe56c-130">INPUTS</span></span>

## <span data-ttu-id="fe56c-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe56c-131">OUTPUTS</span></span>

## <span data-ttu-id="fe56c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe56c-132">NOTES</span></span>

## <span data-ttu-id="fe56c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe56c-133">RELATED LINKS</span></span>

[<span data-ttu-id="fe56c-134">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="fe56c-134">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="fe56c-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="fe56c-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


