---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 734C98C1-0EF7-43E5-AB6F-A1C625FF9CE7
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9713c8b39fa4e2842cdf1cfcbfe962ead86d729
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945535"
---
# <span data-ttu-id="d3a2b-101">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d3a2b-101">Get-AzureVMAccessExtension</span></span>

## <span data-ttu-id="d3a2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a2b-103">Obtém a extensão VMAccess aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3a2b-103">Gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="d3a2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3a2b-104">SYNTAX</span></span>

```
Get-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d3a2b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a2b-106">O cmdlet **Get-AzureVMAccessExtension** Obtém a extensão VMAccess aplicada a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3a2b-106">The **Get-AzureVMAccessExtension** cmdlet gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="d3a2b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3a2b-107">EXAMPLES</span></span>

### <span data-ttu-id="d3a2b-108">Exemplo 1: obter a extensão VMAccess para uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d3a2b-108">Example 1: Get the VMAccess extension for a virtual machine</span></span>
```
PS C:\> Get-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="d3a2b-109">Esse comando obtém a extensão VMAccess para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3a2b-109">This command gets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="d3a2b-110">OS</span><span class="sxs-lookup"><span data-stu-id="d3a2b-110">PARAMETERS</span></span>

### <span data-ttu-id="d3a2b-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d3a2b-111">-InformationAction</span></span>
<span data-ttu-id="d3a2b-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="d3a2b-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d3a2b-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d3a2b-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d3a2b-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="d3a2b-114">Continue</span></span>
- <span data-ttu-id="d3a2b-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="d3a2b-115">Ignore</span></span>
- <span data-ttu-id="d3a2b-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="d3a2b-116">Inquire</span></span>
- <span data-ttu-id="d3a2b-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d3a2b-117">SilentlyContinue</span></span>
- <span data-ttu-id="d3a2b-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="d3a2b-118">Stop</span></span>
- <span data-ttu-id="d3a2b-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="d3a2b-119">Suspend</span></span>

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

### <span data-ttu-id="d3a2b-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d3a2b-120">-InformationVariable</span></span>
<span data-ttu-id="d3a2b-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="d3a2b-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d3a2b-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d3a2b-122">-Profile</span></span>
<span data-ttu-id="d3a2b-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d3a2b-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3a2b-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d3a2b-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3a2b-125">-VM</span><span class="sxs-lookup"><span data-stu-id="d3a2b-125">-VM</span></span>
<span data-ttu-id="d3a2b-126">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="d3a2b-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="d3a2b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a2b-127">CommonParameters</span></span>
<span data-ttu-id="d3a2b-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a2b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a2b-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3a2b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a2b-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3a2b-130">INPUTS</span></span>

## <span data-ttu-id="d3a2b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3a2b-131">OUTPUTS</span></span>

## <span data-ttu-id="d3a2b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3a2b-132">NOTES</span></span>

## <span data-ttu-id="d3a2b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3a2b-133">RELATED LINKS</span></span>

[<span data-ttu-id="d3a2b-134">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d3a2b-134">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)

[<span data-ttu-id="d3a2b-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d3a2b-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


